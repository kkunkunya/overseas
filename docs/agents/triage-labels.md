# Triage Labels

新流程只使用两个状态标签；它们表示是否已经能安全委派，不表达类型、复杂度、模型或固定执行路径。本仓库里已有的 `bug`、`enhancement`、`needs-triage`、`needs-info`、`wontfix` 等标签可保留作历史/搜索用途，但 skill 不再生成、检查或依赖它们。

| 角色 | 实际标签 | 含义 |
| --- | --- | --- |
| `ready-for-agent` | `ready-for-agent` | issue 有目标、可观察验收、相关上下文且无已知 blocker，Agent 可自行选择交付方式 |
| `ready-for-human` | `ready-for-human` | 需要产品决定、外部授权、登录/权限、不可覆盖事实或其他人类动作 |

使用 `gh issue edit <n> --add-label "<标签>"` 添加，恢复委派时去掉 `ready-for-human`。不维护强制状态机。
