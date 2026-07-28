# ADR-0003: 知识库与产品项目仓库分工

- status: accepted
- date: 2026-07-28

## 背景

Kun 有两个相关仓库：

- `~/learn/overseas/`——出海**知识库**：赫兹 227 篇原文 + 二手笔记 + 方法论，纯 markdown，无代码，目标是查阅与学习。
- `~/oversea-project/<产品名>/`——**产品项目仓库**（当前 `amigurumi-pricing-calculator`）：承载具体产品的建站、埋点、读数判定等执行代码与工程性 skill。

第一批从方法论落地出的工程性 skill（`validation-instrument`：建站时埋验证埋点、到期读数判定 build/maintain/abandon）即将创建。若 skill 真身写进知识库，知识库会混进与具体产品绑定的执行代码，且 skill 随产品迭代会频繁改动，污染查阅库的稳定性；若全部留在产品仓库，又会丢失方法论依据，执行 agent 不知为何这么做。

需要一条明确的分工边界，避免后续每个工程性 skill 都重新纠结放哪。

## 决策

1. **知识库 `overseas/` 存「为什么 + 方法论」**：赫兹原文、二手笔记（如 `2-建站开发/上线即量化-...md`）、领域术语（`CONTEXT.md`）、决策记录（`docs/adr/`）、skill 创建指示（`docs/agents/skill-spec-*.md`）。纯 markdown，不存可执行 skill 真身。

2. **产品项目仓库存「怎么执行」**：工程性 skill 真身放 `<产品>/.pi/skills/<name>/`，由该项目的 `sync-project-skills` 分发到 `.agents/skills/` 投影。运行时只认产品仓库内的 skill 路径。

3. **创建指示可在知识库暂存**：跨产品的通用方法论衍生的 skill 创建指示（`docs/agents/skill-spec-*.md`）留在知识库，作为「为什么这么做 + 规格单」；执行 agent 据此到产品项目仓库创建真身。指示文档本身是 markdown，不是运行时依赖。

4. **知识类原则笔记不进产品仓库**：原则、方法论、原文摘要只归知识库对应步骤目录，产品仓库不重复存，避免双份维护与漂移。

## 理由

- 知识库使命是「查阅 + 学习」，稳定性优先；工程性 skill 随产品迭代频繁改动，混入会破坏查阅体验。
- 工程性 skill 与具体产品绑定（埋点接哪个分析后台、读哪个项目的代码），天然属于产品仓库；硬塞进知识库会让 skill 不可移植。
- 创建指示是方法论与执行之间的桥，留在知识库保证「为什么」可追溯，执行 agent 拿规格单去产品仓库落地，职责清晰。
- 两仓分工后，知识库可长期作为所有出海产品的共享方法论底座，产品仓库各自演进互不干扰。

## 后果

- 新建工程性 skill 时先问「这是工程性还是知识类」：工程性 → 产品仓库 `.pi/skills/`；知识类 → 知识库对应步骤目录。
- 知识库不再出现可执行 skill 真身与 `.pi/skills/` / `.agents/skills/` 投影目录。
- `validation-instrument` 的创建指示 `docs/agents/skill-spec-validation-instrument.md` 留本库，真身落 `oversea-project/amigurumi-pricing-calculator/.pi/skills/validation-instrument/`。
- 若某 skill 既是通用方法论又跨多产品复用，评估是否升级为 global skill（`scope: global`，进 `~/.agents/skills/`），不在两个产品仓库各放一份。