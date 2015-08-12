---
layout: post
title: Setting up WebLogic as a Windows Service
date: '2013-04-03T12:40:00.002-07:00'
author: Michael Steward
tags:
- WebLogic
- LiveCycle
- Oracle
- Application Server
modified_time: '2013-04-03T12:40:37.885-07:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-3070786355487607896
blogger_orig_url: http://www.michaelsteward.com/2013/04/setting-up-weblogic-as-windows-service.html
comments: true
---

A common requirement when dealing with any application server install on Windows is to set it up as a Windows service.  It's a bad idea to rely on the command line for running the server as it makes it far harder to administer.   

For WebLogic the steps to do this are available on Oracle's website:  
[http://docs.oracle.com/cd/E11035_01/wls100/server_start/winservice.html](http://docs.oracle.com/cd/E11035_01/wls100/server_start/winservice.html)  

A useful diagnostic if the service doesn't appear to be working is to try and invoke the service using the beasvc command.  See the section "Verifying the Setup" in the above link for more information.  More times than not if your service isn't starting then there was an error in the script you used to create the service in the first place (e.g. JVM argument).
