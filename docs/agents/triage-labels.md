# Triage Labels

skill 用 **2 个类别角色** + **5 个状态角色**说话。每个 triaged issue 带恰好一个类别 + 一个状态。本文件把这些角色映射到本仓库 GitHub issue tracker 里实际用的标签字符串。

## 类别（category）——每个 issue 恰好一个

| skill 里的角色 | 本 tracker 用的标签 | 含义 |
| --- | --- | --- |
| `bug` | `bug` | 坏了（如 README 链接失效、笔记内容有错） |
| `enhancement` | `enhancement` | 新功能或改进（如补某步笔记、精读某篇原文、加方法论） |

## 状态（state）——每个 issue 恰好一个

| skill 里的角色 | 本 tracker 用的标签 | 含义 |
| --- | --- | --- |
| `needs-triage` | `needs-triage` | 维护者需评估这个 issue |
| `needs-info` | `needs-info` | 等报告者补更多信息 |
| `ready-for-agent` | `ready-for-agent` | executable leaf 已完全 spec 好并通过领域 readiness，可给无人值守（AFK）agent 接 |
| `ready-for-human` | `ready-for-human` | 需人实现 |
| `wontfix` | `wontfix` | 不会做 |

## 状态流转

```
新 issue（无标签）→ needs-triage
                     ├→ needs-info  ──报告者回复──→ 回 needs-triage
                     ├→ ready-for-agent
                     ├→ ready-for-human
                     └→ wontfix
```

maintainer 可随时 override 状态。PR 若开 PR-as-triage-surface 也走同一机器（PR 是"带代码的 issue"）。本仓库 PR-as-triage-surface 设为 **no**。

## 怎么用

当 skill 提到某个角色（如"打 `ready-for-agent` 标签"），用上表对应的实际标签字符串（`gh issue edit <n> --add-label "<标签>"`，命令见 `issue-tracker.md`）。

## 建标签

GitHub 内置 `bug` / `enhancement`。其余 5 个状态标签需在仓库创建（setup-project 已建，或在 GitHub 仓库手动 / 用 gh 建）：

```
gh label create needs-triage --color FBCA04
gh label create needs-info --color FBCA04
gh label create ready-for-agent --color 0E8A16
gh label create ready-for-human --color 1D76DB
gh label create wontfix --color BFD4F2
```