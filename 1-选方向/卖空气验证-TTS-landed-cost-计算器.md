# 卖空气验证 · TikTok Shop landed cost / 关税 / 利润计算器

> 2026-07-29。方向候选已过 direction-validator 闸门（tentative go），进入 mvp-validation。
> 主源：赫兹 015/028/029；前置证据见 `方向验证-第4轮-TikTokShop-预查.md`

## 0. 前置闸门确认

- 人群 × 场景 × 重复任务：从中国进货的 TikTok Shop 卖家 × 选品/定价 × 算真实单品边际（HS 关税 + TTS 抽佣 + 运费）
- 缺口命题：现有工具要么只算 TTS 费（不算关税），要么只算关税（generic Amazon 工具，不结合 TTS 费率）；无「HS 关税 + TTS 抽佣 + 运费 → 单品真实利润」一次算清的 TTS 专用工具
- 两类独立证据：① r/TikTokShop 帖层痛点 + 海关经纪 tariff update 帖 ② SERP 工具市场预查（无 dedicated incumbent）
- 触达入口：r/TikTokShop（33.9k，活跃）+ TikTok 卖家 FB 群/Discord
- 用户拍板 go to validation ✅（2026-07-29）

## 1. 验证合同（待用户确认定价/预算后定稿）

- 本轮截止：7–14 天，到期必决 build / revise / reject
- 现金预算：待定（域名+托管 ~$10–20；广告预算待定）
- 合资格访问上限：50–100 个目标卖家
- 成功行动：≥3 卖家提交真实 SKU 参数 + ≥1 点击购买/预付
- 停止条件：曝光够但无人输入 → 归因承接/价格/痛点
- 到期决定：build 最小可用 MVP / revise 承接或切口 / reject

## 2. 痛点等级与核心承诺

- 痛点等级：**赚钱型**（避免选到关税吃掉利润的亏本选品；选错直接亏钱）→ 付费意愿强
- 核心承诺（3 秒理解）：
  > For TikTok Shop sellers importing from China who are picking products after the de minimis exemption ended, **TTS Margin** shows true per-unit profit after US tariff + TikTok Shop commission + shipping from a product's HS code and cost, so they avoid picking losers where tariffs eat the margin.

## 3. 概念页最小结构（待做）

1. 痛点一句话 + 3 卖点（用 r/TikTokShop 卖家原话）
2. 示例输入与结果卡：HS code + 产品成本 + 售价 + 重量 → 真实单品利润 + "是否值得做"
3. 免费即时算 + 一个 Pro 报价（价格待测）
4. 主 CTA 购买/预订 + 次 CTA 提交真实 SKU/留邮箱
5. 信任边界 + 退款/隐私雏形 + 联系方式
6. 埋点：到达 → 开始输入 → 完成 → 看结果 → 点购买 → checkout → 付款

## 4. 待用户拍板

- 定价（Pro 报价）：待测假设，skill 提醒不能太低
- 触达渠道顺序：r/TikTokShop / TikTok 卖家 FB 群 / Discord
- 现金预算 + 对外触达动作授权