---
layout: post
title: Applying focus to Flex application on startup
date: '2011-03-10T03:18:00.000-08:00'
author: Michael Steward
tags:
- Adobe Flex
modified_time: '2012-03-03T11:38:26.124-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-7415086115204924971
blogger_orig_url: http://www.michaelsteward.com/2011/03/applying-focus-to-flex-application-on.html
---

On a recent project we carried out some accessibility testing and one of the problems faced was with keyboard users who couldn't use a mouse. After loading the application (by typing in the URL in the address bar) the users couldn't tab to the input fields on the application, focus would never reach the flex app at all. After searching around I eventually found a little code snippet in a comment on [Flex Examples](http://blog.flexexamples.com/2008/09/23/setting-focus-in-flex-using-the-focus-manager/).  

 {% highlight js %}
 private function setApplicationFocus():void { 
   navigateToURL(new URLRequest("javascript: document.getElementById(<dom_id>).focus();"), "_self"); 
   focusManager.setFocus(); 
 } 
 {% endhighlight %} 

 The above is called in the Application object on creationComplete.