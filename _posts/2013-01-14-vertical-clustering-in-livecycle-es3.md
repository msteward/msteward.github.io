---
layout: post
title: Vertical clustering in LiveCycle ES3
date: '2013-01-14T08:51:00.004-08:00'
author: Michael Steward
tags: 
modified_time: '2013-01-14T08:51:54.877-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-3705175069051573888
blogger_orig_url: http://www.michaelsteward.com/2013/01/vertical-clustering-in-livecycle-es3.html
comments: true
---

Quick note for future reference: the document for ES2 (http://help.adobe.com/en_US/livecycle/9.0/clustering_jboss.pdf) explains how to change the necessary ports in order to get a vertical JBoss cluster up and running.  In ES3 (and therefore JBoss 5) the paths for a number of the ports has changed:  

**JBoss 4:**  
jboss-service.xml file located in [appserver root]\server\[profile]\conf  

**JBoss 5:**  
bindings-jboss-beans.xml file located in [appserver root]\server\[profile]\conf\bindingservice.beans\META-INF
