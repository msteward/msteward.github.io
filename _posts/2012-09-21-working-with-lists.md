---
layout: post
title: Working with lists
date: '2012-09-21T10:03:00.002-07:00'
author: Michael Steward
tags: 
modified_time: '2012-09-29T09:10:08.028-07:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-4538927013763621439
blogger_orig_url: http://www.michaelsteward.com/2012/09/working-with-lists.html
comments: true
---

This is more a note to remind me in future but when dealing with lists in LiveCycle it can sometimes be a little tricky to just keep adding to a list without creating a loop.  An easy way to do this within one set value step is to use the collection size to determine the index for adding something to the list.   

Here's an example XPath statement which will add to the end of the list (where "listAttachments" is your list variable):  

{% highlight js %}
/process_data/listAttachments[number(get-collection-size(/process_data/listAttachments)+1)]  
{% endhighlight %}
