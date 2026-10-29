# SEO / GEO 资源库

这是一份**活文档**：这套 SEO / GEO 方法从哪些来源来，每条取了什么、放进了哪里、哪些没照抄。查一条规则的出处、给人讲解页写资源清单、或判断一份新资料值不值得吸收时读它。各家爬虫名与站长开关不在这里，在[引擎规范手册](engine-playbook.md)的「官方来源」。

## 刷新规则

1. **每次使用先核对。** 动用某条来源的结论前，看它的核对日；超过 90 天、或手册「怎么更新」那轮查到相关变化时，回原链接重读一遍，再用。官方条目优先重查。
2. **结论变了就改两处**：改本表那一行（精髓、核对日），并改用到它的规则文件（[E-E-A-T 框架](eeat-framework.md)、[GEO 写作规则](geo-writing-rules.md)或手册），在手册「变更记录」追加一行。
3. **过期怎么标**：链接失效、页面改版找不到原话、或被更新的官方说法取代时，不删行，在核对日一栏写 `过期 YYYY-MM-DD：原因`，并写替代来源；用到它的规则同轮改掉或标待核。
4. **吸收新来源的门槛**：官方文档直接可用；研究与第三方报告写明「第三方，未经官方确认」；公开 skill 只取能落成规则、且被官方说法或我们的实测支持的部分，其余写进「没照抄」。
5. **对标站会改版。** 引用对标站的具体句子前重新打开核对；对不上就更新例句或换站。

## 官方

| 来源 | 一句话精髓 | 融进了哪里 | 没照抄 / 原因 | 核对日 |
|---|---|---|---|---|
| [Google：Our latest update to the quality rater guidelines: E-A-T gets an extra E](https://developers.google.com/search/blog/2022/12/google-raters-guidelines-e-e-a-t) | 2022-12 在 E-A-T 前加 Experience | [E-E-A-T 框架](eeat-framework.md)第 1 节 | — | 2026-10-04 |
| [Search Quality Rater Guidelines（全文 PDF）](https://guidelines.raterhub.com/searchqualityevaluatorguidelines.pdf)；[概要版](https://services.google.com/fh/files/misc/hsw-sqrg.pdf) | 原话：*The most important member at the center of the E-E-A-T family is Trust.*；YMYL 话题标准更严 | 框架第 1、3 节 | 评估员手册是给评估员的，不是排名算法说明；不把它当打分表照搬 | 2026-10-04（全文 2025-09-11 版） |
| [Google：Creating helpful, reliable, people-first content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) | Who / How / Why 自查；*E-E-A-T itself isn't a specific ranking factor*；没有偏好字数；只改日期是警示信号 | 框架第 1、2 节；[GEO 写作规则](geo-writing-rules.md)第 0、3 节 | — | 2026-10-04 |
| [Google：Search and AI-generated content](https://developers.google.com/search/blog/2023/02/google-search-and-ai-content) | 看内容质量不看是不是 AI 写的；读者会想知道时说明用了 AI | 框架第 1、2 节 | — | 2026-10-04 |
| [Google：AI features and your website](https://developers.google.com/search/docs/appearance/ai-features) | 进 AI 摘要 / AI 模式不需要特殊 Schema 或 llms.txt；结构化数据必须与可见文字一致 | 手册「总原则」；写作规则第 4 节 | — | 2026-10-04 |
| [Google：FAQPage](https://developers.google.com/search/docs/appearance/structured-data/faqpage) | FAQ 富结果 2026-05-07 起不再展示 | 手册「不必做」；写作规则第 4 节 | — | 2026-10-04 |
| [Bing Webmaster：AI Performance](https://www.bing.com/webmasters/help/ai-performance-9f8e7d6c) | 少数能看到「被 AI 引用了多少次」的官方面板 | 手册「逐家清单」「测量」 | — | 2026-10-04 |
| [OpenAI：爬虫说明](https://platform.openai.com/docs/bots) | 搜索引用、训练与用户触发的抓取入口分开管；站点按用途选择是否放行 | 手册「逐家清单」；`distribution-link-loop` 的引用观察 | 不把爬虫放行当作排名保证；不照抄第三方 allowlist | 2026-10-04 |
| [Perplexity：爬虫说明](https://docs.perplexity.ai/guides/bots) | 索引与用户实时请求的爬虫入口分开管 | 手册「逐家清单」；`distribution-link-loop` 的引用观察 | 不把 Publisher Program 当作推荐或引用保证 | 2026-10-04 |
| [Anthropic：Claude 爬虫与站长控制](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler) | 说明 Claude 的网页抓取与站长阻断控制 | 手册「逐家清单」；`distribution-link-loop` 的引用观察 | 不把训练抓取控制误写成 Claude 引用开关 | 2026-10-04 |

## 研究与第三方报告

| 来源 | 一句话精髓 | 融进了哪里 | 没照抄 / 原因 | 核对日 |
|---|---|---|---|---|
| [Aggarwal 等，GEO（KDD 2024）](https://arxiv.org/abs/2311.09735) | 加统计、引语、出处让来源在 AI 回答里可见度提升 30–40%；堆关键词下降；本来排第一的来源加了可能下降 | 写作规则第 2 节；事实台账 | 不把百分比当承诺写进计划；只加真实有用的事实 | 2026-10-04 |
| [Otterly.AI：AI Citations Report 2026](https://otterly.ai/blog/the-ai-citations-report-2026/) | 各家 AI 引用偏好差别大，ChatGPT 与 Perplexity 只有约一成域名重合 | 手册「逐家清单」要求逐家观察；`distribution-link-loop` 第 6 节 | 第三方，未经官方确认；不用它的份额数字做目标 | 2026-10-04 |
| [Wikipedia：Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) | 编辑社区整理的 AI 稿句式表 | `anti-slop-frontend` copy-gate 的 AI 味黑名单 | 只取能扫描的句式；社区判断标准不当排名依据 | 2026-10-04 |

## 指定 SEO 收藏：只取执行规则

五条公开经验的来源链接、执行项与不照搬的说法集中在[出海 SEO 执行清单](overseas-seo-checklist.md)，不保存全文，不新增工具订阅。核对日均为 2026-10-14；S1、S3 读收藏正文快照，S2、S4、S5 读原页。第三方经验未经官方确认，实施时回引擎手册复核。

| 来源编号 | 取什么 | 边界 |
| --- | --- | --- |
| S1 哥飞 | 六步页面竞争力诊断，先相关内链、再判断站外引用 | 不保证每条链接传权重或三四个月见效 |
| S2 大罗 SEO | 五条按证据缺口选工具的规则 | 不照搬工具排名、DA 报价或密度评分 |
| S3 Wyong | 四条关键词、文案、真实引用与分组观察规则 | 品牌词首页第五不是通用关键词效果 |
| S4 borja / Distribb | 六条单页取证、精确编辑与复查规则 | 扫描通过不等于收录；作者改稿尚未应用 |
| S5 Nicholas Dulait | 五条内容质量、规模化、品牌与自动化规则 | 少量运营者经验，不设固定篇数或 hack 有效期 |

## 对标站

只看页面实际怎么写；不抄视觉，不抄品牌首页。

| 站 | 学到什么（对应维度） | 融进了哪里 | 没照抄 / 原因 | 核对日 |
|---|---|---|---|---|
| [Wise 汇率换算器](https://wise.com/us/currency-converter/) | 工具在首屏，下面放 30 / 90 天自有统计（Experience） | 写作规则第 2 节「自有一手数据」 | — | 2026-10-04 |
| [NerdWallet 房贷计算器](https://www.nerdwallet.com/mortgages/mortgage-calculator) | 每个 H2 首句讲怎么用；术语一条一个定义；YMYL 话题署名作者与编辑（Expertise、Trust） | 写作规则第 1 节；框架第 3、4 节 | 署名只在有真实负责人时做 | 2026-10-04 |
| [Tarotap](https://tarotap.com/en/) | 同类塔罗站，FAQ 首句即答（Trust） | 写作规则第 1 节 | 不抄首页人设商店 | 2026-10-04 |
| [Biddy Tarot：The Fool](https://www.biddytarot.com/tarot-card-meanings/major-arcana/fool/) | 内容挂在创始人真人名下；牌义首句即定义（Experience、Expertise） | 框架第 4 节「作者署名」 | 正文后半假热情不学；不据此铺牌义页 | 2026-10-04 |
| [Grammarly 查重](https://www.grammarly.com/plagiarism-checker)（反例） | FAQ 用场景开头不直接答；数字无来源 | 写作规则第 1 节反例 | — | 2026-10-04 |

## 公开 SEO / GEO skill

GitHub 上与我们同格式的 Agent Skill。共同精髓其实就是 E-E-A-T 换了说法：答案前置、可摘取（省读者和引擎的事）；事实有来源、实体一致（Trust、Expertise）；有一手数据和示范（Experience）；被别人提到（Authority）。它们大多从写法入手，很少讲站点层信任——这是我们另写[E-E-A-T 框架](eeat-framework.md)第 4 节的原因。

| skill | 来源 | 精髓 | 融进了哪里 | 没照抄 / 原因 | 核对日 |
|---|---|---|---|---|---|
| ai-seo | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills/blob/main/skills/ai-seo/SKILL.md) | 按问题类型写可摘取的块：定义、步骤、比较表、FAQ | 写作规则第 2 节 | 它的百分比表把论文简化过头、丢了「排第一的可能下降」，数字不抄 | 2026-10-04 |
| programmatic-seo | [同仓库，固定 SHA](https://github.com/coreyhaines31/marketingskills/blob/5b2c0007766c6a1cf1d53fd8fc73e979e0821022/skills/programmatic-seo/SKILL.md) | 批量页的前提是每页有独特数据，否则是规模化内容滥用 | [内容、多语言与 pSEO](content-scale-localization.md) | — | 2026-10-04 |
| seo-geo、seo-content-brief | [AgriciDaniel/claude-seo：seo-geo](https://github.com/AgriciDaniel/claude-seo/blob/main/skills/seo-geo/SKILL.md)、[content brief（固定 SHA）](https://github.com/AgriciDaniel/claude-seo/blob/a1480c7e590b16001bd9dc1627eacdcd44d580f9/skills/seo-content-brief/SKILL.md) | 答案前置、40–60 词答案块；第三方经验与官方说法分开标注 | 写作规则第 1 节；全部规则的来源分级 | 40–60 词只当提示，不设硬数字 | 2026-10-04 |
| seo-hreflang | [AgriciDaniel/codex-seo（固定 SHA）](https://github.com/AgriciDaniel/codex-seo/blob/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills/seo-hreflang/SKILL.md) | 多语言页互相声明、带回链，不靠 IP 跳转 | 内容、多语言与 pSEO | — | 2026-10-04 |
| technical-seo-checker | [aaron-he-zhu/aaron-marketing-skills（固定 SHA）](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/technical-seo-checker/references/pre-migration-playbook.md) | 迁移、改域名前先做 URL 对照表和回滚预案 | [上线、测量与技术迁移交接](launch-technical-handoff.md) | — | 2026-10-04 |
