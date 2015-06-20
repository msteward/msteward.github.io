---
layout: post
title: Flex AutoScroll to component with focus
date: '2011-03-28T06:30:00.000-07:00'
author: Michael Steward
tags:
- Adobe Flex
modified_time: '2012-03-03T11:38:26.119-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-7220930513145139724
blogger_orig_url: http://www.michaelsteward.com/2011/03/flex-autoscroll-to-component-with-focus.html
---

Really useful library for ensuring that the active component (i.e. the one which has focus) is currently viewable: [Flex AutoScroll Library](http://www.darylb.net/flexautoscroll/)  

Particularly useful for users who can only use the keyboard. To setup I added an event listener to my main MXML component:  

{% highlight js %}  
this.addEventListener(FocusEvent.FOCUS_IN, AutoScroll.autoScroll);  
{% endhighlight %} 