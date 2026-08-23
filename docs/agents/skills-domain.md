# Skills domain

本知识库声明 **`overseas-growth`** 方法领域。项目本地实体统一在 `.pi/skills/`，由 `distribute-local-project-skills.py` 投影到 `.agents/skills/`；它们承载方向、搜索、页面策略、分发与增长的可复用判断，不承载具体产品代码。

| 层级 | 项目 skill |
|---|---|
| 路由层 | `ask-overseas` |
| 材料层 | `kb-ingest` |
| 方向层：外部信号还原为客户任务、替代与产品形态 | `direction-validator` |
| 取证层：关键词、竞品、社区、引用与 AI 来源的最小事实 | `treg-research` |
| 选词找方向层：参考站先行，再收核心词与长尾 | `vertical-keyword-loop` |
| 产品首版层：把已取证的承诺做成可用 MVP、页面和站点 | `seo-site-blueprint` |
| 上线质量层 | `seo-readiness-audit` |
| 发现与来源层 | `distribution-link-loop`、`geo-source-loop` |
| 复盘层 | `product-growth-review` |

完整交接图见仓库根目录 [overseas-skill-map.html](../../overseas-skill-map.html)。它是人审用的可视地图；项目 skill 的实际方法仍以 `.pi/skills/` 为准。

做实际网站、App 或服务时另开产品仓库；在那里按技术栈声明 `frontend`、`engineering`、`deploy` 等领域，并实现这里输出的页面 brief、审计问题单和增长实验。知识库不存产品代码或部署配置。
