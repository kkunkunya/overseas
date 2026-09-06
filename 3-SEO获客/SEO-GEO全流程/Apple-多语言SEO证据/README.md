# Apple 多语言 SEO 抓取证据

- 抓取日期：2026-09-06（响应头时间为 UTC）
- 方法：`curl -L --compressed` 获取官方公开页面的初始 HTML 与响应头，再用 `rg` 提取字段。
- 范围：Apple 地区选择页 1 个；iPhone 17 的美国、台湾、加拿大英语、加拿大法语页面各 1 个；Google Search Central 指南 3 页。
- 限制：这是 5 个 Apple 页面的一次公开抓取，不代表 Apple 全站、历史版本、Google 实际索引或排名结果。

## Apple 页面观察值

| 样本 | HTTP | HTML lang | canonical | hreflang 数 | x-default 数 |
|---|---:|---|---|---:|---:|
| `https://www.apple.com/choose-country-region/` | 200 | `en-US` | 自指 | 0 | 0 |
| `https://www.apple.com/iphone-17/` | 200 | `en-US` | 自指 | 137 | 0 |
| `https://www.apple.com/tw/iphone-17/` | 200 | `zh-TW` | 自指 | 137 | 0 |
| `https://www.apple.com/ca/iphone-17/` | 200 | `en-CA` | 自指 | 137 | 0 |
| `https://www.apple.com/ca/fr/iphone-17/` | 200 | `fr-CA` | 自指 | 137 | 0 |

四个产品页的 137 条 `hreflang` 提取结果 SHA-256 都是：

`bf876fb3fa3d2476691fe2bbf2c50e8e5f15c81ca94ce2015cf513a3ae5bb4e6`

这只证明本次四个样本返回了相同 alternate 集合。`iphone17-hreflang-list.txt` 保留一份完整提取结果。

## 文件说明

- 公开请求的响应头仍保留在原临时工作目录，未复制到知识库；本目录只持久保存核对所需字段与哈希。
- `apple-head-and-switch-extract.txt`：HTML `lang`、title、description、canonical、四个目标 alternate 与页脚切换入口。
- `iphone17-hreflang-list.txt`：一份产品页完整 `hreflang` 集合。
- `sha256.txt`：抓取时原始 HTML 与响应头哈希；原始整页 HTML 在提取后删除，以保持证据最小。
