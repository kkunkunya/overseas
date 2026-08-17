# 调研 · Apify 与 treg：选词/方向研究的最小服务调用栈（2026-08-16）

> 结论先说：**换到 treg 是对的。** 你当前不需要熟悉一堆平台，也不需要为每个来源注册 API。把它当成「我说明要查什么，Agent 调对应服务」的服务柜台即可。Apify 保留为以后需要整批、定时抓网页时的备用，不是当前默认入口。
>
> 本轮实际调用：Apify Console 的 Google SERP Actor 一次；treg 的 DataForSEO Google SERP、关键词概览，以及 Reddit 检索各一次。全部为小样本验证，不能替代后续对每个候选的完整取证。

---

## 1. 你只需要提出的需求

以后直接用下面这种人话，不需要说 Actor、MCP、接口名：

| 你说 | Agent 默认服务 | 得到什么 | 何时用 |
|---|---|---|---|
| 「查这个词在**菲律宾/美国** Google 前十是谁，手机端」 | **treg → DataForSEO Google SERP** | 指定国家、语言、设备的前十、标题、URL、摘要、SERP 特性 | 每个候选都要做 |
| 「这 20–50 个词分别有多少量、CPC、趋势、KD，按机会排」 | **treg → DataForSEO Keyword Overview + Bulk KD** | 搜索量、月度变化、CPC/广告竞争、KD；可批量 | 候选池已经人工筛过后 |
| 「围绕这个种子词扩词」 | **treg → DataForSEO Keyword Suggestions / Google autocomplete** | 长尾、相关词、可再筛的词表 | 找词阶段 |
| 「去 Reddit / TikTok / YouTube / Instagram / X / Threads 看真人怎么抱怨、怎么描述、用什么替代、实际怎么做」 | **treg → 对应平台 Search posts / videos + Post comments** | 帖子、评论、视频、原话、竞品/替代方案线索 | 需求验证 / 场景还原阶段 |
| 「这个词的 PAA、AI Overview、图片/视频/本地结果会不会改变页面形态」 | **treg → DataForSEO Google Organic advanced** | 完整 SERP 特性 | 设计工具/内容/目录等承接前 |
| 「用户到底在找工具、比较还是购买；竞品靠哪些词/页面拿流量；我们共同/缺失哪些词」 | **treg → Search Intent + Keywords for Site / Relevant Pages / Domain or Page Intersection / SERP Competitors** | 意图线索、竞品词群、主力页与可验证切口 | 候选已收窄后 |
| 「拆这个竞品的可复制外链来源」 | **treg → Backlinks / authority / domain metrics**，再用 Chrome 看真实来源页 | 引用域、链接页、锚文本、新失链线索；以实际返回字段为准 | 外链机会台账 |
| 「这个竞品站的内容/价格/功能页整体拆出来」 | Chrome + Tavily/网页抓取；需要大量或定期时才上 Apify | 页面与功能缺口，不是 SEO 量/KD | 竞品深挖 |
| 「每周自动抓 100 个 SERP / 一批账号帖子并导出」 | **Apify task / schedule**（或直接官方 API） | 可重跑、导出、定时的采集任务 | 已有稳定、重复的批量需求后 |
| 「上线后我的站有哪些真实搜索查询、点击、行为和转化」 | **连接 treg 的 Google Search Console / Google Analytics** | 自有展示、点击、查询、落地页、行为与转化数据 | 上线后增长复盘 |
| 「AI 是否提及竞品/我们；哪些页面/品牌在 AI 回答里出现」 | **treg → AI Visibility / AEO**（模型回答/搜索结果、mentions、历史增减、AI search volume） | AI 来源、提及与变化线索 | GEO 来源资产与上线后观察 |

### 固定判断顺序

```text
社媒原话（有没有真实任务/痛点）
→ 词与扩词
→ 指定国家 SERP（前十是否可打）
→ 量 / CPC / 趋势 / KD（排序辅助）
→ 小产品能否明显更好
```

KD 不是裁决；社媒热度也不是裁决。每个方向仍须同时有：真实任务、搜索入口、可打 SERP、清楚的产品承接。

---

## 2. 扩展能力地图：按产品阶段调用，不按 endpoint 数量调用

> 2026-08-16 按 treg Catalog / Connections 观察。**Connected / not connected 是当时账户状态，不是永久能力清单**：调用前先看 Catalog 与 Connections。Google DataForSEO 等可由 treg 代转并按调用计费；GSC、GA、GBP 等自有账户数据须完成授权，未连接时不能把第三方估算冒充一方数据。

### A. 方向与搜索机会（上线前）

| 当前问题 | 优先能力 | 什么时候值得加 | 不应怎么用 |
|---|---|---|---|
| Google 结果是否被 PAA、AI Overview、视频、图片或本地包改变 | Google Organic advanced / Images / Videos / AI Mode | 页面形态不清，或工具词 SERP 明显混合 | 对所有词默认跑高级 SERP |
| 用户是要工具、比较、购买还是学习 | Google Search Intent + 真 SERP | 标题/页型/CTA 有分歧 | 把 intent 标签当用户真实动机结论 |
| 竞品靠哪些词和页面获客 | Keywords for Site、Relevant Pages、SERP Competitors、Domain/Page Intersection、历史 SERP | 已锁定 1–3 个对标，正在找窄切口 | 全量导出竞品数据库或照抄词表 |
| 广告主是否在持续为问题付钱、广告承诺是什么 | Google Ads / Ads Transparency | CPC/竞品定价不足以判断商业时刻 | 把有广告直接等同产品必赚 |
| 图片、电商、本地服务才是主入口 | Google Images/Lens、Shopping、Maps/Local Finder、Business Data/Reviews | SERP 或用户任务已经证明属于这些形态 | 普通线上工具也强行做本地/电商研究 |
| 目标市场主要不用 Google | Bing、Yahoo、DuckDuckGo、Baidu、Naver、Yandex、Seznam SERP/关键词数据 | 目标国家、语言或产品入口有明确证据 | 为“覆盖更多搜索引擎”默认复制全部流程 |

Google 是当前默认搜索入口；Bing/鸭鸭适合英语市场有明确入口证据时补查，Baidu/Naver/Yandex/Seznam 只在中国/韩国/俄语市场/捷克等对应生态成为目标时才切换。Google Business Profile 只服务本地商家、`near me`、城市目录或地图意图，不是一般工具站的必接项。

### B. 场景、人群与分发（上线前和冷启动）

| 人群或材料形态 | 默认先查 | 取什么 | 何时升级到 Chrome |
|---|---|---|---|
| 视觉创作者、短视频工作流 | TikTok、YouTube、Instagram | 视频演示、评论、使用步骤、导出/失败点 | 要复读完整流程、频道语境、评论上下文 |
| 开发者、独立站、B2B 工具讨论 | X、Reddit、LinkedIn | 痛点原话、替代方案、预算/迁移语言 | 要看版规、个人资料、长帖或许可式联系 |
| 中文案例、国内平台/内容迁移线索 | 抖音、B 站、知乎、小红书、微博、公众号/视频号 | 已有做法、表达、素材、工作流 | 需要确认原帖、版权、规则与是否适用于目标海外市场 |
| 兴趣、收藏、视觉灵感型人群 | Pinterest、Instagram、Lemon8 | 保存/分享型内容、审美/模板语言 | 需要看单条内容与外链落地页 |

社媒数据只用来提取用户语言、场景和替代方案。每轮先 2–4 个任务/抱怨词、少量强相关帖子/视频/评论；真人触达、发帖、私聊、合作仍要用户明确授权。

### C. 搜索权威、GEO 与上市后的一方数据

| 阶段 | 能力 | 用途 | 连接/成本边界 |
|---|---|---|---|
| 外链机会 | Backlinks / authority / domain metrics | referring domains、链接页、锚文本、新失链线索，供机会台账初筛 | 当前显示 Connected；先按实际返回字段小样本验证，再 Chrome 审来源页 |
| GEO 来源研究 | AI Visibility / AEO：ChatGPT、Gemini、Claude、Perplexity 的回答/搜索结果 | 反推检索词、引用页与来源资产缺口 | 回答抓取约 $0.004–0.036/次；只研究明确 AI 问题 |
| GEO 竞争/趋势观察 | AI mentions、品牌/域名/页面历史、AI search volume | 看提及/来源变化，发现可复查现象 | mentions 常约 $0.1/次；不是日常“AI 分数” |
| 自有搜索表现 | Google Search Console | 查询、展示、点击、页面、索引覆盖与 sitemap 错误 | 当前未连接；站上线后授权，一方数据优先 |
| 自有行为与转化 | Google Analytics | 流量、事件、漏斗、回访和转化 | 当前未连接；站上线后授权，不用第三方估算替代 |
| 本地商家资产 | Google Business Profile | 门店资料、评论、问答、地图可见度 | 当前未连接；只对本地意图产品授权 |

### D. 调用纪律

```text
先问：这个 endpoint 能改变当前 go / watch / narrow / reject，
或能决定当前页面、分发、GEO、复盘的一项动作吗？
→ 能：声明国家/语言/词数/预算/预期判断后小样本调用
→ 不能：不调用
```

数据提供方、日期、国家/语言、设备、费用和未知项必须随证据卡记录。模型答案、关键词指标、外链分数、社媒互动、AI mention 都是线索；关键页面、原帖、产品和一方数据仍要复读或核验。

---

## 3. 为什么 treg 比 Apify 更适合当前阶段

| 对比 | treg | Apify Console |
|---|---|---|
| 操作方式 | 一个目录下选服务，Agent 可直接按参数调用 | 先找 Actor、读其 schema、填输入、开 run、看 dataset |
| 当前最需要的 SEO 数据 | 已聚合 DataForSEO：SERP、autocomplete、关键词概览、KD、扩词等 | 官方 Google SERP Actor 擅长 SERP；量/KD 要另找第三方 Actor，数据来源/口径须额外审核 |
| 社媒小样本 | Reddit / Instagram / X / Threads 均有「关键词搜索 / 帖子详情 / 评论」入口 | 有对应 Actor，但不同作者/定价/schema 不一致；批量时才更有价值 |
| 小样本成本 | 本次的可见价格约：SERP $0.002/词、关键词概览 $0.024/次、Reddit 搜索 $0.00188/次 | Google SERP Actor 标示 $4.50/1,000 个搜索结果页（约 $0.0045/页）；不同 Actor 各自计价 |
| 应用边界 | **现在的人工闭环默认用它** | 需要定时、大批量、网页结构化/导出时再用 |

这不是说 Apify 差：它是「可部署、可调度的抓取执行平台」；而你眼下需要的是一张服务单，不是搭采集流水线。先不额外引入 Actor、task、schedule 和多家数据源的学习/维护成本。

---

## 4. 这次手动小试：`tattoo stencil maker`（美国/英语）

> 这是用于验证服务链和证据纪律的样词，**不是首批建站建议**。本次结果反而证明了：低 KD 不等于蓝海。

### 4.1 Apify：官方 Google Search Results Scraper

- Actor：`apify/google-search-scraper`（Apify 维护）。
- Run：`XuEQfemeoNBqqeA1a`；输入为 `tattoo stencil maker`、`countryCode: us`、英语、只取基础 SERP 项。
- Console 标价：**$4.50 / 1,000 scraped search result pages**。
- 验证结果：能按国家/语言跑出 SERP dataset；因此它符合「指定国家/语言 Google SERP」这个能力。
- 但它不直接给可比较的搜索量/KD；要补量/KD 得再接另一个 Actor 或数据源。这正是当前不把它当默认入口的原因。

### 4.2 treg：同一词的三个服务调用

| 调用 | 参数 | 实测结果 / 花费 | 它证明什么 |
|---|---|---:|---|
| DataForSEO Organic SERP regular | US (`location_code: 2840`)、en、desktop、depth 10 | 成功；**$0.002** | 可低成本抓指定市场的真实前十 |
| DataForSEO Keyword Overview | US、en、`include_clickstream_data: true`、同一词 | 成功；**$0.02412** | 同一调用给搜索量、CPC、竞争与月度序列 |
| ScrapeCreators Reddit Search | `tattoo stencil maker`、relevance | 成功；**$0.00188** | 可快速拉社媒讨论样本，找任务语言与替代品 |

关键词概览返回的 Google Ads 口径：

- 搜索量：**1,900 / 月**（返回更新时间：2026-07-11）。
- CPC：**$1.55**；广告竞争：**Medium**。
- 趋势：近月 `0%`、近季度 `-16%`、同比 `0%`。
- 之前同一词的 DataForSEO Bulk KD 小试返回：**KD 0**（2026-08-16）。

> 这些是第三方/广告系统估算，特别是 KD 只是供应商的排名模型；不能把 1,900、KD 0 读成真实访问或「必做」。

SERP 前十的主要构成：

1. `tat.ink` 的免费 AI tattoo-to-stencil 工具；
2. Rapid Resizer 通用照片转模板工具；
3. Google Play / App Store 的专用 App；
4. `tattoostencilpro.app`、`stencilai.app` 等专用 AI 工具；
5. YouTube 教程、`freestencilmaker.com`；
6. Reddit 讨论。

**读法：** 搜索意图很明确、已有小站排名也证明工具页可获得入口；但结果页已有多个直接同类产品，不能因 KD 0 就误判为未被满足的蓝海。它至多是「可继续找更窄未满足工作流」的 **narrow**，不应直接进入首批站池。

Reddit 返回的有效线索：

- r/stencils 有创作者发布的免费工具，描述了自动拼 A4、SVG/DXF、Cricut/激光切割导出等功能；说明真实用户任务不只是「图片变黑白线稿」。
- 原帖评论继续提出**图层颜色选择、PNG 导出给 Cameo/Cricut、卡通图处理、平滑/打印不一致**等具体要求。
- 这类「已有工具后仍明确提出的工作流缺口」才是下一轮扩词/切窄的素材；不是只看帖子点赞。

原帖（人工在真实 Reddit 页面复读）：
- https://www.reddit.com/r/stencils/comments/1g3skdc/i_made_this_for_us_free_stencil_maker/

---

## 5. 社媒服务：按平台怎么用

treg 目录中，本轮确认到的最小可用组合如下（先关键词找帖子，再对少数高相关帖取评论）：

| 平台 | 第一调用 | 第二调用 | 本轮目录显示的已验证价格 |
|---|---|---|---:|
| Reddit | Search posts by keyword | List / fetch post comments | ScrapeCreators 搜帖 $0.0019/call；TikHub 搜帖 $0.001/success |
| Instagram | Search reels by keyword / List posts under a hashtag | Get post content & stats / List post comments | 搜 Reels $0.0019/call 起；话题帖 $0.001/success 起 |
| X | Search posts by keyword | Get post content & stats / List post comments | 搜帖可用 X provider `free`；TikHub $0.001/success |
| Threads | Search posts by keyword | Get post content & stats / Fetch post comments | 搜帖 $0.0019/call 起；评论 TikHub $0.002/success |

**正确用法：** 每个候选先 2–4 个任务词/抱怨词检索；保存 5 条以上可回看原帖的「时间 + 原话 + 场景 + 替代方案/失败点」。再读评论确认不是单人偶发。不要用评论量/点赞量代替需求，更不要自动群发或触达陌生人。

---

## 6. 我替你收窄后的默认调用配方

你今后可以把一句话发给我，例如：

> 「验证菲律宾 PRC 照片工具：查 `prc passport size photo with name tag` 等 6 个词的菲律宾英文 SERP、量/KD/趋势；再从 Reddit、TikTok、YouTube 找考生怎么说、是否有现成工具。」

我会按下列上限执行，不再让你逐个选网站：

1. **先手动列 6–12 个任务词**（不盲目扩几百词）。
2. **treg / DataForSEO**：每词一个菲律宾 SERP；再把所有词合到 1 次 Keyword Overview + 1 次 Bulk KD。
3. **只为当前缺口追加调用**：页面形态不清才取 advanced SERP / Search Intent；竞品切口不清才查其排名词、主力页、交集或 SERP competitors；不做全库导出。
4. **treg / 社媒**：按目标人群所在平台，每个平台只搜 2–4 次；只对强相关帖/视频拉少数评论。
5. **Chrome 人工复读**：把最关键的 3–5 条帖子/视频、前十竞争页和官方规则打开核对。
6. 输出一张机会卡：`go | watch | narrow | reject`，并明确数据口径、日期、国家及没取到的证据。

粗略成本以当前目录标价估算：12 个常规 SERP（$0.002/词）+ 1 个 Keyword Overview（$0.024）+ 1 个 Bulk KD（$0.012）+ 12 次社媒搜索（约 $0.001–0.002/次）≈ **$0.07–0.10 / 一个小方向**，不含额外评论、趋势和高级 SERP。价格是目录的实时观察值，调用前仍以页面为准。

---

## 7. 边界：现在先不做什么

- **不接新 MCP / 不买 Ahrefs / 不建爬虫流水线。** 当前 treg + Chrome 已覆盖这轮要验证的事实。
- **不让 Agent 无限探索付费接口。** 每轮先列预算、词数和停止条件；超过需你确认。
- **不把 Apify/treg/社媒返回当用户研究结论。** 帖子、模型回答、关键词与外链指标都是线索；关键来源仍要人工读上下文、看替代方案与任务频率。
- **不把 GSC/GA 或 AI Visibility 预先接成找方向工具。** 前者只在自有站上线后连接，后者只在已有明确 AI 问题与来源资产时按预算调用。
- **不把本报告的样词带入首批站。** 它只是服务小试；正式方向仍按 ADR-0013 的独立证据包进入 3–4 站组合。

## 8. 下一步

最顺的下一步不是继续研究平台，而是用这套默认服务配方做 **PRC 菲律宾照片工具的 6 个核心词**，把它和另外 2–3 个独立细分候选做成可比较的机会卡。
