> 持久学习副本：以下为2026-09-06原读取报告，保留当时的只读边界说明。原文链接已转为固定SHA；分组manifest现统一在[457项读取清单](读取清单.json)。最新执行路线见[总览](README.md)。

# Ego Lite SEO Space：五库全文学习索引

读取日期：2026-09-06。范围仅为下载到此目录的五个公开仓库；未安装依赖、未运行仓库代码、未调用任一外部 skill、未联网，也没有向 GitHub 写入任何内容。

## 版本与阅读边界

| 仓库 | 已核对 HEAD | 与 sources.json | 已全文读取的 SKILL.md |
|---|---|---|---:|
| zubair-trabzada--geo-seo-claude | 0a1bb52aba7b05e732c686743f4fa23de8121fa1 | 一致 | 16 |
| AgriciDaniel--claude-seo | a1480c7e590b16001bd9dc1627eacdcd44d580f9 | 一致 | 33 |
| AgriciDaniel--codex-seo | 97c59bcdac3c9538bf0e3ae456c1e73aa387f85a | 一致 | 30 |
| Bhanunamikaze--Agentic-SEO-Skill | 69199160e18372bc5cdf9ddec20ccb9fb1b509f1 | 一致 | 1 |
| TheCraigHewitt--seomachine | e818d5e38551a931333381d69c43da6e767ec775 | 一致 | 25 |

共发现并全文读取 105 个大小写不敏感匹配的 SKILL.md；实际文件名均为大写 SKILL.md。seo-read-manifest.json 只列这 105 个路径。

本笔记中的时长、数量、比例、流量或转化提升、价格、平台能力、案例结果、阈值以及 0–100 或加权评分，均只是作者主张或仓内自定义启发式，不能视作已验证的实效、当前规则或适用于任意站点的证明。本次没有对其做额外联网验证。下文中“评分”“基准”“权重”均应按此限制理解。

## 先读什么、各库放在什么阶段

| 顺序 | 阶段与学习目标 | 优先材料 | 读它的理由 |
|---:|---|---|---|
| 1 | 先建立可审计的诊断表达 | Agentic 的入口、审计 rubric、verifier 与报告说明 | 将发现写成 Finding / Evidence / Impact / Fix，并区分 confirmed、likely、hypothesis。 |
| 2 | 已有站点的基础 SEO 诊断 | Claude/Codex 的 seo、seo-audit、seo-technical、seo-schema、seo-sitemap | 对比总编排、技术、内容、结构化数据和 sitemap 的输入、输出与证据边界。 |
| 3 | 内容与检索意图规划 | Claude/Codex 的 plan、cluster、content 或 content-brief、competitor-pages、programmatic | 从关键词/页面/SERP 到 brief、专题结构与规模化页面质量门槛。 |
| 4 | GEO 专项 | zubair 的 geo-audit、citability、crawlers、llmstxt、platform-optimizer；再读 Claude/Codex 的 geo | 把传统可抓取、可引用、品牌面和 AI 答案页诊断拆开学习，避免把 readiness 当结果证明。 |
| 5 | 数据与持续变化 | Codex/Claude 的 drift、google、dataforseo，以及 seomachine 的 analytics-tracking | 学习 baseline、数据来源、成本/权限和复测思路；并不代表本次取过真实数据。 |
| 6 | 产品信息与转化 | seomachine 的 product-marketing-context、content-strategy、copy、CRO、pricing、onboarding | 适合已有清楚产品、用户和转化事件后阅读；先形成事实输入，再谈优化假设。 |
| 7 | 后期渠道与分发 | seomachine 的 email、social、paid、launch、referral、free-tool | 这些是渠道/生命周期框架，不应替代需求、站点可索引性或真实转化证据。 |

定位概览：Agentic-SEO-Skill 偏“证据格式与大审计”；Claude/Codex 两库是通用模块化 SEO 操作面，Codex 额外强调本地 runner/cache 架构；geo-seo-claude 是 GEO 诊断、报告和服务化工作流；seomachine 覆盖内容生产、产品营销与 CRO 生命周期。它们都是学习材料，彼此的规则和数字存在差异，不能拼成一套未经验证的强制标准。

## zubair-trabzada--geo-seo-claude（16）

| 原文 | 用途 | 输入、方法与产出要点 |
|---|---|---|
| [geo](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/geo/SKILL.md) | 全站 GEO/SEO 总入口。 | 输入站点/范围，按子项分派可见性、内容、技术等审计，汇总为行动优先级；它的多代理结构和总分只是仓内流程/启发式。 |
| [geo-audit](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-audit/SKILL.md) | 生成综合 GEO 体检。 | 输入 URL/页面范围，按内容、技术、可引用性、品牌等分面检查，产出 GEO-AUDIT-REPORT.md；页数上限、代理数和权重为作者流程设定。 |
| [geo-brand-mentions](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-brand-mentions/SKILL.md) | 看品牌在可被 AI/搜索发现的外部表面是否被提及。 | 输入品牌、竞争者和主题，按社区、视频、百科等来源盘点并给补面建议，产出品牌提及报告；来源比例/权重不是实效证明。 |
| [geo-citability](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-citability/SKILL.md) | 评估页面是否易被摘取/引用。 | 输入页面或内容，检查直接回答、自包含、结构、统计与独特信息，输出 GEO-CITABILITY-SCORE.md；五维分数和篇幅建议为仓内 rubric。 |
| [geo-compare](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-compare/SKILL.md) | 比较两个审计快照。 | 输入 baseline/current 报告，逐项算变化、找回退或改善，输出 delta/比较报告；它只比较报告内容，不证明线上效果。 |
| [geo-content](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-content/SKILL.md) | 做内容质量与 AI 可用性检查。 | 输入页面/文稿，按 E-E-A-T、AI 式模板痕迹、主题覆盖和引文可能性提出修订，产出内容报告。 |
| [geo-crawlers](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-crawlers/SKILL.md) | 检查常见 crawler 访问条件。 | 输入 robots、meta、header、页面配置，映射各 crawler 的允许/阻断状态，输出 GEO-CRAWLER-ACCESS.md；清单覆盖范围是作者定义。 |
| [geo-llmstxt](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-llmstxt/SKILL.md) | 分析或生成 llms.txt。 | 输入现有文件与站点资料，核对完整性、准确性、可用性后给分析或文件草案；其评分与“影响”属于仓内启发式。 |
| [geo-platform-optimizer](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-platform-optimizer/SKILL.md) | 按 AI Overview、ChatGPT、Perplexity、Gemini、Copilot 做 readiness 检查。 | 输入站点与目标平台，逐平台列内容/实体/技术缺口和优先级，输出平台准备度建议，不等于被任何平台引用。 |
| [geo-proposal](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-proposal/SKILL.md) | 把 GEO 服务发现整理为客户 proposal。 | 输入客户背景、需求和审计发现，按范围、套餐、交付物、报价/ROI 模板形成提案；任何价格或 ROI 是作者模板，不是已证实收益。 |
| [geo-prospect](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-prospect/SKILL.md) | 管理潜在客户研究。 | 输入公司/联系人线索，记录评分、状态与下一步到本地 prospect 数据；这是销售辅助流程，不是实际外联执行。 |
| [geo-report-pdf](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-report-pdf/SKILL.md) | 将报告排版成 PDF。 | 输入 Markdown 审计报告，走转换/排版流程输出 PDF；skill 与仓内文档对具体工具说法不完全一致，均只作为实现说明阅读。 |
| [geo-report](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-report/SKILL.md) | 汇总多个 GEO 子报告为面向业务的报告。 | 输入各检查输出，提取优先级、路线图与摘要，产出综合报告；预测、商业影响和分数均不是独立证明。 |
| [geo-schema](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-schema/SKILL.md) | 检测、校验或建议 JSON-LD。 | 输入 HTML/页面实体资料，查现有 schema、缺口和可生成的 JSON-LD，输出校验/建议；不应凭空编造实体或评价。 |
| [geo-technical](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-technical/SKILL.md) | 从技术面审计 GEO 相关准备度。 | 输入页面或站点，检查索引、性能、渲染、结构、可访问性等，产出技术报告；分类和得分是仓内诊断框架。 |
| [geo-update](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/skills/geo-update/SKILL.md) | 更新本工具包副本。 | 输入本地安装状态，描述同步/更新与兼容性检查步骤；本次未执行该工作流。 |

补充全文材料：根目录 [README.md](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/README.md)、[architecture.md](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/docs/architecture.md)、[skills-and-agents.md](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/docs/skills-and-agents.md)、[scoring-methodology.md](https://github.com/zubair-trabzada/geo-seo-claude/blob/0a1bb52aba7b05e732c686743f4fa23de8121fa1/docs/scoring-methodology.md) 和 agents 说明。仓内文档称“14 subskills”，实际物理集合为 15 个子 skill 加 1 个 geo 入口，故清单以文件系统的 16 为准。

## AgriciDaniel--claude-seo（33）

| 原文 | 用途 | 输入、方法与产出要点 |
|---|---|---|
| [seo 总入口](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo/SKILL.md) | 路由全站 SEO 工作。 | 输入域名/目标，检查已有结果并编排审计、内容、技术等子流程，产出汇总与后续动作；健康分为仓内启发式。 |
| [seo-audit](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-audit/SKILL.md) | 通用 SEO 审计。 | 输入网站/范围，抓取并按技术、内容、页面、schema、性能等组织发现，输出审计报告和修复优先级。 |
| [seo-backlinks](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-backlinks/SKILL.md) | 做外链资料充分性、差距和机会分析。 | 输入 backlink 数据/竞争者资料，先判断数据是否足够，再输出缺口与行动建议；不能用少量数据伪造量化结论。 |
| [seo-cluster](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-cluster/SKILL.md) | 规划关键词专题集群。 | 输入关键词和 SERP 重叠资料，按意图/重叠建立 hub-spoke、URL/内链建议，输出 cluster map。 |
| [seo-competitor-pages](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-competitor-pages/SKILL.md) | 规划比较页、替代页和竞争页。 | 输入产品、竞争者和受众，选择页面类型、证据要求与内容结构，输出页面计划而非虚构比较事实。 |
| [seo-content-brief](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-content-brief/SKILL.md) | 将关键词研究变成可写 brief。 | 输入关键词、SERP/受众资料，形成意图、角度、标题层级、问题、证据与内链要求。 |
| [seo-content](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-content/SKILL.md) | 审阅或改善页面内容。 | 输入 URL/草稿，按 helpfulness、E-E-A-T、事实支撑、结构和意图找缺口，输出修订建议/报告。 |
| [seo-dataforseo](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-dataforseo/SKILL.md) | 通过 DataForSEO 取研究数据。 | 输入关键词/域名/任务，按成本和范围选择端点，规范化为研究结果；需真实凭据，且本次没有调用。 |
| [seo-drift](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-drift/SKILL.md) | 监测 SEO 基线变化。 | 输入 crawl/旧基线，写入 SQLite 后按多条规则比对标题、canonical、robots、链接等，输出 drift 报告。 |
| [seo-ecommerce](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-ecommerce/SKILL.md) | 审计商品、类目和电商结构。 | 输入电商 URL/站点，检查商品资料、schema、筛选、缺货页与内部结构，输出修复清单。 |
| [seo-flow](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-flow/SKILL.md) | 提供任务式 SEO 提示流程。 | 输入目标/阶段，选择一组有次序的 prompts，产出下一步工作序列；“41 prompts”等数量只是作者资料。 |
| [seo-geo](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-geo/SKILL.md) | 将 SEO 内容按 AI 回答/引用场景复核。 | 输入页面/主题，检查答案格式、实体、来源和传统 SEO 基础，输出 GEO 建议；有关 llms.txt 或平台机制的说法未在本次外验。 |
| [seo-google](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-google/SKILL.md) | 连接 Google 数据面。 | 输入授权状态、站点和查询范围，规定 GSC/Google 数据请求与权限分层，输出数据/诊断；没有凭据就应停在说明。 |
| [seo-hreflang](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-hreflang/SKILL.md) | 校验多语言 hreflang。 | 输入区域语言 URL 集和页面标签，检查 reciprocal、x-default、canonical 与冲突，输出矩阵/修复建议。 |
| [seo-image-gen](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-image-gen/SKILL.md) | 为 SEO 页面规划或生成配图。 | 输入页面主题、品牌和版位，形成图像 brief/调用路径及 alt/文件名要求；生成能力取决于外部 provider，本次未调用。 |
| [seo-images](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-images/SKILL.md) | 审计既有图片 SEO。 | 输入页面/图片集合，检查格式、尺寸、alt、lazy-load、可发现性和结构化数据，输出图片改进清单。 |
| [seo-local](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-local/SKILL.md) | 审计本地业务网站信号。 | 输入地域、服务与站点资料，检查 NAP、地点页、本地实体/内容和引用面，输出本地 SEO 计划。 |
| [seo-maps](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-maps/SKILL.md) | 面向地图/商家资料做诊断。 | 输入商家/地点与 API 可用性，按资料完整度、评论、类别和竞争结果给建议；API 层级、费用说法均为仓内说明。 |
| [seo-page](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-page/SKILL.md) | 做单页页面内 SEO 检查。 | 输入 URL/HTML 和目标词，检查 title、heading、正文、链接、canonical、媒体等，输出页面修复报告。 |
| [seo-plan](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-plan/SKILL.md) | 形成 SEO 项目计划。 | 输入业务目标、网站现状和资源，按依赖与影响分阶段列 backlog、优先级和成功信号。 |
| [seo-programmatic](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-programmatic/SKILL.md) | 规划规模化页面。 | 输入模板、数据、关键词和目标，审查唯一价值、数据质量、索引风险和 QA gate，输出结构/样本/上线计划。 |
| [seo-schema](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-schema/SKILL.md) | 管理结构化数据。 | 输入页面实体与已有 JSON-LD，检测、校验、选择适当类型并生成建议，输出 schema 报告/片段。 |
| [seo-sitemap](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-sitemap/SKILL.md) | 审计或生成 XML sitemap。 | 输入 sitemap/URL 集，核对索引性、canonical、状态与分片，输出问题和 sitemap 建议。 |
| [seo-sxo](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-sxo/SKILL.md) | 将 SERP 意图与页面体验结合。 | 输入目标查询、SERP 和页面，反推合适页面类型、用户任务、信息结构与转化摩擦，输出 SXO brief；分数为内部模型。 |
| [seo-technical](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-technical/SKILL.md) | 技术 SEO 审计。 | 输入站点/crawl，按爬取、渲染、索引、canonical、性能、HTTP 与站点结构分组，产出按风险排序的报告。 |
| [seo-ahrefs 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/ahrefs/skills/seo-ahrefs/SKILL.md) | 使用 Ahrefs 数据做关键词/外链研究。 | 输入项目、域名或关键词，定义查询和规范输出；依赖外部授权/API，本次没有使用。 |
| [seo-image-gen Banana 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/banana/skills/seo-image-gen/SKILL.md) | 借 Banana 生成图像。 | 输入图像 brief，组织 provider 调用和资产交接；外部能力/费用不在本次验证范围。 |
| [seo-bing 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/bing-webmaster/skills/seo-bing/SKILL.md) | 查询 Bing Webmaster 信号。 | 输入站点和指标，规定认证与数据查询，输出可解释的发现；本次未认证或请求。 |
| [seo-dataforseo 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/dataforseo/skills/seo-dataforseo/SKILL.md) | 扩展版 DataForSEO 数据接口。 | 输入研究任务，选择端点、限制成本并输出数据摘要；与核心同名 skill 是独立文件。 |
| [seo-firecrawl 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/firecrawl/skills/seo-firecrawl/SKILL.md) | 通过 Firecrawl 取页面/crawl 材料。 | 输入 URL/范围，规定抓取、清洗和输出形态；依赖外部服务，本次未调用。 |
| [seo-profound 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/profound/skills/seo-profound/SKILL.md) | 使用 Profound 研究 AI 可见性/引用。 | 输入品牌、主题或 prompts，组织查询和报告；平台结果与效果均未外验。 |
| [seo-seranking 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/seranking/skills/seo-seranking/SKILL.md) | 使用 SE Ranking 读取排名研究。 | 输入项目/关键词/日期，约束查询与结果输出；需外部连接。 |
| [seo-unlighthouse 扩展](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/extensions/unlighthouse/skills/seo-unlighthouse/SKILL.md) | 用 Unlighthouse 做批量浏览器性能审计。 | 输入 URL 列表/配置，描述运行和报告解释；本次没有运行任何浏览器或脚本。 |

补充全文材料：根 [README.md](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/README.md)、[AGENTS.md](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/AGENTS.md) 与 [CLAUDE.md](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/CLAUDE.md)。扩展是可选 provider 接口，不是本次已连接或已验收的服务。

## AgriciDaniel--codex-seo（30）

| 原文 | 用途 | 输入、方法与产出要点 |
|---|---|---|
| [seo 总入口](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo/SKILL.md) | Codex 版总路由。 | 输入域名/目标，检查 .seo-cache 并分派子模块，汇总健康与行动；health score 是仓内权重，不是实测排名预测。 |
| [seo-audit](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-audit/SKILL.md) | 综合网站审计。 | 输入域名/页面，按技术、内容、页面、schema、性能、图片和 AI 准备度输出审计和优先级。 |
| [seo-backlinks](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-backlinks/SKILL.md) | 外链分析。 | 输入已获数据/竞争者，做资料充分性、质量、差距与机会判断，输出可追溯建议。 |
| [seo-cluster](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-cluster/SKILL.md) | 专题集群设计。 | 输入关键词、SERP 重叠和现有 URL，构建 hub-spoke、意图分组和内链图。 |
| [seo-competitor-pages](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-competitor-pages/SKILL.md) | 比较/替代页面策略。 | 输入竞争对象、产品资料、受众与证据，输出页面选择、内容结构和事实核验要求。 |
| [seo-content](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-content/SKILL.md) | 内容审计与增强。 | 输入草稿或 URL，按意图、E-E-A-T、来源、结构和可读性给问题与修订顺序。 |
| [seo-dataforseo](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-dataforseo/SKILL.md) | 核心 DataForSEO 接口。 | 输入关键词/域名/任务，规划受成本约束的查询及标准化输出；本次未调用 API。 |
| [seo-drift](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-drift/SKILL.md) | 站点 SEO 漂移检测。 | 输入当前 crawl 与 SQLite 基线，按仓内规则找元数据、canonical、链接和索引变化，输出差异报告。 |
| [seo-ecommerce](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-ecommerce/SKILL.md) | 电商 SEO 专项审计。 | 输入商品/类目/站点，检查结构、筛选、库存、产品资料和 schema，输出风险与行动清单。 |
| [seo-firecrawl](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-firecrawl/SKILL.md) | 核心 Firecrawl 抓取接口。 | 输入 URL 或 crawl 范围，规定抓取、内容清洗、缓存/结果交接；没有外部请求即无真实结果。 |
| [seo-flow](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-flow/SKILL.md) | SEO 任务 prompt 流。 | 输入目标和所处阶段，选择阶段性提示/交接，输出工作序列；提示数量为仓内资料。 |
| [seo-geo](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-geo/SKILL.md) | GEO/AEO 内容诊断。 | 输入页面/主题，检查明确回答、实体、可引用段落、来源与基础 SEO，输出 readiness 建议，不承诺 AI 引用。 |
| [seo-google](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-google/SKILL.md) | Google 数据访问策略。 | 输入授权状态/站点/问题，明确何时用 GSC 或 Google 数据，产出数据驱动检查；本次无认证调用。 |
| [seo-hreflang](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-hreflang/SKILL.md) | 国际化标签检查。 | 输入语言地域 URL/HTML，校验 reciprocal、canonical、x-default 和覆盖缺口，输出矩阵与修复建议。 |
| [seo-image-gen](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-image-gen/SKILL.md) | 图像生成与 SEO 资产规划。 | 输入主题、版位、品牌限制，形成 prompt/文件/alt 交接；外部图像生成未执行。 |
| [seo-images](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-images/SKILL.md) | 图片 SEO 审计。 | 输入页面/图像，检查格式、传输、alt、尺寸、lazy load 和 image sitemap/schema，输出改进清单。 |
| [seo-local](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-local/SKILL.md) | 本地业务可见性审计。 | 输入地点、服务、NAP/站点，分析本地页面、实体资料、内容和引用机会，输出计划。 |
| [seo-maps](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-maps/SKILL.md) | Google Maps/商家档案流程。 | 输入商家与地点，按可用 API/资料分析商家信息、类别、评价和竞争环境；层级、费用及结果未验证。 |
| [seo-page](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-page/SKILL.md) | 单页 SEO 检查。 | 输入目标页面和关键词，检查 metadata、heading、正文、链接、媒体与 URL，输出页面级任务。 |
| [seo-performance](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-performance/SKILL.md) | 性能与 CWV 检查。 | 输入页面/现场或实验数据，区分 field 与 lab，避免推断 INP，输出性能问题、证据和修复建议。 |
| [seo-plan](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-plan/SKILL.md) | SEO 路线图。 | 输入商业目标、站点、资源、现有资料，按依赖、影响和阶段输出计划/backlog。 |
| [seo-programmatic](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-programmatic/SKILL.md) | 规模化 SEO 页面方案。 | 输入数据源、模板、关键词和样本，评估数据防御性、页面唯一价值、质量门槛与发布 QA。 |
| [seo-schema](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-schema/SKILL.md) | schema 检测与设计。 | 输入 HTML/实体资料，发现已有标记、校验并输出恰当 JSON-LD 建议，不应加入无法证明的字段。 |
| [seo-sitemap](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-sitemap/SKILL.md) | XML sitemap 检查/生成。 | 输入 sitemap 或 URL 清单，筛掉不可索引/非 canonical URL，输出修复或生成建议。 |
| [seo-sxo](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-sxo/SKILL.md) | 搜索体验优化。 | 输入查询、SERP 和页面，判断页面型态/任务/用户故事/摩擦，输出 SXO 改进；自定义 SXO 分数不是结果证明。 |
| [seo-technical](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-technical/SKILL.md) | 技术 SEO 诊断。 | 输入 crawl/网站，按爬取、渲染、索引、HTTP、canonical、性能与结构输出报告。 |
| [seo-visual](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-visual/SKILL.md) | 视觉和移动端审查。 | 输入页面截图/浏览器结果，评估首屏、层级、可读性、CTA、移动布局，输出视觉问题和证据需求。 |
| [seo-image-gen Banana 扩展](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/extensions/banana/skills/seo-image-gen/SKILL.md) | Banana provider 的图像生成扩展。 | 输入图像 brief 后定义 provider 调用和资产回传；与核心同名 skill 是独立文件，未调用。 |
| [seo-dataforseo 扩展](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/extensions/dataforseo/skills/seo-dataforseo/SKILL.md) | DataForSEO provider 扩展。 | 输入研究目标，按端点、凭据、成本及结果格式操作；与核心同名 skill 独立，未调用。 |
| [seo-firecrawl 扩展](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/extensions/firecrawl/skills/seo-firecrawl/SKILL.md) | Firecrawl provider 扩展。 | 输入抓取范围，约束调用与内容输出；与核心同名 skill 独立，未调用。 |

补充全文材料：根 [README.md](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/README.md)、[AGENTS.md](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/AGENTS.md)、[ARCHITECTURE.md](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/docs/ARCHITECTURE.md)、[DEMO-RUNBOOK.md](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/docs/DEMO-RUNBOOK.md)、[API-READINESS-MATRIX.md](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/docs/API-READINESS-MATRIX.md)。仓内“测试数”“runner 可用性”“provider readiness”等文字没有在本次执行中运行或验证。

## Bhanunamikaze--Agentic-SEO-Skill（1 个 SKILL.md；另读 16 个实际子工作流）

| 原文 | 用途 | 输入、方法与产出要点 |
|---|---|---|
| [Agentic-SEO-Skill 入口](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/SKILL.md) | LLM-first 的综合 SEO 审计入口。 | 输入站点/范围，组织 16 个资源子流程和审阅角色；统一以 Finding / Evidence / Impact / Fix 报告，标 confidence，并由 verifier 去重/处理矛盾。总分、代理/脚本数量均为仓内设计。 |

下列文件不是 SKILL.md，故不放入 manifest；但它们是该唯一入口实际承载的子工作流，均已全文读取。

| 实际子工作流原文 | 用途 | 输入、方法与产出要点 |
|---|---|---|
| [seo-audit](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-audit.md) | 总体网站审计。 | 聚合技术、内容、页面、性能、图片与 AI 面，输出证据化审计报告。 |
| [seo-aeo](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-aeo.md) | 答案引擎优化。 | 输入查询/页面，关注摘录、PAA、知识图谱和直接回答结构，输出 AEO 缺口。 |
| [seo-article](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-article.md) | 文章审阅/生产辅助。 | 输入主题/草稿/资料，组织意图、结构、来源和质量门，产出写作/改进建议。 |
| [seo-competitor-pages](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-competitor-pages.md) | 比较与替代页。 | 输入竞争对象和产品事实，形成页面结构、事实要求和更新点。 |
| [seo-content](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-content.md) | 内容质量审计。 | 输入页面/草稿，按帮助性、经验、证据、结构和意图输出可核对发现。 |
| [seo-geo](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-geo.md) | 生成式搜索优化。 | 输入内容/主题，检查 AI 引用面、实体、直接答案和多表面资料，输出 readiness 建议。 |
| [seo-github](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-github.md) | GitHub 仓库 SEO。 | 输入仓库，检查 metadata、README、社区资料、查询基准和流量线索，输出仓库可发现性报告。 |
| [seo-hreflang](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-hreflang.md) | 国际 SEO。 | 输入地区语言页面及标签，校验 annotations、canonical 与 fallback。 |
| [seo-images](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-images.md) | 图片 SEO。 | 输入图片/页面，检查 alt、尺寸、格式、传输和结构化关联，输出优化建议。 |
| [seo-links](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-links.md) | 内外链检查。 | 输入站点/URL，找断链、孤儿页、锚文本和权威/相关性问题，输出链接任务。 |
| [seo-page](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-page.md) | 页面内诊断。 | 输入页面/关键词，检查 metadata、heading、内容、意图、链接和可访问性。 |
| [seo-plan](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-plan.md) | SEO 规划。 | 输入业务目标和审计资料，按阶段/依赖输出执行路线图。 |
| [seo-programmatic](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-programmatic.md) | 程序化页面质量计划。 | 输入模板/数据/目标词，做可扩展性、唯一价值、质量 gate 和抽检规划。 |
| [seo-schema](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-schema.md) | 结构化数据。 | 输入页面实体/已有标记，检查类型和字段、输出验证/补充建议。 |
| [seo-sitemap](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-sitemap.md) | sitemap 诊断。 | 输入 XML/URL 集，检查格式、范围、索引条件和更新策略。 |
| [seo-technical](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/skills/seo-technical.md) | 技术诊断。 | 输入 crawl/页面证据，按索引、渲染、性能、HTTP、结构与安全性分项输出。 |

另全文读取 [README.md](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/README.md)、[Audit-Workflow.md](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/wiki/Audit-Workflow.md)、[Reports-and-Outputs.md](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/wiki/Reports-and-Outputs.md)、[Command-Reference.md](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/wiki/Command-Reference.md)、resources/agents 的 10 个角色说明、resources/references 的全部参考说明与 [scoring.json](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/blob/69199160e18372bc5cdf9ddec20ccb9fb1b509f1/resources/config/scoring.json)。其 25/20/15 等权重和声称的脚本/流程能力只能当内部 rubric。

## TheCraigHewitt--seomachine（25）

| 原文 | 用途 | 输入、方法与产出要点 |
|---|---|---|
| [ab-test-setup](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/ab-test-setup/SKILL.md) | 设计 A/B 测试。 | 输入问题、基线、流量和约束，预先写假设、主/次/护栏指标、样本和停止规则，输出测试文档；样本表和显著性表述为作者教学资料。 |
| [analytics-tracking](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/analytics-tracking/SKILL.md) | 规划分析事件与质量检查。 | 输入业务决策、现有工具与隐私约束，倒推 event、properties、trigger、UTM、验证项，输出 tracking plan。 |
| [competitor-alternatives](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/competitor-alternatives/SKILL.md) | 写/审竞品和替代方案页面。 | 输入产品、竞争者、受众、可证明资料，选择 comparison/alternative 页面结构并规定准确性与更新；其中 schema 建议可能与其他库的较新限制不一致。 |
| [content-strategy](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/content-strategy/SKILL.md) | 建内容策略。 | 输入产品背景、客户旅程、现有内容和资源，划分 searchable/shareable、内容支柱、专题和优先级，输出内容 roadmap；其 40/30/20/10 想法分数是内部启发式。 |
| [copy-editing](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/copy-editing/SKILL.md) | 多轮编辑既有营销文案。 | 输入文案和品牌资料，按清晰、语气、利益、证明、具体、情感、降风险七轮检查，输出逐处问题和建议。 |
| [copywriting](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/copywriting/SKILL.md) | 新写营销页面文案。 | 输入页面目的、受众、产品、证据和流量上下文，按价值主张/版块/CTA 输出页面文案、备选标题和 meta。 |
| [email-sequence](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/email-sequence/SKILL.md) | 生命周期邮件序列。 | 输入触发、受众、目标和现有沟通，设计每封邮件的单一任务、时序、分段、退出条件和指标计划。 |
| [form-cro](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/form-cro/SKILL.md) | 优化非注册表单。 | 输入表单种类、字段、流失和业务用途，检查字段成本、顺序、错误、移动端、信任和测量，输出改版与假设。 |
| [free-tool-strategy](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/free-tool-strategy/SKILL.md) | 工具化营销评估。 | 输入产品、受众痛点、目标与维护资源，比较 calculator/generator/analyzer 等，评估获客、SEO、交接和 MVP；打分阈值为作者框架。 |
| [launch-strategy](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/launch-strategy/SKILL.md) | 规划产品/功能发布。 | 输入产品、受众、渠道、时点和资源，以 owned/rented/borrowed 渠道与五阶段发布组织清单；案例数字/排名均为作者材料。 |
| [marketing-ideas](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/marketing-ideas/SKILL.md) | 按阶段挑选增长点子。 | 输入产品、受众、阶段、预算和已有尝试，从作者整理的 139 类点子中筛 3–5 个，输出匹配理由、第一步和资源需求；“proven”是作者主张。 |
| [marketing-psychology](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/marketing-psychology/SKILL.md) | 用心理模型审视营销表达。 | 输入受众/场景/目标，匹配行为与说服模型、风险和实验想法，输出适用的沟通/测试建议；模型集合不是对具体产品效果的证明。 |
| [onboarding-cro](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/onboarding-cro/SKILL.md) | 优化注册后的激活。 | 输入产品、aha moment、漏斗和流失点，减少到价值的步骤，设计首会话、空状态、checklist、邮件协同与指标。 |
| [page-cro](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/page-cro/SKILL.md) | 审计营销页面转化。 | 输入页面类型、主转化和流量来源，按价值主张、标题、CTA、层级、信任、异议、摩擦输出 quick wins、重大变更和测试假设。 |
| [paid-ads](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/paid-ads/SKILL.md) | 规划付费广告。 | 输入目标、预算、产品、受众、落地页、像素和历史数据，输出平台选择、账户结构、创意、受众、归因与复盘；平台效果/比例为作者教学基准。 |
| [paywall-upgrade-cro](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/paywall-upgrade-cro/SKILL.md) | 优化产品内升级点。 | 输入免费/付费边界、触发点、用户已获价值和定价，设计 feature gate、限额/试用到期页面、逃生出口和实验指标。 |
| [popup-cro](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/popup-cro/SKILL.md) | 设计弹窗/横幅。 | 输入弹窗目的、触发、流量、移动端和表现，定义触发、频控、文案、可访问性、隐私和冲突规则；转化基准为作者主张。 |
| [pricing-strategy](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/pricing-strategy/SKILL.md) | 定价与打包框架。 | 输入客户、价值、替代品、现有 ARPU/流失和目标，研究 value metric、tier、价格测试和调价方式，输出定价决策清单；任何门槛/折扣是作者启发式。 |
| [product-marketing-context](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/product-marketing-context/SKILL.md) | 先沉淀可复用产品营销上下文。 | 输入定位、ICP、JTBD、竞争者、异议、客户语言、证据和目标，输出 .claude/product-marketing-context.md，供其他营销 skill 先读取。 |
| [programmatic-seo](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/programmatic-seo/SKILL.md) | 程序化 SEO 策略。 | 输入数据、模板、搜索任务、产品关联和维护能力，评估数据防御性、页面质量、索引策略、样本和 QA，输出 MVP 与扩展计划。 |
| [referral-program](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/referral-program/SKILL.md) | 推荐/联盟项目。 | 输入 LTV、CAC、分享性、激励预算和现有表现，设计触发—分享—转化—奖励闭环、反欺诈、归因和邮件；LTV/流失提升数字是作者主张。 |
| [schema-markup](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/schema-markup/SKILL.md) | 选择和生成 schema。 | 输入页面类型、实体事实与目标，选择 JSON-LD 类型、生成/校验和部署清单；其 FAQPage/HowTo 等泛化建议应与当前官方规则另行核验。 |
| [seo-audit](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/seo-audit/SKILL.md) | 传统站点 SEO 审计。 | 输入站点背景、范围和 GSC/analytics 可用性，按 crawl/index、技术、页面、内容、链接输出带 Evidence/Fix/Priority 的报告。 |
| [signup-flow-cro](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/signup-flow-cro/SKILL.md) | 优化注册/试用路径。 | 输入字段、步骤、流失、合规和注册后动作，审计字段、认证、错误、移动端、验证、漏斗与测试假设。 |
| [social-content](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/.claude/skills/social-content/SKILL.md) | 社媒内容与复用。 | 输入目标、平台、受众、品牌、资源与已有内容，设计支柱、hooks、内容日历、互动、复盘和跨平台改写；频率/案例为作者框架。 |

补充全文材料：[README.md](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/README.md)、[CLAUDE.md](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/CLAUDE.md)、[QUICK-START.md](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/QUICK-START.md)、[data_sources/README.md](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/data_sources/README.md) 与 [context/seo-guidelines.md](https://github.com/TheCraigHewitt/seomachine/blob/e818d5e38551a931333381d69c43da6e767ec775/context/seo-guidelines.md)。README 写“26 marketing skills”，物理集合为 25；manifest 以实际文件为准。data source、WordPress、CLI 与 API 内容仅作流程阅读，均未执行。

## 跨库可复用的阅读结论与限制

1. 更有学习价值的是“输入是否明确、证据怎样留、输出如何可复核、何时应停止”的结构，不是把任何单一自定义分数当成 SEO 成果。
2. 三个 GEO 体系都把可抓取、实体/来源、直接回答、内容结构拆成检查项，但没有一个文本本身能够证明某平台会引用页面。应将 readiness、实际抓取、实际引用、真实转化分开记录。
3. schema、FAQ/HowTo、llms.txt、篇幅、关键词密度、性能阈值和渠道频率在库间存在不同或较泛化的说法。遇到要实施的决定，需在另一个已授权工作中以当前一手规则和目标环境验证。
4. provider 扩展、API、抓取、浏览器审计、发布、CRM 和外联均只是可读的工作流描述；本次没有调用，不能从本笔记推断权限、凭据、成本、连通性或结果。

完整已读文件集合见同目录 [seo-read-manifest.json](读取清单.json)。
