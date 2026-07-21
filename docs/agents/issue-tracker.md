# Issue tracker：GitHub

本知识库用 **GitHub issues** 做 issue tracker。所有操作用 `gh` CLI。本文档告诉其他 skill（如 `code-review` 的 Spec 轴、`triage`、`wayfinder`）怎么读写这张 issue tracker——它是这些 skill 与具体 issue tracker 之间的**适配层**：skill 只说抽象术语（"fetch the relevant ticket"），本文档翻译成具体 `gh` 命令。

仓库归属从 `git remote -v` 推断——`gh` 在 clone 内运行时自动识别，零配置。

> **本项目说明**：当前知识库主要用 issue 记录**学习任务**（整理某步笔记、精读某篇原文、补方法论、修 README 失效链接）。下方 PR / sub-issue / wayfinder 段是适配层，供未来做产品引入代码工程 skill（`code-review` / `to-tickets` / `wayfinder`）时用，现阶段可忽略。

## Issue 操作

- **建 issue**：`gh issue create --title "..." --body "..."`。多行 body 用 heredoc。
- **读 issue**（含评论与标签）：`gh issue view <number> --comments`，需要结构化时加 `--json number,title,body,labels,comments --jq '...'`。
- **列 issue**：`gh issue list --state open --json number,title,body,labels,comments --jq '[.[] | {number, title, body, labels: [.labels[].name], comments: [.comments[].body]}]'`，按需加 `--label` / `--state` 过滤。
- **评论**：`gh issue comment <number> --body "..."`
- **加 / 去标签**：`gh issue edit <number> --add-label "..."` / `--remove-label "..."`
- **关闭**：`gh issue close <number> --comment "..."`

## Pull request 操作

- **读 PR**（含评论）：`gh pr view <number> --comments`
- **读 PR diff**：`gh pr diff <number>`
- **列 PR**：`gh pr list --state open --json number,title,body,labels,headRefName,baseRefName,author,authorAssociation,comments`
- **评论 / 标签 / 关闭**：`gh pr comment`、`gh pr edit --add-label` / `--remove-label`、`gh pr close`

GitHub 的 issue 和 PR **共享编号空间**，裸 `#42` 可能是任意一种——用 `gh pr view 42` 和 `gh issue view 42` 各试一次来分辨。

## PR 作为 triage surface

**PR 作为请求入口：no。**

> `no` = owner 自行开发，外部 PR 不作为 feature request。`yes` = 接受外部 PR 作为需求入口，`/triage` 读这个标志。

设为 `yes` 时，PR 走和 issue 同样的标签与状态机，用 `gh pr` 等价命令；列外部 PR 时只保留 `authorAssociation` 为 `CONTRIBUTOR` / `FIRST_TIME_CONTRIBUTOR` / `NONE` 的（丢掉 `OWNER` / `MEMBER` / `COLLABORATOR`）。

## Sub-issue 与依赖（blocking）关系

`to-tickets` 把一份 spec 拆成子 issue 时，要把每片链到 parent 作 **sub-issue**、把依赖接成 **blocking edge**。先用 `gh issue create --help` 与 `gh issue edit --help` 确认当前 host/CLI 暴露 `--parent`、`--blocked-by`、`--add-sub-issue`、`--add-blocked-by`；支持时用原生关系：

- **建 issue 时直接挂关系**：
  - `gh issue create --title "..." --body "..." --parent <PARENT-N>`——作为 PARENT-N 的 sub-issue
  - `--blocked-by <N1,N2>`——标记被这些 issue 阻塞
  - `--blocking <N>`——标记本 issue 阻塞 N
- **给已有 issue 接关系**：
  - `gh issue edit <n> --add-sub-issue <child>` / `--remove-sub-issue <child>`
  - `gh issue edit <n> --set-parent <PARENT-N>` / `--remove-parent`
  - `gh issue edit <n> --add-blocked-by <blocker>` / `--remove-blocked-by <blocker>`
  - `gh issue edit <n> --add-blocking <N>` / `--remove-blocking <N>`
- 编号支持跨仓库 URL；`gh issue view <n>` 会显示 parent / sub-issues（带完成进度）/ blocked-by / blocking。

**当前 host 或 CLI 不支持原生关系，或原生命令返回 unsupported / 404 时**，用 issue body 的 `## Parent` 和 `## Blocked by` 段兜底（写 issue 编号引用），`to-tickets` 已规定这个 fallback。

## Wayfinding operations

`/wayfinder` 只说抽象操作；本 adapter 优先使用 GitHub 原生 sub-issue、dependency 与 assignee。先确保 `wayfinder:map` 与 `wayfinder:research|prototype|grilling|task` labels 存在；缺少时用 `gh label create <name> --color <hex>` 创建。

- **Map**：`gh issue create --title "<map name>" --body-file <file> --label wayfinder:map`。
- **Child**：`gh issue create --title "<ticket name>" --body-file <file> --label wayfinder:<type> --parent <MAP>`。
- **Blocking**：所有 child 建完后第二遍运行 `gh issue edit <CHILD> --add-blocked-by <BLOCKER>`；多 blocker 传逗号分隔编号。
- **Frontier**：`MAP=<number>; gh issue list --state open --limit 100 --json number,title,url,parent,assignees,blockedBy --jq "[.[] | select(.parent.number == $MAP and (.assignees | length) == 0 and .blockedBy.totalCount == 0)] | sort_by(.number)"`。结果第一张是默认 frontier ticket。
- **Claim**：任何调查或对话前先运行 `gh issue edit <n> --add-assignee @me`；assignee 就是 claim。
- **Resolve**：先 `gh issue comment <n> --body-file <answer-file>`，再 `gh issue close <n>`；随后读取 map body、向 `Decisions so far` 追加一行 gist + ticket link，并用 `gh issue edit <MAP> --body-file <map-file>` 写回。

若 preflight 不支持原生关系：map body 用 task list 链 child；child body 顶部用 `## Parent` + `Part of #<MAP>` 和 `## Blocked by`。Frontier 按 task-list 顺序读取仍 open 的 child，逐张用 `gh issue view <n> --json state,assignees,body` 排除已 claim 或存在 open blocker 的票。Claim 与 Resolve 仍用 assignee / comment / close；map pointer 写回不变。

map 是索引：resolution detail 只住 child 的 comment，map 只保留 gist + link。

## skill 术语映射

- **"publish to the issue tracker"** → 建一个 GitHub issue：`gh issue create`。
- **"fetch the relevant ticket"** → `gh issue view <number> --comments`。
- **"link as a native sub-issue" / "wire a native blocking edge"**（`to-tickets`）→ `gh issue create --parent` / `--blocked-by`，或 `gh issue edit --add-sub-issue` / `--add-blocked-by`；不支持就用 body 的 `## Parent` / `## Blocked by` 段兜底。见上"Sub-issue 与依赖关系"段。
- **"map / child / blocking / frontier / claim / resolve"**（`wayfinder`）→ 见上 `Wayfinding operations`；原生关系不可用时使用 task-list/body fallback。
- **"the spec for this change"**（`code-review` 的 Spec 轴）→ 从 commit / PR 的 issue 引用（`Closes #<n>` / `Part of #<n>` / `Refs #<n>`）找到驱动 issue，读其正文与评论作为 spec。**只到 issue 这一层**——不要回溯 issue 之前的 discussion / 对话记录，那是未收敛的噪声。都没找到就问用户 spec 在哪；用户说没有，Spec 轴报 "no spec available"。