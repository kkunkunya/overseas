> 持久学习副本：以下为2026-09-06原读取报告，保留当时的只读边界说明。原文链接已转为固定SHA；分组manifest现统一在[457项读取清单](读取清单.json)。最新执行路线见[总览](README.md)。

# Aaron SEO/GEO Space 学习笔记

## 范围、版本与证据边界

本次只做静态阅读和索引：未安装 skill、未调用其工作流、未运行仓库代码、未写源仓库，也未做外网效果验证。

| 仓库 | 已核对 HEAD | SKILL.md 全文数 | 定位 |
| --- | --- | ---: | --- |
| `aaron-he-zhu--aaron-marketing-skills` | `888dd38edbd43e7eaeeb4ba053d6c290fb21b89d` | 120 | 当前 v20.1.0 的七个营销领域加八个 protocol skill |
| `aaron-he-zhu--seo-geo-claude-skills` | `3a1578a63cdde8037ee16d32a3ea9f808eae6bd0` | 20 | archived v9.9.12 的迁移/指针层，链接到前者的当前 skill |

**数值与评分解释。** 下文中所有“80/40 项”、权重、阈值、分级、版本、技能数量及“优先级”均是源作者的框架定义或自述；没有独立验证其排名、AI 引用、收入、转化或其他实效。源仓库自己的 [scoring-semantics](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/scoring-semantics.md) 也明确把八套框架定位为 advisory，在完成预注册的可靠性和结果校准研究前不得当作业务结果预测。

## 两仓关系、适用阶段与高价值阅读顺序

1. 先读 [共享执行契约](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/skill-contract.md)、[评分语义](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/scoring-semantics.md)、[测量协议](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/measurement-protocol.md)。它们分别解释边界/权限、Unknown 与分数、以及 proxy 与真实结果的差别。
2. SEO/GEO 学习主线用当前仓的 **Survey → Implement → Tune → Evaluate**：从关键词/竞争/搜索结果事实，到内容/标记/页面方案，再到结构/技术/质量检查，最后才观察排名、站外信号和域名层面。
3. 若学习其他增长环节，按系统架构的 L1→L3 阅读：[narrative](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/README.md) 先定可证实的叙事，随后 SEO、social、email、ad、influencer 作为渠道，最后 [launch](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/README.md) 作为时限发布协调。
4. 八个 protocol skill 是“谁拥有何种事实”的读法，不是普通产出 skill：普通 skill 的笔记、意图和 proposal 不自动成为 canonical truth。细节见 [state model](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/state-model.md)。
5. 旧仓的 20 个文件适合最后读作迁移地图：它们并非 20 套独立的当前执行流程。尤其旧的 `entity-optimizer` 指向历史名称，当前仓实际已有的是 [entity-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/entity-registry/SKILL.md)，不能擅自视为一一同义。

## 当前仓：`aaron-he-zhu--aaron-marketing-skills`（120）

### SEO/GEO：Survey

- [keyword-research](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/keyword-research/SKILL.md)：输入种子词、市场/地区、目标及可用自有数据；输出按意图、集群、GEO 机会整理的优先 brief。来源不足时应标记未评分；机会公式和权重是作者方法，不是效果证明。
- [competitor-analysis](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/competitor-analysis/SKILL.md)：输入自身和 3–5 个竞争对象的可核查材料；输出内容、结构、技术、链接与 GEO 信号的对照及短中长期行动。没有数据的格子保留 N/A 或 Estimated。
- [serp-analysis](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/serp-analysis/SKILL.md)：输入精确 query、地区、设备和观察时间；输出搜索意图、结果构成、特征与竞争难度说明。其权重化“True Difficulty”是作者诊断，不可当排名保证。
- [content-gap-analysis](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/content-gap-analysis/SKILL.md)：输入自身/竞品内容清单和用户旅程；输出主题、格式、覆盖、GEO 与旅程缺口及内容日历，不把缺口本身当成需求或排名结果。

### SEO/GEO：Implement

- [content-writer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/content-writer/SKILL.md)：输入已确认的 brief、受众、证据和当前内容；输出新稿或刷新计划，并以自有基线说明变化。它不替代内容质量 gate 或真实搜索表现。
- [geo-content-optimizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/geo-content-optimizer/SKILL.md)：输入页面/问题和来源；输出可独立抽取的定义、问答、表格、结构化信息及前后 GEO 覆盖对照。可提取性只是 proxy，不能证明 AI 会无提示引用。
- [serp-markup-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/serp-markup-builder/SKILL.md)：输入页面事实和页面类型；输出 title/meta/OG/canonical/schema 方案与验证清单。标记正确不保证 rich result、抓取或排名。
- [page-play-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/page-play-builder/SKILL.md)：输入目标、实体、竞争信息和约束；输出 programmatic、comparison、alternative、parasite/local 等页面玩法的安全计划，含薄内容和 site-reputation-abuse 防护，而非直接发布。

### SEO/GEO：Tune

- [content-quality-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/content-quality-auditor/SKILL.md)：输入一项冻结内容证据与上下文；输出 CORE-EEAT typed audit。80 项、权重、veto 和分数是作者质量框架，audit 本身不预测排名或引用。
- [on-page-seo-checker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/on-page-seo-checker/SKILL.md)：输入已渲染页面与目标 query；输出 11 类 on-page 检查及 P0/P1/P2 修复单。结构通过不等于 EEAT、索引或业务成效。
- [site-structure-optimizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/site-structure-optimizer/SKILL.md)：输入 URL/页面库存及主题关系；输出信息架构、内链图与优先次序。其结构评分只诊断结构，不是发布/排名 gate。
- [technical-seo-checker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/technical-seo-checker/SKILL.md)：输入站点、环境和抓取证据；输出抓取、索引、渲染、CWV、sitemap 等九步技术检查，区分 raw 与 rendered；静态检查不是被搜索引擎实际收录的证据。

### SEO/GEO：Evaluate

- [domain-authority-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/domain-authority-auditor/SKILL.md)：输入域名、peer cohort、市场/阶段和可观测证据；输出 CITE audit。40 项与各阈值必须相对同类 cohort 解释，且源文将它标为 advisory。
- [offsite-signal-analyzer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/offsite-signal-analyzer/SKILL.md)：输入反链、提及、AI referral 等带日期来源；输出站外信号和 CITE 输入。referral 不是 AI 引用/因果证明。
- [performance-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/performance-monitor/SKILL.md)：输入来源、周期、控制对象和指标；输出定期报告、异常提示和因果假设，明确 observation 与 explanation 分离。
- [rank-tracker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/rank-tracker/SKILL.md)：输入 query、地区、设备、基线和时间窗；输出可比的位置变化与可能原因。上下文或基线不一致、数据陈旧时不能声称排名变化。

### Protocol：真相、同意与记忆边界

- [channel-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/channel-registry/SKILL.md)：输入渠道身份、状态请求与证据；输出/处理渠道 proposal 与受控状态转换。它是渠道 canonical owner，普通渠道计划不能越权写真相。
- [consent-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/consent-registry/SKILL.md)：输入最小化、假名化的同意/抑制事实；输出 consent 状态查询或协议内 proposal。其 suppress 是 deny-only 安全路径，不能变成发送授权。
- [creator-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/creator-registry/SKILL.md)：输入创作者身份、证据和变更提议；输出 creator registry 的受控状态/投影读取或 proposal，不以表格草稿冒充 canonical 记录。
- [entity-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/entity-registry/SKILL.md)：输入可证实的品牌、人、产品等实体材料；输出实体 proposal/读模型，强调不重复/不把不可靠材料写成实体真相。
- [launch-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/launch-registry/SKILL.md)：输入发布阶段、日期、embargo 和证据；输出 launch 状态的唯一 owner 路径。proposal、SHIP、runbook 或 URL 都不是已接受的发布事实。
- [memory-management](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/memory-management/SKILL.md)：输入记忆对象和保留/删除请求；输出 HOT/WARM/COLD 生命周期判断或授权路径，不能代替 registry owner 接受业务事实。
- [narrative-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/narrative-registry/SKILL.md)：输入 narrative canon/版本/claims 依赖；输出叙事 canonical 状态的 proposal 或读取，要求版本与 claims 边界清晰。
- [offer-claims-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/offer-claims-registry/SKILL.md)：输入产品/比较/价格等声明及证据；输出 claims proposal/状态，未证实主张应保持 `[needs source]`，不因营销文案而自动批准。

### Paid Ads：Research

- [audience-segment-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/research/audience-segment-builder/SKILL.md)：输入自有 CRM/GA4 信号、漏斗和 suppression 约束；输出可审核的人群段、排除规则和证据说明，不暴露原始 PII。
- [campaign-architect](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/research/campaign-architect/SKILL.md)：输入目标、产品、预算约束和查询/受众材料；输出 campaign/group/match/negative/cannibalization 架构及完整度检查。
- [product-feed-optimizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/research/product-feed-optimizer/SKILL.md)：输入产品 feed 与事实来源；输出 title、属性、GTIN、可用性与问题清单，禁止为 feed 捏造产品/比较主张。
- [search-term-miner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/research/search-term-miner/SKILL.md)：输入 search-term export；输出 add/negative/move 分类和 n-gram 洞见，记录来源窗口，不把单次词表当长期因果。

### Paid Ads：Orchestrate

- [ad-creative-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/orchestrate/ad-creative-builder/SKILL.md)：输入受众、offer、canon/claims 和 placement；输出资产矩阵、文案和落地页匹配草案，主张需与事实/声明账本绑定。
- [ad-test-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/orchestrate/ad-test-designer/SKILL.md)：输入假设、目标、控制和指标；输出不可变绑定的测试设计，统计显著与实际价值分开，未预先指定 owner 规则时不直接扩量。
- [bid-strategy-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/orchestrate/bid-strategy-planner/SKILL.md)：输入自有历史量、目标和约束；输出 bid strategy 与 target/baseline 计划，区分 learning-state 和成熟期。
- [landing-experience-checker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/orchestrate/landing-experience-checker/SKILL.md)：输入广告与目标页；输出五类体验/匹配检查和交接项，非 conversion 或业务结果证明。

### Paid Ads：Activate

- [ad-account-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/activate/ad-account-auditor/SKILL.md)：输入账户/组合、归一化归因窗和自有订单真相集；输出 ROAS typed audit。RQS 不是平台 ROAS 比率，分数/门槛均为作者框架。
- [conversion-signal-qa](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/activate/conversion-signal-qa/SKILL.md)：输入事件、UTM、去重与窗口配置；输出 signal preflight 和缺口，配置存在不等于转化真实或可扩量。
- [conversion-value-mapper](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/activate/conversion-value-mapper/SKILL.md)：输入收入、边际、退款等有来源数据；输出 conversion value 映射与算术依据，不能替代订单去重或增量测量。
- [placement-exclusion-manager](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/activate/placement-exclusion-manager/SKILL.md)：输入 placement/safety 证据与政策；输出排除建议和未知项，缺失证据必须保留未知。

### Paid Ads：Scale

- [attribution-reconciler](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/scale/attribution-reconciler/SKILL.md)：输入平台、analytics 和订单 ID/时间戳；输出去重、窗口/币种归一化及模型差异，不把平台自报当结果真相。
- [budget-pacing-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/scale/budget-pacing-monitor/SKILL.md)：输入计划、实际 spend、学习状态与限制；输出 pacing/hold 读数，计划对比不是自动追加预算授权。
- [fatigue-frequency-manager](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/scale/fatigue-frequency-manager/SKILL.md)：输入频次、reach、CTR/CVR 斜率和窗口；输出 fatigue 与 saturation 的区分。频次带是作者的 Estimated 起点，不能单独触发轮换。
- [paid-measurement-loop](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/scale/paid-measurement-loop/SKILL.md)：输入预注册测量合同、控制、证据和决策 owner；输出 Keep/Promote/Rollback/Unproven 的候选读数。它不替代 audit gate 或实际广告修改权限。

### Email：Setup

- [deliverability-qa](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/setup/deliverability-qa/SKILL.md)：输入 DNS、DMARC、headers、provider/seed 证据；输出 sender preflight。完整 S 维度评分只在覆盖完整时有意义，不能保证 inbox placement。
- [list-growth-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/setup/list-growth-designer/SKILL.md)：输入受众、lead magnet、渠道和 consent 要求；输出 acquisition/opt-in/referral 设计及同意交接，不自动发送或收集。
- [list-hygiene-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/setup/list-hygiene-monitor/SKILL.md)：输入 cohort、bounce/complaint、活跃与窗口数据；输出卫生监控、sunset/抑制建议，缺少数据不冒充健康。
- [list-segment-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/setup/list-segment-builder/SKILL.md)：输入可用行为、RFM、生命周期和抑制事实；输出 segment 规则及边界，不从推测补齐个人资料。

### Email：Engage

- [dynamic-content-personalizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/engage/dynamic-content-personalizer/SKILL.md)：输入经批准的字段、内容与 fallback；输出个性化逻辑和 PII guard，强调默认内容与缺失值路径。
- [email-creative-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/engage/email-creative-builder/SKILL.md)：输入目的、segment、canon/claims/offer；输出 subject、preheader、正文与 CTA 草案，交付的是草稿而非发送事实。
- [email-render-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/engage/email-render-builder/SKILL.md)：输入设计/内容；输出响应式表格、暗色模式、无障碍、client matrix 和纯文本一致性要求，未实测客户端即非已验证渲染。
- [subject-line-lab](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/engage/subject-line-lab/SKILL.md)：输入主题、受众、offer；输出变体与启发式检查。主观评分/语法检查不能承诺送达、打开或收入。

### Email：Nurture

- [email-sequence-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/nurture/email-sequence-designer/SKILL.md)：输入生命周期、触发、目标和偏好；输出 flow、exit、quiet/cap/sunset 规则。设计与真实 send 分属不同证据。
- [newsletter-monetization-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/nurture/newsletter-monetization-planner/SKILL.md)：输入名单、内容、成本和可验证约束；输出付费、赞助、推荐等模型。收入数字须标 Measured/User-provided/Estimated，不能编造成果。
- [preference-frequency-manager](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/nurture/preference-frequency-manager/SKILL.md)：输入 topic/cadence 选择、同意和运营能力；输出偏好中心/暂停/单击退订与规则映射，退订权不能由频率偏好替代。
- [reactivation-specialist](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/nurture/reactivation-specialist/SKILL.md)：输入沉默 cohort、合法基础和历史行为；输出 reactivation/reconsent/sunset 方案，避免把沉默推断为许可。

### Email：Deliver

- [cold-outbound-sequencer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/deliver/cold-outbound-sequencer/SKILL.md)：输入目标账户、相关性证据、合法基础和 suppression；输出单线序列/回复分支/预热草案，明确不自动触达或排程未来发送。
- [email-quality-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/deliver/email-quality-auditor/SKILL.md)：输入一个发送项目、窗口与 DNS/consent/outcome 证据；输出 SEND audit。MPP opens 是 proxy，EQS 和 veto 是作者 gate 语义而非业绩预测。
- [inbox-placement-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/deliver/inbox-placement-monitor/SKILL.md)：输入已发送的 provider/seed/Postmaster/SNDS 读数；输出 placement 趋势。provider 数据缺失是 needs-input，不能因此判定 inbox。
- [send-experiment-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/deliver/send-experiment-designer/SKILL.md)：输入 A/B、多变量、send-time 或 holdout 假设；输出绑定、样本/窗口与 owner 规则，统计结果没有预先决策规则就不代表业务动作。

### Narrative：Trace

- [audience-belief-mapper](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/trace/audience-belief-mapper/SKILL.md)：输入访谈、异议、替代方案和原话；输出 beliefs、four-forces 和语料地图，保留来源与未知项。
- [category-narrative-mapper](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/trace/category-narrative-mapper/SKILL.md)：输入类别/竞品表述和日期；输出类别故事、竞争叙事、漂移与 claim candidates，不能把竞品语句当产品真相。
- [narrative-baseline-mapper](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/trace/narrative-baseline-mapper/SKILL.md)：输入自有页面/渠道快照；输出有日期的叙事基线和 drift 观察，不把基线视作 canon。
- [positioning-truth-tracer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/trace/positioning-truth-tracer/SKILL.md)：输入产品事实、替代、受众和 claims；输出 positioning truth trace、onlyness/阶段检查与待证实主张。

### Narrative：Architect

- [brand-language-codifier](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/architect/brand-language-codifier/SKILL.md)：输入自有材料和 approved canon；输出 voice、命名、词汇/禁用词规则，不从竞品文本提炼“品牌声音”。
- [message-system-architect](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/architect/message-system-architect/SKILL.md)：输入定位、证据、persona 与版本；输出 message house、pillers/proof 和 canon candidate，要求版本绑定。
- [story-bank-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/architect/story-bank-builder/SKILL.md)：输入真实案例、原始证据和 claim ID；输出按 pillar/claim 标记的 story bank，未验证故事保留为待证。
- [strategic-narrative-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/architect/strategic-narrative-designer/SKILL.md)：输入真相追踪和受众信息；输出 old-world→shift→赢家/输家→promised-land→proof 的策略叙事，模式是作者设计工具而非市场验证。

### Narrative：Land

- [narrative-cascade-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/land/narrative-cascade-planner/SKILL.md)：输入 canon、表面和受众；输出各触点的 message match/brief 与所有者，不交付未经证实的完成稿。
- [narrative-enablement-kit](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/land/narrative-enablement-kit/SKILL.md)：输入 canon、proof 和使用场景；输出 10/30/120 秒版本、Q&A、boilerplate 和 do/don't，保持 canon/claim 绑定。
- [pitch-narrative-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/land/pitch-narrative-builder/SKILL.md)：输入 positioning、proof 和听众；输出 slide beats/讲述结构及证据 claim ID，不把 pitch 当成真实销售结果。
- [proof-point-packager](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/land/proof-point-packager/SKILL.md)：输入 claims ledger 与证据；输出仅含批准 proof 的包装材料和 gap list，避免用无来源“社会证明”补位。

### Narrative：Evaluate

- [message-test-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/evaluate/message-test-designer/SKILL.md)：输入 canon、刺激物、假设和阈值；输出消息测试设计/绑定。设计、理解、回忆与行为效果不能混称。
- [narrative-drift-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/evaluate/narrative-drift-monitor/SKILL.md)：输入有日期的表面/竞品材料；输出 drift 证据、触发器和回退建议，监测不自动改 canon。
- [narrative-quality-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/evaluate/narrative-quality-auditor/SKILL.md)：输入一个 truth/system/effectiveness 生命周期 read；输出 TALE profile audit。三种读数不应平均，叙事连贯也不能证明效果。
- [narrative-resonance-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/evaluate/narrative-resonance-monitor/SKILL.md)：输入锁定 query/panel、时间和信号；输出 echo/SOV/answer-engine 等归因说明，AI 回答和 SOV 是 proxy，非理解或行为的替代。

### Social：Explore

- [channel-portfolio-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/explore/channel-portfolio-planner/SKILL.md)：输入受众、目标、访问能力和产能；输出渠道组合 proposal，不能把计划视为已开通/已运营渠道。
- [participation-warmup-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/explore/participation-warmup-planner/SKILL.md)：输入社区规则、历史与角色；输出 give:ask、tenure/参与计划和人工毕业条件。估计门槛需标 Estimated。
- [platform-norm-profiler](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/explore/platform-norm-profiler/SKILL.md)：输入平台、市场与最新规则来源；输出带日期的 norm cards，区分官方规则和社区 folklore，过期材料要标明。
- [voice-dossier-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/explore/voice-dossier-builder/SKILL.md)：输入自有内容 corpus/canon；输出各平台 register、内容支柱和表现规则，不挪用竞品材料。

### Social：Craft

- [advocacy-program-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/craft/advocacy-program-designer/SKILL.md)：输入自愿参与者、政策和披露要求；输出 opt-in advocacy 方案、变体/披露规则，不组织协同互动。
- [short-video-scripter](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/craft/short-video-scripter/SKILL.md)：输入受众、消息和平台规格；输出 hook→确认→payoff→CTA 的脚本/披露/规格，既不渲染也不上传。
- [social-calendar-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/craft/social-calendar-builder/SKILL.md)：输入内容承诺、owner、队列和趋势信息；输出发布日历。排期/审计不会成为已发布事实，需单条意图和平台回执。
- [social-creative-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/craft/social-creative-builder/SKILL.md)：输入 canon、claims、素材权利和平台要求；输出平台原生内容包、provenance/alt text/披露，不能直接发布。

### Social：Host

- [crisis-response-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/host/crisis-response-planner/SKILL.md)：输入事件、证据、渠道和 owner；输出 P0–P3 分级、暂停/升级/恢复计划和回执要求，方案不是行动回执。
- [engagement-inbox-manager](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/host/engagement-inbox-manager/SKILL.md)：输入已收消息/评论、分类和 SLA；输出 inbox register、情绪/路由、回复草稿和 UGC 权利核查，人工实际回复另需回执。
- [social-quality-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/host/social-quality-auditor/SKILL.md)：输入一个 asset 或 program 和证据；输出 ECHO asset-gate 或 maturity audit。资产质量与计划成熟度不可合并，结果指标不因评分而被证明。
- [social-selling-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/host/social-selling-planner/SKILL.md)：输入目标、触发、社区规则和能力；输出限时价值评论/warm touch 的方案，禁群发/自动化；SSI 等无来源值只能为 Estimated。

### Social：Observe

- [dark-social-attributor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/observe/dark-social-attributor/SKILL.md)：输入 UTM、自报、direct 及时间窗；输出 dark-social 归因假设与透明度标签，皆为 Estimated/proxy 直至有更强对照。
- [share-of-voice-tracker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/observe/share-of-voice-tracker/SKILL.md)：输入锁定 panel、query 与窗口；输出 SOV/情绪观察。panel 变更须重新开始，未人工编码的情绪是估计。
- [social-measurement-loop](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/observe/social-measurement-loop/SKILL.md)：输入 denominator 字典、organic/boosted 证据及控制；输出稳健汇总、readback 和决策输入。EMV 只是翻译，不能取代真实目标。
- [social-pulse-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/observe/social-pulse-monitor/SKILL.md)：输入 query variants、7 日基线、渠道与路由；输出 spike/异常读数。封闭平台缺数据时是 proxy/export gap，而不是零信号。

### Influencer：Scout

- [audience-mapper](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/scout/audience-mapper/SKILL.md)：输入创作者或 niche、目标受众和证据；输出 audience/niche map。Brand Fit X/25 是作者的社区进入评估，非 STAR/SQS 或商业结果。
- [fit-scorer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/scout/fit-scorer/SKILL.md)：输入 creator、tier×platform×niche cohort 和证据；输出 Suitability 读数/商业矩阵，正式 veto/SQS 仍只由 creator-content-auditor 作出。
- [influencer-discovery](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/scout/influencer-discovery/SKILL.md)：输入品牌、受众、平台/市场和证据；输出 READY/REFRESH/INELIGIBLE 的候选队列与 opaque creator refs，不造排名。
- [trend-spotter](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/scout/trend-spotter/SKILL.md)：输入当前证据、市场和品牌约束；输出趋势候选与适配判断。趋势代理和 X/25 rubric 都是作者方法，不是 go/skip 的实效证明。

### Influencer：Target

- [brief-generator](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/target/brief-generator/SKILL.md)：输入目标、creator、canon、claims 和权利边界；输出 ref-safe brief，未给予发送/签约/发布授权。
- [budget-optimizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/target/budget-optimizer/SKILL.md)：输入总预算、报价、目标与约束；输出 100% 分配、公式和假设。没有自有基准时不能伪造预测，回报算术非回报证明。
- [campaign-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/target/campaign-planner/SKILL.md)：输入目标、creator、交付物、窗口和风险；输出计划/追踪器、不可变绑定和关闭回执要求。计划不等于付款、发布或已完成。
- [competitor-tracker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/target/competitor-tracker/SKILL.md)：输入已知竞品、窗口和公开证据；输出带日期的合作观察与估计区分，不根据相似内容推断合作关系。

### Influencer：Activate

- [content-amplifier](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/activate/content-amplifier/SKILL.md)：输入冻结且已审核资产、明确权限和渠道计划；输出 paid/repurpose 路径。未具备五项观察时不评分/不花费，且无自动动作。
- [contract-helper](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/activate/contract-helper/SKILL.md)：输入商业条款、权利、披露与市场；输出模板/审阅清单，法律意见和签约/发送仍需单独授权。
- [creator-content-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/activate/creator-content-auditor/SKILL.md)：输入单个 creator partnership、deliverable、assessment time 与证据；输出唯一的 STAR/SQS audit。S2/S6/T1/T2/T3 是该框架的 veto，分数不预测 ROI。
- [outreach-manager](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/activate/outreach-manager/SKILL.md)：输入名单、单触达文本、同意/抑制/合法基础；输出草稿与 dispatch gate。任何实际触达须逐笔授权，不排程未来自动跟进。

### Influencer：Report

- [landing-optimizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/report/landing-optimizer/SKILL.md)：输入 campaign message、页面、creator asset 权利和证据；输出 message-match/结构/测试路线图，使用资产须有精确批准与现行 scoped rights。
- [performance-analyzer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/report/performance-analyzer/SKILL.md)：输入带来源/日期的结果、订单/UTM/平台数据；输出归一化比较和异常解释。没有预注册设计/对照不能声称因果。
- [report-generator](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/report/report-generator/SKILL.md)：输入已经算好的真实/估计结果和受众；输出格式化报告，不新增数学或外部分发授权。
- [roi-calculator](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/report/roi-calculator/SKILL.md)：输入成本、收入/利润、分母和 LTV 假设；输出 ROI/ROAS 等算术与标签。计算正确也不证明盈利、归因或增量。

### Launch：Research

- [early-access-designer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/research/early-access-designer/SKILL.md)：输入产品状态、用户、反馈/同意和约束；输出 waitlist→concept→alpha→beta→GA 的阶段/招募与毕业方案。proposal 不是 registry stage truth。
- [launch-tier-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/research/launch-tier-planner/SKILL.md)：输入目标、影响、风险、资源和历史；输出 T1/T2/T3、类型、kill criteria、D0/W1/M1 目标。等级/计数是作者模板，须由自有基线复核。
- [launch-window-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/research/launch-window-planner/SKILL.md)：输入至少两个窗口、冲突/顺风/风险和时区；输出选择、缓冲与 embargo 信息。候选窗口不改写 authoritative date。
- [positioning-mapper](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/research/positioning-mapper/SKILL.md)：输入产品、受众、替代（含手工/现状）和证据；输出 launch positioning、价值、beachhead/onlyness 与待证 claim。

### Launch：Assemble

- [launch-asset-packager](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/assemble/launch-asset-packager/SKILL.md)：输入 tier、canon、claims、渠道和技术事实；输出 manifest/press kit/demo/FAQ/store 字段与 hash。manifest/SHIP 都不是执行或上线回执。
- [message-house-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/assemble/message-house-builder/SKILL.md)：输入 positioning、canon、claims 和 proof；输出 tagline、one-liner、pillers、PRFAQ/angles 与阻塞 claims，不把文案当真实发布。
- [pricing-packaging-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/assemble/pricing-packaging-planner/SKILL.md)：输入价值、成本、受众、条款和证据；输出 tier/price/guarantee/beta-to-GA 候选。价格与比例启发式为作者方法，候选不是 live offer。
- [sales-enablement-kit](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/assemble/sales-enablement-kit/SKILL.md)：输入 message house、产品事实、claims、异议和 embargo；输出 battlecards/talk track/FAQ，逐项追溯来源，不替代成交证据。

### Launch：Mobilize

- [community-launch-runner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/mobilize/community-launch-runner/SKILL.md)：输入冻结 manifest、SHIP、平台当前规则和受众；输出 PH/Show HN/subreddit/directory/地区渠道包及 red-line 检查。要求逐平台意图/回执；禁止拉票或投票圈。
- [launch-day-conductor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/mobilize/launch-day-conductor/SKILL.md)：输入 hash 匹配的 SHIP、权威日期、owner、kill criteria 和 telemetry；输出小时 runbook、观察窗、CONTINUE/ROLLBACK 记录与事件 proposal。runbook/SHIP/URL 都不是行动回执。
- [launch-readiness-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/mobilize/launch-readiness-auditor/SKILL.md)：输入一个 launch 的 preflight/execution/outcome 证据；输出单生命周期 RAMP audit。不同时间读取不可平均；SHIP 仅说明 gate eligibility，不授予外部执行许可。
- [press-media-relations](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/mobilize/press-media-relations/SKILL.md)：输入 tier、权威日期/阶段、message house、claims、媒体关系；输出三级名单、embargo skeleton、新闻稿/分析师 brief 草案。节奏为 Estimated，草案/名单不等于实际 outreach。

### Launch：Prove

- [launch-feedback-synthesizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/prove/launch-feedback-synthesizer/SKILL.md)：输入评论/评测/工单等有窗口的反馈；输出主题频次/严重度/原话、状态环、you-asked-we-shipped 和合规社会证明方案。商店评测不得激励。
- [launch-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/prove/launch-monitor/SKILL.md)：输入 manifest、回执、测量合同、目标和平台/自有分析；输出 preflight instrumentation 或 T0–T30 的 D0/W1/M1 读数。平台数字为 reference，HN flamewar 比例是 Estimated heuristic。
- [launch-retro-analyzer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/prove/launch-retro-analyzer/SKILL.md)：输入 manifest、完整回执、预注册目标和自有归因分析；输出渠道 actual-vs-target、单一最大 miss 的 5-Whys、keep/kill/change 与学习。缺回执/窗口只能 provisional。
- [momentum-planner](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/prove/momentum-planner/SKILL.md)：输入 spike/decay、自有分析、roadmap 和 calendar；输出 T+1→T+30 的 milestone/shipped-loop/badge 时刻、relaunch 判断、owned handoff 与下一 T1 间隔。阶段分级是 Estimated，安排不是实际分发。

## 旧仓：`aaron-he-zhu--seo-geo-claude-skills`（20 个历史指针）

该仓 README 说明这些文件是旧 v9.9.12 的 archive/signpost。每项的输入是旧调用名或迁移需求，输出是当前仓的路径指针/冻结来源说明；**均不包含可独立执行的当前工作流**。

### Research

- [competitor-analysis](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/research/competitor-analysis/SKILL.md)：历史入口，指向当前 [seo-geo/survey/competitor-analysis](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/competitor-analysis/SKILL.md)。
- [content-gap-analysis](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/research/content-gap-analysis/SKILL.md)：历史入口，指向当前 [seo-geo/survey/content-gap-analysis](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/content-gap-analysis/SKILL.md)。
- [keyword-research](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/research/keyword-research/SKILL.md)：历史入口，指向当前 [seo-geo/survey/keyword-research](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/keyword-research/SKILL.md)。
- [serp-analysis](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/research/serp-analysis/SKILL.md)：历史入口，指向当前 [seo-geo/survey/serp-analysis](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/survey/serp-analysis/SKILL.md)。

### Build

- [geo-content-optimizer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/build/geo-content-optimizer/SKILL.md)：历史入口，指向当前 [seo-geo/implement/geo-content-optimizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/geo-content-optimizer/SKILL.md)。
- [meta-tags-optimizer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/build/meta-tags-optimizer/SKILL.md)：历史入口，合并到当前 [seo-geo/implement/serp-markup-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/serp-markup-builder/SKILL.md)。
- [schema-markup-generator](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/build/schema-markup-generator/SKILL.md)：历史入口，合并到当前 [seo-geo/implement/serp-markup-builder](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/serp-markup-builder/SKILL.md)。
- [seo-content-writer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/build/seo-content-writer/SKILL.md)：历史入口，指向当前 [seo-geo/implement/content-writer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/content-writer/SKILL.md)。

### Optimize

- [content-refresher](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/optimize/content-refresher/SKILL.md)：历史入口，合并到当前 [seo-geo/implement/content-writer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/implement/content-writer/SKILL.md) 的刷新模式。
- [internal-linking-optimizer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/optimize/internal-linking-optimizer/SKILL.md)：历史入口，指向当前 [seo-geo/tune/site-structure-optimizer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/site-structure-optimizer/SKILL.md)。
- [on-page-seo-auditor](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/optimize/on-page-seo-auditor/SKILL.md)：历史入口，指向当前 [seo-geo/tune/on-page-seo-checker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/on-page-seo-checker/SKILL.md)。
- [technical-seo-checker](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/optimize/technical-seo-checker/SKILL.md)：历史入口，指向当前同名 [seo-geo/tune/technical-seo-checker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/technical-seo-checker/SKILL.md)。

### Monitor

- [alert-manager](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/monitor/alert-manager/SKILL.md)：历史入口，合并到当前 [seo-geo/evaluate/performance-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/performance-monitor/SKILL.md) 的 alert/read 路径。
- [backlink-analyzer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/monitor/backlink-analyzer/SKILL.md)：历史入口，指向当前 [seo-geo/evaluate/offsite-signal-analyzer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/offsite-signal-analyzer/SKILL.md)。
- [performance-reporter](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/monitor/performance-reporter/SKILL.md)：历史入口，合并到当前 [seo-geo/evaluate/performance-monitor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/performance-monitor/SKILL.md)。
- [rank-tracker](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/monitor/rank-tracker/SKILL.md)：历史入口，指向当前同名 [seo-geo/evaluate/rank-tracker](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/rank-tracker/SKILL.md)。

### Cross-cutting

- [content-quality-auditor](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/cross-cutting/content-quality-auditor/SKILL.md)：历史入口，指向当前 [seo-geo/tune/content-quality-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/content-quality-auditor/SKILL.md)。
- [domain-authority-auditor](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/cross-cutting/domain-authority-auditor/SKILL.md)：历史入口，指向当前 [seo-geo/evaluate/domain-authority-auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/evaluate/domain-authority-auditor/SKILL.md)。
- [entity-optimizer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/cross-cutting/entity-optimizer/SKILL.md)：历史入口，README 指向历史 `protocol/entity-optimizer` 名称；当前仓文件集合中没有该路径，只有 [entity-registry](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/entity-registry/SKILL.md)，因此仅作为迁移遗留信息。
- [memory-management](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/cross-cutting/memory-management/SKILL.md)：历史入口，指向当前 [protocol/memory-management](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/protocol/memory-management/SKILL.md)。

## 额外全文阅读的工作流承载文档（不计入 manifest）

- [当前仓 README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/README.md)、[SEO/GEO README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/README.md)、[ad README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/ad/README.md)、[email README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/email/README.md)、[narrative README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/narrative/README.md)、[social README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/social/README.md)、[influencer README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/influencer/README.md)、[launch README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/README.md)、[旧仓 README](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0/README.md)。
- [workflow graph](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/docs/workflow-graph.md) 与 [system architecture](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/docs/system-architecture.md)：用于核对 7×16 + 8 的拓扑、交接和 protocol 层。
- [Skill Contract](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/skill-contract.md)、[Scoring Semantics](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/scoring-semantics.md)、[Measurement Protocol](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/measurement-protocol.md)、[Auditor Runbook](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/auditor-runbook.md)、[Runtime Invocation](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/runtime-invocation.md)。
- [State Model](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/state-model.md)、[Registry Event Protocol](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/registry-event-protocol.md)、[Launch Action Control](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/launch/assemble/launch-asset-packager/references/action-control.md)：用于核对 proposal、canonical state、intent、receipt 和外部动作之间的边界。
- 八个 framework 正文：[CORE-EEAT](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/core-eeat-benchmark.md)、[CITE](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/cite-domain-rating.md)、[ROAS](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/roas-benchmark.md)、[SEND](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/send-benchmark.md)、[TALE](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/tale-benchmark.md)、[ECHO](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/echo-benchmark.md)、[STAR](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/star-benchmark.md)、[RAMP](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/references/ramp-benchmark.md)。

## 覆盖结论

- 已全文读取并索引：**140/140** 个大小写不敏感匹配 `SKILL.md`；当前营销仓 **120**，旧指针仓 **20**。
- 缺失/阻塞：**无**。源仓库保持只读；未执行、安装、发布、发送、注册表写入或调用任何外部 skill。
- 精确路径清单见同目录 [aaron-read-manifest.json](读取清单.json)。
