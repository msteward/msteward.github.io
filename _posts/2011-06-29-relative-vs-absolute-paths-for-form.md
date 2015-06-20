---
layout: post
title: Relative vs Absolute paths for Form fragments
date: '2011-06-29T03:25:00.000-07:00'
author: Michael Steward
tags:
- Adobe Forms
modified_time: '2012-03-03T11:38:26.103-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-5501983904441497584
blogger_orig_url: http://www.michaelsteward.com/2011/06/relative-vs-absolute-paths-for-form.html
---

Here's another gotcha when using LiveCycle Output ES2 that's had me stumped for a few hours.  I designed a form which used a number of fragments which tested fine within designer.  Once deployed to the server I was always getting blank forms.  A quick check of the logs revealed the following warning:  

> ALC-OUT-002-058: Cannot retrieve the resource from Repository Path.

A bit of digging around and I hit the a [knowledge base article on Adobe's site](http://kb2.adobe.com/cps/521/cpsid_52158.html).  Basically there's a "limitation" with the way the form is compiled which means relative paths within fragments and XDPs can cause problems.  The solution is to turn the relative path references (which are inserted by default in Designer) into absolute paths.  Doing this sorted the problem for me but this is something that needs fixing!