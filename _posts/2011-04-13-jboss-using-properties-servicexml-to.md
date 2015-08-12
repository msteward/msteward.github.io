---
layout: post
title: JBoss - using properties-service.xml to set environment variables
date: '2011-04-13T06:01:00.000-07:00'
author: Michael Steward
tags:
- JBoss
modified_time: '2012-03-03T11:38:26.067-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-4361400992959587976
blogger_orig_url: http://www.michaelsteward.com/2011/04/jboss-using-properties-servicexml-to.html
---

In every JBoss installation there will be a file called "properties-service.xml" in the deploy folder.  This file allows you to setup environment variables (rather then setting them at the JVM/System level) which all deployed applications can then use by calling the System.getProperty() method.  Just uncomment the section shown below to enable some global properties or use the URLList to point to external properties files:  

{% highlight xml %}
 <!--  
 Set raw properties file style properties.  
 -->  
 <attribute name="Properties">  
 ATTRIBUTE_NAME_1=somevariable  
 ATTRIBUTE_NAME_1=anotherVariable  
 </attribute>  
{% endhighlight %}
