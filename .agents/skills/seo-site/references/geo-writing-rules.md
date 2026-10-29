# GEO 写作规则：任务页正文、FAQ 与结构化数据

把 brief 写成可上线正文时读这份。它回答四件事：每段内容对应哪个搜索问题、哪句话可以被直接引用、实体与事实怎么写、结构化数据怎么配。SEO 和 GEO 用同一份正文，不为 AI 另写一套（Google 明说不需要，另写还可能踩「规模化内容滥用」）。

本文件挂在 [E-E-A-T 框架](eeat-framework.md)下，管块级的 Expertise、Experience 与 Trust；站点层的信任页和体检表在框架里。

文字质量的底线归 `anti-slop-frontend` 的 copy-gate：没有 AI 味、强档撰写定稿、扫描脚本过一遍。本文件只管「这段为搜索和 AI 引擎做了什么」。两边都要过。

## 0. 先认清楚：长文不是凑字数的地方

Google 明说没有偏好字数，按字数写是「搜索引擎优先」的警示信号；GEO 论文测到堆关键词让 AI 引擎可见度下降。长文的唯一理由是回答真实问题、给出别处没有的事实。一段删掉后读者能知道的、能做的都没少，它就不该在页上。任务页下半截宁可五段实在的，也不要十段车轱辘话。

## 1. 每段对应一个搜索问题

动笔前列「问题表」，再写正文。问题只从这些地方来，并记下来源与日期：

- 真实 SERP 的「People also ask」、相关搜索、排名页的小标题；
- GSC 查询、站内搜索、客服与用户反馈；
- 已有工具授权时，在各家 AI 引擎问同一任务看到的追问方向（Google 把 AI 模式的一个问题拆成多个子查询去找来源，所以子问题都要有段落承接）；
- 竞品 FAQ 与对标站的页内问题（只作为线索，回到 SERP 核实）。

然后一行一块：

| 块（H2 / FAQ 条） | 对应的搜索问题（用户原话） | 首句直接答 | 可引用句 | 事实来源 | 结构化数据 |
|---|---|---|---|---|---|

规则：

1. **H2 用用户问法写**，一个 H2 回答一个问题。两个 H2 回答同一个问题就合并；一个 H2 里塞了三个问题就拆开或删掉两个。
2. **首句直接回答**，不铺垫、不讲背景、不用场景开头（反例：Grammarly 的 FAQ「What is plagiarism?」第一句是 *You're working on a paper, and you've just written a line that seems kind of familiar.*）。正例：NerdWallet 的术语区 *Total monthly payment: An estimate of all your monthly housing costs, covering your loan principal, interest, taxes, insurance, and PMI.*；Tarotap 的 FAQ「Can tarot cards predict the future?」首句 *Not in a deterministic way.*
3. **段落能单独成立**：被 AI 引擎单独摘走时也看得懂。主语写名字不写「it / this」，不依赖上一段。长短不设硬数字；第三方经验常说 40–60 词的答案块好摘，只当提示。
4. **答案、关键事实放在页面早段、初始 HTML 里。** 首屏仍是操作区；操作区下面第一块就放最能被引用的那段，不放品牌故事。第三方统计称 AI 引用多半出自页面前三成（未经官方确认）。
5. **没有对应问题的段落删掉。** 「仪式感」「旅程」之类的过渡段、首屏承诺的复述，都属于这类。

## 2. 每块至少一句可被直接引用的话

可引用句 = 摘出来单独放进一个 AI 回答里，仍然准确、完整、有来源可追。常见几种：

| 句型 | 例 |
|---|---|
| 定义：`X is …` | *A tarot spread is a fixed layout where each position gives the card a question to answer.* |
| 数字事实（带单位与范围） | *A standard Rider–Waite–Smith deck has 78 cards: 22 Major Arcana and 56 Minor Arcana.* |
| 规则与边界 | *Drawing is free and unlimited; an AI reading needs a free account.* |
| 步骤（有序列表） | *1. Choose a spread. 2. Shuffle. 3. Turn the cards one at a time.* |
| 比较（表格） | 1 / 3 / 5 / 10 张牌型各自适合什么问题 |
| 自有一手数据 | Wise 在汇率换算器下给出 30 天 / 90 天的最高、最低、均值和涨跌，这是别处没有的数 |

依据与分寸：

- GEO 论文（KDD 2024）测到加统计数字、加可信引语、加出处这三种改法让来源在 AI 回答里的可见度提升 30–40%；同一表里，本来排第一的来源加这些反而可能下降。所以加的是**真实且有用**的事实，不是为了 GEO 往每段塞数字。
- 数字必须进事实台账（claim ledger）：来源、日期、owner。没有来源的数字不写；示例与演示要明确标出来。
- 引语只引真实、具名、可查的人或机构。不编造「专家说」，也不写「研究表明」却不给出处（copy-gate 黑名单第 8 类）。

## 3. 实体与事实怎么写

AI 引擎和 Google 靠「实体」理解你是谁、页面讲的是什么。ChatGPT 的引用里 Wikipedia 占很大比重（第三方统计），说明它偏好写法稳定、定义清楚的实体来源。

1. **一个实体一种叫法，全站一致**：品牌名、产品名、功能名、牌组名（Rider–Waite–Smith）、牌名（The Fool，不在别处写成 Fool card）。正文、FAQ、title、结构化数据、站外资料（目录、社交主页）用同一写法。
2. **首次出现给定义**：领域词第一次出现时用一句话说清它是什么，后文不再换同义词。
3. **事实单源**：价格、限额、张数、支持的付款方式这类事实在产品里只有一个来源，页面文字从那里取。改了事实，所有出现的地方同一次改完，包括结构化数据和 FAQ。
4. **写清是谁、怎么来的**：Google 的有用内容自查要求读者能看出内容是谁做的、怎么做的（例如「由 AI 生成，仅供娱乐与自省」这类说明放在相关位置）。YMYL 类话题（健康、财务、法律）不作承诺；娱乐类产品写清边界。
5. **日期只在内容真改了的时候更新。** 第三方统计显示 Perplexity 偏好新内容，但 Google 明确把「内容没变却改日期」列为警示信号。要新鲜就去更新事实，不要只改日期。

## 4. 结构化数据怎么配

原则（Google 官方）：出现在 AI 摘要 / AI 模式里不需要特殊 Schema、不需要 llms.txt；结构化数据必须和页面上**看得见**的文字一致。

| 页面 / 区块 | 建议类型 | 备注 |
|---|---|---|
| 全站（通常挂首页） | `Organization`（`name`、`url`、`logo`、`sameAs` 指向官方社交与目录主页）+ `WebSite` | `sameAs` 只放真实存在、由我们控制的主页，帮引擎对上同一实体 |
| 工具 / 任务页 | `WebApplication` 或 `SoftwareApplication`（`applicationCategory`、`isAccessibleForFree`、`offers` 仅在价格真实可见时） | `description` 与页面首屏承诺同一句意 |
| 面包屑 | `BreadcrumbList` | 与页面上可见的面包屑一致 |
| 文章 / 指南 | `Article`（`author`、`datePublished`、`dateModified`） | 作者要真实；`dateModified` 遵守第 3 节第 5 条 |
| FAQ | `FAQPage` 可选 | **Google 自 2026-05-07 起不再展示 FAQ 富结果**（文档 2026-06 更新）；标记本身无害、也不再带来 SERP 展示。保留的前提是问答在页面上可见且与标记逐字一致；不为它新增 FAQ |
| 价格页 | `Product` / `Offer` | 只在价格来自已建好的支付 catalog 且页面可见时写 |
| 评分 | `AggregateRating` / `Review` | 只有真实、可核对的评价才写；不自评 |

不做：为 AI 加特殊标记、标记页面上没有的内容、用标记堆关键词、自造评分。

## 5. FAQ 怎么写

1. 问题来自第 1 节的问题表，用用户原话；不把正文 H2 换个说法再问一遍。
2. 答案第一个词或第一句就是答案：Yes / No / 一个数字 / 一个动作。然后最多两句补充条件与下一步。
3. 每条答案能单独成立（主语写全称）。
4. 只答本页任务相关的问题；跨页问题一句话答完并链到那一页。
5. 同一问题全站只在一处回答，别的页链过去。

## 6. 交付时附什么

正文交付物里附第 1 节的问题表（每块对应的问题、可引用句、事实来源、结构化数据类型），以及过 copy-gate 的记录（扫描结果、定稿出自哪个强档）。完工体检时 `seo-site` 第三段逐页对这张表。

## 来源（查阅 2026-10-04）

官方：

- Google，[AI features and your website](https://developers.google.com/search/docs/appearance/ai-features)：AI 摘要 / AI 模式没有额外要求，不需要特殊 Schema 或 AI 文本文件；结构化数据要和可见文字一致；重要内容要有文字形式。
- Google，[Creating helpful, reliable, people-first content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)：没有偏好字数；内容没变却改日期是警示信号；用「谁、怎么、为什么」自查。
- Google，[FAQPage structured data](https://developers.google.com/search/docs/appearance/structured-data/faqpage)：FAQ 富结果 2026-05-07 起不再展示。

研究与第三方方法：

- Aggarwal 等，[GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735)（KDD 2024）：加统计、引语、出处让来源可见度提升 30–40%，堆关键词下降；对本来排第一的来源，这些改法可能反而降低可见度。
- Corey Haines，[marketingskills / ai-seo](https://github.com/coreyhaines31/marketingskills/blob/main/skills/ai-seo/SKILL.md)：按问题类型写可摘取的块（定义、步骤、比较表、FAQ）；分开管 AI 搜索爬虫与训练爬虫。缺点：把论文的数字简化成了一张百分比表，丢了「对排名靠前的来源可能下降」这一条。
- AgriciDaniel，[claude-seo / seo-geo](https://github.com/AgriciDaniel/claude-seo/blob/main/skills/seo-geo/SKILL.md)：答案前置、问句式小标题、40–60 词答案块；并且把第三方经验（130–170 词、前三成页面）和 Google 官方说法分开标注。本文件沿用这种分开标注的做法。
- Wikipedia，[Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)：编辑社区整理的 AI 稿句式表，是 copy-gate 黑名单的主要来源。
- Otterly.AI，[AI citations report 2026](https://otterly.ai/blog/the-ai-citations-report-2026/)（第三方，未经官方确认）：ChatGPT、Perplexity、Google AI 摘要各自的引用来源偏好差别很大，只有约一成域名被两家同时引用，所以要逐家观察。

对标站（2026-10-04 页面观察）：

- Wise [currency converter](https://wise.com/us/currency-converter/)：工具在首屏，下面是实时汇率表、30 / 90 天统计和 4 条 FAQ。自有数据就是它最容易被引用的部分。
- NerdWallet [mortgage calculator](https://www.nerdwallet.com/mortgages/mortgage-calculator)：每个 H2 首句直接说怎么用；术语区一条一个定义，最容易被摘走。
- Tarotap [/en/](https://tarotap.com/en/)：同类塔罗站。FAQ 首句就是答案（*Try not to.* / *Not in a deterministic way.*），后面接具体做法，没有空话。
- Biddy Tarot [The Fool](https://www.biddytarot.com/tarot-card-meanings/major-arcana/fool/)：首句定义 *The Fool is a card of new beginnings, opportunity and potential.*，带 `Article`、`FAQPage`、`BreadcrumbList`。正文后半有假热情（*The time is NOW!*），可引用的只有定义那几句。
- Grammarly [plagiarism checker](https://www.grammarly.com/plagiarism-checker)（反例）：FAQ 用场景开头而不直接回答；「16 billion」「94% of students」这些数字页面上没有来源。
