# 网站出海每日分享：重大 Next.js 漏洞问题，小心账单爆炸

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484584&idx=1&sn=42b4674d57f0e684283013c897fd29f0&chksm=c28d20f3f5faa9e5eac9116e436e92a4c57147f857533d7dbd53d5960fe415f0c2918ecfded6#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

最近Next.js 爆出重大安全漏洞，CVE-2025-66478 未经鉴权即可远程执行代码。我起初并没有在意，发现很多群友都中招了，有的被加密勒索了，有的被远程植入挖矿程序了。然后我去看我vercel，发现我的项目也中招了。

[图] 

有一个没什么流量的网站，cpu 占用激增，但是访客并没有什么变化。还好账单消耗的不对，要是发现的晚，可能就账单爆炸了。

所有朋友们一定要去检查修复这个漏洞。

[图] 

[图] 

Vercel 的顶部会有你异常项目的提示，点击可以查看到被影响的项目，然后依次升级next js 和 react版本，我的react版本是19.0.0  nextjs 版本是15.2.1，可以问AI建议升级到哪个版本，我Nextjs升级到15.2.6，React升级到19.0.1, 改动其实也很小,大家一定要重视啊。

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第198天，每天都会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

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
