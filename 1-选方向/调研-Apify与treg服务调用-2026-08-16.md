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
| 「去 Reddit / Instagram / X / Threads 看真人怎么抱怨、怎么描述、用什么替代」 | **treg → 对应平台 Search posts + Post comments** | 帖子、评论、原话、竞品/替代方案线索 | 需求验证阶段 |
| 「把这个竞品站的内容/价格/功能页整体拆出来」 | Chrome + Tavily/网页抓取；需要大量或定期时才上 Apify | 页面与功能缺口，不是 SEO 量/KD | 竞品深挖 |
| 「每周自动抓 100 个 SERP / 一批账号帖子并导出」 | **Apify task / schedule**（或直接官方 API） | 可重跑、导出、定时的采集任务 | 已有稳定、重复的批量需求后 |

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

## 2. 为什么 treg 比 Apify 更适合当前阶段

| 对比 | treg | Apify Console |
|---|---|---|
| 操作方式 | 一个目录下选服务，Agent 可直接按参数调用 | 先找 Actor、读其 schema、填输入、开 run、看 dataset |
| 当前最需要的 SEO 数据 | 已聚合 DataForSEO：SERP、autocomplete、关键词概览、KD、扩词等 | 官方 Google SERP Actor 擅长 SERP；量/KD 要另找第三方 Actor，数据来源/口径须额外审核 |
| 社媒小样本 | Reddit / Instagram / X / Threads 均有「关键词搜索 / 帖子详情 / 评论」入口 | 有对应 Actor，但不同作者/定价/schema 不一致；批量时才更有价值 |
| 小样本成本 | 本次的可见价格约：SERP $0.002/词、关键词概览 $0.024/次、Reddit 搜索 $0.00188/次 | Google SERP Actor 标示 $4.50/1,000 个搜索结果页（约 $0.0045/页）；不同 Actor 各自计价 |
| 应用边界 | **现在的人工闭环默认用它** | 需要定时、大批量、网页结构化/导出时再用 |

这不是说 Apify 差：它是「可部署、可调度的抓取执行平台」；而你眼下需要的是一张服务单，不是搭采集流水线。先不额外引入 Actor、task、schedule 和多家数据源的学习/维护成本。

---

## 3. 这次手动小试：`tattoo stencil maker`（美国/英语）

> 这是用于验证服务链和证据纪律的样词，**不是首批建站建议**。本次结果反而证明了：低 KD 不等于蓝海。

### 3.1 Apify：官方 Google Search Results Scraper

- Actor：`apify/google-search-scraper`（Apify 维护）。
- Run：`XuEQfemeoNBqqeA1a`；输入为 `tattoo stencil maker`、`countryCode: us`、英语、只取基础 SERP 项。
- Console 标价：**$4.50 / 1,000 scraped search result pages**。
- 验证结果：能按国家/语言跑出 SERP dataset；因此它符合「指定国家/语言 Google SERP」这个能力。
- 但它不直接给可比较的搜索量/KD；要补量/KD 得再接另一个 Actor 或数据源。这正是当前不把它当默认入口的原因。

### 3.2 treg：同一词的三个服务调用

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

## 4. 社媒服务：按平台怎么用

treg 目录中，本轮确认到的最小可用组合如下（先关键词找帖子，再对少数高相关帖取评论）：

| 平台 | 第一调用 | 第二调用 | 本轮目录显示的已验证价格 |
|---|---|---|---:|
| Reddit | Search posts by keyword | List / fetch post comments | ScrapeCreators 搜帖 $0.0019/call；TikHub 搜帖 $0.001/success |
| Instagram | Search reels by keyword / List posts under a hashtag | Get post content & stats / List post comments | 搜 Reels $0.0019/call 起；话题帖 $0.001/success 起 |
| X | Search posts by keyword | Get post content & stats / List post comments | 搜帖可用 X provider `free`；TikHub $0.001/success |
| Threads | Search posts by keyword | Get post content & stats / Fetch post comments | 搜帖 $0.0019/call 起；评论 TikHub $0.002/success |

**正确用法：** 每个候选先 2–4 个任务词/抱怨词检索；保存 5 条以上可回看原帖的「时间 + 原话 + 场景 + 替代方案/失败点」。再读评论确认不是单人偶发。不要用评论量/点赞量代替需求，更不要自动群发或触达陌生人。

---

## 5. 我替你收窄后的默认调用配方

你今后可以把一句话发给我，例如：

> 「验证菲律宾 PRC 照片工具：查 `prc passport size photo with name tag` 等 6 个词的菲律宾英文 SERP、量/KD/趋势；再从 Reddit、TikTok、YouTube 找考生怎么说、是否有现成工具。」

我会按下列上限执行，不再让你逐个选网站：

1. **先手动列 6–12 个任务词**（不盲目扩几百词）。
2. **treg / DataForSEO**：每词一个菲律宾 SERP；再把所有词合到 1 次 Keyword Overview + 1 次 Bulk KD。
3. **treg / 社媒**：每个平台只搜 2–4 次；只对强相关帖拉少数评论。
4. **Chrome 人工复读**：把最关键的 3–5 条帖子、前十竞争页和官方规则打开核对。
5. 输出一张机会卡：`go | watch | narrow | reject`，并明确数据口径、日期、国家及没取到的证据。

粗略成本以当前目录标价估算：12 个常规 SERP（$0.002/词）+ 1 个 Keyword Overview（$0.024）+ 1 个 Bulk KD（$0.012）+ 12 次社媒搜索（约 $0.001–0.002/次）≈ **$0.07–0.10 / 一个小方向**，不含额外评论、趋势和高级 SERP。价格是目录的实时观察值，调用前仍以页面为准。

---

## 6. 边界：现在先不做什么

- **不接新 MCP / 不买 Ahrefs / 不建爬虫流水线。** 当前 treg + Chrome 已覆盖这轮要验证的事实。
- **不让 Agent 无限探索付费接口。** 每轮先列预算、词数和停止条件；超过需你确认。
- **不把 Apify/社媒抓取当用户研究结论。** 帖子是线索，最终仍要人工读原帖、看替代方案与任务频率。
- **不把本报告的样词带入首批站。** 它只是服务小试；正式方向仍按 ADR-0013 的独立证据包进入 3–4 站组合。

## 7. 下一步

最顺的下一步不是继续研究平台，而是用这套默认服务配方做 **PRC 菲律宾照片工具的 6 个核心词**，把它和另外 2–3 个独立细分候选做成可比较的机会卡。
