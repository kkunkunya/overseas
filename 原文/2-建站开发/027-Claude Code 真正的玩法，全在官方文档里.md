# 网站出海每日分享：Claude Code 真正的玩法，全在官方文档里

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247485662&idx=1&sn=73f29a003c5c14fa82e7f60bfa442f9d&chksm=c28d2c85f5faa593c270337aa0fd406846d985719cc73e91d1f49aa5da662c2b7754341b7118#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

最近有在想怎么更好的去用claude code，看了一些文档，然后发现自己好像忽视了官方的文档，我去看了官网文档后发现，有很多用法都是可以在开发中提效的。建议大家都去看看。

官网地址：https://code.claude.com/docs/zh-CN/overview 有一说一，虽然官方不支持中国，但是他的中文文档还是适配挺好的。

尽量是都看一遍，这里推荐大家可以去看的点

各种操作的快捷键

https://code.claude.com/docs/zh-CN/keybindings 比如Windows 粘贴图片，我以前一直以为是windows不支持，ctrl+v 没有反应，看了群友的分享，才知道windows 是 alt+v  这个也是在官方的快捷键文档写的很清楚的。有特别多的快捷键，说不定你就发现原来有些笨拙的操作是可以快捷键一键解决的。

[图] 

Claude Code 最佳实践

根据官方推荐的方式去写代码，能减少一些返工问题。

给 Claude 一种验证其工作的方式，比如列出截图，让它自己对比修复

先探索，再规划，最后编码，避免直接编码导致的错误结果

在提示中提供具体的上下文：图片、url、错误信息等

配置一些环境来提升开发效率：claude.md 、权限、cli、mcp、hook、skill、subagent

有效沟通：提出代码库问题、让claude反过来问你

管理你的会话，对话是持久和可逆的，发现错误可以立即撤销

自动化和扩展，可以多个任务同时进行，或者自主进行

claude 的存储和记忆

这个也是平时开发里面挺重要的，有可能每次都需要输入上下文，没有记录。可以合理的利用他的记忆机制，设置项目的记忆，全局的记忆，自动记忆等，减少每次输入重复内容

skill

大家skill 应该是用的比较多了，一些常用的操作做成skill或者用现成的skill 对开发提效还是挺有帮助的。可以看看这个章节更好的去创建、使用skill，以及排查一些skill 可能出现的问题

subagent

用subagent同时扮演多个不同角色来协同完成任务，在任务执行是各司其职，做成一个分工协作的团队，在开发时效果后更好，同时多个子agent 并发执行，效率也会更高

mcp

使用mcp 调用三方的工具，也是开发提效的一个很重要的方式， 官方有推荐一些常见的mcp和怎么使用，大家都可以去看看

还有很多内容，我也一时半会没看完，但是我发现看了之后确实了解补齐了之前很多不知道的用法，建议是去看看，侧边栏和顶部导航栏都去点一下，内容很多。

[图] 

我是赫兹，专注网站出海第351天，持续分享网站出海内容。新朋友可以看看之前的文章合集；想系统学习，也推荐关注哥飞老师，我很多方法是向他学习的，微信搜索 361079 就可以找到他。

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
