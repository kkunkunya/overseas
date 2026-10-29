# E-E-A-T 框架：SEO / GEO 的根

开工画骨架、完工体检、给人讲这一轮改了什么，三处都从这份开始。它回答一件事：**凭什么信这个站**。抓取规则在[引擎规范手册](engine-playbook.md)，正文写法在 [GEO 写作规则](geo-writing-rules.md)，本文件不重复它们，只说它们各自补的是哪一维信任。

## 1. 四个维度，Trust 在中心

E-E-A-T 出自 Google 质量评估员手册（Search Quality Rater Guidelines），2022-12 在 E-A-T 前加了 Experience。

| 维度 | 它问的是 | 站上的典型信号 |
|---|---|---|
| **Experience** 亲身经验 | 做内容的人真的用过、做过吗？ | 完整的示范结果、真实截图、自有使用记录或一手数据 |
| **Expertise** 专业 | 懂不懂这个领域？ | 术语与事实写准；说明按什么体系、什么规则产出结果 |
| **Authoritativeness** 权威 | 别人认不认你？ | 站外提及、链接、目录收录、社区讨论、AI 回答里的引用。**只能在站外挣** |
| **Trust** 信任（核心） | 这页诚实、安全、可靠吗？ | 谁运营、怎么联系、怎么收钱退款、AI 生成有没有标明、有没有过度承诺 |

四条不能写错的事（官方说法，见文末来源）：

1. **Trust 最重要。** 不可信的页面，其他三维再高，E-E-A-T 也是低的。补缺口时先补 Trust。
2. **E-E-A-T 不是一个排名因素。** 没有「给页面加 E-E-A-T」这种操作；只能把下面的信号一项项做实。不写「提升 E-E-A-T 分」这类目标。
3. **AI 生成内容不因为是 AI 写的被惩罚**，看的是有没有用。用 Google 的 Who / How / Why 自查（第 2 节）。
4. **SEO 和 GEO 用同一份信任。** AI 引擎挑引用来源时，也在候选里找最可信、最直接回答问题的那页；不为 AI 另建一套信任页。

## 2. Who / How / Why 自查

每张要索引的页和全站各过一次，答不上来就是缺口：

- **Who**：读者看得出这页、这个站是谁做的吗？有没有 About、联系方式；适用时有没有作者或编辑署名。
- **How**：内容怎么产生的？用了 AI 或自动化、且读者会想知道时，在相关位置说明用了什么、按什么规则、人怎么把关。
- **Why**：这页首先是为了帮访问者完成任务，还是为了拿搜索流量？后者的信号：按字数写、为关键词拆页、只改日期不改内容。

## 3. YMYL 边界

YMYL（Your Money or Your Life）指健康、钱、法律、安全、人生大事这类话题，评估标准更严。

- 先判断产品本身是不是 YMYL。是，就必须有真实具名的专业作者或审核人；拿不出就不做那类内容，不用 AI 冒充专家。
- **娱乐、自省、工具类产品被拿来问 YMYL 问题时**（例：塔罗站用户问感情、工作、钱；星盘站问健康）：页面和结果里写清它是什么、不是什么（例如 *for entertainment and self-reflection; not medical, legal, or financial advice*），不承诺结果、不给具体医疗、法律、投资指令，必要时指向专业帮助。这句声明是 Trust 信号，放在用户能看到的位置，不藏进条款。
- 边界文字是事实陈述，按 [GEO 写作规则](geo-writing-rules.md)第 3 节全站同一写法。

## 4. 站点层信任页清单

上一轮只有写法规则时最容易漏的就是这一层。开工画骨架时把这些页放进页面清单（角色多为「公开、可索引或 noindex 视情况」，不是任务页，不违反「一页一任务」）：

| 页 / 位置 | 写什么 | 维度 |
|---|---|---|
| About | 谁在运营、为什么做、怎么联系；有真实一手素材（使用记录、截图）就放这里 | Trust、Experience |
| 方法说明（How it works / How readings work） | 内容或结果怎么产生：数据或体系来源、AI 怎么用、人怎么把关、明确不做什么 | Expertise、Trust |
| 法务与退款 | Terms、Privacy、Refund；与支付后台实际政策一致 | Trust |
| 收款方说明 | 谁收钱（含 Merchant of Record）、账单上显示什么名字 | Trust |
| 官方支付标志 | 用支付方官方资产，按 `anti-slop-frontend` 的 brand-assets | Trust |
| 作者 / 编辑署名 | 只在有真实个人对内容负责时；YMYL 内容必需 | Expertise、Experience |
| 联系方式 | 可用的邮箱或表单，与结构化数据 `contactPoint` 一致 | Trust |

**法律主体没成立时，只写真实的**：个人开发者就写个人或产品名，不编公司名、地址、注册号；主体成立后再同一次改全站和结构化数据。

## 5. 体检表：开工打底，完工复评

模板在[E-E-A-T 体检表](../assets/eeat-scorecard.md)。用法：

- **开工**：复制模板进本项目文档，按当时线上（或尚未上线时按计划）打「改前」分，缺口变成页面清单与 brief 里的条目。
- **完工体检**：同一张表打「现在」分，写「下一步」；分数只按当天线上能看到的东西打，看不到的写 `?`，不按「已写好未上线」给分。
- 0 = 没有，1 = 有一部分，2 = 做实了。不加总成一个总分：E-E-A-T 不是分数，总分只会让人去凑容易的项。
- 每轮站内改动后，按[讲解页模板](../assets/seo-geo-briefing-template.html)给人出一份中文讲解，体检表原样进第 4 节。

## 6. 各份规则补的是哪一维

| 规则 | 主要补的维度 |
|---|---|
| 本文件第 4 节：信任页清单 | Trust、Expertise |
| [GEO 写作规则](geo-writing-rules.md)：问题表、首句即答、可引用句 | Expertise（答得准）、Experience（示范与一手数据） |
| [GEO 写作规则](geo-writing-rules.md)第 3、4 节：实体一致、事实单源、Schema 只标可见内容 | Trust |
| `anti-slop-frontend` copy-gate：没有 AI 味、不过度承诺 | Trust |
| [引擎规范手册](engine-playbook.md)：抓得到、初始 HTML 有内容 | 前提：没被抓到，四维都无从谈起 |
| `distribution-link-loop`：站外来源、目录、AI 引用观察 | Authority |
| `product-growth-review`：Search Console、AI Performance、AI referral | 验证四维有没有变成结果 |

## 7. Authority 的交接

Authority 只能在站外挣，归 `distribution-link-loop`。两边的分工：

- **本 skill 交出**：可分发的任务页、信任页、全站统一的实体写法（品牌名、产品名、关键事实），以及体检表上 Authority 行的当前分。
- **`distribution-link-loop` 负责**：站外提及、目录、社区、AI 引擎里实际引用的逐家观察；站外主页（社交、目录条目）真建好后，回本 skill 把 `Organization.sameAs` 补上——**主页不存在时不写 `sameAs`**。
- **回来的结果**：它的观察（被谁引用、引用准不准）写回体检表 Authority 行；引用不准时回本 skill 改对应页的问题表。

## 来源

官方说法以[资源库](source-library.md)的「官方」一栏为准，核对日与刷新规则也在那里。本文件依据的四条：Google 2022-12 E-E-A-T 博客、Search Quality Rater Guidelines、Creating helpful content、AI 生成内容指引。
