# AGENTS.md

> 本仓库的 agent 配置锚点（Cordex / Codex 读本文件；Claude Code 读同目录 `CLAUDE.md`，两者同步同一块）。提示词本体（命令 / 约定 / 架构地图 / skill 路由）由 `/project-prompt` 补全，与下面的 `## Agent skills` 锚点块零冲突共存。

## Agent skills

### Issue tracker
工作单住 GitHub Issues，用 `gh` CLI 操作。见 `docs/agents/issue-tracker.md`。

### Triage labels
用默认角色名当标签字符串（bug / enhancement / needs-triage / needs-info / ready-for-agent / ready-for-human / wontfix）。见 `docs/agents/triage-labels.md`。

### Domain docs
单 context（single-context）——根目录一个 `CONTEXT.md` + `docs/adr/`，由 domain-modeling 惰性创建。见 `docs/agents/domain.md`。

### Skills domain
暂不声明领域——知识库学习阶段纯靠 global skill。未来建站做产品时回来加。见 `docs/agents/skills-domain.md`。