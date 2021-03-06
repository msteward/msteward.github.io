---
layout: post
title: LiveCycle Content Services in the ADEP world
date: '2011-10-10T01:30:00.000-07:00'
author: Michael Steward
tags:
- DSC
- Content Services
- Adobe
- ADEP
- LiveCycle
- Adobe Digital Enterprise Platform
modified_time: '2012-03-03T11:38:26.112-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-638273963695539684
blogger_orig_url: http://www.michaelsteward.com/2011/10/livecycle-content-services-in-adep.html
--- 

A source of confusion I've come across when explaining the new world of ADEP to those familiar with the LiveCycle days is what has happened to Content Services.  Content Services was essentially the repository for storing files and anything else you needed persisting in your application.  It was built around the Open Source CMS by Alfresco and was used on almost all of the projects I worked on.  In the move to ADEP it's the one module the fate of which I wasn't 100% sure of.  

![Server](http://mrg.bz/P1mJor "Content Services Server") 

On the one hand ADEP now brought in the exciting world of a Java Content Repository (JCR) in the form of CRX with its RESTful API and many [other features](http://www.day.com/day/en/products/crx.html "Adobe CRX") but on the other there didn't seem to be any clear way of utilising this fancy new repository from within processes designed in ADEP Workbench.  Sure, you could use the API, but that seemed a little too "manual" in the world of drag and drop process design.  Then I read a [blog post ](http://blogs.adobe.com/ADEP/2011/10/prerelease-next-week-easily-connect-from-document-services-to-the-content-repository-in-experience-services.html "ADEP Blog")on the official ADEP blog about a new pre-release DSC which will allow for easy access to Content Repository and it all started making sense.  Why this wasn't released with the rest of ADEP I'm not sure (after all, this DSC will deprecate the content services DSC) but it will certainly make using that shiny new CRX repository a whole lot easier for process designers who don't fancy getting their hands dirty.  

The DSC should be available on the 14th October via Adobe's Pre-Release programme and I'll be posting an update when it's out and I've had a chance to play with it.  

**Edit: Thanks to Jayan for pointing out an error in my original post.  The new DSC will not replace the existing content services DSC.  The content services DSC will just be deprecated.**
