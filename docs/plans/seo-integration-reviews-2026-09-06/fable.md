# fable 独立评议原文

日期：2026-09-06。以下为独立席位意见，不代表已采纳或实测结论；主会话核对与取舍见上一层整合迁移方案。

**评议结论（Fable 席位，独立意见）**

**1. 推荐**：选 B 的收窄版，我叫它「归档全量 + 吸收 ≤4 个方法切片 + 脚本类审计工具按 ADR-0003 走产品仓」。不新增 skill，不替换体系，不并存安装到本库或 mono。9 仓快照以一篇带 SHA 的材料笔记进 `3-SEO获客/`（kb-ingest 路线），方法切片只作为现有 skill 的 references/assets 段落进 mono。

**2. 决定性理由与证据**
- 现有 11 个入口是一条**有先后门槛的路由链**（每个 SKILL.md 都有「先接上一环」和「退出与交棒」），外部 9 仓全是**按名词分工的扁平菜单**（claude-seo 33 个、aaron 120 个、Nexscope 162 个）。C 会丢掉 3+15 锁定、观察窗不归档这两条本库刚在 8 月 25 日花力气锁死的裁决（mono 提交 b34f5ed，ADR-0017 背景段）。
- 外部体系的价值集中在**证据表达契约**，不在流程：Agentic 的 Confirmed / Likely / Hypothesis 与 environment limitation（SKILL.md 第 97、160 行）；aaron 的 Measured / User-provided / Estimated（performance-monitor 第 110 行）。这些是段落级可移植物，不需要装整仓。
- 已有借鉴基线不为零：赫兹 038 原文已推荐 coreyhaines31/marketingskills；mono 8 月 19 日已加「quality directory route」。所以 directory-submissions 一类净新增很低。
- 维护成本已经在漏：`.agents/skills` 十个软链先指 `.pi/skills` 再指 mono（两跳），`.codex/skills/mvp-validation` 指向不存在的 `/Users/kun/learn/...`。11 个入口就已漂移，D 方案装几百个只会放大。
- claude-seo / codex-seo / Agentic 带 89 个脚本、SQLite、provider 扩展，本质是**工程性能力**。ADR-0017 第 3 条已规定这类进独立产品仓，这就是 D 的唯一合理落点，而不是知识库。

**3. 最强替代及适用条件**：A（只归档）。若未来 3 个月没有任何站点走到「上线审计」或「第二语言版本」环节，下面的切片没有真实场景可验证，那时 A 与 B 等价，B 只多了维护面。

**4. 假设与未知**
- 假设三组笔记对外部文件的描述准确；我只抽查了 6 份原文。
- 未知：任何外部方法在 Kun 的站上是否改变决策。Corey 的「引用 vs 推荐」阶梯依据一份 2026 年春的单一研究（Lily Ray），是作者主张。
- 现有本地规则本身也有未验证处：`product-growth-review` 的 8–12 周观察窗与外部各家评分同属启发式；`vertical-keyword-loop` 写「不改用 treg 顶上」，而 `CONTEXT.md` 第 258 行把 treg 定为「默认研究服务柜台」，两处互相矛盾，这不该由本次整合顺手裁掉，但应记票。

**5. 会改变结论的新证据**
- 若一次真实上线审计显示，本地 `seo-readiness-audit` 漏掉的项（hreflang、CWV）确实阻塞了收录，说明应吸收整段 checklist 而非一条。
- 若产品仓里实际跑 Agentic 脚本产出的证据被采用为决策依据，那么 D 在产品仓的范围应扩大。
- 若 Kun 明确改路径为程序化多页或比较页，aaron/claude-seo 的 thin-page 守门会从「延后」升为「首批」。

**6. 置信度**：策略层 0.7；具体映射的净价值 0.4，因为没有一条经过实测。

**候选映射（外部方法 → 落点 → 净新增 → 首批验证）**
1. Agentic 的 Confirmed/Likely/Hypothesis 与「环境限制不算站点问题」→ `seo-readiness-audit` 输出块新增每条置信标签 → 本地只有整段「证据边界」→ 对一张真实页面做审计，看标签是否改变修复顺序。
2. Corey `seo-audit/references/international-seo.md`（hreflang 互指、x-default、canonical 压过 hreflang、分语言 sitemap）→ `seo-readiness-audit` 加检查项、`seo-site-blueprint` 的「语言版本」角色 → 本地完全没有 hreflang，虽 `CONTEXT.md` 已有「多语言 SEO」术语 → 延后到第一个第二语言版本上线时验证。
3. Corey `ai-seo/references/citations-vs-recommendations.md`（Retrieved / Cited / Mentioned / Recommended 四阶、自评榜单帮竞品）→ `geo-source-loop` 第 3 步与 `distribution-link-loop` 的来源判断 → 本地把 AI 提及只当观察，缺「推荐由站外共识决定」这一层 → 对一个目标问题记录当前到达哪一阶，看是否改变分发优先级。
4. codex-seo `seo-drift` 的「上线快照 + 后续 diff」思路（不引 SQLite 工具）→ `product-growth-review` 第 1 步基线 → 本地基线只有指标，无页面状态快照，分不清自伤回归与需求下降 → 一个站上线时留快照，观察窗内一次下跌能否被 diff 解释。
5. aaron `page-play-builder` 守门（thin/duplicate、site-reputation-abuse、比较页断言 `[needs source]`）+ claude-seo `seo-programmatic` 的 QA gate → `seo-site-blueprint` 的「稍后验证」栏作 reference → 中等 → **延后**，直到某站真要做程序化或比较页。
6. seomachine 的 CRO / 邮件 / 投放、aaron 的 8 个 protocol registry 与评分框架、Nexscope 电商模板、geo-proposal/prospect 等代理商销售流程 → **只归档不吸收**：面向有流量后的阶段或团队治理，与当前单人、上线前路径不匹配。

**决策票建议（≤3）**
- 票 A：脚本类审计仓（Agentic、claude-seo/codex-seo）是否按 ADR-0003 作为工程 skill 装进产品仓试用，边界与 mono 方法层如何分工。
- 票 B：`vertical-keyword-loop` 的「只认 Semrush、不用 treg」与 `CONTEXT.md` treg 柜台条目的冲突由谁裁，这决定 aaron/claude-seo 那些以 API 数据为前提的选词方法能否有落点。
- 票 C：/tmp 快照的持久形态：仅一篇带 SHA 的材料笔记，还是 vendored 到某处；同时修复 `.agents`/`.codex` 软链漂移的归属。
