---
layout: post
title:  "Quickly switch directory in terminal"
date:   2019-01-05 00:10:57 +0530
categories: [mac, ubuntu, terminal]
---

Here's a quick hack to quickly switch directory in terminal. It comes in handy when I am simultaneously working on multiple projects.

# Before

{% highlight bash %}

$ cd ~/arena/iw/projects/teachmore/TeachMoreWeb
$ .
$ . Do something awesome for the first project!
$ .
$ cd ~/arena/eec/projects/eecglobal/EecGlobalWeb
$ .
$ . Do something awesome for the second project!
$ .
$ cd ~/arena/iw/projects/teachmore/TeachMoreAndroid

{% endhighlight %}

# After

{% highlight bash %}

$ gototmw
$ .
$ . Do something awesome for the first project!
$ .
$ gotoeecw
$ .
$ . Do something awesome for the second project!
$ .
$ gototma

{% endhighlight %}

# How to do this?

We use [Aliases](https://www.gnu.org/software/bash/manual/html_node/Aliases.html) to do this. We are basically creating shortcuts for above commands using Aliases. It saves us a lot of keystrokes.

{% highlight bash %}

# Put below lines in ~/.bash_profile (For Mac) or ~/.bashrc (For Ubuntu)
alias gototmw="cd ~/arena/iw/projects/teachmore/TeachMoreWeb"
alias gotoeecw="cd ~/arena/eec/projects/eecglobal/EecGlobalWeb"
alias gototma="cd ~/arena/iw/projects/teachmore/TeachMoreAndroid"

{% endhighlight %}

# That's it. Set your keyboards on fire 🔥

<iframe src="https://giphy.com/embed/fQZX2aoRC1Tqw" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/fQZX2aoRC1Tqw">via GIPHY</a></p>