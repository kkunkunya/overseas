# 网站出海每日分享：grok 上奏折,监测新词

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484597&idx=1&sn=8a14edb22dbf221cf64945813eadbc92&chksm=c28d20eef5faa9f81f8dafa018f6575aa1565fb9a8f06cc3d43a84a08dc14e7fb11b838cc362#rd
> 分类：需求挖掘
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们今天分享grok 给你上奏折。

我们之前分享过chatgpt 可以让他给你设置定时任务，grok也是有同样的能力。之前分享监测新词推特是一个很好的信息源，很多的AI模型都是第一时间在推特上爆料，而grok 又是能获取到这些数据的。所以我们就使用grok进行监测。

打开grok.com 登录后，在左下角头像哪里找到task，创建任务。选择一个每天的定时任务，输入你要监测的内容，创建完成后任务右侧有个测试运行的按钮，可以先运行看看效果。确定后就等待每天他给你上奏折了。

[图] 

[图] 

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第199天，每天都会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

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
