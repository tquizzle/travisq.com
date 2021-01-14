---
layout: post
title: "Add Spacers to your OSX Dock"
modified: 2015-11-23
categories: blog
excerpt: "Using the terminal, you can quickly add a spacer to your OSX dock."
tags: [OSX, Mac, spacers, dock]

---

Have you ever felt like putting a spacer in your OSX dock? I certainly have, and wanted to but never took the time to figure it out. Today I stumbled across [a post that explains it perfectly](https://awesometoast.com/add-spacers-to-your-macs-dock/).

![Dock with spacers](https://awesometoast.com/wp-content/uploads/2011/08/CapturFiles.png)

You have to get into the terminal to do this, but never fear, it's your friend.

{% highlight bash %}
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="spacer-tile";}'
{% endhighlight %}

Then you'll have to kill the Dock and it will relaunch.

{% highlight bash %}
killall Dock
{% endhighlight %}

Now just move that sucker around wherever you'd like it to go.
