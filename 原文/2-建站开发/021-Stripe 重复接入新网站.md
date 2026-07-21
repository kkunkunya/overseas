# 网站出海每日分享：Stripe 重复接入新网站

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247485224&idx=1&sn=e6464715e73e6f363d713aedb1aad25d&chksm=c28d2373f5faaa6506eaf80f02ec7ed250172d5a19674baa781131405273392d7e7ce52255cb#rd
> 分类：开发
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！
今天分享已经有Stripe了，新网站如何接入现有的Stripe。

一般有3种操作方式，新建产品、新建账号、新建组织。新建组织这个我没有用过，我们来聊一下新建产品和账号。

新建产品

新建产品和之前分享的产品配置差不多，具体细节可以看之前的分享
1、首先在产品目录配置你新的产品的名称、价格、收费方式
2、在webhook 里面添加新的接收端，按照之前的方式，筛选要监听的事件，输入新的Webhook 名称和URL即可

[图] 

3、然后同样的方式复制密钥，价格配置到网站即可

新建账号

1、点击左上角的账号，选择创建，选择创建账户，然后我选择的是创建单独的账户

[图] 

2、然后接下来的流程就是和Stripe 注册的流程基本是一致的，可以去看看之前的注册流程分享
3、创建商家的流程直接选择之前创建过的商家

[图] 

4、最后修改一下网站的url 和 账单描述符 为新的网站。

[图] 

5、然后也是前面说的产品配置流程

这2种方式的优缺点

新建产品：共用一个 Stripe，配置产品简单，资金管理集中，但是用户看到的网站信息可能是另外网站的，可能一个网站出问题，其他网站被连带了。

新建账号：配置更繁琐一些，资金管理也更分散，但是每个网站信息独立，支付相关的信息都是对应的网站的信息，会一定程度上隔离其他网站带来的风险。

我是赫兹，专注网站出海第302天，持续分享网站出海内容。新朋友可以看看之前的文章合集；想系统学习，也推荐关注哥飞老师，我很多方法是向他学习的，微信搜索 361079 就可以找到他。

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
