# 网站出海每日分享：stripe 收款设置，避免不必要的损耗

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484803&idx=1&sn=47caf3cb1e5ccd9ad98f203a390c9a59&chksm=c28d21d8f5faa8ce9b1623e423bfabcd3ef617ce8e38b211004f1644d7889a1274b375aaedec#rd
> 分类：支付
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

今天分享stripe 收款设置，避免不必要的损耗。

起因是我昨天偶然发现，stripe 费用那里的扣费，有一笔货币兑换费用，因为我收款是用港币收款的，但用户支付的是美元，这个费用是2%。

[图] 

我就调整了一下收款的类型，改成了美元收款。

调整方法是

右上角设置，选择商家，银行账号与货币，添加结算货币。然后选择收款是美元收款，输入统一的银行卡账号，就添加好了。然后把新添加的收款设置为默认方式，可以看到会有1%的提现费用，相较于货币转化的费用也少了1%。

[图] 

[图] 

而且我之前购买美元产品，也都是用的这个账号，所以那里也就有货币的转化费用，现在直接美元购买，相当于少了2次磨损了。

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第220天，定期会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

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
