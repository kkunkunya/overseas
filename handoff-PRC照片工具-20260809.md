# Handoff · PRC 照片工具——从选词到 PRD 交付，进入开发

> 2026-08-09 · 以此文件为准
> 知识库：`/Users/kun/learn/overseas` · `main`
> 下一会话：**在另开项目文件夹开发 PRC 照片工具**（带 frontend 领域），本知识库只作依据

---

## 一句话

选词第 8 轮从「AI 求职头像」深挖出**菲律宾 PRC 执照照片**这个垂直缺口，规格已官方取证，**PRD v0.2 已交付**，Kun 拍板：不做最小验证、直接开发，**开发期就把 SEO/GEO 做好，产品成熟后再触达**（ADR-0012）。

## 建议技能（下个 agent）

1. **开发另开项目**：走 `/project-design-prompt` → `/layout-priority-design` → `/design-recon` → `/to-tickets`（frontend 领域），PRD 和规格表作输入。
2. **查规格**：读 `1-选方向/PRC照片规格表-2026-08-09.md`（权威依据）。
3. 拿不准路由 → `/ask-me`。

## 下一会话目标

**在独立项目文件夹按 PRD v0.2 开发 PRC 照片工具**，里程碑 M1→M4：
- M1 工具核心：上传→人脸检测→2x2 生成→免费下载
- M2 名字条 + 现场版（1½×1½）+ 4 张打印纸 PDF
- M3 SEO/GEO 基线 + 5 个内容页
- M4 支付（Stripe Payment Links）+ 上线闭环
- M5 触达（M4 后才做，ADR-0012）

## 已确认事实（方法/决策）

- **方向三件套**：ADR-0008 旧需求薄弱点 / ADR-0010 纯数字产品（无重线下耦合、有体感、能做出来）/ ADR-0011 小众关键词做透 = 自然保护。
- **ADR-0012**：不做「先卖空气/最小触达」；AI 时代粗劣 demo 没人回复，个人出海无投流预算 → **先做产品力，产品成熟再触达**；多种打法综合。
- **本/术/发现三结合**：KD/月搜/稳定词都是术（工具），Kun 判断是本（本质），Agent 取证是发现；指标不替代判断。
- **协作契约**：主动提问；找到词先沟通再深挖；给词让 Kun 开 AITDK 筛查；不独自跑完整条链。
- **趋势验证**：逐词下载 CSV 算首末均值，截图口述不作数（ADR-0009）。
- **找词渠道**：社媒（ins/reddit/x/threads）+ autocomplete + Ahrefs + SERP 并列；蓝海不局限东南亚。
- **技术架构原则（PRD v0.3）**：AI 是可选增强，规范是硬约束。不把方案卡死——未来可接 GPT 视觉模型生成/识别，但**所有输出必须过「规范校验器」**（确定性规则：尺寸/白底/头部占比/名字条格式/分辨率），AI 不做最终裁决，避免幻觉导致照片被拒收。AI 能力（视觉识别/全名解析/抠图）可插拔。

## 产品关键事实（PRC 照片工具）

### 规格核心（线上 vs 现场）

| 环节 | 尺寸 | 背景 | 名字条 |
|---|---|---|---|
| 线上（LERIS 上传） | 2x2 英寸 | 纯白 | **不需要** |
| 现场（申请表/递交） | 1½ × 1½ 英寸 | 纯白 | **必须带 COMPLETE Name Tag** |

- 6 个月内近照；有领得体衣服；4 张彩色；不接受扫描件
- 名字条格式：**Surname, First Name M.I.**（姓，名 中间名首字母）；**白底黑字**（TikTok 纠错）
- 来源：PRC 官网 FAQ（线上）+ 官方申请表 PDF PRC Form No. 001（现场）

### 痛点证据（无需再验证）

- Reddit：r/AccountingPH「护照尺寸还是 2x2？还是都要？」、r/NursingPH「PRC 严格吗」
- TikTok：@buyayi 11.5K 赞教程（白底黑字纠错）、@nursenoime、@binibining_mena；话题页 passport-size-with-name-tag-for-prc
- YouTube：PRC ID 名字签名教程 36K、LET 115K、Board exam 347K
- SERP：前排全是通用工具站（PhotoAiD/PhotoGov/Passport-Photo.Online），**无 PRC 专用工具** = 缺口成立

### 变现

- 免费：带水印预览 + 低分辨率
- 付费一次性 **$2-5 / P99-199**：无水印高清 + 4 张打印纸 PDF + 合规自检
- 锚点：照相馆 P150-300/次；不做订阅

### 技术建议

- Next.js/Vite + React 静态站；MediaPipe 人脸检测；Canvas 处理；remove.bg 兜底；jsPDF 打印纸；Stripe Payment Links；Vercel/Netlify/Railway

## 关键路径 / URL

### 知识库（依据）

- `/Users/kun/learn/overseas/1-选方向/PRD-PRC照片工具-2026-08-09.md`（**开发输入**）
- `/Users/kun/learn/overseas/1-选方向/PRC照片规格表-2026-08-09.md`（**权威规格**，含官方来源链接）
- `/Users/kun/learn/overseas/1-选方向/实践-垂直选词-第8轮-2026-08-09.md`（找词过程）
- `/Users/kun/learn/overseas/docs/kun-profile.md`（画像 + 13 条原则 + 协作契约）
- `/Users/kun/learn/overseas/docs/adr/0008/0010/0011/0012`（方向三件套 + 触达策略）
- `/Users/kun/learn/overseas/1-选方向/实践-垂直选词-第6轮-2026-08-09.md`（GEO 基线实证：结构化/可引用/Trust 分水岭，小站拿 A 不难）

### 官方来源（规格核对）

- PRC 官网 FAQ：https://www.prc.gov.ph/prc-frequently-asked-questions
- PRC 线上 FAQ（照片要求第 X 条）：https://www.prc.gov.ph/frequently-asked-questions-prc-online-services
- 官方申请表 PDF：https://www.prc.gov.ph/uploaded/documents/applicationform.pdf
- LERIS：https://online.prc.gov.ph/

### 竞品参考（SERP 实测）

- PhotoAiD 2x2 页：https://photoaid.com/photo-2x2-inches
- PhotoGov：https://photogov.net/
- Passport-Photo.Online：https://passport-photo.online/en-ph/photo-2x2-inch
- YouTube 名字条教程：https://www.youtube.com/watch?v=fd7jmkMtBZo（Canva 2x2 nametag）

## 待办 / 未决

- 产品名未定（开发项目里定）
- 域名未定
- 支付接入细节（Stripe Links 即可，PayMongo V1.1）
- 触达计划：**M4 后再做**（ADR-0012），不要提前
- 知识库侧：第 8 轮笔记已记录；本 handoff 是临时桥，不提交 git

## 约束

- 开发**另开项目文件夹**（带 frontend 领域），本知识库只作查阅
- 规格矛盾以 PRC 官网原文为准，回写规格表 + PRD
- 不做通用护照照片 / AI 头像 / 真人修图 / 订阅
- 不编造 SEO 数字；量/KD 取证纪律（ADR-0007）
- 密钥不落盘；handoff 在 OS 临时目录
