# AGENTS.md

> Cordex / Codex 读本文件；与 `CLAUDE.md`（Claude Code）同步同一份提示词。

## 项目是什么

出海学习**知识库**（查阅库，不是产品代码库）——把赫兹 227 篇出海文章按 6 步重排，配二手笔记，目标是跑通商业闭环实现躺赚 + 复利。当前阶段：**学习 / 选方向（第 1 步）**，资料可覆盖到最小销售验证；具体产品开发仍另开独立项目文件夹（带 `frontend` 领域），本仓库只作查阅参考。

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

笔记层是二手提炼，原文层是一手素材。术语词典 / 架构决策指向 `CONTEXT.md` / `docs/adr/`（已有 ADR-0001：赫兹主源）。

## 约定与边界

- **方法论以赫兹主源为准（ADR-0001）**——学法/选方向/下一步怎么做，优先 `原文/` 赫兹篇目；目录站视频、YC、小耳朵等为**辅源**，冲突时以赫兹为准。术语见 `CONTEXT.md`「权威与来源」。
- **新内容按 6 步归类**——新文章 / 新笔记判断属 1-6 哪一步再归档，**不**按赫兹原 12 大类。归错步骤 → 查不到 → 知识库失效。
- **每步入口是 `_本步导航.md`**——补笔记先更新本步导航，再放具体笔记文件。
- **原文层保留"编号-标题"原始格式**——`原文/` 227 篇是赫兹原文，**精读某步时才重命名那一步**，不批量改原文。
- **2 / 4 / 5 步暂无笔记**——待探索时补；技术细节先查原文。
- **外部 playbook 先做阶段翻译**——辅源的长期经营建议必须标出适用阶段；没有合资格用户真实行动前，不能把涨粉、自动化、Creator 合作、生态或 holding company 当作当前待办。
- **验证以行动为准**——概念页必须承接一个核心承诺；优先记录合资格用户的真实输入、联系、预约、点击购买、预付或付款，不把点赞和称赞写成需求成立。
- **私聊是许可式研究**——仅在社区规则允许或对方愿意交流时一对一触达；不群发陌生私信、不伪装身份，先记录触达入口、对象资格、消息和行动结果。
- 不要碰：`.DS_Store`（已 gitignore）、`原文/` 批量重命名。

## skill 路由

本仓库是**查阅库**，不走 idea→ship 代码流程。常用：

- `/grilling`——精读某篇原文 / 笔记，逐句追问理解
- `/domain-modeling`——把出海术语（目录站、躺赚、复利、SEO、外链…）谈拢落 `CONTEXT.md`
- `/research`——调研方向 / 竞品 / 赛道
- `/project-prompt`——项目阶段、约定或 Agent 路由发生稳定变化时，刷新 `AGENTS.md` / `CLAUDE.md` 的短地图
- `direction-validator`（项目 skill）——从增长人群与词到方向，Query-first / Community-first 两入口汇合到赫兹 018 闸门；选方向阶段用
- `mvp-validation`（项目 skill）——方向拍板后「卖空气验证」：做一页可丢弃 Landing Page + 真实价格 + Reddit 为主/X 为备的合资格触达，观察真实行动信号才进 MVP；赫兹 015/028/029 主源

不知道下一步怎么走 → 先读 `README.md` + 对应步骤的 `_本步导航.md`。做产品时**另开项目**（带 `frontend` 领域，走 `/project-design-prompt` → `/layout-priority-design` → `/design-recon` → `/to-tickets`），本库只作资料背景。

## 指针

- `CONTEXT.md` / `docs/adr/`——出海术语词典 + 决策记录（ADR-0001 赫兹主源）
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
