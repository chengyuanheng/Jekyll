---
layout: post
title:  "install django for windows"
date:   2014-11-21 11:38:21
categories: jekyll update
---

- download  python from  https://www.python.org/downloads/windows/

  download  django from  https://www.djangoproject.com/download/

- install python and configuration environment variable for example: add 'G:\python' to '计算机->属性->高级->环境变量'

- unzip Django to the directory of python

- come into the directory of python use dos, run "python setup.py install", django will be installed into the
  directory of  "lib/site-packages/"

- add 'G:\python\lib\site-packages\django' into environment variable

  add 'G:\python\Scripts' into environment variable

- check whether success : in the directory of G:\python in dos, run 'python', run 'import django',
  run ' django.get_version()',you will get the version of python and django

