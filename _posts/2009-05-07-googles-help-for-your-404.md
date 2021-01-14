---
title: "Google's Help for your 404"
layout: post
excerpt: "Google has your back when creating a better 404 Error page"
categories: blog
tags: [404, error, google]

---

So you're already ahead of the game by having a good <a rel="nofollow" target="_blank" href="http://www.alistapart.com/articles/perfect404/">404</a> <a rel="nofollow" target="_blank" href="http://www.google.com/support/webmasters/bin/answer.py?answer=93641&#038;hl=en">page</a>, right? Good, now you can even add a bit more spice to them.

While on Google's Webmaster Tools page, I noticed this little gem:  
{% highlight javascript %}
<script type="text/javascript"><br />
  var GOOG_FIXURL_LANG = 'en';<br />
  var GOOG_FIXURL_SITE = 'http://www.mydomain.com';<br />
</script><br />
<script type="text/javascript" src="http://linkhelp.clients.google.com/tbproxy/lh/wm/fixurl.js"></script>
{% endhighlight %}

Since users need to find what they're looking for within 7 seconds to avoid them leaving your site, use this little guy to help out. It will make it easier for them to find the information they are looking for.

So, you're probably wondering, "What does that do to help me?" Good question, here's a rundown of what Google says:

- It adds a search box for your site with appropriate search suggestions.
- It tries to provide alternatives to incorrect URLs.

If you really want to tweak how this gadget looks, <a rel="nofollow" target="_blank" href="http://www.google.com/support/webmasters/bin/answer.py?answer=100044&#038;hl=en">Google's provided</a> custom classes that its script uses to give you full customization.
