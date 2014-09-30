---
layout: post
title: "迁移到了Octopress"
date: 2013-11-23 22:59:02 -0500
comments: true
categories: Blog, Octopress
---
之前一直在不同的地方写博客，最开始没有什么技术，就只托管到了一些博客网站，从国内的点点到国外的Weebly，一直觉得用的很不爽，总觉得一直用博客网站的模板不自由（虽然可以自己改写css),不能体现自己独（zhuang）特(bi)的个性. 后来还想过使用Wordpress，但是还是觉得wp实在是太老的技术了，作为一个新时代的Coder，怎么还能用十年前的技术呢.于是在这个周六的早上，睡到了十二点然后就决定起来把博客迁移到Octopress.

<!--more-->

 {% img /images/blog_image/octopress.jpg %}
 
 Octopress号称A blogging framework for hackers，自然少不了折腾。官方介绍是基于Jekyll的静态博客生成系统，原理是自己在本地搭建一个博客目录经过Markdown和Liquid转换，在本地生成静态页面，再通过Git部署到Github上. 由于Github可以让用户自己生成Page，这样连买主机的钱都省了，只需要买个域名就可以搭建自己的独立博客了。
 
 简单说下这次的建站感受，由于之前玩过Ruby,所以很简单的在bash里面就可以直接安装文档装Gem了，按照官方文档走一遍程序基本上一两个小时就可以搭好所需要的一切环境。接下来写文章就容易了，```rake new_post["title"]```就在本地生成一个Markdown文件，然后自己修改Markdown文件就可以写好日志，接着```rake generate```就可以在本地把Markdown文件转换成静态Jekyll网页，```rake preview```可以在本地<http://localhost:4000/>预览生成的页面，觉得不错就可以发布到服务器了，```rake deploy```.
 
 当然，要是建网站这么简单，怎么会叫A blogging framework for hackers呢，就算按照官方程序走一遍都会遇到一些小问题，下篇文章就来说说怎么解决这些问题的。
 
 最后推荐一个Markdown编辑器，[Mou](http://mouapp.com/)，国内一个独立开发者写的，用过的都说好。