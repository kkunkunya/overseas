# 网站出海每日分享：白嫖neon 数据库

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484013&idx=1&sn=a2ba651f3ae5f3b2b6ffa5222326ad87&chksm=c28d2636f5faaf2018b52d059e321759c72e619a0abfb07f4d8f1f0bf7a546eea4e424462c1b#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们。

今天分享 neon 数据库白嫖。

我之前一直白嫖的supabase数据库，但是一个账号只能注册2个，我现在差不多注册了5个账号，创建了10个数据库。

supabase数据库，其实还有一个问题就是一段时间不用就会给你停掉，我有个项目的数据库就是被关停导致无法使用了，还挺坑的

最近发现了一个neon数据库，这个数据库一个账号就可以免费创建10个数据库，并且不会给你关停。我看mksaas 模板也是推荐这个数据库，今天把这个数据库分享给大家。

1.打开https://neon.com/ 网站，注册一个账号。

2.输入项目名称，选择数据库地区，点击创建就生成了。[图] 

3.因为我使用mksaas ,直接复制链接url配置环境变量 ，就能直接使用这个数据库了

[图] 

完了，没错就是这么简单。核心其实就是那个数据库连接的url。

我是赫兹，一个专注「网站出海」的生意人。 想了解网站出海的朋友，可以去看看我之前的文章

第一次赚美元！纯新手深度复盘网站出海，一文掌握全流程

聊天就能做出精美的网站，你上你也行

网站出海：技术重要，思维更关键——复盘深海圈“排学”的认知转变

网站出海就是一个种树的故事，浇水施肥，静待开花结果

网站出海每日分享

 
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
