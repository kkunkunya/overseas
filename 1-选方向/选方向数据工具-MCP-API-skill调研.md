# 选方向数据工具：MCP / API / skill 调研

> 调研日期：2026-07-21  
> 目标：让 Agent 帮助筛选“有真实需求、有搜索流量、竞争可打、能做成自有资产”的方向。  
> 边界：本报告只调研，未购买、注册、安装或修改任何配置。

## 当前执行约束（2026-07-23 确认）

当前仍处于**首个 MVP 前阶段**：找词 → 找方向 → 跑 018 → Kun 拍板 → 才进入第一个 MVP。趋势发现只做成能用的入口，不先建设完整监控平台。

数据获取固定保留两条路：

1. **Chrome 浏览器观察**
   - 用户明确指定 Chrome 时，Agent 用 Chrome 查看真实页面、登录态和已安装插件。
   - 适合 Google Trends、真实 SERP、Reddit/HN 原帖、AITDK/Similarweb 等网页或插件面板。
   - 每次结果必须说明：查看页面、目标地区/时间范围、看到的指标、没拿到的数据和估算性质，不能只说“查过”。
   - 付费 API 暂时不方便时，优先用浏览器/插件完成少量候选实查，不阻塞找词流程。

2. **官方 API / 官方 MCP 直连**
   - 适合批量关键词、重复采集、跨候选排序和站点上线后的定期复盘。
   - 有官方直连就优先官方；没有则回退 Chrome，不连接来路不明的 MCP。
   - 只有出现明确批量需求时才接入，避免为了“Agent 化”提前搭系统。

最小执行链固定为：

```text
线索/趋势发现
→ 候选词
→ Chrome 少量实查
→ 018 四步评估
→ Kun 拍板
→ 第一个 MVP
```

`trending` 只负责发现候选，不直接决定做站；后续 GSC、GA/Plausible、Clarity 等站点分析工具先记录，等第一个 MVP 上线时再接。

### Skill 治理结论

**已改进项目本地 `direction-validator`，不新建第二个 skill。**

- Greg Isenberg 的完整字幕提供了可复现的“增长社区 → audience → pain/advice/solution → 候选词 → wireframe”方法，已满足真实方法来源要求。
- 改进后的 skill 保留 Query-first，并加入 Community-first；二者在关键词证据卡和赫兹 018 闸门汇合。
- 社区调研强制路由 Codex Chrome，复用用户登录态；遇到首次登录或权限墙时停下交给用户，登录后继续同一状态。
- 只新增一张轻量 `audience-opportunity-card.md`，不建设社区数据库、爬虫或多 Agent 调度平台。

## 一句话结论

**现在先用免费栈完成候选发现和人工 SERP 判断；候选词积累到一批后，再接 DataForSEO 官方 MCP 做批量搜索量 / KD / SERP / 竞品关键词验证。站点上线后再接 Google Search Console API，用自己的真实数据取代第三方估算。**

不建议起步就购买 Ahrefs、Similarweb 或 Wappalyzer API。它们有能力，但对“第一个资产站的选方向”来说成本过早，也不会替代对真实 SERP 和用户痛点的人工判断。

## 推荐栈：按使用阶段排序

### 阶段 0：现在就能用，不花钱

1. **AITDK Chrome 扩展：快速看竞品站**
   - 官方列出的能力包括月访问、跳出率、停留时间、流量来源、地区、顶部关键词、WHOIS 和页面 SEO 分析，并标明可免费添加 Chrome：https://aitdk.com/extension
   - 定位：**只浏览器可用**。本次未在官方网站找到公开 API 或 MCP 文档，因此不应把它当作 Agent 可稳定批量调用的数据源。
   - 用法：候选词的 SERP 里出现小工具站时，快速判断它是否真有流量、靠哪些页和词获得流量。

2. **Google Trends 网页 + CSV：验证趋势和季节性**
   - Google 官方支持从 Trends 图表导出 CSV：https://support.google.com/trends/answer/4365538?hl=en
   - 公开 Google Trends API 仍是受限 alpha，需申请早期访问，不应当作当前稳定依赖：https://developers.google.com/search/apis/trends
   - Google 还提供 BigQuery 公共趋势数据，但它只是各地区 Top 25 / Rising 查询，适合“发现正在上升的话题”，不能替代任意关键词的搜索量工具。BigQuery sandbox 可免信用卡使用，免费层为每月 1 TB 查询：https://support.google.com/trends/answer/12764470?hl=en

3. **真实 Google SERP：做最后的“能不能打”判断**
   - 免费用浏览器检查前 10 名，重点看：是否被大品牌垄断、是否有小站/单页工具排名、页面是否很旧或难用、搜索意图是否明确要“现在完成一件事”。
   - 任何 KD 分数都只是厂商自己的模型。例如 DataForSEO 明确说其 KD 是 0–100 的对数尺度，通过分析前 10 名等因素计算：https://docs.dataforseo.com/v3/dataforseo_labs-google-bulk_keyword_difficulty-live/

4. **Reddit / 论坛 / 社区：只做痛点证据，不做早期 API 依赖**
   - 用 Google/Tavily/Firecrawl 做 `site:reddit.com <问题>`、`<任务> frustrating`、`alternative to <竞品>` 等查询，然后人工阅读少量原帖。这一步用于回答“人们是否反复遇到同一问题、现有解决方案哪里难用”。
   - Reddit 2026 官方政策要求：通过 API 访问 Reddit 数据需明确批准，商业使用还需许可/合同：https://support.reddithelp.com/hc/en-us/articles/16471395473812-Moderation-Bots-Tooling 和 https://support.reddithelp.com/hc/en-us/articles/14945211791892-Developer-Platform-Accessing-Reddit-Data
   - 因此，不建议安装来路不明的“Reddit MCP”或依赖未授权爬虫。早期用公开搜索 + 少量人工原帖即可。

### 阶段 1：候选池形成后，最值得接入

#### DataForSEO 官方 MCP / API（首选）

**类别：现成官方 MCP + 可直接调 REST API。**

它一次覆盖了当前最需要的几项能力：

- 关键词思路、长尾词、搜索量、CPC、搜索意图、12 个月趋势和 KD。Keyword Overview 官方文档：https://docs.dataforseo.com/v3/dataforseo_labs-google-keyword_overview-live/
- 批量 KD：单次最多 1,000 个词：https://docs.dataforseo.com/v3/dataforseo_labs-google-bulk_keyword_difficulty-live/
- 长尾词扩展：Keyword Suggestions 可按搜索量、竞争等字段筛选：https://docs.dataforseo.com/v3/dataforseo_labs-google-keyword_suggestions-live/
- 竞品排名词、SERP 竞品、历史排名和估算自然流量：https://docs.dataforseo.com/v3/dataforseo_labs-google-overview/
- 实时 Google SERP，可指定地区和语言：https://docs.dataforseo.com/v3/serp-overview/
- 站点技术栈：可查单域名的技术，也可查某技术被哪些域名使用：https://docs.dataforseo.com/v3/domain_analytics-technologies-overview/

官方 MCP 支持 SERP、Keywords Data、DataForSEO Labs、Backlinks、On-Page、Domain Analytics 等模块：

- 官方介绍与远程地址 `https://mcp.dataforseo.com/mcp`：https://dataforseo.com/help-center/setting-up-the-official-dataforseo-mcp-server-simple-guide
- 官方源码：https://github.com/dataforseo/mcp-server-typescript
- npm 包精确名称：`dataforseo-mcp-server`：https://www.npmjs.com/package/dataforseo-mcp-server

成本与门槛：

- SERP API 是按量付费，标准队列从 $0.0006 / SERP 起；注册试用额度 $1，正式充值最低 $50，没有月费：https://dataforseo.com/apis/serp-api/pricing
- Labs 的基础端点通常按任务 + 返回条目计价；官方给出的基础参考为 $0.01 / task + $0.0001 / item，但不同端点和 clickstream 附加数据会增加费用：https://dataforseo.com/apis/dataforseo-labs-api
- 不要让 Agent 没有限额地自由探索。接入后应设每日支出上限，先用 20–50 个人工过滤后的候选词试跑。

**为什么是首选：** 相比拼接多个第三方 MCP，它有官方维护的 MCP，而且同一数据源可同时回答“有多少人搜”、“前十是谁”、“竞品靠哪些词活着”和“站点用什么做”。

### 阶段 2：站点上线后必接

#### Google Search Console API

**类别：官方直接 API；本次未找到 Google 官方的 Search Console MCP。**

- 可读取自己已验证站点的查询、页面、国家、设备、点击、展现、CTR 和排名：https://developers.google.com/webmaster-tools
- Search Analytics API 单次最多 25,000 行，但 Google 明确说不保证返回所有行，而是返回顶部数据：https://developers.google.com/webmaster-tools/v1/searchanalytics/query
- 它只能看自己有权限的站，不能用来做上线前的竞品调研。但上线后，它是优先级最高的“真实需求反馈”：用真实展现找到已经排到 8–30 名、稍微加强就可能上首页的词。
- 配额对个人站非常宽松：Search Analytics 的同站点限额为 1,200 QPM；URL Inspection 同站点为 2,000 QPD：https://developers.google.com/webmaster-tools/limits?hl=en

## 用途—工具映射

| 需要回答的问题 | 免费/当前方案 | Agent 批量方案 | 判断要点 |
|---|---|---|---|
| 有多少人搜、有没有商业价值 | Google Trends 只看相对趋势；搜索广告多少做辅证 | DataForSEO Keyword Overview / Suggestions | 搜索量与 CPC 都是估算，需同时看搜索意图 |
| 竞争是否可打 | 人工看真实前 10 | DataForSEO KD + SERP API | 决策以前 10 的站点类型和页面质量为准，不单看 KD |
| 趋势是上升还是季节性 | Google Trends 网页 / CSV / BigQuery Top Rising | DataForSEO Google Trends Explore 端点；官方 Trends API alpha 当前不稳定可得 | 至少看 5 年、分国家看 |
| 竞品从哪些词和页获流量 | AITDK 人工查单站 | DataForSEO Ranked Keywords / Relevant Pages / Competitors | 这是估算自然搜索流量，不是竞品 GA 真实访问 |
| 竞品整站流量 | AITDK 快速看量级 | Similarweb API 或其他 clickstream 数据，但前期不建议购买 | 第三方只能估算，小站偏差可能很大 |
| 竞品用什么技术 | AITDK / Wappalyzer 网页单站查 | DataForSEO Domain Technologies | 技术栈只影响实现难度，不证明市场需求 |
| 用户是否真的在抱怨 | Google/Tavily/Firecrawl 搜索 + 人工读原帖 | 不建议早期自动化 Reddit API | 保留原话、时间、赞同和反复出现频率 |
| 自己站上线后该增长什么 | 手工看 Search Console | Search Console API | 自有真实数据优先于任何第三方 KD/流量估算 |

## 其他工具：可用，但不是现在的首选

### Ahrefs 官方 MCP

- **现成官方 MCP**，但只向 Lite 及以上计划开放；MCP 与直接 API 共用 API units。Lite 每月 100,000 units，单次最多 100 行，每次调用最少消耗 50 units：https://help.ahrefs.com/en/articles/13913559-getting-started-with-ahrefs-mcp
- 优点：数据和 UI 成熟，关键词/外链/竞品分析全。
- 结论：如果未来已经付费订阅 Ahrefs，直接用官方 MCP；不为了第一轮选方向单独购买。精确搜索词：`Ahrefs official MCP`。

### Google Ads Keyword Plan API

- **可直接调用的官方 API**；可返回过去 12 个月的平均/按月搜索量、广告竞争和出价区间：https://developers.google.com/google-ads/api/docs/keyword-planning/generate-historical-metrics
- 不是最快的早期方案：需 Google Ads 经理账户和 developer token；Explorer Access 还限制 `KeywordPlanIdeaService`，需申请 Basic/Standard 权限：https://developers.google.com/google-ads/api/docs/api-policy/access-levels
- 结论：等有稳定批量需求、愿意处理 Google Ads 权限时再做；早期 DataForSEO 更快。

### Similarweb API

- **可直接调 API**，Traffic & Engagement 可返回 visits、bounce rate、visit duration、pages/visit 等，官方字段明确写的是 estimated：https://docs.similarweb.com/api-v5/similarweb-api/website-analysis-api/website-performance/traffic-and-engagement
- 结论：适合有预算的市场规模研究；第一资产站初筛用 AITDK 看量级即可。不要把 estimated visits 当成竞品真实 GA 数据。

### Wappalyzer API

- **官方 API** 能查站点技术，但 Technology Lookup API 需 Business 计划：https://www.wappalyzer.com/docs/api/v2/lookup/
- 当前官方定价页显示 Business 为 $450/月；免费账户可有每月 50 次网站查询，但 API 需付费计划：https://www.wappalyzer.com/pricing/
- 结论：早期不接 API，用免费网页/扩展或 DataForSEO Technologies 替代。

## 现有 skills / 通用网页 MCP 该怎么用

这些工具擅长“找页面、读原文、爬站点”，**不等于关键词搜索量/KD 数据库**。

### 当前已有的 skills

- `/research`：适合像本报告一样的一手源调研和落盘，不提供 SEO 指标。
- `/search`：本地 skill 使用 Tavily Search API，需 `TAVILY_API_KEY`，适合找官方文档、社区讨论、竞品页；不提供 Google 搜索量或 KD。
- `/crawl`：本地 skill 使用 Tavily Crawl/Map，适合把竞品文档、定价、功能页批量取回做功能缺口分析；不提供 SEO 指标。
- `/firecrawl`：适合 JS 页面的 search/scrape/map/crawl 和结构化提取；不提供关键词搜索量/KD。
- `/browser-task`：只有需真实 Chrome 状态、登录态或扩展时才路由到浏览器，适合 AITDK 和 Google Trends 网页 spot-check，不适合大批量取数。

Tavily 官方免费层是 1,000 API credits/月，且有 Search、Extract、Crawl 和 Map API：https://www.tavily.com/pricing 与 https://docs.tavily.com/documentation/api-reference/introduction

Firecrawl 官方免费层是 1,000 credits/月，scrape/crawl/map 通常每页 1 credit：https://www.firecrawl.dev/pricing

### 可考虑的官方通用 MCP

- **Tavily MCP**：官方远程 MCP 为 `https://mcp.tavily.com/mcp/`，npm 名为 `@tavily/mcp`，用于网页搜索和提取：https://docs.tavily.com/documentation/mcp
- **Firecrawl MCP**：官方远程形式为 `https://mcp.firecrawl.dev/{FIRECRAWL_API_KEY}/v2/mcp`，本地 npm 名为 `firecrawl-mcp`，用于 search/scrape/crawl/map/extract：https://docs.firecrawl.dev/ai-onboarding

两者选一即可，不需要同时接。若当前 Codex 自带网络搜索已足够，甚至可以都不装。它们解决的是“读互联网”，DataForSEO 解决的是“取 SEO 结构化数据”。

## 应搜索/安装时使用的精确名称

> 以下只是后续操作指针，本次未安装。安装前必须再核对发布者与官方仓库，不要只按名字相似就安装。

| 用途 | 精确搜索词/包名 | 官方校验点 |
|---|---|---|
| SEO 结构化数据 | `DataForSEO MCP Server` / `dataforseo-mcp-server` | GitHub org 必须是 `dataforseo`，官方 repo 为 `dataforseo/mcp-server-typescript` |
| 已有 Ahrefs 订阅时 | `Ahrefs official MCP` | 从 `help.ahrefs.com` 官方文档进入 |
| 通用搜索与抽取 | `Tavily MCP` / `@tavily/mcp` | GitHub org `tavily-ai`，官方远程域名 `mcp.tavily.com` |
| JS 站点爬取 | `Firecrawl MCP` / `firecrawl-mcp` | 官方文档 `docs.firecrawl.dev`，远程域名 `mcp.firecrawl.dev` |
| 自有站真实搜索数据 | `Google Search Console API` | 只信 `developers.google.com/webmaster-tools` 的 OAuth/API 文档 |
| 趋势 | `Google Trends API alpha` | 只信 `developers.google.com/search/apis/trends`；不把 `pytrends` 当官方 API |

## 不可行或不稳定的路径

1. **把 AITDK 当 API**：官方当前只公开描述网页/Chrome 扩展能力，未找到公开 API/MCP 文档。
2. **把 `pytrends` 当 Google 官方 API**：它是非官方封装，可随 Google 网页变化失效；Google 官方 API 目前仍是受限 alpha。
3. **随便安装 Reddit scraper / Reddit MCP**：API 访问需审批，商业用途限制更严；非授权爬取还有合规和稳定性问题。
4. **把第三方流量估算当真值**：Similarweb/AITDK/其他 clickstream 工具的竞品数据都不是对方的 GA/GSC，小站样本尤其容易偏。
5. **用单一 KD 阈值选产品**：KD 只衡量某种排名难度，不衡量需求强度、用户付费意愿、产品可做性和维护成本。

## 建议的实际工作流

1. 从原文、大佬案例、Reddit/论坛和现实工作流中，收集具体任务词，不先追大词。
2. 免费查 Google SERP + Trends + AITDK，删掉大品牌垄断、伪需求、短期波峰和无法差异化的词。
3. 累积 20–50 个候选词后，用 DataForSEO 一次性补齐：美国/英语搜索量、月度趋势、CPC、意图、KD、前 10 和竞品排名词。
4. 对剩下的 3–5 个方向做“机会证据包”：5 条以上用户痛点原话、真实 SERP 截图/结构、主要竞品页、趋势、可做的最小产品以及一句话差异化。
5. 仅在某个方向同时满足“有需求证据 + 有搜索入口 + SERP 可打 + 能做出明显更好的小产品”时，才决定开站。
6. 上线后接 GSC，每周围绕真实 impressions / queries 迭代，让站点从“猜方向”进入“用自有数据复利”。

## 最终推荐的 5 个能力

1. **DataForSEO 官方 MCP**：批量关键词、KD、SERP、竞品词与技术栈，是唯一值得在候选池成熟后优先接入的付费能力。
2. **真实 SERP 人工审查**：决定“能不能打”，不可被 KD 分数替代。
3. **Google Trends 网页/CSV**：免费排除季节性、短期波峰和长期下降需求。
4. **Tavily 或 Firecrawl（二选一）**：搜集论坛痛点、竞品定价/文档/功能页，补足“为什么用户会用”的定性证据。
5. **Google Search Console API**：站点上线后用自有真实数据驱动复利，但不用于上线前选方向。
