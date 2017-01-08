---
layout:		post
title:			"Jekyll搭建Blog的总结(1)"
subtitle:		"Why is Jekyll"
date:			2017-1-5 22:00:00
author:		"Parsifal"
header-img:	"img/postresources/using-jekyll.jpg"
catalog:     true
tags:
- 我的博客 
- Web前端
- Jekyll 
- Github Pages 
- 总结与教程
---

## 扯扯闲话
  于此时，博客大体是完成了，感谢[黄玄的开源模板](https://github.com/Huxpro/huxpro.github.io)。从自己从零搭建，到最后选择喜欢的模板搭建，前后走了些弯路，零零散散花了些时间，不过总算能重新有个地方记录自己的一些想法与琐碎。其实，刚毕业那会儿就有过一个，凭着愣头青的充沛精力，更新频率一直挺稳定。但不到两年就逐渐懈怠了，久而久之也就没了写东西的习惯。2017年，希望重新养成学习与记录这个好习惯。
 
## 为什么写这个系列
  不知道其他人有没有这种感觉：在和别人解释你新掌握的技能时，你总会再次发现自己知识的遗漏和模糊之处。有些老师傅在教徒弟的过程中，会喜欢让徒弟来反过来教自己，其实是同一个道理。而这也是现在我写这个系列日志的初衷。希望能够在讲述的过程中，再次巩固一遍Jekyll建站的相关知识。PS:这个系列**非详细教程贴**（Jekyll官方文档已足够完善，而且网上的手把手教程也很多），且本人水平也有限，陈述过程中难免会有遗漏有误之处，若有缘看到这篇文章，多多包涵。欢迎留言交流。
## 什么是Jekyll
Jekyll（音标ˈdʒɪ:kɪl）是一个简单方便的静态网站生成器，它通过标记语言[Markdown](https://zh.wikipedia.org/wiki/Markdown) 或[Textile](https://zh.wikipedia.org/wiki/Textile)和模板引擎[Liquid](https://zh.wikipedia.org/wiki/Liquid)将纯文本转换生成HTML网页。虽然只是静态网站，但Jekyll对于评论、标签等功能都有很好的方案。如果你喜欢混迹全球最著名的[同性交友网站](https://github.com)，应该对它不陌生。因为[Github Pages](https://pages.github.com/)就是使用的Jekyll作为引擎.
> *简单* --- 不再需要数据库，不需要开发评论功能，不需要不断的更新版本--只用关心你的博客内容。  
>   				
> *静态* --- Markdown（或 Textile）、Liquid 和 HTML & CSS 构建可发布的静态网站。    
> 
> *博客支持* --- 支持自定义地址、博客分类、页面、文章以及自定义的布局设计。  

这是Jekyll官网（[中文](http://jekyllcn.com/)|[English](https://jekyllrb.com/)）给自己打出的标签，但它最诱惑程序员的是来自于Github Pages——选择了将网站部署在Github Pages上，就相当于拥有了稳定安全足够（[1GB](https://help.github.com/articles/what-is-my-disk-quota/)）的免费空间，且依托于Git管理，十分方便。对于非前端工程师，Jekyll可以让Blogger把精力专注于写的同时可以收获属于自己个性的独立博客站点。（当然，如果只是写博客而言，诸如LOFTER、简书等这些平台提供的博客功能也是极好的。）由于GithubPages的存在，使用Jekyll做自己的博客就变得更简单轻松。
## 如何最快速地上手Jekyll
通过Github Pages你能迅速拥有一个以Jekyll为引擎的独立博客。现在使用Jekyll的博客站点已经很多了，有些很不错的主题也都是开源的。对于熟悉Github的同学来说，简单使用Jekyll搭建Github Pages博客的方法有两种：

###### 1. 自己新建Repo
在自己的Github上新建一个Repo，名为"***your_username.github.io***"（[比如我的这样](https://github.com/ParsifalC/parsifalc.github.io)），然后进入***setting***页面，GithubPages页面会有个***Choose a theme***，点击它之后会跳往一个主题选择页面，选择好主题后，commit&push改动，Github就会帮你自动生成一个你的Github Pages了。
 ![GithubPagesSettings_1](http://ojg3xdx9d.bkt.clouddn.com//1483859445.png)

###### 2. 从已有的Repo fork
Github上面有个简单的官方模板[Jekyll-Repo](https://github.com/jekyll/jekyll)(当然这里也可以是其他优秀的开源repo)。如果偷懒的话，fork过来，进入Settings修改Repo name为"***your_username.github.io***"，就可以直接生成自己的Github Pages。
![GithubPagesSettings_2](http://ojg3xdx9d.bkt.clouddn.com//1483858856.png)

接着只要改改对应的title等信息，就可以往_posts文件夹里扔指定格式的post提交发布了。往后像维护其他Repo一样维护这个Repo就可以。再多啰嗦几句提醒：		

1. Repo name必须是“**your_username.github.io**”这种格式的，且为username而非nickname；  
2. 生成后可能会有一小段时间的配置，遇到404后稍等再刷新即可；   
3. 需要掌握**Markdown**语法与**Github的基本流程**；

上面提到的这两种方法都可以迅速地搭建起自己的Github Pages。同时Jekyll的定制性也是非常高的。如果对于博客的个性化要求比较高，建议配置Jekyll的本地环境，官网教程非常详细，且配有（[中文](http://jekyllcn.com/)|[English](https://jekyllrb.com/)）双版本（中文版本是由国内热心网友自发翻译的）。配置好Jekyll的本地环境后，会同时集成了一个开发用的服务器，可以使用浏览器在本地进行实时预览与调整，十分便利。	
## Jekyll的相关资源   
以下是我整理的一些网友资源，从中我也获益匪浅，有些教程相对从零开始的朋友也会更友好一些。感叹一句，啊，万能的Google：

- **Wiki上面的优秀开源博客模板**，懒虫们可以上去选妃啦，fork后就可以使用，建议保留开发者的博客链接：    
[Link to Jekyll-powered blogs and other sites here.](https://github.com/jekyll/jekyll/wiki/sites)   
- **YouTube上面的系列视频教程**：	      
[Installing Jekyll on a Mac through the Terminal.
](https://www.youtube.com/playlist?list=PLWjCJDeWfDdfVEcLGAfdJn_HXyM4Y7_k-)   
- **几篇手把手教学的文章**：    
[每个人都应该有一个Jekyll博客(这是一个设计师写的哦)](http://www.jianshu.com/p/ca8dba93ebd5)    
[Github Pages + Jekyll 独立博客一小时快速搭建&上线指南](http://playingfingers.com/2016/03/26/build-a-blog/)    
[如何搭建一个独立博客——简明 Github Pages与 jekyll 教程](http://www.cnfeat.com/blog/2014/05/10/how-to-build-a-blog/)    
[Jekyll-now](https://github.com/barryclark/jekyll-now)    
[使用Github建独立博客](https://beiyuu.com/github-pages)       

- **知乎上的答案**（其实是博客炫耀帖😝）:    
 [如何在 GitHub 上写博客？
](https://www.zhihu.com/question/20962496)||[有哪些简洁明快的 Jekyll 模板？
](https://www.zhihu.com/question/20223939)||[github上利用jekyll搭建自己的blog的操作顺序？
](https://www.zhihu.com/question/30018945)    
- **一些Jekyll主题资源的网站**：    
[jekyllthemes](http://jekyllthemes.org/)    
[有收费的主题，慎选](https://jekyllthemes.io/)    
[themes](http://themes.jekyllrc.org/)    
[几个好看的主题](http://www.zhanxin.info/themes.html)    
[beautiful-jekyll](https://github.com/daattali/beautiful-jekyll)


