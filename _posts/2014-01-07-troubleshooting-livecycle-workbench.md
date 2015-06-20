---
layout: post
title: Troubleshooting LiveCycle Workbench Compatibility errors
date: '2014-01-07T11:08:00.000-08:00'
author: Michael Steward
tags:
- Adobe
- LiveCycle
modified_time: '2014-01-07T11:08:07.394-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-3675398668333329536
blogger_orig_url: http://www.michaelsteward.com/2014/01/troubleshooting-livecycle-workbench.html
---

I've come across a problem a few times using Workbench when trying to connect to servers only to be told I can't because there is a version number mismatch (even though both Workbench and the server are at the same service pack level).  One way around this temporarily (if you know the versions are the same but for some reason the server version is being reported incorrectly) is to disable the compatibility check in Workbench:

1.  Open your workbench.ini file (usually located in C:\Users\<user_name>\Apps\Adobe LiveCycle Workbench ES3\workbench
2.  Locate the line "-Dcom.adobe.connection.compatibilitycheck.disable=false
3.  Change the value to "true"
4.  Open Workbench and try to connect to the server again
