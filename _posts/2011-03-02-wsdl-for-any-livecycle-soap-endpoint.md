---
layout: post
title: WSDL for any LiveCycle SOAP Endpoint
date: '2011-03-02T09:17:00.000-08:00'
author: Michael Steward
tags:
- Adobe Digital Enterprise Platform
modified_time: '2012-03-03T11:35:30.302-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-1126957360363769851
blogger_orig_url: http://www.michaelsteward.com/2011/03/wsdl-for-any-livecycle-soap-endpoint.html
---

Little tip but one that took me an age to find; if you want a WSDL for your LiveCycle workflow SOAP endpoint just use the following generic URL:  

`http://[server_name]/soap/services/[process_name]?wsdl`