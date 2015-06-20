---
layout: post
title: get-collection-size() vs size() in LiveCycle
date: '2011-04-06T02:42:00.000-07:00'
author: Michael Steward
tags:
- Adobe Digital Enterprise Platform
modified_time: '2012-03-03T11:38:26.108-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-5525532488176970126
blogger_orig_url: http://www.michaelsteward.com/2011/04/get-collection-size-vs-size-in.html
---

Just a note to be careful when using the XPath expressions get-collection-size() and size() in LiveCycle to count the number of elements in a list variable. If your list is empty the two functions will **not return the same value**  

Creating a test process to demonstrate this I added three variables:  

* lstTestList
* intCountList -> count(/process_data/lstTestList)
* intCollectSizeList -> get-collection-size(/process_data/lstTestList)

Running this process on an empty list gives the following output:  

* intCountList -> 1
* intCollectSizeList -> 0

So if trying to find out whether or not a list is empty use get-collection-size() and **not** count()