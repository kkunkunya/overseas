# NanoSkill：做站、产品、增长与内容技能调研

- 调研日期：2026-08-16
- 目录源：[NanoSkill 中文技能目录](https://nanoskill.ai/zh/skills)
- 方法：只读检查当前中文目录完整 DOM、页面控件与 Next.js 网络请求；逐条按官方中文卡片简介筛选，并链接至官方详情页。
- **覆盖范围**：目录标题称“已收录 150 个技能”，但本次访问时 `/zh/skills` 实际渲染 **50 条**，已全部检查。
- **目录机制**：仅有关键词搜索框；未发现分类、分页、加载更多/无限加载或可补页的公开列表接口。网络中只见已列详情页的 Next.js RSC 预取，不是额外目录数据。因此本报告覆盖的是**当前中文页面可见的完整 50 条**，不声称已经找回标题所说、但页面未展示的另 100 条。
- 筛选结果：**27 项直接相关**；另列 3 项渠道/买量后期的外围技能。
- 排除原则：泛办公/邮件、学术、PPT、图表、Amazon 实物电商运营链条，以及不构成工具站主线的“AI 去痕”等。
- 证据等级：下表能力均是 NanoSkill 官方目录/详情页的**自述**，不是我们独立验证过的效果、安全性或合规性。

## 先说结论

对当前「垂直细分 + 长期稳定增长」的工具站路径，最值得看的不是把 27 个都装上，而是先拿它们补齐以下闭环：

`真实痛点与用户语言 → 搜索/SERP 证据 → 竞品切口 → 最小承接页 → 文案/转化 → 内容和持续分发`

建议优先研究的次序：

1. 利基市场研究
2. SEO/GEO 关键词研究
3. 社交媒体监听 + Reddit 内容检索
4. 竞争对手分析
5. 创意转设计方案
6. 产品营销背景 → 产品营销文案 → CRO
7. 只有需求、数据资产与独立页面价值已经验证后，才考虑程序化 SEO

这与本库已有 `vertical-keyword-loop`、`direction-validator`、`mvp-validation` 的顺序高度重叠：NanoSkill 更适合按需借其中某一个执行模块，**不要整包替代现有验证闸门，更不要未审源代码就批量安装**。

## 直接相关的 27 项

优先级：**P0** = 当前路径优先；**P1** = 紧随其后；**P2** = 有稳定需求/内容后；**P3** = 开始买量后。

| 类别 | 技能（官方详情 / 证据） | 官方关键能力（压缩转述） | 适用场景与建议 |
|---|---|---|---|
| 产品发现 | [利基市场研究技能](https://nanoskill.ai/zh/skills/niche-research) | 扫论坛、Reddit、行业站、活动与平台，提取痛点、用户说法、机会和可售软件方向。 | 垂直选题、验证用户语言；**P0**。与 `direction-validator` 的社区/需求证据卡重叠。 |
| 产品发现 | [竞争对手分析技能](https://nanoskill.ai/zh/skills/competitive-analysis-skill) | 比较定位、信息传递和内容策略，发现缺口、机会、威胁。 | 找更窄的产品句子与 SERP 分食切口；**P0**。 |
| 产品 / MVP | [将创意转化为设计方案的智能体技能](https://nanoskill.ai/zh/skills/brainstorming-ideas-to-designs) | 以结构化对话和推理把模糊想法转为清晰、验证过的设计与规范，避免过早实现。 | 确定 MVP 承诺和范围；**P0**。不能代替需求验证。 |
| 做站 / UX | [网页模型草图生成器](https://nanoskill.ai/zh/skills/html-mockup-sketcher) | 生成 2–3 个可交互网页模型变体，比较 UI/UX 方向并收集反馈。 | 落地页或工具界面探索；**P1**。应在承诺已确定之后使用。 |
| 做站 / 视觉 | [视觉设计代理技能](https://nanoskill.ai/zh/skills/visual-design-skill) | 生成 PNG/PDF 视觉设计成品。 | 做首屏、说明图或营销素材；**P2**。 |
| 品牌 | [品牌工具包图像生成技能](https://nanoskill.ai/zh/skills/brandkit-image-generation) | 生成 Logo、色彩、字体和风格体系。 | 从零建立基础视觉识别；**P2**。 |
| 品牌 | [品牌指南代理技能](https://nanoskill.ai/zh/skills/brand-guidelines) | 把既定品牌色彩和版式应用到文档/展示物，保持一致。 | 与品牌工具包不同：前者“从零产出”，本项“按规范应用”；**P2**。 |
| 做站动效 | [GSAP AI 代理技能](https://nanoskill.ai/zh/skills/gsap-ai-skills) | 指导代理使用 GSAP 核心 API、插件和框架。 | 真有交互动效需求才用；**P2**。不应为炫技增加复杂度。 |
| SEO / GEO | [搜索引擎优化与生成引擎优化关键词研究技能](https://nanoskill.ai/zh/skills/seo-geo-keyword-research-skill-c162) | 关键词研究、GEO 评分、AI 引用分析、竞品缺口检测。 | 搜索需求、竞争和内容/工具页机会；**P0**。数值仍须回真 SERP 与独立数据源取证。 |
| SEO | [程序化 SEO 技能](https://nanoskill.ai/zh/skills/programmatic-seo-skill) | 批量建立数据驱动的独特页面以争取排名，并避免惩罚。 | **条件式 P0**：只在有真实、可维护的数据资产和独立页面任务后使用；不能用来批量造薄页。 |
| SEO | [SEO 审计代理技能](https://nanoskill.ai/zh/skills/seo-audit) | 审计单页与站点层问题，输出可操作的修复报告。 | 上线后技术 SEO 排查；**P1**。 |
| SEO / GEO | [SEO 内容 AI 优化器](https://nanoskill.ai/zh/skills/ai-seo-content-optimizer) | 面向 Google AI Overviews、ChatGPT、Perplexity 做内容与引用就绪优化。 | 内容已能解决真实问题后加强可见度；**P1**。不是绕过 SEO 的捷径。 |
| 产品营销 | [产品营销背景代理技能](https://nanoskill.ai/zh/skills/product-marketing-context) | 生成/更新产品营销背景文档，集中定位与信息传递。 | 定位、目标用户和承诺的单一事实源；**P1**。 |
| 转化 | [转化率优化代理技能](https://nanoskill.ai/zh/skills/cro-agent-skill-c168) | 分析营销页面，给出落地页和表单的转化改进建议。 | 有真实访问/行为数据后迭代；**P1**。无流量时先修触达与承接，别空做 CRO。 |
| 文案 | [文案写作专家](https://nanoskill.ai/zh/skills/copywriting) | 为网页写清晰、有说服力、面向转化的营销文案。 | 通用页面文案；**P1**。 |
| 文案 | [产品营销文案撰写代理技能](https://nanoskill.ai/zh/skills/product-marketing-copywriting) | 按目标受众为 SaaS 等产品写标题、正文与 CTA。 | 比通用文案更适合产品落地页；**P1**。先有产品营销背景再用。 |
| 用户研究 / 选题 | [社交媒体监听代理技能](https://nanoskill.ai/zh/skills/social-listening-skill) | 扫 Reddit、X、YouTube、TikTok 近 30 天内容，按真实互动排序。 | 找正在升温的问题、原话和内容角度；**P0**。观察不等于需求已验证。 |
| 用户研究 | [Reddit 内容检索代理技能](https://nanoskill.ai/zh/skills/reddit-content-retrieval) | 通过公开 JSON API 获取帖子、评论、社区与用户资料。 | 深挖特定 subreddit 的痛点和规则；**P1**。应遵守平台规则，不把用户当群发名单。 |
| 内容研究 | [油管转录代理技能](https://nanoskill.ai/zh/skills/youtube-transcript) | 通过 URL/ID 下载转录、字幕、封面；支持翻译、章节、说话人识别。 | 拆竞品演示、复原真实场景、找内容选题；**P1**。 |
| 内容写作 | [内容研究撰稿代理技能](https://nanoskill.ai/zh/skills/content-research-writer) | 研究、列大纲、写草稿和润色，同时保留个人声音。 | 核心内容/深度文章；**P1**。事实与案例需人工复核。 |
| 内容 / SEO | [Claude Code 的 AI 博客写作代理技能](https://nanoskill.ai/zh/skills/ai-blog-writing-skill) | 批量生成、优化、审核博客，兼顾 Google 排名和 AI 引用。 | 成熟内容流水线；**P1**。不能批量生产无独立价值的 SEO 薄页。 |
| 内容视觉 | [创意内容生成代理技能](https://nanoskill.ai/zh/skills/creative-content-generation) | 生成 ASCII、手绘图表和视觉设计。 | 文章与社媒配图；**P2**。 |
| 社媒运营 | [社交媒体管理代理技能](https://nanoskill.ai/zh/skills/social-media-management) | 自动发布、内容监控和账户操作。 | 有稳定内容策略与人工审核后再自动化；**P2**。 |
| 社媒发布 | [自动发布到 X（Twitter）代理技能](https://nanoskill.ai/zh/skills/post-to-twitter) | 用真实 Chrome 发布文字、图片、视频和长文。 | X 成为固定获客渠道后；**P2**。最终发布动作应保留人工确认。 |
| 社区营销 | [Reddit 帖子技能](https://nanoskill.ai/zh/skills/reddit-posts-skill-c167) | 生成推动互动且遵守社区规则的 Reddit 帖子。 | 先人工读版规、真实参与后再用；**P2**。不能批量硬广。 |
| 视频 | [视频编辑代理技能](https://nanoskill.ai/zh/skills/video-editing) | 自动剪填充词、调色、烧录字幕并导出 MP4。 | 有自媒体视频生产后；**P2**。 |
| 内容视觉 | [社交卡片智能体技能](https://nanoskill.ai/zh/skills/social-card-generation) | 将内容转为社交卡片，适合小红书轮播和微信封面。 | 长内容复用、中文渠道包装；**P2**。 |

## 外围但不是当前主线的 3 项

| 技能 | 官方详情 / 证据 | 为什么后置 |
|---|---|---|
| Google Ads 分析代理技能 | [详情](https://nanoskill.ai/zh/skills/google-ads-analysis) | 适合已在投放搜索/展示/效果广告后做诊断；当前应先验证自然承接和转化。 |
| YouTube 广告分析代理技能 | [详情](https://nanoskill.ai/zh/skills/youtube-ads-analysis) | 是 YouTube 广告创意、受众与衡量优化，不是自媒体内容生产。 |
| 电商视频营销 | [详情](https://nanoskill.ai/zh/skills/ecommerce-video-marketing) | 偏实物电商转化视频；和当前工具站路径不匹配。 |

## 采用建议：先审，后借，不批量安装

1. 先挑 **1 个**要补的环节，而非安装全部。例如下一轮选方向，可先审“利基市场研究”或“社交媒体监听”。
2. 安装前读其 `SKILL.md`、脚本、依赖、访问范围、是否会发帖/调用付费 API；不要仅凭目录卡片安装。
3. 把外部 skill 当作可借鉴的执行段，保留本库的硬闸门：真实 SERP、真实场景、可验证的行动信号与人工拍板。
4. pSEO、批量博客、自动发帖只在有独立页面价值、人工审核与平台规则检查时启用；它们不是冷启动捷径。
