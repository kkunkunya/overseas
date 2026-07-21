# 网站出海每日分享：stripe 测试续费逻辑小技巧

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484539&idx=1&sn=6c559780d8d1280dbcb83692e232cb87&chksm=c28d2020f5faa9360d3d721689d1d14882f93caff289fce4362c5f521deaa828286720ffb8fe#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

分享一个测试stripe 续费逻辑的小技巧。

背景是我有个用户自动续费了，发现用户续费了，但是积分没有到账，修改了这个问题，但是这种场景很难测试。

没想到stripe的订阅时间，可以是一天，这样的话就可以自己设置一个一天的订阅，然后测试自动续费了，看到时候第二天续费订阅的时候，积分是否到账。大家初期的时候，就可以这样测试看看。

[图] 

如果是某些webhook 事件失败了，还可以在stripe的开发后台里面的webhook 重试一下

[图] 

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第193天，每天都会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

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
