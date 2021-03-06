---
layout: post
title: Debugging Flex 3 applications with Flash Player 10
date: '2011-04-07T03:46:00.000-07:00'
author: Michael Steward
tags:
- Adobe Flex
modified_time: '2012-03-03T11:38:26.152-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-936078293761182366
blogger_orig_url: http://www.michaelsteward.com/2011/04/debugging-flex-3-applications-with.html
---

I came across a problem recently when trying to debug my application after upgrading from Flash Player 9 (Debug version) to 10.2 (Debug version).  As soon as I upgraded my application stopped logging.  I searched everywhere and whilst I found a lot of people with the same problem never really found an answer.  

After a lot of digging it appears to be the way you target the flash player version.  My application was targetting Flash Player 9 (in my flex-config.xml):  

{% highlight xml %}
<target-player>9.0.124</target-player>
{% endhighlight %} 

Changing this to 10 started the trace logging again.  As I wanted to maintain the v9 target I've ended up reverting back to Flash Player 9 to get the logging working again.