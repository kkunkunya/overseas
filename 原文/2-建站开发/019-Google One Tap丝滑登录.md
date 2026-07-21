# 网站出海每日分享：Google One Tap丝滑登录

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484873&idx=1&sn=fd495bd25593f091274c829501f5cfd2&chksm=c28d2192f5faa88456268548c4b5f212c6bb3d805ad6241cd68f2a3f90a1cff359392ed05952#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

今天分享一下Google One Tap 登录，让你实现丝滑登录。

它就是那种你一打开网站，右上角会弹出一个小卡片，提示用 Google 账号一键登录的东西，不用跳转页面，也不用输密码，点一下就进了，体验非常顺。

[图] 

这一套流程是Google 官方已经提供好了的，要接入实现，我其实就是告诉AI让他 “在首页接入Google-one-tap登录”，就自己给我实现好了。

我是在原有Google 登录上加的，需要需要配置的的id也是现成的，这个过程中需要注意Google cloud 后台的已获授权的 JavaScript 来源需要配置上url

[图] 

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第228天，定期会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

• 网站出海每日分享

• 网站出海深度总结

 
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
