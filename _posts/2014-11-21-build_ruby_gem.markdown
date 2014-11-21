---
layout: post
title:  "how to build a ruby gem"
date:   2014-11-21 11:22:20
categories: jekyll update
---


-  first you will create a user in rubygem.org (https://rubygems.org/)

-  create the directory structure like this:

{% highlight ruby %}
$ tree .
    ├── cc_hola.gemspec
    └── lib
        └── cc_hola.rb
{% endhighlight %}

you can use any name but you must keep consistency

-  in your .gemspec file

{% highlight ruby %}
Gem::Specification.new do |s|
    s.name        = 'CcHola'
    s.version     = '0.0.0'
    s.date        = '2014-10-20'
    s.summary     = "A ruby gem build test!"
    s.description = "A ruby gem build test!"
    s.authors     = ["cckkll"]
    s.email       = '237178842@qq.com'
    s.files       = ["lib/cc_hola.rb"]
    s.homepage    = 'https://github.com/chengyuanheng'
end
{% endhighlight %}

- in your .rb file

{% highlight ruby %}
class CcHola
  def self.hi
    puts "Hello World!"
  end
end
{% endhighlight %}

- compiled gem

{% highlight ruby %}
$ gem build cc_hola.gemspec
    Successfully built RubyGem
    Name: CcHola
    Version: 0.0.0
    File: CcHola-0.0.0.gem

$ gem install ccHola-0.0.0.gem
    Successfully installed CcHola-0.0.0
    <span>1 gem installed</span>
{% endhighlight %}

- test your gem

{% highlight ruby %}
$ irb
    > require "cc_hola"
    => true
    > CcHola.hi
    Hello World!
    => nil
{% endhighlight %}

- release your gem

{% highlight ruby %}
$ curl -u cckkll https://rubygems.org/api/v1/api_key.yaml >~/.gem/credentials
    Enter host password for user 'cckkll':

$ gem push CcHola-0.0.0.gem
    Pushing gem to https://rubygems.org...
    Successfully registered gem: CcHola (0.0.0)
{% endhighlight %}

- you will find it in your rubygems account and all people can use it by

{% highlight ruby %}
    gem 'CcHola', '~> 0.0.0'
{% endhighlight %}