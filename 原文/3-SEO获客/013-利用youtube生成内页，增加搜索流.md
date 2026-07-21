# 网站出海每日分享：利用youtube生成内页，增加搜索流

> 原文链接：http://mp.weixin.qq.com/s?__biz=MzkzNzYzNzE3Mg==&mid=2247484403&idx=1&sn=d72deaa6b4bb3f3db45bc7c5a00ee098&chksm=c28d27a8f5faaebed237fbffaf7c87dfa7c53dfd854c4ebbd20595f21d911501ed5c539d72f0#rd
> 分类：SEO
> 作者：droidHZ 赫兹（@hezhiyan7）

---

早上好，朋友们！今天分享youtube字幕提取，制作高高质量的内页。我们都知道youtube上面有很多高质量的内容，要是能够直接在第一时间用上这些高质量的内容再我们的网页上，还是能够带来搜索流量的。

分享一个chrome 插件

https://chromewebstore.google.com/detail/youtube-transcript/jgibaoklabopileepldnlkbbcibhbgmd

使用这个插件，可以在看youtube 的时候，右侧直接把所有字幕提取出来了。

[图] 

除了这个插件，还有对应的API，你可以直接代码集成

https://github.com/jdepoix/youtube-transcript-api

想要实现其实很简单，你就告诉cc：“视频链接xxx  帮我把这个视频的详细文稿整理出来，需要安装什么工具或者插件你自己搞。”

这个时候，可能要问这个对我网站有什么作用呢？

其实你可以考虑把这个youtube的视频放到你的网页上面，把提取的文案当做网页的内容，毕竟这个是博主写的属于优质内容。

比如这个秋芝的sora 2讲解，只有你放到你的网站上足够快，也算是一手优质内容。视频配合文案的展示，也能够提示用户观看视频的体验，同时增加你网站的收录，在你网站上观看视频也能增加停留时长。

我是赫兹，一个专注「网站出海」的生意人，这是我探索网站出海的第174天，每天都会分享网站出海的相关知识。 想了解网站出海的朋友，可以去看看我之前的文章合集。

网站出海每日分享

网站出海深度总结

 
 var first_sceen__time = (+new Date());
 if ("" == 1 && document.getElementById('js_content')) {
 document.getElementById('js_content').addEventListener("selectstart",function(e){ e.preventDefault(); });
 }
