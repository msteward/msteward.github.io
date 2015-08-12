---
layout: post
title: Achieving Consistency
date: '2014-06-21T15:58:00.002-07:00'
author: Michael Steward
tags:
- Tools
- HTML5 / JS
modified_time: '2014-06-21T20:53:28.575-07:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-5320954539491939506
blogger_orig_url: http://www.michaelsteward.com/2014/06/achieving-consistency.html
comments: true
---

One of the more challenging aspects of managing a team of developers is maintaining standards and style of coding. It may seem trivial but even small things like an individual developer's tab setting can quickly lead to check-in chaos and code review hell.  

There are loads of tools out there no to help but one of my favourites is EditorConfig. It doesn't do a lot but goes a long way to help keep the style consistent.  

[http://editorconfig.org/](http://editorconfig.org/)  

There are already plugins for multiple editors (including Sublime, Notepad++, Vim, Atom etc.) so you don't have to fight for everyone to use a single IDE (and with this being such a personal choice I wouldn't advocate trying!). Get the team together at the start of a project, agree on the settings you'll use and make sure everyone has the plugin to keep the styling consistent. Obviously this only affects the basics such as tabbing, line spacing etc. but combined with a good JSHint config (for example, if developing JS) really goes a long way to helping maintain a consistent code base.
