---
layout: post
title:  " how to generate a task in ruby on rails"
date:   2014-11-21 12:15:31
categories: jekyll update
---

- ruby on rails 生成task的方法：

{% highlight ruby %}
$ rails g task task_namespace task_name1 task_name2

$ create lib/tasks/task_namespace.rake
{% endhighlight %}

- task文件里面：

{% highlight ruby %}
namespace :task_namespace do
  desc "this is describe"
    task :task_name1 => :environment do
  end

  desc "this is also describe"
    task :task_name2 => :environment do
  end
end
{% endhighlight %}

- 使用 rake -T 查看所有task

{% highlight ruby %}
rake task_namespace:task_name1    # this is describe

rake task_namespace:task_name2    # this is also describe
{% endhighlight %}