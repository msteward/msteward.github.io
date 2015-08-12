---
layout: post
title: Connecting to LiveCycle ES2 Repository outside of Workbench
date: '2011-06-12T12:57:00.000-07:00'
author: Michael Steward
tags:
- Adobe Digital Enterprise Platform
modified_time: '2012-03-03T11:38:26.100-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-5318131148246069803
blogger_orig_url: http://www.michaelsteward.com/2011/06/connecting-to-livecycle-es2-repository.html
---

When trying to test some forms I was struggling to remember the location of the LiveCycle repository.  Turns out that you can access it via WebDav from Windows or directly from a browser using the following:  

{% highlight js %}
http://<server_name>:<port>/repository    
{% endhighlight %}

Login with your usual username and password and you'll be able to browse the repository hierarchy.
