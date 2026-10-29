# 搜索与 AI 引擎规范手册

这是一份**活文档**。SEO 管传统搜索（Google、Bing 等），GEO 管 AI 引擎（ChatGPT、Perplexity、Gemini、Claude、Copilot、Google AI 模式等）回答时会不会引用、推荐你。两样都要做，每家都要过，不只盯一家。

`seo-site`、`distribution-link-loop`、`product-growth-review` 都读这一份；各家规则只在这里写，别的 skill 指过来。

## 怎么更新（每次都主动做）

1. **每次用到就先查**：对照下面「官方来源」逐家看一遍，重点找：新爬虫或爬虫改名、新的抓取/引用开关、新的站长报告或数据、官方明确说「要做」或「不必做」的事、新的 AI 引擎进入目标市场。每条的查阅日超过 30 天，这次必须重查。
2. **主动探索，不只查清单**：顺手搜一下「{引擎名} + site owners / webmasters / publishers + 当前年份」，看有没有清单外的新入口或新引擎。第三方文章只当线索，回一手来源核实后才写进来。
3. **写回来**：有变化就改对应条目、更新查阅日，并在文末「变更记录」追加一行（日期、改了什么、来源、影响哪个 skill）。写回走 mono 仓库改 `skills/selfmedia/seo-site/references/engine-playbook.md` 开 PR；当场改不了就在任务里写清变化并开一张 Multica 任务，不能只口头提一句。
4. **别的 skill 跟着变**：规范变化影响到其他 skill（比如埋点口径、分发打法）时，一并改掉，并在变更记录里写上改了哪个 skill。
5. **实战经验也写回**：真实项目里验证过或踩过的坑，写进「实战经验」，带项目、日期和证据位置。没验证的想法不写。

官方说法优先于第三方经验；第三方经验可以试，写明「第三方经验，未经官方确认」。

## 总原则（2026-09-26 查阅）

- **GEO 的地基就是 SEO。** Google 官方说法：想出现在 AI 摘要（AI Overviews）和 AI 模式（AI Mode）里，不需要额外优化，照常做好 SEO 就行；llms.txt、把内容切碎、专门的 Schema 都不是必需。所以先把页面任务、初始 HTML、抓取索引做对，别在「GEO 专用技巧」上瞎忙。
- **AI 引擎引用的是具体事实。** 能被引用的通常是：直接回答问题的段落、真实样例与数据、比较、限制说明、有出处的数字、清楚的更新日期。这些本来就是好页面该有的，写进 brief 的「可被引用的事实」一栏。具体写法（每段对应哪个问题、可引用句、实体、Schema）见 [GEO 写作规则](geo-writing-rules.md)。
- **AI 引擎大多不跑 JavaScript。** 关键内容必须在服务器返回的初始 HTML 里。
- **搜索爬虫和训练爬虫分开管。** 各家都把「给搜索/回答抓取」和「拿去训练模型」拆成不同的爬虫名。**搜索类默认放行**（挡了就不会被引用）；训练类挡不挡是商业决定，由人拍板并记录，不由 Agent 默认。
- **第三方站点常常比自家站更容易被引用**（Wikipedia、Reddit、测评榜单等）。站外来源归 `distribution-link-loop`。

## 逐家清单

每家在体检时标 `可用 / 待接入 / 不适用`。爬虫名和开关以查阅日为准，用前按上面的流程重查。

| 引擎 | 抓取用的爬虫（robots.txt 名） | 站长能做的事 | 能看到的数据 |
|---|---|---|---|
| **Google 搜索 + AI 摘要 + AI 模式** | `Googlebot`；`Google-Extended` 管 Gemini 训练与 grounding，不影响 Google 搜索收录 | Search Console 验证所有权、提交 sitemap；Search Console 里有是否允许被 AI 摘要/AI 模式引用的开关（2026-08-31 起全球开放），上线时当成一次明确决定写进记录 | Search Console 效果报告 |
| **Gemini（App）** | 用 Google 的索引；训练与 grounding 由 `Google-Extended` 控制 | 同 Google | 暂无第一方引用报告；看 referral 流量 |
| **Bing 搜索 + Copilot** | `Bingbot` | Bing Webmaster Tools 验证、提交 sitemap；**IndexNow**：页面一更新就通知 Bing，Copilot 不会拿旧内容回答（Google 不支持 IndexNow） | Bing Webmaster **AI Performance** 报告（2026-02 起）：Copilot 引用了哪些页、因为什么问题；2026-06 起加了意图、话题、引用份额。**目前唯一由平台官方给的「AI 推荐了你没有」数据** |
| **ChatGPT 搜索** | `OAI-SearchBot`（搜索引用，挡了就进不了 ChatGPT 搜索结果）；`GPTBot`（训练）；`ChatGPT-User`（用户让它打开某页时） | 放行 `OAI-SearchBot`；卖实物商品可在 chatgpt.com/merchants 申请提交商品 feed（Agentic Commerce Protocol），价格库存由 feed 提供 | 来自 ChatGPT 的点击带 `utm_source=chatgpt.com`，在分析工具里单列 |
| **Perplexity** | `PerplexityBot`（索引）；`Perplexity-User`（用户实时请求） | 两个都放行；有出版商分成计划（Publisher Program），内容站可评估是否申请 | 看 referral（perplexity.ai） |
| **Claude** | `Claude-SearchBot`（搜索索引）；`ClaudeBot`（训练）；`Claude-User`（用户请求时抓取）。挡训练不会挡另两个 | 放行 `Claude-SearchBot` 和 `Claude-User` | 看 referral（claude.ai） |

新的引擎（比如目标市场本地的 AI 助手、Apple 等）进入目标市场时，按同样四列补一行。

## 测量

- **分开记三件事**：被引用/提及了没有、引用得准不准、点进来的人完成任务没有。只有第三件是业务结果。
- **官方数据先用**：Search Console、Bing Webmaster AI Performance。
- **AI referral 单列**：在分析工具里把 chatgpt.com、perplexity.ai、gemini.google.com、claude.ai、copilot.microsoft.com 等来源单独分组；随引擎变化更新这份域名清单。
- **固定问题集抽查**：没有官方数据的引擎，用一组固定的真实用户问题定期去问，记平台、日期、地区/语言、是否开搜索、原始回答快照；自然提问和带自家 URL 的辅助测试分开记。一次回答只说明「那一刻看到了什么」，不外推份额。
- 第三方「AI 可见度」工具的分数只当线索，不当结论。

## 不必做 / 别做（2026-09-26 查阅）

- 不为 AI 单独写一套页面或把内容切碎；不把 llms.txt 当成必需项（Google 明确不需要；其他家没有官方承诺会读它）。
- 不给 AI 爬虫看和用户不一样的内容。
- 不堆不可见的 Schema、FAQ 或评价。
- 不为 FAQ 富结果写 FAQ：Google 自 2026-05-07 起不再展示 FAQ 富结果（2026-10-04 查阅）；`FAQPage` 标记无害，但只在问答本来就该在页上时保留。
- 不按字数写：Google 明说没有偏好字数；GEO 论文测到堆关键词让 AI 引擎可见度下降。
- 不买「保证被 AI 推荐」的服务或批量软文。

## 实战经验

真实项目里验证过的做法和踩过的坑写在这里，每条带项目、日期、证据位置。

- （暂无。第一个真实上线的出海站跑完后补。）

## 官方来源

- [Google：AI 功能与你的网站](https://developers.google.com/search/docs/appearance/ai-features)
- [Google：FAQPage 结构化数据（富结果已停）](https://developers.google.com/search/docs/appearance/structured-data/faqpage)
- [Google：有用、可靠、以人为本的内容](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)
- [Google：给网站所有者的新控制与洞察](https://blog.google/products-and-platforms/products/search/new-controls-website-owners/)
- [Google 爬虫列表（含 Google-Extended）](https://developers.google.com/search/docs/crawling-indexing/google-common-crawlers)
- [Bing Webmaster：AI Performance](https://www.bing.com/webmasters/help/ai-performance-9f8e7d6c)
- [Bing 博客：AI 可见度新报告（2026-06）](https://blogs.bing.com/search/2026/6/New-AI-Visibility-Insights-in-Bing-Webmaster-Tools-Intents-Topics-Citation-Share-Compare/)
- [IndexNow](https://www.indexnow.org/)
- [OpenAI：爬虫说明](https://platform.openai.com/docs/bots)、[ChatGPT 搜索帮助](https://help.openai.com/en/articles/9237897-chatgpt-search)、[ChatGPT 商家入口](https://chatgpt.com/merchants/)
- [Perplexity：爬虫说明](https://docs.perplexity.ai/guides/bots)
- [Anthropic：Claude 爬虫与站长控制](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler)

## 变更记录

| 日期 | 改了什么 | 来源 | 影响的 skill |
|---|---|---|---|
| 2026-09-26 | 建立本手册：Google/Gemini、Bing/Copilot、ChatGPT、Perplexity、Claude 逐家清单；Google「GEO 仍是 SEO」、AI 引用开关、Bing AI Performance、IndexNow、OpenAI/Anthropic 搜索与训练爬虫分离、ChatGPT 商品 feed | 见上方官方来源 | `seo-site`（新建，并入原 seo-site-blueprint 与 seo-readiness-audit）、`distribution-link-loop`、`product-growth-review` |
| 2026-10-04 | Google FAQ 富结果 2026-05-07 起停止展示；补「不按字数写」；新增 [GEO 写作规则](geo-writing-rules.md)（问题表、可引用句、实体一致、Schema 配法，附对标站与方法来源） | Google FAQPage 文档、有用内容文档、GEO 论文（KDD 2024）；DENE-1302 | `seo-site`、`distribution-link-loop`、`anti-slop-frontend`（copy-gate） |
| 2026-10-04 | 新增 [E-E-A-T 框架](eeat-framework.md)作为 SEO / GEO 的根（Trust 为核心、Who / How / Why、YMYL、信任页清单、体检表、Authority 交接）与[资源库](source-library.md)（含刷新规则）；讲解页模板进 `seo-site/assets/` | Google E-E-A-T 博客、Search Quality Rater Guidelines（2025-09-11 版）、Creating helpful content；DENE-1323 | `seo-site`、`ask-selfmedia`、`distribution-link-loop` 及其他出海 skill 的「SEO / GEO」一节 |
