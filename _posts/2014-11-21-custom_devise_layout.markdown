---
layout: post
title:  "custom layout for devise in ruby on rails"
date:   2014-11-21 11:34:38
categories: jekyll update
---

in your config/application.rb puts:

{% highlight ruby %}
config.to_prepare do
    Devise::SessionsController.layout      "application"
    Devise::RegistrationsController.layout "application"
    Devise::RegistrationsController.layout "application"
    Devise::ConfirmationsController.layout "application"
    Devise::UnlocksController.layout       "application"
    Devise::PasswordsController.layout     "application"
    Devise::InvitationsController.layout   "application"
end
{% endhighlight %}

you will custom layout for any controller of devise