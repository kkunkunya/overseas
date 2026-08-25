# ADR-0017: 出海方法 skill 真身在 kun-agent-mono，本库只导入

- status: accepted
- date: 2026-08-25

## 背景

ADR-0003 把**工程性** skill 赶到产品仓库，并写过「知识库不再出现可执行 skill 真身与投影」。后来本库仍需要一套可复用的出海方法 skill（选词、方向验证、页面蓝图、分发、复盘）。它们曾以 `.pi/skills/` 本地实体演进，和 kun-agent-mono `skills/overseas/` 各改一份，路由表分叉：一边已经是参考站先行 / 3+15 锁定，另一边仍把选词当可反复重开的闭环。合入时还发现「上线数周没排名」会被送回选词。

需要单独写清：方法 skill 和工程性 skill 不是同一类落盘。

## 决策

1. **出海方法 skill 真身在 GitHub `kkunkunya/kun-agent-mono` 的 `skills/overseas/`**，一律 `scope: project`。改触发、职责或交接，在 mono 的独立 feature 分支改，合并后再导入本库。
2. **本知识库只声明领域并导入**：`docs/agents/skills-domain.md` 写一行 `overseas`；`import-project-skills.py` 把软链写进 `.pi/skills`、`.agents/skills`、`.claude/skills`、`.grok/skills`。`.pi/skills/<name>` 是指向 mono 集成源的软链，不是第二份真身。
3. **工程性 skill 仍按 ADR-0003** 进独立产品仓库；frontend / engineering / deploy 不在本库声明。
4. **人审流程图**在仓库根目录 `overseas-skill-map.html`；它派生于现行方法 skill，不反向规定方法。

## 理由

- 方法要跨出海项目复用；继续在本库写本地实体，下一次改路由还会和 mono 分叉。
- 工程性 skill 绑具体产品代码，仍然不能进查阅库或 overseas 域。
- 软链导入让 Cursor / Claude / Grok / Pi 能发现同一份方法，而不把 markdown 真身复制进知识库 git。

## 后果

- 在本库改 `.pi/skills/<name>/SKILL.md` 等于改软链目标；应到 mono 改源。
- ADR-0003 关于工程性 skill 与两仓分工的条款仍有效；其「知识库不再出现 `.pi/skills` 投影」只对**工程性** skill 成立，方法 skill 的投影由本 ADR 允许。
- 选词、方向、上线、分发、复盘的现行交接以 mono 里的 `ask-overseas` 等 skill 为准；3+15 锁定后停扩词，上线数周没排名先走索引审计。
