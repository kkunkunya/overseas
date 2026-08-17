# AGENTS.md

> Cordex / Codex 读本文件；与 `CLAUDE.md`（Claude Code）同步同一份提示词。

## 项目是什么

出海学习**知识库**（查阅库，不是产品代码库）——6 步结构收纳**多源**材料（赫兹 227 篇只是其中一批；还有 PDF、Viking、Marc Lou、YC 等，会持续加）。目标：你**亲自试出**一条可复制产品的商业闭环（躺赚 + 复利）。当前默认路径菜单：**垂直细分 + 长期稳定增长**（ADR-0005）；热词抢占不做。**没有任何单一作者是主体/教主**——材料只提供经验切片，裁决是路径 + 你的实测。产品开发另开独立项目文件夹，本库只作查阅参考。

技术栈：纯 markdown，无代码。版本管理 git + GitHub（`kkunkunya/overseas`）。

## 命令

无 build / test / run（纯知识库）。常用：

- `git add -A && git commit -m "..." && git push`——整理后提交
- `gh issue create --title "..." --body "..."`——登记学习任务（补哪步笔记、精读哪篇原文）
- `gh issue list --state open`——看待办

无特殊 flag / env。

## 架构地图

```
overseas/
├─ README.md          ← 总导航（6 步 + 两份实战共识 + 怎么用）
├─ 1-选方向/ … 6-复盘增长/   ← 笔记层：每步入口 _本步导航.md
└─ 原文/              ← 原文层：赫兹 227 篇按 6 步重排
   ├─ README.md       ← 227 篇一句话索引
   └─ 0-工具与资源/ 1-选方向/ … 6-复盘增长/
```

笔记层是二手提炼；`原文/` 主要是赫兹历史一手包（**工具箱一格**，非教主）。术语 / 决策：`CONTEXT.md` / `docs/adr/`（**ADR-0005 路径主导**；**ADR-0006** 淘汰旧三方向）。

## 约定与边界

- **路径主导 + 亲测（ADR-0005）**——先对齐当前路径与垂直方向，再从材料抽片段；冲突时以**路径目标 + 你实测**裁决，**不以作者身份**裁决。赫兹 / 未署名 PDF / Viking / 其他视频帖子都是工具箱。
- **疯狂收集、按步归档**——新资料进对应 1–6 步笔记；标作者与出处便于检索，**不设主源等级**。
- **当前路径菜单**——默认：**垂直细分** + **长期稳定增长**；**热词抢占不做**。术语见 `CONTEXT.md`「当前路径」。
- **旧候选**——TTS / 激光清洗 / 专业服务已 **reject**（ADR-0006），不续研。
- **新内容按 6 步归类**——新文章 / 新笔记判断属 1-6 哪一步再归档。归错步骤 → 查不到 → 知识库失效。
- **每步入口是 `_本步导航.md`**——补笔记先更新本步导航，再放具体笔记文件。
- **原文层保留"编号-标题"原始格式**——`原文/` 不批量改名；精读某步时才重命名那一步。
- **外部 playbook 先做阶段翻译**——长期经营建议须标适用阶段；未验证前不把涨粉、自动化、Creator 合作、holding company 当当前待办。
- **结果用行动衡量**——优先记录真实输入、联系、预约、点击购买、预付或付款；点赞和称赞不算需求成立。卖空气 / 018 等为**可选检查**，非强制门禁。
- **私聊是许可式研究**——规则允许或对方愿意时一对一；不群发陌生私信、不伪装身份。
- 不要碰：`.DS_Store`（已 gitignore）、`原文/` 批量重命名。

## skill 路由

本仓库是**查阅库**，不走 idea→ship 代码流程。常用：

- `/grilling`——精读某篇原文 / 笔记，逐句追问理解
- `/domain-modeling`——把出海术语（目录站、躺赚、复利、SEO、外链…）谈拢落 `CONTEXT.md`
- `/research`——调研方向 / 竞品 / 赛道
- `/project-prompt`——项目阶段、约定或 Agent 路由发生稳定变化时，刷新 `AGENTS.md` / `CLAUDE.md` 的短地图
- `ask-overseas`（项目 skill）——出海机会与增长问题混在一起时，定位当前最早缺口并路由唯一下一步
- `direction-validator`（项目 skill）——**可选**从人群/社区/工作流选择 SEO 资产、Workflow SaaS 或混合楔子路线
- `vertical-keyword-loop`（项目 skill）——**可选** SEO-first 选词：词群/SERP/竞争/场景取证与 go/watch/narrow/reject
- `mvp-validation`（项目 skill）——**可选**用真实价格与行动信号验证承诺
- `seo-site-blueprint` / `seo-readiness-audit`（项目 skill）——已拍板词群的页面/内链/首版蓝图；以及上线时的可抓取/索引审计
- `distribution-link-loop` / `geo-source-loop`（项目 skill）——首批分发、外链机会与台账；AI 搜索来源资产与引用机会
- `product-growth-review`（项目 skill）——用 GSC、产品行为、分发与收入定位最早瓶颈并决定加码/收窄/停止
- `kb-ingest`（项目 skill）——外部资料提炼进笔记层、归步、更新索引；与当前路径及其他材料交叉引用

不知道下一步怎么走 → 先用 `ask-overseas`；只想查阅学习材料 → 先读 `README.md` + 对应步骤的 `_本步导航.md`。做产品时**另开项目**实现代码；本库保留方向、搜索与增长方法，具体工程 skill 在产品仓库按其技术栈启用。

## 指针

- `CONTEXT.md` / `docs/adr/`——术语词典 + 决策记录（ADR-0005 路径主导）
- `docs/agents/`——issue tracker / triage / domain / 领域声明（setup-project 产出）
- `## Agent skills` 块（下方）——归 setup-project

## Agent skills

### Issue tracker
工作单住 GitHub Issues，用 `gh` CLI 操作。见 `docs/agents/issue-tracker.md`。

### Triage labels
用默认角色名当标签字符串（bug / enhancement / needs-triage / needs-info / ready-for-agent / ready-for-human / wontfix）。见 `docs/agents/triage-labels.md`。

### Domain docs
单 context（single-context）——根目录一个 `CONTEXT.md` + `docs/adr/`，由 domain-modeling 惰性创建。见 `docs/agents/domain.md`。

### Skills domain
本库声明 `overseas-growth` 方法领域：项目 skill 真身统一在 `.pi/skills/`，覆盖方向、搜索、页面蓝图、上线审计、分发/GEO 与增长复盘；具体产品工程仍在独立产品仓库声明 frontend/engineering/deploy。见 `docs/agents/skills-domain.md`。
