# 网站出海每日分享：Stripe API 分析数据

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484996&idx=1&sn=5ff29a66792bdafc99ee679520133539&chksm=c28d221ff5faab0962ef4161efa5d856d7dd3e27fa85bc2845ea25ba21c6be280e74494755c8#rd
> 分类：数据分析
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

最近发现，最近想要要 stripe 分析查看一些数据，但是发现不是特别方便，比如想要看哪些国家支付比较多，从而调整投流，多语言的一些策略，但是里面可以看到的国家比较有限，看起来也不方便，但是用Stripe Sigma 会有收费。

这个时候就找到了Stripe API：

通过Stripe API 可以

通过 Stripe API，可以拿到：

每一笔订单 / 支付记录

支付金额、币种、时间

用户来自哪个国家、用的什么卡

是否成功、是否退款、是否争议......

所以我前面的需求就可以用 API 拉数据自己算，接到我自己的后台，增加一个看板，反正AI 编程一个数据面板也是很快的，我就简单一句话，让AI接入了Stripe api 查看数据： “管理后面里面新增一个stripe 管理页面，通过stripe api 获取到订单信息，统计每个国家的收益，每个人员的收益 ”，AI就用 Stripe api，生成了每个国家，每笔订单，每个用户的数据了，大家也可以用这个api 生成更酷炫的数据分析面板

[图] 

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第245天，定期会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

网站出海每日分享

网站出海深度总结

 
 var first_sceen__time = (+new Date());
 if ("" == 1 && document.getElementById('js_content')) {
 document.getElementById('js_content').addEventListener("selectstart",function(e){ e.preventDefault(); });
 }
