---
layout: post
title: Using PopUpManager.addPopUp from ActionScript classes
date: '2010-08-25T09:50:00.000-07:00'
author: Michael Steward
tags:
- Adobe Flex
modified_time: '2012-03-03T11:35:30.169-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-5568235292246099885
blogger_orig_url: http://www.michaelsteward.com/2010/08/using-popupmanageraddpopup-from.html
---

A fairly typical use case I frequently run into is the need to display some form of TitleWindow using the PopUpManager class (usually when a simple Alert won't do the job).  This is simple when addPopUp is invoked from within a view (MXML):  
 
`PopUpManager.addPopUp(titleWindow, this);`   

The keyword **_this_** is fine when calling from within an view as it refers to the current DisplayObject.  When calling from a pure ActionScript class however this won't work as "this" refers to the class and not a Display Object.  

Instead, to get a reference to the root application (which is normally good enough if you just want to display a simple popup) use the following:  

`PopUpManager.addPopUp(titleWindow, Application.application.getChildAt(0));`

This will add the popup to the root display object contained within the Application.