---
layout: post
title:  "what do rake spec do"
date:   2014-11-21 12:20:04
categories: jekyll update
---

### spec是ruby的dsl,为ruby on rails框架提供单元测试功能,但是spec在运行过程中都做了哪些事情呢?下面我们来一起看一下: ###

when run rake spec --trace, you can see something like this:

{% highlight ruby %}
** Invoke spec (first_time)
** Invoke db:test:prepare (first_time)
** Invoke db:abort_if_pending_migrations (first_time)
** Invoke environment (first_time)
** Execute environment
** Execute db:abort_if_pending_migrations
** Execute db:test:prepare
** Invoke db:test:load (first_time)
** Invoke db:test:purge (first_time)
** Invoke environment
** Execute db:test:purge
** Execute db:test:load
** Invoke db:schema:load (first_time)
** Invoke environment
** Execute db:schema:load
** Execute spec
{% endhighlight %}

- Don’t run the specs if there are pending migrations in the development database. (db:abort_if_pending_migrations)

- Drop the test database (db:test:purge)

- Load the schema into the test database (db:schema:load in environment “test”)
