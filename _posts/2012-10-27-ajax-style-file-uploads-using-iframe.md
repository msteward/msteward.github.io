---
layout: post
title: AJAX Style file uploads using an iFrame
date: '2012-10-27T15:09:00.003-07:00'
author: Michael Steward
tags: 
modified_time: '2012-10-27T15:36:53.232-07:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-1140157534990877809
blogger_orig_url: http://www.michaelsteward.com/2012/10/ajax-style-file-uploads-using-iframe.html
comments: true
---

I was recently trying to solve a strange issue with Internet Explorer 8 (it's always IE...) on redirecting the user after successfully uploading a file.  Couldn't use HTML5's FileUpload API as we had to be able to support older browsers but what we wanted was AJAX style in place uploads without having to redirect users back to the page after they had uploaded a file.  

Then I came across the following blog post:  
[http://www.alfajango.com/blog/ajax-file-uploads-with-the-iframe-method/](http://www.alfajango.com/blog/ajax-file-uploads-with-the-iframe-method/)  

This method feels like a bit of a hack but is a decent solution to the problem.  Target the empty iFrame and you can keep users on the same page.  It seems to be a popular method and one I'll use again until we can finally move to using the proper HTML5 API for doing this.
