# 网站出海每日分享：SEO 插件看关键词，Google趋势

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247485499&idx=1&sn=99094bcf3d5432791205ee2d30a37003&chksm=c28d2c60f5faa57601f49b13ffb47742cee4fa88b7abdd4a9b6df3ddcefe67c225f4d02bf89f#rd
> 分类：SEO
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！
今天分享一个SEO 的chrome 插件：Keywords Everywhere
插件地址：
https://chromewebstore.google.com/detail/keywords-everywhere-keywo/hbapdpeemoojbophdfndmlgdhppljgmp

安装开启后，右侧可以看 关键词难度，可以直接看到这个词对应的Google trends 趋势，可以选择 7天，30天，3个月，12个月的变化趋势，和Google trends 看到的效果差不多。

[图] 

下方还有Trendibng Keywords，Related Keywords, Long-Tail Keywords。通过趋势词，相关词，长尾词，可以用来进行词根找词。付费版本还能看到对应词的cpc,流量

[图] 

我是赫兹，专注网站出海第333天，持续分享网站出海内容。新朋友可以看看之前的文章合集；想系统学习，也推荐关注哥飞老师，我很多方法是向他学习的，微信搜索 361079 就可以找到他。

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
