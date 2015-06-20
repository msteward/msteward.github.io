---
layout: post
title: Acrobat Reader Extension limitations
date: '2011-09-26T02:53:00.000-07:00'
author: Michael Steward
tags:
- Adobe Digital Enterprise Platform
- Adobe Forms
modified_time: '2012-03-03T11:38:26.142-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-8426599331117247731
blogger_orig_url: http://www.michaelsteward.com/2011/09/acrobat-reader-extension-limitations.html
---

I've been doing a piece of work for a customer who wanted a simple form distributed around their organisation for staff to fill in and return.  The only additional requirement was that end users need to be able to save the document whilst filling it in.  Most of my work to date has been using the Adobe LiveCycle product suite and so I naturally turned to Reader Extensions ES2 which would give end users the ability to save documents offline but comes at a rather large premium in terms of licence costs.   

I'd always ignored Acrobat as I'd never needed to use it's standalone functionality but something about the simplicity of this requirement made me look again.  Sure enough since a few versions ago Acrobat now has a form of Reader Extension capability.  Form designers can use Acrobat (or Designer) to create their form and distribute it via Acrobat and reader extend it (note to Adobe: make this easier to find in Acrobat X Pro, currently it's hidden under the "Save As" file menu for some reason).  

This all seemed a little too easy and instantly made me want to find some sort of limitation as otherwise Reader Extensions ES2 would look a very expensive option compared to the relative inexpense of purchasing Acrobat X Pro licences.  I eventually turned to the EULA, searching for some sort of "gotcha" for this feature.  Sure enough there is one ([section 16.8.3](http://www.adobe.com/products/eulas/pdfs/Reader10_combined-20100625_1419.pdf)).  

My interpretation of the restriction of Acrobat reader extended forms is as follows:  

*   If sending out to more than 500 users the Acrobat author cannot collect more than 500 unique responses (electronic and hard copies included)
*   If sending out to less than 500 unique users then the  Acrobat author can collect as many responses from these users as required.

As an example my customer had an organisation in excess of 1000 people.  Making the reader extended PDF form available on the company intranet isn't a problem but the total number of responses which can be processed from that form couldn't exceed 500 without breaking the EULA. In this instance it looks as if Reader Extensions ES2 is the way forward but it's worth being aware of the limitations as I've worked with customers in the past where the 500 user limit may not have been reached.

I'd searched initially for "Reader Extensions vs Acrobat" posts but it seems now as if they both have their use cases depending on the size and scale of distribution of the form being designed.