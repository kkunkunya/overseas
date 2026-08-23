# ADR-0002: 选方向标准免费工具含 AITDK

- status: accepted
- date: 2026-07-21

## 背景

选方向需要可重复的免费工具路径。用户要求把 AITDK 纳入标准；赫兹原文也将 AITDK 列为 SEO 必备插件。此前实践清单以 Google/Trends 为主，未强制 AITDK。

## 决策

1. **标准免费三件套**：AITDK + Google SERP（含搜索语法）+ Google Trends。
2. **AITDK 用法**：插件优先用于看站/看页 SEO 与流量粗览；网页端 Keywords Generator 等用于扩词与内容辅助。
3. **主框架仍是赫兹 018**：工具只提供数据与候选，不自动等于「值得做」。
4. **Agent**：能开网页版 AITDK 则必须用；插件若当前 Chrome 会话未安装/不可见，应注明缺口并请用户安装，同时用 SERP/Trends 继续，不阻塞。

## 理由

- 与赫兹工具推荐一致，且免费、适合第 0～3 步早中期。
- 用户明确要求纳入标准，减少每次临时换工具。
- 与「赫兹主源」不冲突：AITDK 是工具层，赫兹是方法层。

## 后果

- 实践清单 / 调研动作默认写上 AITDK 步骤。
- 精确月搜/KD/外链仍可补 🔑，不因有 AITDK 而假装已有 Ahrefs 级精度。
- **量/KD 必取证、参考带不卡死** 由 [ADR-0015](0015-reference-site-first-keywords.md) 继承（原 ADR-0007）：AITDK 扩词 ≠ 量化通过。
