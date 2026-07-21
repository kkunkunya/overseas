# 网站出海每日分享：stripe自动设置优惠

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484292&idx=1&sn=1969b605a8b0bd47262099359f65b911&chksm=c28d27dff5faaec9b5f0500e374420c45f50b8e863e81cd99fa4bb5fab4782dcc999d0099b4b#rd
> 分类：支付
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

今天分享如何使用stripe 设置优惠，在用户购买时，自动设置上优惠码，无需手动填写(如需手动填写，可以直接设置allow_promotion_codes为true，用户可以填写上自己得到的优惠码)。

[图] 

首先是stripe平台上新增一个优惠券，然后填写上优惠名称，折扣，持续次数

[图] 

[图] 

创建完成后，需要在stripe的支付代码的checkout逻辑里，添加上discounts信息和优惠码id，注意一定要去掉allow_promotion_codes，否则请求支付时，会报错。

官方参考文档：

https://docs.stripe.com/payments/checkout/discounts

[图] 

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第162天，每天都会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

网站出海每日分享

网站出海深度总结

 
 var first_sceen__time = (+new Date());
 if ("" == 1 && document.getElementById('js_content')) {
 document.getElementById('js_content').addEventListener("selectstart",function(e){ e.preventDefault(); });
 }
 
 

 
 
 
 if ("0" == 1) {
 document.addEventListener("keydown",function(e){
 if ((e.metaKey || e.ctrlKey) && (e.key === 'c' || e.key === 'C' || e.key === 'x' || e.key === 'X' || e.key === 'a' || e.key === 'A')) {
 if (e.target.tagName === 'INPUT' || e.target.tagName === 'TEXTAREA') { return; }
 e.preventDefault();
 }
 });
 document.addEventListener("copy",function(e){
 var sel = window.getSelection();
 var content = document.getElementById('js_content');
 if (sel && sel.rangeCount > 0 && content && content.contains(sel.getRangeAt(0).commonAncestorContainer)) {
 e.preventDefault();
 }
 });
 }
 

 
预览时标签不可点
