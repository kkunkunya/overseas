# SERP 与竞品流量爬取法（Chrome + AITDK，实测固化）

> 2026-08-09 第 6 轮踩坑后固化。目标：**块锚定、双源核对、不混厂商**。

## 0. 一句话

```text
SERP 块锚定读 AITDK 注入 → 详情页 traffic.cv 双源核对 → 竞品站逐站读功能/定价
→ 表里每格标来源与性质（域级 vs 页级、精确 vs 线索）
```

## 1. SERP 页读 AITDK 注入指标（Chrome）

AITDK 扩展会在 Google SERP 每个结果块旁注入 `.aitdk-site-metrics-container`（月访问/平均停留/建站日）。

**正确姿势（块锚定）：**

```js
// 以结果块为锚，块内找 h3 + 链接 + metrics；禁止全局抓 a[href]
[...document.querySelectorAll('div[data-hveid]')]
  .filter(d => d.querySelector('h3'))
  .map(b => ({
    title: b.querySelector('h3').innerText.slice(0,60),
    url: b.querySelector('a[href^="http"]')?.href,
    metrics: b.querySelector('.aitdk-site-metrics-container')?.innerText.replace(/\n+/g,' | ')
  }))
```

**踩过的坑（禁止）：**
- ❌ `document.querySelectorAll('a')` 抓链接文本 → 会把 AITDK 注入的「相似站点」/详情链接混进结果，SERP 顺序错乱（第 6 轮把 aseatawaits/usemezze 误当第 1、2 名，实际不在前 8）。
- ❌ 把「域级月访」（canva 869M、reddit 4.17B、apple 143M）当产品页流量。表里要标 `域级`。

**注意：**
- SERP 结果有个性化，同一词两次打开顺序可能不同；以块锚定读到的为准，并注明日期。
- 注入指标是**异步加载**，打开后等 2–5 秒再读；读不到 = `NO-AITDK`，不猜。

## 2. 详情页双源核对（traffic.cv）

AITDK SERP 旁数字跳转详情页：`https://traffic.cv/<domain>`（aitdk.com/traffic/* 会重定向到这）。

**必读字段：** TOTAL VISITS、GLOBAL/COUNTRY RANK、AVG. DURATION、PAGES PER VISIT、BOUNCE RATE、DOMAIN AGE、TRAFFIC SOURCES（Direct/Search 占比）、TOP REGIONS、TOP KEYWORDS（KEYWORD/TRAFFIC/VOLUME/CPC）、WHOIS。

**意义：**
- TOP KEYWORDS 是**金矿**：看它靠什么词拿流量（如 wedding.studio 全是「婚礼照片共享」词 → seating chart 只是引流页，流量来自老业务）。
- TRAFFIC SOURCES：Search >60% = 纯 SEO 站；Direct 高 = 老客/品牌。
- 与 SERP 旁数字不一致时，**以详情页为准**并在表里标注。

## 3. 竞品功能/定价（逐站真页读）

每个前排站开真页读：
- 首页 + 功能页（Features）+ 定价页（Pricing/Plans）
- 记：核心功能清单、免费额度、付费价（$/€/£/月、一次性、积分）、有无账号墙、导出能力
- Reddit/Facebook 帖读「人话凑合方案」（sticky notes、PPT、Sheets）→ 痛点与付费理由
- 404 的定价页链接 = 记下来，不编价

## 4. 记录纪律

| 格子 | 写什么 |
|------|--------|
| 月访问 | `站 + AITDK traffic.cv + 日期`；注明 `域级` 或 `页级` |
| 月搜/KD | 厂商 + 日期；精确/线索/No data（ADR-0007） |
| 功能 | 从真页读的清单；不确定不写 |
| 付费 | 标价 + 货币 + 周期 |

**跨厂商不可横比**：Ahrefs 的 traffic 与 AITDK 口径不同（第 6 轮 wedding.studio：Ahrefs ~6K vs AITDK 65K），同一张表**只用同一来源**，或双列标注。
