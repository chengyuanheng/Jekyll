---
layout: post
title:  "google “DNS污染系统”攻击后无法访问google解决方法"
date:   2014-11-21 10:52:47
categories: jekyll update
---


1.下面的这些ip可以直接复制到浏览器上访问，但是只能使用google的搜索功能。

   64.233.167.165

   64.233.167.164

   64.233.167.163

   64.233.167.166

   173.194.72.31

   91.213.30.150

2.这些dns在hosts文件里面改了之后也很卡，可以正常访问google的地图、邮件、登录等

  173.194.72.31 www.google.com.hk

  173.194.72.31 accounts.google.com

  173.194.72.31 plus.google.com

  173.194.72.31 mail.google.com

  173.194.72.31 maps.google.com

  173.194.72.31 play.google.com

3.使用代理搜索网站

  http://www.opengg.cn/

  http://www.gfsoso.com/

这两个网站都可以代替google，搜索结果和google是一样的