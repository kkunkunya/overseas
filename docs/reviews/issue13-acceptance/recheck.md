# #13 独立只读增量复验（2026-09-07）

结论：`pass`。本轮仅四文件增量及原 F1–F4 关闭条件；原 report.md 保留，不覆写旧候选结论。不继承 writer 自检。

## 开始/结束锁

| 对象 | 本地与远端 head（开始=结束） | PR base（开始=结束） | clean / branch |
| --- | --- | --- | --- |
| mono PR450 | 7d47f21395388bde00598cb6e15d430a49571547 | 4cfe044401ec8150a46a2f583aadb834589ed40a | 开始/结束 clean；fix/13-writer-tmpoverseas-framework-fix-20260907sp |
| 知识 PR14 | e962a139c262dd84949dd5e8d302c1afd90b3c7d | 5b87c4c9acd6e893ec08b3a2440c5ee2b2fdcb98 | 开始/结束 clean；fix/13-framework-entry-handoff |

mono merge-base 仍为 9b3be32e4205f0123ae9f473fd3dad837f3133de；知识 merge-base 仍为 5b87c4c9acd6e893ec08b3a2440c5ee2b2fdcb98。远端通过个人 `env -u GH_TOKEN -u GITHUB_TOKEN gh pr view` 只读核验。

增量范围精确为：mono 的 skills/_shared/ask-me/SKILL.md、skills/overseas/direction-validator/SKILL.md；知识的 3-SEO获客/SEO-GEO全流程/路线数据.json、overseas-skill-map.html。比较起点分别为 88d445dbef7666109208ee41866aa498a99f274a、5a1193c3286fc98440edaf341c77c6bfb08ab2cb。

## F1 pass：GEO 待核不再误交技术审计

证据：ask-me 的 GEO 行明确仅自有页访问、初始 HTML、抓取、索引阻塞交 seo-readiness-audit；授权交账户/权限负责人，来源真实性交取证负责人，标待补项并继续可做准备。

独立合同演练（模拟输入，无真实账号调用）：

- 真实 AI 问题、计划页、授权未知：进入 geo-source-loop，记录平台、问题、来源范围、待授权 owner 与观察条件；不生成已核实来源或引用效果，不进入页面审计。
- 已授权但来源不能复读：标待核并交取证负责人，继续问题/目标页准备，不伪造原始答案。
- 页面已定义但返回访问错误或初始正文缺失：交 seo-readiness-audit，以页面任务/URL角色及具体故障为输入。授权/证据边界与页面技术问题分开。

以上是对实际候选指令的独立路由演练，不是宿主自动加载或真实 AI 服务行为测试。

## F2 pass：有限反证重评可直接退出，常规门保留

证据：ask-me 明确已核合格反证优先进入 direction-validator；其第0节跳过第1–4节、历史资料记 unknown、只作具名范围 narrow/reject/停止，并有独立完成/退出合同。新来源、冲突或时效变化才另核实；无新缺口不回 radar。

独立合同演练（模拟）：原承诺依赖一项能力，已核实且有日期的一手规则直接否定该能力在市场A的可交付性，历史3+15与参考站unknown。直接第0节列原前提/反证/unknown，停止市场A对应任务或页面投入；市场B没有被证据覆盖，保留原状态；交具名owner与唯一动作后退出，不补跑选词、不回radar、不删除资产。

对照：只有新想法或替代方向、没有合格反证时，不能进入第0节；仍需常规参考站、锁定3+15与人工Semrush证据。单次波动、免费版、几周无排名被明确排除；未核新信号交radar。新方向不能随有限重评获得go。

## F3 pass：真实 Ego 锚点恢复与定位

独立 Task Space 21；自有只读 http.server 127.0.0.1:8765，加载本次知识候选。

实际点击 current-next 前先用搜索或阶段按钮隐藏 tools，再点击链接，等待平滑滚动稳定；重复点击通过滚回链接并再次真实点击完成。未调用页面 click handler 模拟结果。

| 视口 | 前置状态 | 点击后 |
| --- | --- | --- |
| 1280×844 | 搜索GEO，tools.hidden=true | hash=#tools；hidden=false；搜索清空；25/25；卡top=180.03125、bottom=470.7265625 |
| 1280×844 | 上线之后，tools.hidden=true，6/25 | 同上 |
| 1280×844 | 已是#tools，再次点击 | 同上 |
| 390×844 | 搜索GEO，tools.hidden=true | hash=#tools；hidden=false；搜索清空；25/25；卡top=180.234375、bottom=460.9296875 |
| 390×844 | 上线之后，tools.hidden=true，6/25 | 同上 |
| 390×844 | 已是#tools，再次点击 | 同上 |

390px document.scrollWidth=390，无横向溢出。实际截图 recheck-390-cdp.png 已视觉检查：tools卡单列、正文与边界完整、目标可见。默认 captureScreenshot 生成的 recheck-390.png 为空白，保留为失败取图证据，不作为视觉通过依据；改用同一Ego/CDP的实际视口截图成功。首次1秒取样尚在平滑滚动，后续3秒稳定态六个场景全部通过。

## F4 pass：25卡同步与受影响搜索

独立解析JSON/HTML：25行、25唯一id、25卡、11 helpers；逐卡phase、keywords、title、owner、trigger、inputs、output、check、next、tools、actions与source核对零差异。

1280与390两视口真实输入均得到：GEO→geo（1/25）；反证→review（1/25）；重评→review（1/25）；writer→brief（1/25）；渠道→measurement/distribution/messaging/ads/review（5/25）。

两仓增量diff-check通过；独立运行frontmatter和索引校验均95项通过、无stale引用。

## 边界与交回

- 原报告与历史证据保留；本轮四项均关闭，无新增blocking finding，无park。
- 未测：真实AI/GSC/搜索服务、账号权限、产品效果、索引/排名/引用/收入；宿主加载及多模型自动路由行为；四文件之外未重新全验，457篇未重读。
- 未修改候选、未派工、未merge/分发、未进行产品操作、未发GitHub评论、未调用review_submit。
- 自有Ego Task Space 21已关闭（done=true）；8765服务已Ctrl-C退出。
- 初次网络/端口请求受sandbox限制，通过已授权只读/本机检查的工具提权后成功；无自动审批拒绝，无GitHub写入尝试。
- 交主会话：仅本轮精确head/base的增量复验pass；是否合并分发由持权主会话按已有授权与最终锁决定。
