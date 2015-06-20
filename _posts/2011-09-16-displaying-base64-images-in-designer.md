---
layout: post
title: Displaying Base64 images in Designer
date: '2011-09-16T08:40:00.000-07:00'
author: Michael Steward
tags:
- Adobe Forms
modified_time: '2012-03-03T11:38:26.095-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-5302114012818309397
blogger_orig_url: http://www.michaelsteward.com/2011/09/displaying-base64-images-in-designer.html
---

A recent project required me to write a custom component to merge image data with some text.  This was simple enough in itself but testing the output Base64 image data with PDF files proved a pain.  As a result I made a very simple PDF in Designer which allows you to test your Base64 encoded image strings to see how they'll look in a PDF document.  The following link will let you download the form which can be opened in designer.  The archive also contains a very basic data schema and test data to get you started.  Just replace the Base64 string in the "sampleData.xml" file with your own string.  Fire up Designer and click the Preview tab to see if the image is displaying properly.  

[Download Base64ImageTest.zip](http://dl.dropbox.com/u/150823/Base64ImageTest.zip)