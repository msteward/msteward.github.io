---
layout: post
title: WebLogic LiveCycle ES3 Installation
date: '2012-09-20T09:50:00.002-07:00'
author: Michael Steward
tags: 
modified_time: '2012-09-20T09:50:35.782-07:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-6679050090594292713
blogger_orig_url: http://www.michaelsteward.com/2012/09/weblogic-livecycle-es3-installation.html
comments: true
---

On a recent installation of LiveCycle ES3 on WebLogic I realized that I had started creating a list of "extras" which I often needed to do before the installation would work properly.  These might not always be required and may in fact be buried in the documentation somewhere but here's the list regardless:  

*   Setting up the servers (both Admin and Managed Server) as Windows Services.  Not strictly a LiveCycle step but useful nonetheless.  Just don't forget to copy the lines you added to "startManagedServer.cmd" into your new service. 

*   [Setting Up Oracle servers as Windows Services](http://docs.oracle.com/cd/E13222_01/wls/docs81b/adminguide/winservice.html)

*   Adding the SQL driver to the classpath.  When using SQL Server we need the sqljdbc4 JAR file in the CLASSPATH.  Unfortunately the text LiveCycle gives you during the installation to copy into your startup script doesn't include this.  Again this might be the way we had configured WebLogic but I needed to add the path onto the end of the CLASSPATH supplied in order to get us talking to the database (we had setup the data source manually in WebLogic rather than bundling it into the LiveCycle EAR files.  

I'll keep adding to this as and when I come across other configurations.
