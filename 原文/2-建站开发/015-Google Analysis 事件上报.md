# 网站出海每日分享：Google Analysis 事件上报

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484483&idx=1&sn=b87ae2ed921724fbbca672989175f10c&chksm=c28d2018f5faa90e11a06f216cfef43a7aab1d9ccdad64a8d971a4c6938bce33f2cdaa4460dd#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

今天分享一下，Google Analysis 自定义收集事件，收集到的事件，可以在报告->查看用户互动度和留存率 -> 事件 里面查看。

上报后，方便分析自己产品的一些情况。

[图] 

收集事件，其实就是在前端调用gtag，传递一些参数即可。格式如下

gtag('event', '<event_name>', {// 推荐参数（GA4 内置支持）value: 99.99,              // 事件价值currency: 'USD',           // 货币transaction_id: 'T12345',  // 交易IDitems: [...],              // 电商商品数组// 自定义参数（任意键值对）custom_param: 'any_value',another_param: 123});

官方文档：https://support.google.com/analytics/answer/9234069?hl=zh-Hans&ref_topic=13367566&sjid=11941205814201191673-NC

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第185天，每天都会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

网站出海每日分享

网站出海深度总结

 
 var first_sceen__time = (+new Date());
 if ("" == 1 && document.getElementById('js_content')) {
 document.getElementById('js_content').addEventListener("selectstart",function(e){ e.preventDefault(); });
 }
