---
layout: post
title:  "Updating default version for Bundler"
date:   2020-05-04 15:31:00 +0530
categories: [mac, bundler, ruby]
---

You might get below error if you have multiple versions of bundler installed and the default one is not the one required in your project.

# The Problem

{% highlight bash %}

Warning: the running version of Bundler (2.1.2) is older than the version that created the lockfile (2.1.4). We suggest you to upgrade to the version that created the lockfile by running `gem install bundler:2.1.4`.
  
{% endhighlight %} 

# The Fix

{% highlight bash %}

$ gem uninstall bundler
$ gem install bundler --default
$ gem list bundler
> bundler (default: 2.1.2, default: 2.1.4)
$ rm versions/2.7.0/lib/ruby/gems/2.7.0/specifications/default/bundler-2.1.2.gemspec

{% endhighlight %} 
