# AGENTS.md

> Cordex / Codex 读本文件；与 `CLAUDE.md`（Claude Code）同步同一份提示词。

## 项目是什么

出海学习**知识库**（查阅库，不是产品代码库）——把赫兹 227 篇出海文章按 6 步重排，配二手笔记，目标是跑通商业闭环实现躺赚 + 复利。当前阶段：**学习 / 选方向（第 1 步）**，没开始动手做产品。**做产品另开独立项目文件夹**（带 `frontend` 领域），本仓库只作查阅参考。

技术栈：纯 markdown，无代码。版本管理 git + GitHub（`kkunkunya/overseas`）。

## 命令

无 build / test / run（纯知识库）。常用：

- `git add -A && git commit -m "..." && git push`——整理后提交
- `gh issue create --title "..." --body "..."`——登记学习任务（补哪步笔记、精读哪篇原文）
- `gh issue list --state open`——看待办

无特殊 flag / env。

## 架构地图

```
overseas/
├─ README.md          ← 总导航（6 步 + 两份实战共识 + 怎么用）
├─ 1-选方向/ … 6-复盘增长/   ← 笔记层：每步入口 _本步导航.md
└─ 原文/              ← 原文层：赫兹 227 篇按 6 步重排
   ├─ README.md       ← 227 篇一句话索引
   └─ 0-工具与资源/ 1-选方向/ … 6-复盘增长/
```

笔记层是二手提炼，原文层是一手素材。术语词典 / 架构决策指向 `CONTEXT.md` / `docs/adr/`（domain-modeling 惰性建，当前不存在）。

## 约定与边界

- **新内容按 6 步归类**——新文章 / 新笔记判断属 1-6 哪一步再归档，**不**按赫兹原 12 大类。归错步骤 → 查不到 → 知识库失效。
- **每步入口是 `_本步导航.md`**——补笔记先更新本步导航，再放具体笔记文件。
- **原文层保留"编号-标题"原始格式**——`原文/` 227 篇是赫兹原文，**精读某步时才重命名那一步**，不批量改原文。
- **2 / 4 / 5 步暂无笔记**——待探索时补；技术细节先查原文。
- 不要碰：`.DS_Store`（已 gitignore）、`原文/` 批量重命名。

## skill 路由

本仓库是**查阅库**，不走 idea→ship 代码流程。常用：

- `/grilling`——精读某篇原文 / 笔记，逐句追问理解
- `/domain-modeling`——把出海术语（目录站、躺赚、复利、SEO、外链…）谈拢落 `CONTEXT.md`
- `/research`——调研方向 / 竞品 / 赛道

不知道下一步怎么走 → 先读 `README.md` + 对应步骤的 `_本步导航.md`。做产品时**另开项目**（带 `frontend` 领域，走 `/project-design-prompt` → `/layout-priority-design` → `/design-recon` → `/to-tickets`），本库只作资料背景。

## 指针

- `CONTEXT.md` / `docs/adr/`——出海术语词典 + 决策记录（domain-modeling 惰性建，当前无）
- `docs/agents/`——issue tracker / triage / domain / 领域声明（setup-project 产出）
- `## Agent skills` 块（下方）——归 setup-project

## Agent skills

### Issue tracker
工作单住 GitHub Issues，用 `gh` CLI 操作。见 `docs/agents/issue-tracker.md`。

### Triage labels
用默认角色名当标签字符串（bug / enhancement / needs-triage / needs-info / ready-for-agent / ready-for-human / wontfix）。见 `docs/agents/triage-labels.md`。

### Domain docs
单 context（single-context）——根目录一个 `CONTEXT.md` + `docs/adr/`，由 domain-modeling 惰性创建。见 `docs/agents/domain.md`。

### Skills domain
暂不声明领域——知识库学习阶段纯靠 global skill。未来建站做产品时回来加。见 `docs/agents/skills-domain.md`。