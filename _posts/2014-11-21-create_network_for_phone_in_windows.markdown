---
layout: post
title:  "win7下给手机建立共享网络"
date:   2014-11-21 12:17:50
categories: jekyll update
---

- 以管理员身份运行cmd（只要保证有权限即可，不知道cmd是什么的童鞋，请直接跳到第五步。）

- 在cmd中输入下面的命令：netsh wlan set hostednetwork mode=allow ssid=cc  key=123456 （其中ssid为建立的网络名称 key为密码）

- 打开网络共享中心 更改适配器 有一个“无线网络连接2”的网络连接，这是win7自带的虚拟WIFI网卡 我们要做的就是把正在连接着的网络共享给“无线网络连接2” 方法就是右键共享之类的了，图就不上了，表在心里骂作者好不啦。。。。

- 在cmd中输入：netsh wlan start hostednetwork  这句话是要启动承载网络，然后你的手机就可以搜到这个名叫cc的网络了，输入密码就可以连接上网了。

- 如果没有成功，请各位再去找其他的教程吧。毕竟电脑与电脑不一样，手机与手机也不一样额。博主的手机小米2s是可以了，博主很高兴。