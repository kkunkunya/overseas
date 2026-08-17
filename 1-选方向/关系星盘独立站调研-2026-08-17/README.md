# 关系星盘独立站调研（2026-08-17）

> 主题：英语市场的 `synastry` / relationship astrology 独立站。关注用户怎样生成、理解与探索两人的关系图；不做关系去留、伴侣意图、命运或准确性判决。
>
> 当前处置：**条件性 GO，列入首批 3–4 个独立站组合候选。**不押注免费 calculator 主词；在独立产品仓库做可用 MVP，以 8–12 周观察窗决定加码、收窄或归档。见 [ADR-0013](../../docs/adr/0013-bounded-parallel-site-portfolio.md) 与 [ADR-0014](../../docs/adr/0014-product-first-observation-window.md)。

## 读法

| 文件 | 回答的问题 |
| --- | --- |
| [市场与产品判断.md](市场与产品判断.md) | 用户困惑、搜索入口、收费先例、产品边界与早期候选价值是什么？ |
| [竞品足迹与引用样本.md](竞品足迹与引用样本.md) | Astro-Seek、AstroLibrary、Michele Knight 的具体免费入口、升级路径、排名词与引用样本是什么？ |
| [竞品产品地图.md](竞品产品地图.md) | Astro-Charts、Cafe Astrology、Astrotheme、Prokerala 如何承接工具、报告、内容和回访？ |
| [关键词与相邻赛道复核.md](关键词与相邻赛道复核.md) | 关系星盘、BaZi、塔罗、日运势的关键词、SERP 和竞品对比后，哪些可保留、哪些排除？ |

## 已对齐的产品方向

```text
用户从搜索 / 分享 / 社区进入
→ 首页选择一个关系探索问题或完整地图
→ 分步交出双方必要出生资料（未知出生时间可继续）
→ 生成可视化 Synastry Relationship Map
→ 从用户语言的关系主题进入图表依据
→ Agent 只在当前图 + 当前主题的上下文中解释
→ 保存、分享、回访；后续再观察升级和付费时刻
```

对外暂定表达：

> **Turn your synastry chart into a relationship map you can actually explore.**
>
> **See the patterns between you — not a verdict on your relationship.**

完整产品交接在 OS 临时文件，不进知识库：

```text
/var/folders/kp/chf3dwc13pq4pyqxkw9_qgn00000gn/T/
overseas-relationship-map-product-handoff-2026-08-17.md
```

## 当前边界

- 不能把 `synastry chart calculator` / `free synastry report` 当作可直接硬刚的 SEO 首发承诺；它们是成熟免费供给与入口背景。
- 产品差异在“图表 → 用户能理解的互动主题 → 图表绑定的探索”，不在更多相位、兼容度打分、长 PDF 或泛聊天框。
- 不使用焦虑、倒计时或确定性预测促成留存/付费；高风险关系情境中止占星解释。
- 产品代码、计算库/API、数据模型、UI 和部署均在独立产品仓库处理；本目录只保存方向与市场研究。
