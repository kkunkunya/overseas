# 网站出海每日分享：创建claude code命令，减少重复操作

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484034&idx=1&sn=6573e8234b7eaa45c766fd3e694ec5b8&chksm=c28d26d9f5faafcf090b642332ab02af502f3fe0ec72fee62ceb8d35d93e1bd3701749a42500#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们

今天分享如何创建claude code命令

在不同项目中，不知道大家会不会有让 claude code 做重复的事，比如：

SEO 检查

代码检查

基于关键词生成SEO内容

与其每次都重新输入，不如做成 个人命令，方便在任何项目里面都能调用。

其实就是创建一个md文件，三步就能实现

一、找到.claude 路径（我的是在用户路径下），创建一个commands 目录

[图] 

二、在里面建一个 .md 文件，文件名就是命令名，比如：

我创建了一个SEO检查的命令，名称就叫 seo-check.md

三、在文件里写上你想让 Claude 执行的提示语，比如：

You are an SEO expert. Check the SEO quality of the following page:Page: $ARGUMENTSPlease analyze from the following aspects:1. Title tag quality and keyword usage2. Meta description clarity and length3. Heading structure (H1/H2/H3)4. Internal linking opportunities5. Image alt text usage6. Content quality and keyword density7. Page load speed and mobile friendliness8. Overall recommendations for improvementProvide a clear, structured report.

里面用 $ARGUMENTS 接收参数

在 .md 文件里加上 $ARGUMENTS，就能在调用时传不同的内容。这里就是调用时传入页面

调用就是用文档名称就可以使用了。

[图] 

[图] 

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
