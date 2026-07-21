# 网站出海每日分享：定价时需要考虑stripe 的手续费

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484839&idx=1&sn=2c5cc3b2d5bcdffb2deb9bca27a98f70&chksm=c28d21fcf5faa8eae03ef618b8585f0949e49eb96c198ee3e2058cadba5a82806332a26b6c77#rd
> 分类：支付
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

今天分享一下定价时需要考虑stripe 的手续费。

最近算 Stripe 账单，发现一个手续费的问题，跟大家分享下。

定价真的不能太低，不然 Stripe 手续费会把你吃掉。

[图] 

Stripe 常见是 2.9% + $0.30/笔，重点在这个 $0.30 是固定的。

比如卖 $4.99，手续费接近 10%；

卖 $9，也要 7%+；

到 $19 / $29 才慢慢回到 5% 左右。

[图] 

如果再叠加国际卡、换汇，实际成本会更高。

所以低价档需要考虑里面很大的一个手续费率折损。定价时可以按照“最坏手续费”倒推。

还有就是之前说的换成美元结算网站出海每日分享：stripe 收款设置，避免不必要的损耗，这个账单里面的79.8 就是没有换之前的，还有一个2%的货币兑换费，换了之后就是1%的提现费了

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第223天，定期会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

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
