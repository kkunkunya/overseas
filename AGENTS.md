# 出海学习知识库

## 项目职责

本库 `kkunkunya/overseas` 保存多源出海学习材料、六步笔记与自包含 HTML 路线图，不承载产品代码或真实工具接入。赫兹227篇只是其中一批，没有单一作者是裁决权威；默认路径为垂直细分、长期稳定增长（ADR-0005），以用户实测校正材料。

## 归属与入口

- 查资料从 `README.md` 和对应步骤 `_本步导航.md` 进入；新笔记归入1–6步并更新本步导航，保留作者、出处和适用阶段。
- 全流程看 `overseas-skill-map.html`，路线数据与来源索引在 `3-SEO获客/SEO-GEO全流程/`。地图说明启动条件，不是产品实时状态或效果证明。
- 可复用方法真身在 kun-agent-mono `skills/overseas/`；本库 `.agents/skills/` 仅为导入投影，不能沿软链直接修改 live 源。方法在 mono 独立工作面改、验收合并后导入，见 ADR-0017。
- 工具安装与接入、抓取/性能/快照、埋点、修复复测、发布及运行证据均归具体产品仓；产品执行票也在产品仓跟踪。本库只保留通用方法和交棒链接，见 `docs/agents/issue-tracker.md`。
- 不知道出海下一步时用 `ask-overseas`；精确触发、准备态、证据要求与交接以当前正式 Skill 为准，不在本提示词复制另一套路由表。正文制作归 `seo-site-blueprint` 的交付或具名交接。

## 方法边界

- 3+15锁定后不泛扩词；Semrush取证和正式商业词池遵循 ADR-0016。支持内容选题不等于重开立项。
- 短期无排名先诊断，不单独据此放弃；已有判断遇合格决定性反证可按正式方法有限重评，不要求补齐历史词表，也不自动删除资产。
- GEO问题/来源基线及渠道素材可提前准备；真实观察、账号连接和对外执行按各自条件核实，不把准备完成当作已执行。
- 结果优先看真实任务完成、回访、购买或付款；点赞和称赞不算需求成立。材料中的窗口与阈值不是效果保证。
- 热词抢占不做；旧TTS、激光清洗、专业服务候选已reject（ADR-0006），不据历史笔记续研。
- 私聊是许可式研究，不群发陌生私信、不伪装身份；原文层不批量改名，不处理 `.DS_Store`。

## 验证与提交

无应用构建或测试套件。Markdown检查链接和引用；HTML改动需检查实际搜索、筛选、跳转及受影响布局，静态检查不替代实页验证。

- `git diff --check` 检查本次修改；仅暂存本任务文件，保留其他未提交笔记。
- `gh issue list --repo kkunkunya/overseas --state open` 查看知识任务；跨仓操作显式指定仓库。

术语与决策见 `CONTEXT.md`、`docs/adr/`；运行与跟踪适配见 `docs/agents/`。不在本库复制产品配置或秘密。

## Agent skills

### Issue tracker
工作单住 GitHub Issues，用 `gh` CLI 操作。见 `docs/agents/issue-tracker.md`。

### Triage labels
使用 `ready-for-agent` / `ready-for-human`；仓库里已有的 bug / enhancement / needs-* / wontfix 可保留检索。见 `docs/agents/triage-labels.md`。

### Domain docs
单 context（single-context）——根目录一个 `CONTEXT.md` + `docs/adr/`，由 domain-modeling 惰性创建。见 `docs/agents/domain.md`。

### Skills domain
本库声明 `overseas` 方法领域；真身在 kun-agent-mono `skills/overseas/`，本库只导入软链。见 `docs/agents/skills-domain.md` 与 ADR-0017。
