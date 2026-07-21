# 网站出海每日分享：批量查看Google trends开源项目

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247485432&idx=1&sn=e4a4c3597f16613f4d682f86dca6ed73&chksm=c28d23a3f5faaab51c769b462746ab4b64aeda8bdf47900f5ea694bdf3c6011948f6a77b879e#rd
> 分类：需求挖掘
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！
想必刷Google trends 是很多网站出海朋友的日常活动，今天分享一个开源项目pytrends
https://github.com/GeneralMills/pytrends

然后大家就可以用这个 开源项目做Google trends 的热词抓取，我就直接让claude code 帮我实现对应的逻辑
使用 prtrends 开源项目，写一个 pyhton 的搜索热点抓取项目，有一个输入框可以输入一些词根，然后展示这些词根最近 7 天增长比较多的相关词，注意做好限流处理，避免风控。

然后输入哥飞老师公众号分享的一些词根，就可以去抓取数据了，可以一次设置几十个词根，等一段时间，让它抓好，然后慢慢看这些数据，提升Google trends的效率。

[图] 

不过pytrends 本质是模拟浏览器请求 Google Trends，不是官方 API，免费，但是有速率限制，抓取多个词时间会久一点，请求频繁了Google 也会返回429异常。大家也可以试试一些付费的api ,比如：DataForSEO ，这种就更稳定，速率限制也还好。

我是赫兹，专注网站出海第321天，持续分享网站出海内容。新朋友可以看看之前的文章合集；想系统学习，也推荐关注哥飞老师，我很多方法是向他学习的，微信搜索 361079 就可以找到他。

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
