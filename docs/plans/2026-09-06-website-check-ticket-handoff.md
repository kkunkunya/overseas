## 拆票与总体验收责任

已按本规格拆为5张原生子票：

| 子任务 | 当前状态 | 原生依赖 | 父标准覆盖 |
|---|---|---|---|
| [通用方法与HTML](https://github.com/kkunkunya/overseas/issues/7) | 可准备实施 | 无 | I1、I2–I7方法准备、I8分发与界面切片 |
| [首个产品现场](https://github.com/kkunkunya/overseas/issues/8) | 待Kun指定产品，Agent核实现场 | 无 | I2/I8前置 |
| [抓取、性能、快照初始化](https://github.com/kkunkunya/overseas/issues/9) | 阻塞 | 方法与现场 | I2/I3、I8产品工具切片 |
| [问题闭环与发布检查](https://github.com/kkunkunya/overseas/issues/10) | 阻塞 | 初始化 | I4/I7及I3历史保留 |
| [数据接入与经营复盘](https://github.com/kkunkunya/overseas/issues/11) | 阻塞 | 方法与现场 | I2/I5/I6、I8数据切片 |

所有结果仍为未测。未指定产品的接入票不贴ready-for-agent；不因子票建好而派工。数据票与工具票没有虚构串行依赖，但共享产品文件时由编排者协调单writer或顺序执行。

父任务由编排者负责I1–I8总体验收与证据汇总，不另建“验收通过即自动关闭父票”的机械任务。方法票通过不能替代产品实测；缺真实域名、服务或支付依赖仍需回填状态和承接，父票不可冒充完整接入通过。

## Tracker回写限制

已核实5张子票均为父票6的原生子票，依赖为9被7/8阻塞、10被9阻塞、11被7/8阻塞。创建请求附带的标签在回读中未出现；随后显式add-label被addLabelsToLabelable权限拒绝，父票评论被addComment权限拒绝。所有子票实际标签为空。未切换凭据或绕过权限。

预期标签：7为ready-for-agent；8为ready-for-human；9/10/11因依赖未满足保持无ready标签。此文件为交棒记录，不替代实际远端标签。本次仅拆票，未实施。
