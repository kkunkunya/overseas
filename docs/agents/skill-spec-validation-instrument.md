# Skill 创建指示：validation-instrument（上线即量化）

> 本文件是给**执行 agent** 的创建规格，不是 skill 本身。
> 执行 agent 照此产出 `.pi/skills/validation-instrument/` 真身 + `.agents/skills/validation-instrument` 投影，并更新 `docs/agents/skills-domain.md`。
> 方法论主源：赫兹《卖空气验证需求》(015)、《需求的痛点决定了转化率》(029)；ADR-0001 赫兹主源。
> 完整原则已落 `2-建站开发/上线即量化-建站时就埋好验证与归因.md`——skill 是它的可执行版。

## 0. 一句话目的

让验证站**上线第一天就能量化归因**：建站配置阶段埋好埋点 + 验证合同 + 触达记录卡；验证到期时模型读漏斗与触达记录，按顺序闸门判定 build / maintain / abandon。解决新手盯自然流量等噪声指标、到期只能凭感觉说「结果一般」的问题。

## 1. Skill 身份

```yaml
---
name: validation-instrument
description: 建站或配置验证站时埋好 7 个决策级埋点、验证合同与触达记录卡，让验证数据上线即量化；验证到期读取埋点漏斗与触达记录按顺序闸门归因，判定 MVP 该 build / maintain / abandon。用于站点上线前的埋点方案、排除扫描器与去重真人、验证合同填写，以及验证到期时的读数归因与判定。承接 mvp-validation 的可量化层，不重复 Landing Page 设计与触达姿势。
scope: project
---
```

- **model-invoked**（不加 `disable-model-invocation`）。leading word：建站/配置验证站时、验证到期读数判定时。
- **scope: project**——与 `mvp-validation` / `direction-validator` 同源同仓，共享赫兹方法论。
- 写完跑：`python3 "$HOME/.agents/skills/ask-skill/scripts/validate-skill-frontmatter.py" .pi/skills/validation-instrument`

## 2. 触发与边界（两个 branch，单一职责）

职责 = **让验证可量化归因**。两个 entry branch 共用同一套闸门框架：

- **Branch A · 建站侧（埋设）**：用户在建站 / 配置站点 / 即将上线验证页时触发。产出：7 事件埋点方案（含排除扫描器与去重真人规则）+ 填好的验证合同 + 空白触达记录卡就位。
- **Branch B · 判定侧（读数）**：验证合同到期 / 用户问「该做 / 放弃 / 维护吗」时触发。读埋点漏斗 + 触达记录卡 → 顺序闸门归因 → build / maintain / abandon 判定 + 唯一下一步。

### 与 mvp-validation 的关系（必须写清，防重复）

`mvp-validation` 拥有：卖空气验证全流程、Landing Page 检查清单、触达姿势与合规、价格实验。
本 skill 拥有：**建站时的埋点实现 + 到期读数判定**——验证的「仪表盘层」。

共享资产（**不重创，引用 mvp-validation 的**）：
- 验证合同模板 → `mvp-validation/assets/landing-page-checklist.md` §0
- 触达记录卡模板 → `mvp-validation/assets/outreach-record.md`

本 skill 独有资产（见 §5）：
- `assets/instrumentation-guide.md`——7 事件埋点实现 + 排除扫描器/去重真人规则
- `assets/gate-verdict.md`——顺序闸门归因表 + build/maintain/abandon 判定线 + 模型读取协议

SKILL.md 正文用内联指针点名何时读哪个 asset；不写「需要时读 references/」弱指针。

## 3. 方法骨架（从笔记五节映射，写成动作不是汇编）

执行 agent 按 `write-skill` §1 的五项落进 SKILL.md：

1. **问题模型**：验证站上线后，新手用 PV/访客数/排名等噪声指标（混扫描器、爬虫、订阅轮询）判断做不做，归因不准。真实判据是合资格人接触页面后的行动序列：到达 → 输入 → 看结果 → 询价 → 点购买 → 付款。
2. **执行顺序（Branch A 埋设）**：
   - 先填验证合同（截止时间 / 成功标准 / 停止条件 / 到期决定）——没合同不埋点，因为不知道埋点要回答什么。
   - 按 7 事件清单装埋点（到达 / 开始输入 / 完成输入 / 查看结果 / 点击购买 / checkout / 付款）。
   - 配置排除规则：自己 IP、扫描器 UA、订阅轮询路径（`.env` / `phpinfo` / `mihomo.yaml` / `stash.yaml` 等）。
   - 确认示例结果可看不可挡（无注册墙、无付费墙挡漏斗上层）；价格与 CTA 真实。
   - 触达记录卡就位（空白模板引用 mvp-validation）。
3. **执行顺序（Branch B 读数）**：见 §6 模型读取协议——先查合同 → 读触达卡 → 读漏斗（排除后只看去重真人）→ 顺序闸门归因 → 判定线 → 给推荐 + 唯一下一步，每轮最多补一次关键未知后交还用户。
4. **关键判断**：顺序闸门归因——前置闸失败不能被后置指标补偿。判定线见 `assets/gate-verdict.md`。
5. **工具路由**：建站侧——读项目代码确定技术栈与埋点接入点（Vercel Analytics / Plausible / GA4 / Cloudflare Web Analytics / 自建），按栈给接入指令；不假设特定后端。判定侧——读分析后台或日志，必要时用 `bash` 跑排除脚本。
6. **可靠性验证**：建站侧完成后用自己设备走一次完整漏斗，确认 7 事件全部触发且排除规则生效（自己访问不被计数）。判定侧给出归因必须能指到具体闸门 + 唯一下一步，不能用「再优化一下」代替结论。

## 4. 反护栏（必写，防止 skill 被误用）

- **「自然流量为零」不进判定线**。卖空气验证靠主动触达，不靠自然流量。单独的自然流量缺失不构成 abandon。
- **渠道失败 ≠ 需求不存在**。版规禁止 / 账号被过滤 / 帖子归档只能标渠道失败，换渠道，不判方向死刑。
- **「有人说感兴趣」「点赞」不算成功行动**。成功标准至少是 3 人提交真实项目参数 + 1 人点购买/愿预付；订金/付款更强。
- **build/abandon 是用户决定**，Agent 给推荐 + 理由，不越权拍板。

## 5. 产物清单

### `SKILL.md`（目标 ≤ 200 行）

主层 `##` 结构建议：
- `## 何时用`——两 branch 触发边界（model-invoked，只留 description 增量，不重复身份）。
- `## Branch A：建站时埋好可量化层`——执行顺序 §3.2，内联指针到 `assets/instrumentation-guide.md`。
- `## Branch B：到期读数与判定`——执行顺序 §3.3，内联指针到 `assets/gate-verdict.md`。
- `## 反护栏`——§4 四条硬护栏 + 正向目标。
- `## 与 mvp-validation 的分工`——§2 关系，两三行点到。
- `## 参考资料`——赫兹 015 / 029 指向 `原文/`，内联指针已覆盖 assets。

不写 `## 你的角色`（无 load-bearing 定义需要）。`## 不做什么` 并入 `## 反护栏`（已是正向 + 硬护栏结构）。

### `assets/instrumentation-guide.md`

内容（建站侧可执行）：
1. **7 事件清单表**：事件名 / 判断什么 / 缺它会怎样 / 触发时机（如 `start_input` = 用户首次聚焦输入框）。
2. **排除规则**：
   - 排除自己 IP（列出所有常用 IP，含移动热点）。
   - 排除扫描器 UA 与路径（`.env` / `.git` / `phpinfo` / `wp-login` / `.aws` 等已知扫描指纹）。
   - 排除订阅客户端轮询（`mihomo` / `stash` / `clash` / `yaml` 订阅拉取路径）——这些是客户端拉配置，不是网站访问。
   - 排除搜索引擎爬虫（sitemap 抓取不算真人）。
3. **去重真人定义**：按去重 IP + UA 算「人」，不按 PV。一个真人翻 5 页 = 1 人不是 5 人。
4. **按技术栈接入**：分别给 Vercel Analytics / Plausible / GA4 / Cloudflare Web Analytics 的 7 事件接入要点（自定义事件 API）；不假设栈，按项目实际选。
5. **自检**：上线后用自己设备走一次完整漏斗，7 事件全触发且自己访问被排除 = 通过。

### `assets/gate-verdict.md`

内容（判定侧可执行）：
1. **顺序闸门归因表**（从笔记 §4）：

   | 量化结果 | 归因闸 | 结论方向 | 唯一下一步 |
   |---|---|---|---|
   | 合资格触达量 < 上限，到站去重真人个位数 | 流量闸 | 不放弃 | 换触达姿势/渠道/账号 |
   | 曝光够但 `start_input` ≈ 0 | 承接闸 | revise 页面 | 改承诺/示例/文案 |
   | 有 `complete_input` 但 `click_buy` ≈ 0 | 价值/价格闸 | revise 切口或价格 | 改价格/痛点切口/付费时刻 |
   | 有 `click_buy`/`checkout` 但 `pay` ≈ 0 | 支付/信任闸 | revise 支付路径 | 查信任/退款说明/支付摩擦 |
   | 出现询价/订金/付款 | 商业证据 | build | 做最小可用 MVP，不急扩量 |
   | 触达够多 + 换过渠道/页面/价格 + 三层行动全零 | 方向级反证 | reject | 记失败闸门回 Seed Pool |

2. **判定线**：
   - **build** = 强信号（询价/订金/付款）。量小也先做最小可用 MVP。
   - **maintain** = 中信号（留联系方式/接受访谈/提交真实项目）无付款。保持触达，小步改承接，不投入重开发。
   - **abandon** = 触达达合同上限 + 至少换过一轮渠道/页面/价格 + 三层行动全零。唯一可判方向死刑的条件。
3. **模型读取协议**（笔记 §5，照搬成 6 步动作）。
4. **不进判定线的指标**：自然流量、PV、排名、点赞、口头好评、熟人鼓励。

## 6. 模型读取协议（写入 `assets/gate-verdict.md` 末段，也作 SKILL.md Branch B 的步骤）

用户问「这个 MVP 该做/放弃/维护」时按序执行：

1. 查验证合同是否存在；没有 → 第一步补合同，不分析数据。
2. 读触达记录卡：合资格触达了多少人；没记录 → 第一步补记录卡。
3. 读埋点漏斗：7 事件各多少人；先排除扫描器/订阅轮询/自己 IP，只看去重真人。
4. 顺序闸门归因：找第一个失败的闸，给唯一下一步；不用后置指标补偿前置失败。
5. 对照判定线给 build / maintain / abandon + 理由 + 下一个动作。
6. 不越权：build/abandon 是用户决定，给推荐 + 理由；每轮最多补一次关键未知（通常是「合资格触达了多少人、行动分几层」）后交还用户。

## 7. 来源与边界

- 主源：赫兹 015《卖空气验证需求》、029《需求的痛点决定了转化率》。方法论以赫兹为准（ADR-0001）。
- 触达合规顺序、平台特性引用 `mvp-validation/references/community-outreach.md`，不重写。
- 本 skill 是**通用仪表盘层**，不限平台、不限产品形态、不限技术栈。具体 Landing Page 设计、触达姿势、价格实验归 `mvp-validation`。
- 「自然流量为零」不在判定线内。

## 8. 落盘与分发（按 ADR-0003 两仓分工）

本 skill 是**工程性 skill**（建站埋点、读数判定，与具体产品绑定），真身落**产品项目仓库**，不落本知识库。本创建指示文档（`docs/agents/skill-spec-validation-instrument.md`）留本库作为方法论依据。

1. 真身写 **产品项目仓库** `/Users/kun/oversea-project/amigurumi-pricing-calculator/.pi/skills/validation-instrument/`（SKILL.md + assets/）。注意该仓库是 `dev`/`main` 双 worktree，按 `write-skill` 选分支。
2. 在产品项目内运行 `sync-project-skills`（或 `distribute-local-project-skills`）建 `.agents/skills/validation-instrument` 投影。
3. 本知识库 `docs/agents/skills-domain.md` **不改**——本 skill 不属于知识库的 project skill，归产品项目自己的领域声明。
4. 本知识库 `2-建站开发/_本步导航.md` 已有原则笔记指针；无需再加 skill 指针（skill 真身在产品仓库，知识库读者点不过去）。
5. 若未来 `validation-instrument` 被多产品复用，按 ADR-0003 评估升级为 `scope: global` 进 `~/.agents/skills/`，不在每个产品仓库各放一份。

## 9. 验收清单（执行 agent 交付前自查一轮）

- [ ] frontmatter 校验通过：`validate-skill-frontmatter.py .pi/skills/validation-instrument`
- [ ] `wc -l SKILL.md` ≤ 200 行（超 200 做 branch audit 下推 references/）。
- [ ] 两个 branch 各用一个代表场景走一遍：A = 建站配置时触发→产出埋点方案+合同+记录卡就位；B = 验证到期触发→读数→归因→判定。指出 Agent 关键判断、调用什么工具、怎样知道完成。
- [ ] 与 mvp-validation 无重复：验证合同/触达卡是引用不是重创；Landing Page 设计/触达姿势/价格实验不进本 skill。
- [ ] 内联指针：每个 asset 在正文使用处点名「包含什么、何时读」，无弱指针。
- [ ] 反护栏四条齐全且配正向目标。
- [ ] 真身落在产品项目仓库 `.pi/skills/validation-instrument/`（非本知识库），符合 ADR-0003。
- [ ] 产物在写作现场就绪后调 `/deliver-skill` 走交付门禁。

## 10. 给执行 agent 的提示

- 默认往简单拉：7 事件是直线漏斗，不要为每事件加 fallback / 重试 / 状态机。排除规则用清单 + 自检，不写通用扫描器检测脚本（依赖具体后台，强写反而不可移植）。
- 技术栈接入按项目实际选，不在 SKILL.md 里穷举四个后端的全量代码——`assets/instrumentation-guide.md` 给要点指针，具体接入让 Agent 读项目代码后给。
- 判定侧是 model-invoked 的核心价值：把读取协议写成祈使句动作，模型照着跑就能给 build/maintain/abandon + 理由。