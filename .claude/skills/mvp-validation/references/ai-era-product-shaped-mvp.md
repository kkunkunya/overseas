# AI 时代的 product-shaped MVP

> 只在设计卖空气页面的承诺、demo 与“未来功能”时读取。本文件不替代真实用户行动。

## 核心判断

AI 能很快生成单点功能、公式和文案；用户仍会为一个可信的结果、专有上下文、可靠数据、重复工作流和风险更低的决定付费。故 MVP 要证明的不是“能不能生成”，而是：用户是否愿意把一个真实任务交给这个方案。

## 三层表面

| 层 | 作用 | 本轮要求 |
|---|---|---|
| Core outcome | 用户用它完成的最终决定或可发送交付物 | 真实可用，或用 concierge 人工兑现 |
| Adjacent workflow | 同一用户完成同一任务的紧接步骤 | 用 workflow / 样例展示；只有被反复需要才开发 |
| Expansion | 管理、协作、自动化或其他人群的能力 | 标 `Planned`，不作为当前价值证明 |

以“同一人、同一时刻、同一任务的下一步”筛选 adjacent workflow。不能通过这个筛选的功能不进验证页。

## 让承诺可信的最小证据

页面至少选一种：

- 脱敏的真实输入到最终报告/报价/素材；
- 可编辑 demo，能产出关键 verdict；
- concierge 入口，写清用户提交什么、何时收到什么；
- 数据、人工核验或责任边界，解释为什么结果比一次泛 Prompt 更可信。

每个尚未做的能力都标为 `Planned` 或 `Founding-member input`；只有实际能交付的能力可以写 `Available now`。

## 如何解释“为什么不是 ChatGPT”

不用贬低通用 AI。具体说明产品替用户承担了哪一种工作：收集专用输入、选择正确规则/数据、生成可复用的交付物、保存项目上下文、比较方案、或在错误有成本时提供核验边界。若无法写出这一句，先收窄承诺或回到用户访谈。

## 方法来源

- Anthropic, [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)：其团队观察到有效实现常使用简单、可组合的模式，并区分 workflow 与 agent。
- OpenAI, [A practical guide to building agents](https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf)（2025）：从最小架构和合适任务起步，随任务复杂度扩展。

这些资料支持“内部实现可以从小开始”，不证明任何具体细分市场有付费需求；市场判断只能由真实任务、付款或订金验证。
