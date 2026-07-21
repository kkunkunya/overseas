# 网站出海每日分享：

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247485270&idx=1&sn=09dc06c35f29c336c450b581cc680341&chksm=c28d230df5faaa1b9d33ec23b9ab79a5dd390315741256ef264e2b222bb4781b7a9ca8fa852e#rd
> 分类：数据分析
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！
今天分享clarity 看网站的BUG，之前分享过用clarity 看网站的录屏，可以发现用户在使用过程的一些交互和BUG问题。但是每次这些录屏都看会很花时间。发现其实他的面板也会有展示网站的一些数据信息和性能错误信息。

这个在首页的dashboards 页面，可以往下滑，看到很多数据分析卡片，我这里是看到这个JavaScript errors ，发现了网站存在的一些BUG。

比如这里有个用户点击全屏的错误信息，然后点击右侧的录屏按钮，还可以直接看到用户在这个错误时的录屏，错误的地方会有红色定位，在这个红色定位的地方，用户就疯狂点击全屏按钮，没有反应，就帮我定位到了一个挺严重的BUG。

[图] 

另外大家也可以挖掘一下其他的数据面板，比如性能分析，网页加载时长，会告诉你哪些页面加载时长，还可以看看对应的录屏，会不会就是因为加载太久了，用户就退出了。

我是赫兹，专注网站出海第305天，持续分享网站出海内容。新朋友可以看看之前的文章合集；想系统学习，也推荐关注哥飞老师，我很多方法是向他学习的，微信搜索 361079 就可以找到他。

[图:图片] 

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
