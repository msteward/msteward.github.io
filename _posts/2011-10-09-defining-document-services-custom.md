---
layout: post
title: Defining Document Services Custom Components (DSCs)
date: '2011-10-09T13:47:00.000-07:00'
author: Michael Steward
tags:
- Adobe Digital Enterprise Platform
modified_time: '2012-03-03T11:38:26.029-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-1628501581578081446
blogger_orig_url: http://www.michaelsteward.com/2011/10/defining-document-services-custom.html
--- 

I've written a few custom components in my time working with ADEP but recently came across an excellent summary of what exactly these little (or in some cases large!) pieces of code actually are.  A [recent blog post](http://blogs.adobe.com/ADEP/2011/10/prerelease-next-week-easily-connect-from-document-services-to-the-content-repository-in-experience-services.html) on the Adobe ADEP blog summarised it nicely:  

![Plugs](http://michaeljsteward.files.wordpress.com/2011/10/1193276_60947540.jpg?w=150 "Plugs") 

> A DSC is a component that can be installed on a Documents Server and introduces new functionality. It stands for Document Service Component. Most product components are DSCs but customers can write their own DSCs to create new integrations or functionality that require a higher level of sophistication than is appropriate with the use of standard integration options (e.g SOAP) or scripting/process maps. They are basically POJOs with nifty enterprise configurations around them that allow enterprise class life cycle, versioning and configuration (e.g. in an enterprise BPM system you don’t necessarily want a new version of a component to alter the way an inflight process is operating, or how a completed process reports audit data…) or even have to bounce the server to change the implementation of the DSC. It is definitely part of the secrete sauce of LiveCycle/ADEP Document Services.

[Source: ADEP Blog](http://blogs.adobe.com/ADEP/2011/10/prerelease-next-week-easily-connect-from-document-services-to-the-content-repository-in-experience-services.html "Adobe ADEP Blog")
