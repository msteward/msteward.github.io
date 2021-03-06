---
layout: post
title: Pesky setters
date: '2010-12-21T03:22:00.000-08:00'
author: Michael Steward
tags:
- Adobe Flex
modified_time: '2012-03-03T11:35:30.267-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-3594410743523255251
blogger_orig_url: http://www.michaelsteward.com/2010/12/pesky-setters.html
---

Having moved to using getters and setters to access properties of my data model (I need to perform some validation on the set and apply some logic if the conditions aren't met) I came across a "feature" of setters which is designed to stop code executing unnecessarily.  There are many instances when I am trying to set the value of a property to what it's currently set to (but this time the validation may deem it an invalid value).  After a lot of head scratching I finally found that when trying to do this the setter is never called.  Flex first calls the getter of the property and if the value is the same as the one you're trying to set it will bypass the call to the setter in an effort to increase efficiency.  If this is not desired (in my case) then the following forces the setter to be called regardless:  

{% highlight js %} 
 public function set someVariable(val:int):void {  
 if (condition) {  
 //some logic to alter val  
 }  
 else {  
 //some logic to alter val  
 }  
 _someVariable = val;  
 dispatchEvent(new Event("someVariableUpdated"));  
 }  

[Bindable(event="someVariableUpdated")]  
 public function get speedOptionsArray():int {  
 return _someVariable;  
 }  
{% endhighlight %} 