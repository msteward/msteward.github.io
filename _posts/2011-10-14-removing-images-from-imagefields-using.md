---
layout: post
title: Removing images from ImageFields using JavaScript
date: '2011-10-14T07:02:00.000-07:00'
author: Michael Steward
tags:
- Adobe Forms
modified_time: '2012-05-12T17:35:16.584-07:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-6948352026616805710
blogger_orig_url: http://www.michaelsteward.com/2011/10/removing-images-from-imagefields-using.html
comments: true
---

When adding an ImageField to a form it's a common requirement to allow a user to remove the image.  By default clicking on the image field will only let the user replace it with another image.  If you want to remove it altogether then this little piece of code attached to a button will help:  

{% highlight js %}
imageField.rawValue = null;  
{% endhighlight %}
