# SEO Skill 整合迁移方案（讨论稿）

状态：历史讨论稿，已被2026-09-06用户后续决定取代。用户明确要求全流程方法现在沉淀、未来按条件启动，并制作阶段HTML；详见[执行规范](2026-09-06-seo-full-route-spec.md)与[当前路线](../../overseas-skill-map.html)。下文保留早期评议，不再作为当前实施范围；尤其“只试一个切片、遇到场景再写”已不适用。GitHub旧票的待决文字因认证失败尚未更新。

[决策地图](https://github.com/kkunkunya/overseas/issues/1) · [净新增价值](https://github.com/kkunkunya/overseas/issues/2) · [策略与落点](https://github.com/kkunkunya/overseas/issues/3) · [首批验证与回退](https://github.com/kkunkunya/overseas/issues/4)

## 想得到什么

形成能支持出海产品实际工作的最小整合方案：哪些方法值得借鉴、放在哪里、先试什么、如何证明值得保留。当前11个方法入口与9个外部项目都是待比较对象，不以作者、star数或skill数裁决。

## 当前事实

- 9个外部项目有457份 SKILL.md；已全文分组阅读，含20份旧仓迁移指针。另读Agentic的16份实际子流程及必要资料。文件数不等于457种独立能力。
- 本库只保存知识与方法说明；出海方法skill真身在mono；产品工程能力在产品仓。见 [ADR-0017](../adr/0017-overseas-method-skills-live-in-mono.md)。
- 当前11个方法入口已覆盖参考站/选词、需求验证、页面规划、上线审计、GEO来源、分发和增长复盘。正文和已有资产已承担不少外部项目同名能力。
- 原文学习资料临时保存在 `/tmp/seo-skills-study-20260906/`；不将该目录设成skill运行依赖。
- 知识库工作树有既有未提交修改，本轮不清理、不改写这些文件。

## 综合推荐（Astra / Fable / Sol 一轮评议后）

选“在现有入口按净新增价值吸收方法”，同时整理学习笔记。每项必须能解释：现有方法已做到什么、外部具体多了什么、为何值得加载、用哪个任务检验。没有净增价值就只保留来源索引。

| 去向 | 计划内容 | 迁移边界 |
|---|---|---|
| 出海知识库 | 中文方法提炼、来源和固定版本、按适用阶段归档 | 不复制另一套可执行skill真身；不全量提交9个仓库 |
| mono `skills/overseas/` | 确有价值的方法片段、按需reference、必要小模板 | 优先改现有owner；不新增同义路由，不为迁移重写底座 |
| 独立产品仓 | 真正需要的抓取/数据/报表脚本、平台适配与项目状态 | 有具体产品与依赖验证后再迁；不进入知识库或全局启动层 |

## 候选顺序

1. **先试审计证据表达一个切片**：比较Agentic的发现/证据/影响/修复与置信度/未知项，和现有seo-readiness-audit的证据、责任与复查输出。只有后者产物实际缺少有用区分时才迁。原作任意分数、缺schema即critical示例及未证实效果数字不带入。
2. **第二候选是页面brief细节**：新页/改旧页分支、保留有效部分、补充可兑现的独有信息。落seo-site-blueprint的按需资料；不用硬字数、固定关键词位置或机械排除某类搜索结果代替页面任务。
3. **其余先归档并候选化**：已有站的URL迁移映射、营销上下文、基线差异报告、GEO观测资料。是否吸收取决于实际场景；现有本地过强前置条件也应被质疑和复核，不默认其正确。
4. **暂不迁**：Aaron整套registry/多bot契约、另一套Claude/Codex代理调度、自动发文/投放/目录提交、多平台电商Beta模板。它们在有相应产品和持续工作量后可重新评估，不因收集齐就进入当前待办。

## 首批验证与回退的建议

冻结当前版本和一个真实任务输入，对照现有产物与候选产物。检查证据可回溯、未知不冒充事实、下游能指出要改的对象，以及新增资料是否真的减少返工。暂未选择真实站点，也未运行对照。

只有候选切片通过代表场景，才按授权走mono独立候选、检查、人审与分发。若只增加篇幅或重复问题，撤回该切片；不以“新增更多检查”“文档更长”作为成功。

## 三方意见与最终取舍

- [Fable独立原文](seo-integration-reviews-2026-09-06/fable.md)：推荐全量材料保留来源索引，吸收不超过四个方法切片；先抓证据表达，hreflang、引用层次、页面状态快照按场景启用。策略较有把握，具体净价值尚无实测。
- [Sol独立原文](seo-integration-reviews-2026-09-06/sol.md)：同意沿用11个入口，首批倾向于证据合同、技术审计和测量合同；强调本地固定规则同样要接受证据复核。
- Astra：首批进一步收窄为审计证据表达一个切片。统一栏目或检查清单可能有价值，但当前还没有现行产物失败的证据；直接大范围改写依据不足。

**给Kun的推荐：选择性吸收 + 知识归档，先试一个切片。** 后续候选暂定为页面brief、页面状态diff、按需多语言/专项检查。GEO引用层次可作观察用的分类，关于“何者决定推荐”的因果机制不随原文直接采纳。没有真实场景就先归档，运行方法不改。

### 主会话对评议的核对与保留

1. Fable把外部9仓概括为扁平菜单，这个概括过强：Aaron有共享契约与状态协议，部分SEO套件也有编排流程。保留本地入口的理由是任务匹配与维护成本，不是外部没有流程。
2. “目前所有产品都在上线前”没有本轮实时项目证据，不能据此统一排除增长方法；按选定产品的实际阶段激活。
3. Semrush与treg存在表述张力，但CONTEXT第84–85行已写明参考站选词的Semrush特例；通用服务柜台与专门例外未必构成逻辑矛盾。只记为待核对的规则表达，不本轮重开选词政策。
4. 本轮核实 `.codex/skills/mvp-validation` 是断链；现有 `seo-readiness-audit` 为经 `.pi/skills` 指向mono的两跳软链但目标可达。断链是环境发现，双跳本身不是失效证明，均未修复。
5. 原文提到CWV、hreflang等不等于本地已经漏检；按真实页面类型和数据验证后，才判断新增专项是否必要。

## 材料持久保存的建议

本轮已保存计划和三方讨论证据。后续若确认整理资料，建议以一份带作者、固定SHA、用途和阶段的来源总索引进入知识库，按步骤链接相关方法摘要；仅将被选中、需要脱网阅读的原文及其必要许可证/依赖单独保留。不要把457份都变成运行时skill，也不要把整个9仓源码并入本库。完整下载快照是否另放长期资料目录仍待决定，当前/tmp副本未搬迁。

## 待决与权限状态

- 整合目标：增强现有方法 / 只做学习资料 / 整套替换，尚待Kun确认；当前推荐第一种。
- 首批具体对象和成功证据尚未敲定；不把上述候选顺序当实施票。
- Fable与Sol的独立评议已返回并保存，未互读答案。三方共识是选择性吸收；用户尚未确认方向，因此票保持未决。
- 地图和3张子票已创建，原生依赖为：净新增价值→策略；前两者→首批验证。GitHub当前集成身份拒绝updateIssue/addComment，#3/#4正文初始的Blocked by: None未能更正，原生关系为准；也暂时不能把本文指针写回地图。未关闭任何决策票。

## 固定来源

- [zubair-trabzada/geo-seo-claude @ 0a1bb52a](https://github.com/zubair-trabzada/geo-seo-claude/tree/0a1bb52aba7b05e732c686743f4fa23de8121fa1)
- [aaron-he-zhu/seo-geo-claude-skills @ 3a1578a6](https://github.com/aaron-he-zhu/seo-geo-claude-skills/tree/3a1578a63cdde8037ee16d32a3ea9f808eae6bd0)
- [Bhanunamikaze/Agentic-SEO-Skill @ 69199160](https://github.com/Bhanunamikaze/Agentic-SEO-Skill/tree/69199160e18372bc5cdf9ddec20ccb9fb1b509f1)
- [AgriciDaniel/claude-seo @ a1480c7e](https://github.com/AgriciDaniel/claude-seo/tree/a1480c7e590b16001bd9dc1627eacdcd44d580f9)
- [nexscope-ai/eCommerce-Skills @ ee0fb294](https://github.com/nexscope-ai/eCommerce-Skills/tree/ee0fb29433d02ccc22e3e6cea9ab4586d49fd42e)
- [coreyhaines31/marketingskills @ 5b2c0007](https://github.com/coreyhaines31/marketingskills/tree/5b2c0007766c6a1cf1d53fd8fc73e979e0821022)
- [AgriciDaniel/codex-seo @ 97c59bcd](https://github.com/AgriciDaniel/codex-seo/tree/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a)
- [aaron-he-zhu/aaron-marketing-skills @ 888dd38e](https://github.com/aaron-he-zhu/aaron-marketing-skills/tree/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d)
- [TheCraigHewitt/seomachine @ e818d5e3](https://github.com/TheCraigHewitt/seomachine/tree/e818d5e38551a931333381d69c43da6e767ec775)
