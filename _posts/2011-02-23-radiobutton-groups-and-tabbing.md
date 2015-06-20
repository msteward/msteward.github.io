---
layout: post
title: RadioButton Groups and Tabbing
date: '2011-02-23T07:29:00.000-08:00'
author: Michael Steward
tags:
- Adobe Flex
modified_time: '2012-03-03T11:35:30.284-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-7230658612518625703
blogger_orig_url: http://www.michaelsteward.com/2011/02/radiobutton-groups-and-tabbing.html
---

Making your Flex application accessible can be challenging and one of the more recent quirks I've encountered is the use of radio button groups.  One particular application used a number of radio button groups in the same view.  The buttons were created using Repeaters which assigned each RadioButton a group property, binding it to one of the predefined RadioButtonGroups.  

This works great for mouse users but when it comes to keyboard input you'll notice that the tabbing order is thrown out the window.  This is because Flex uses the "groupName" property of radio buttons to calculate tabbing order.  If not specified (in my case) then all radio buttons are given the same default groupName and hence tabbing can break as they are all considered one entity.  The following simple example demonstrates the fix:  

{% highlight xml %} 
 <mx:RadioButtonGroup id="radioButtonGroup1"/>  
 <mx:RadioButtonGroup id="radioButtonGroup2"/>  

<mx:VBox>  
 <mx:RadioButton id="radioButton1"  
 label="My radio button"  
 group="{radioButtonGroup1}"  
 groupName="Group 1"/>  
 <mx:RadioButton id="radioButton2"  
 label="My radio button"  
 group="{radioButtonGroup1}"  
 groupName="Group 1"/>  
 </mx:VBox>  

<mx:VBox>  
 <mx:RadioButton id="radioButton3"  
 label="My radio button"  
 group="{radioButtonGroup2}"  
 groupName="Group 2"/>  
 <mx:RadioButton id="radioButton4"  
 label="My radio button"  
 group="{radioButtonGroup2}"  
 groupName="Group 2"/>  
 </mx:VBox>  
{% endhighlight %} 