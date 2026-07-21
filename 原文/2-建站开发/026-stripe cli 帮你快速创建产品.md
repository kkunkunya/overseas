# 网站出海每日分享：stripe cli 帮你快速创建产品

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247485642&idx=1&sn=08e043551ed7ddcc71a3253f50a1157d&chksm=c28d2c91f5faa587d0f1bdee98145a1b5e91edefef41679125847de95063cba63c06e4685334#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！

不知道大家每次网站要接入支付是什么样的流程，我之前是创建一个Stipe 账号，然后添加webhook，手动创建自己产品，然后苦逼的去把对应的价格id 放到对应的产品上，这一套操作还挺花时间的。然后发现stripe 其实提供了cli ，可以让AI 去帮我们做这一套的操作。

stripe cli 官方文档：docs.stripe.com/stripe-cli

[图] 

安装cli

这个可以按照文档里的教程安装，不过现在这些操作我一般让AI 去做了。

我就告诉claude : 参考文档docs.stripe.com/stripe-cli ，帮我安装stripe cli 即可。然后AI 会执行 stripe login 让你在网页端进行授权登录。

直接使用cli 接入支付创建产品

接入这个也是口喷（我是让他基于模板修改的，大家可以根据自己的模板调整）：pro 会员是 9.9 每月的订阅费，把lifetime 换成Premium订阅，29.9每月，同时支持年费，分别是99 和 299 一年，参考文档：cli 创建对应的webhook 和 产品，完成stripe 的支付接入。

不过需要注意的是，stripe cli 要创建线上产品，需要配置线上环境的密钥 sk_lice_xxxx。

等待AI处理完成之后，你就会发现AI帮你创建好了对应价格的产品，webhook也按照要求，把监听的事件配置好了。也能直接在线上环境付款了。

我是赫兹，专注网站出海第348天，持续分享网站出海内容。新朋友可以看看之前的文章合集；想系统学习，也推荐关注哥飞老师，我很多方法是向他学习的，微信搜索 361079 就可以找到他。

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
