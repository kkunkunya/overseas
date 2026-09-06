# Apple 多语言 SEO 增量独立验收

- 日期：2026-09-06
- 身份与范围：fresh、独立、只读；仅补验 `languages` 卡、Apple 案例与关联导航。未重开旧版 24 项规格，也未重验已通过的全量 HTML。
- 页面：`http://127.0.0.1:8766/`，来自 `/tmp/seo-skills-study-20260906/preview/`。
- 浏览器：独立 Ego Task Space `211`；已在收尾前关闭。

## 源锁定与预览一致性

开始锁定与结束锁定相同，且下列源文件均与 preview 副本逐字一致：

| 项目 | SHA-256 |
|---|---|
| `overseas-skill-map.html` | `c38ce007d176b2f16621f1556d350bf70441c7fc51b5181c416e7dffccae571c` |
| `Apple-多语言SEO案例-2026-09-06.md` | `d801669f283324a9b5371fd3c65529f7f3006a35f908604989f18c6d9920eeb3` |

逐字匹配的关联文件：HTML、案例、`路线数据.json`、案例证据 README、SEO-GEO 总 README、`3-SEO获客/多源-SEO-GEO全流程方法.md`。

## 验收结果

| 检查项 | 结果 | 证据 |
|---|---|---|
| 搜索 `Apple` 与 `苹果` | pass | 两次都只显示 `languages`，计数为 `1 / 25 项`。 |
| 展开卡片 | pass | 原生 summary 激活后 `details.open=true`；可见 Apple 的 `/ca/iphone-17/`、`/ca/fr/iphone-17/`、`/tw/iphone-17/` 路径。 |
| 当前规划、第二语言执行与适用边界 | pass | 卡片写明现在可先规划语言/网址；第二语言发布前走上线审计；并明确 Apple 是可观察案例、Google 提供规则，二者均不保证排名，未完成页不批量公开。 |
| Apple 案例链接 | pass | 页面链接实际导航到 `/3-SEO获客/SEO-GEO全流程/Apple-多语言SEO案例-2026-09-06.md`。 |
| 桌面 1440 | pass | 1440×1000；展开后的单卡可见；`scrollWidth=1425`、`bodyScrollWidth=1425`，未超过视口。 |
| 手机 390 | pass | 390×844；卡片边界为 x=18..372；`scrollWidth=390`、`bodyScrollWidth=390`，无横向溢出。 |
| 不受影响的数量门槛 | pass | 浏览器 DOM：25 张 `.card`、11 个 `.helper` 入口、6 张 `data-phase=现在准备`。默认计数 `25 / 25 项`。 |
| A1 中文案例与持久证据 | pass | 案例有 2026-09-06 观察日期、1 个地区选择页 + 4 个 iPhone 17 样本、各自直接 Apple 官方 URL、样本边界和未知范围。持久提取包含各页 `lang`、canonical、四个目标 alternate 与切换入口；`iphone17-hreflang-list.txt` 为 137 行，SHA-256 为 `bf876fb3fa3d2476691fe2bbf2c50e8e5f15c81ca94ce2015cf513a3ae5bb4e6`。 |
| Apple 事实与 Google 规则区分 | pass | 案例明确 Apple 为样本实现、Google Search Central 为规则来源；不声称 Apple 代表全站、实际索引、排名或商业效果。 |
| 私有会员页面边界 | pass | 案例明确登录后会员、账号、付款页按访问权限和索引角色处理，不为了多语言 SEO 公开私有页，也不要求其全部进入 `hreflang` 或 sitemap。 |

## 截图

- `languages-card-desktop-1440.png`（1440×1000，SHA-256 `1ddf38ae182ba37686655129e5e8a11848bd3fdc764460881f56cf3aed22dcda`）
- `languages-card-mobile-390.png`（390×844，SHA-256 `1c8d9778636052d4e8da69d0747abc5b9baa6ea4bb255ea50b3aab0353dbea89`）

## needs-work / park / 未测

- needs-work：无。
- park：无。
- 未测：Apple 与 Google 的当前实时响应、Google 实际索引/排名、产品真实使用与收入、mono 方法实现、GitHub 评论/合并/分发事实，以及未受本次变更影响的全量卡片功能。GitHub 私库评论权限未尝试切换身份或绕过。
