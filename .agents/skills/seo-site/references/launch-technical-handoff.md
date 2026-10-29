# 上线、测量与技术迁移交接

## 支付、域名与部署上线包

**触发**：产品已可演示，准备接支付、购买/绑定域名或部署；本方法产出可审交接，不代替授权执行。

**输入**：产品/仓库与环境、生产 owner、经营主体与目标市场、域名候选与 registrar/DNS owner、支付商与币种、套餐/退款/取消/税务事实、实际数据流与采集用途、适用的同意/许可及记录 owner、条款/隐私/退款页面 owner、部署平台、秘密清单、分析工具、备份/回滚、上线窗口。

**步骤**：

1. 建依赖图：`域名/DNS/TLS → 部署 → 支付 webhook/回跳 → 分析 → sitemap/搜索控制台`；为每项标 draft、approved、executed、verified。
2. 域名只做候选冲突、品牌/拼写、历史/商标和 DNS 方案检查；购买、转移和 nameserver 修改在动作前取得授权。
3. 支付先定义商品/价格、币种、税费、退款、失败/重复/取消、权限与 webhook 验签；用 provider sandbox 覆盖成功、失败、重试和退款，再申请生产动作。选收款平台、商户开户审核、切真钱前的链路体检与 live 验收按 `overseas-merchant-payment` 做。
4. 上线前准备与实际业务一致的 Terms、Privacy、Refund/Cancellation、联系与支付说明。逐页核对经营主体、商品/服务、价格、续费、取消、退款路径、支持渠道和生效日期；模板或生成稿必须由相应业务/法律 owner 复核，不能冒充法律意见。
5. 画实际数据流：收集什么、为哪个用途、流向谁、保存多久、用户怎样查询/撤回/删除。按目标市场、数据类型、渠道与当前官方规则判断是否需要 consent、notice、合同或其他许可；只实现适用要求，不武断假设所有地区都必须同一种同意。保存政策版本、同意/许可来源、时间、scope 与撤回/suppression 记录。
6. 部署记录构建命令、环境变量名、迁移顺序、健康检查、日志入口、上一个可恢复版本和回滚 owner；秘密值不进仓库或评论。
7. 在发布前写测量合同（做法见 `seo-site` 第二段「埋点」）：业务问题、event、触发点、必需 properties、身份/适用同意、用途、来源/UTM、owner 和 QA；先验证事件，再把它当基线。
8. 发布后核对 DNS/TLS、HTTP、关键页面、支付回跳/webhook、政策页面/版本、同意或许可记录、事件、robots/canonical/sitemap，以及各搜索与 AI 引擎爬虫放行情况（见[引擎规范手册](engine-playbook.md)）；回执分别保存，不能用“部署成功”覆盖整条链。

**判断**：缺生产 owner、回滚、经营/支付主体、与实际业务一致的政策页面、适用的数据用途/许可记录、关键秘密或事件 QA 时 `park` 对应动作；其他可审准备继续。实时 provider、隐私、消费者、平台规则与费用在执行日查目标市场官方源，不写死，也不把某地区要求泛化到全部地区。

**输出**：上线依赖表、逐动作授权队列、配置/秘密名清单、sandbox 证据、政策页面与业务事实核对表、数据用途/适用同意或许可记录、测量计划、smoke/回滚 runbook、未知项。

**验证与交棒**：未持权者只演练和产出 proposal；真实购买、配置、部署或支付由持权 owner 执行并回传 receipt。产品代码进产品仓；上线后搜索检查留在 `seo-site`，结果复盘交 `product-growth-review`。

## 技术 SEO、性能与 Schema

**触发**：上线前、刚上线、索引异常、页面改造或性能问题。

**输入**：URL 角色、服务器响应与初始 HTML、robots/canonical/sitemap/内链、渲染路径、移动/桌面 lab 与 field 数据、页面实体/可见事实、当前官方资格规则。

**步骤**：

1. 先按现有正文检查可访问、抓取、索引和页面任务；用 `Finding / Evidence / Impact / Fix / Confidence / Owner / Recheck` 记录。
2. 性能分开 field 与 lab，按具体瓶颈定位服务器、关键资源、图片/字体、主线程、布局与交互；没有 field 数据时标 `unknown`，不推断真实用户体验。
3. Schema 先盘点可见实体和现有 JSON-LD，再选与页面真实类型相符的最少标记；不添加不可证明的评价、价格、作者、FAQ 或关系。
4. 用语法/Schema validator 检查，再按当日官方 rich-result eligibility 核对；验证通过只证明格式/资格准备，不证明展示。
5. 按最早阻塞排序修复，并指定产品仓文件/owner 与复测方式；不在本知识仓写实现。

**判断**：抓取/索引阻塞先于性能微调；lab 退化但 field 稳定时先查发布差异；标记与可见内容冲突时删除或修正文，而不是补造字段。

**输出**：证据化 findings、优先级、责任位置、复测命令/页面和未知项。

**验证与交棒**：复查服务器响应、渲染页面、移动交互、validator 与搜索平台；每种证据单列。需要代码修复交产品仓 writer，复测仍由 `seo-site` 承接。

## 站点迁移与发布前后快照

**触发**：换域名、URL、框架/CMS、协议、主机，或大规模模板/信息架构变化。

**输入**：当前/目标 URL 清单、流量/链接/索引基线、内容与 metadata、canonical/robots/sitemap/Schema、重定向表、环境与回滚 owner、发布时间窗。

**步骤**：

1. 冻结旧站快照：重要 URL、状态、title/H1、canonical、robots、Schema、内链、sitemap、关键查询/流量与外链。
2. 建一对一 URL mapping；不能保留的内容明确 410/合适父级，禁止全部重定向首页。
3. 在 staging 检查内容/metadata parity、redirect hops、canonical、robots、sitemap、hreflang、Schema、分析事件和关键交易路径。
4. 预写切换顺序、DNS/部署/redirect owner、验证清单和回滚触发；迁移期间避免同时做无关大改。
5. 切换需授权。切换后立即抓关键 URL，再按既定窗口比较索引、查询、流量、错误和转化；将差异归因到具体变更，不靠总分。

**判断**：mapping、staging parity、owner 或 rollback 缺一项就不切；差异无法解释时先停止后续批次。

**输出**：旧→新映射、前后快照、执行/授权清单、异常与回滚决定。

**验证与交棒**：抽查高流量、深层、重定向、删除和 locale URL；实际迁移由产品/基础设施 owner 执行，观察窗交 `product-growth-review`。

## 固定来源

- AgriciDaniel，technical/performance/schema/drift（MIT，固定 SHA）：https://github.com/AgriciDaniel/codex-seo/tree/97c59bcdac3c9538bf0e3ae456c1e73aa387f85a/skills
- Aaron He Zhu，pre-migration playbook（固定 SHA）：https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/888dd38edbd43e7eaeeb4ba053d6c290fb21b89d/seo-geo/tune/technical-seo-checker/references/pre-migration-playbook.md
- Google Search Central，官方 structured data 总览（执行时复核当前规则）：https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data
- web.dev，官方 Core Web Vitals（执行时复核当前指标）：https://web.dev/articles/vitals
