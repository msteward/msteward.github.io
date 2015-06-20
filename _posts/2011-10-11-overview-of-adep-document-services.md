---
layout: post
title: Overview of the ADEP Document Services modules
date: '2011-10-11T03:00:00.000-07:00'
author: Michael Steward
tags:
- Forms
- Adobe
- ADEP
- LiveCycle
- Adobe Digital Enterprise Platform
- Document Services
- Adobe Forms
modified_time: '2012-03-03T11:38:26.040-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-2496581792513744668
blogger_orig_url: http://www.michaelsteward.com/2011/10/overview-of-adep-document-services.html
---

When LiveCycle became ADEP Document Services all of the existing modules were ported over but I thought it would be useful to revisit them all and see what as new.  This post gives a summary of the modules which are available to any Document Services solution (excluding the foundation services which come with all Document Services modules) and should be familiar to those who have worked with LiveCycle ES1/ES2 in the past.   

## Business Process Management

### Adobe Digital Enterprise Platform Document Services - Process Management 10.0  
Process Management allows the designer to create processes which assign and move tasks around a business.  End users can login using the Workspace web application to view and update any task assigned to them.  This module is commonly used in conjunction with the Forms modules in order to create workflows for forms built by the designer.  ADEP Mobile also comes as part of this module allowing your end users to interact with their tasks on the go.  

### Content Services  
As described in one of my [earlier posts](https://michaeljsteward.wordpress.com/2011/10/10/livecycle-content-services-in-the-adep-world/) this one has now been **deprecated**.  It’s still included for legacy purposes but you should really be using the new CRX service.  


## Forms Automation

### Adobe Digital Enterprise Platform Document Services - Forms 10.0  
The bread and butter of many ADEP solutions, Forms is what allows data to be merged and retrieved from forms rendered to PDF, HTML or Guides.  It also allows forms to be assembled from fragments.  If you are designing to form to be dynamic and it doesn’t have a fixed layout then you will almost certainly need the Forms module.  Together with the Process Management module it allows for some fancy data collection and presentation to your end users!  

### Adobe Digital Enterprise Platform Document Services - Adobe Reader Extensions 10.0  
If you need to distribute those forms you’ve just designed to external parties then chances are you’ll probably run into the need for Reader Extensions.  A “rights-enabled” form opened in Adobe Reader allows the end user to perform tasks that are normally reserved for the commercial Acrobat software such as adding attachments, saving a PDF form locally (the most common use case) and digitally signing forms.  Can be used standalone or as part of a workflow.  


## Document Security

### Adobe Digital Enterprise Platform Document Services – Rights Management 10.0  
Document need securing to prevent it being passed around without restriction?  Then you probably need the Rights Management module.  This one gives you the ability to lock down documents and specify who can open your protected documents.  Allows fine control over the details of a documents usability including offline usage and also the collection of usage data (e.g. track the number of users clicking a particular button).  

### Adobe Digital Enterprise Platform Document Services – Digital Signatures 10.0  
Another security module, this one specifically for securing documents using digital signatures.  Not a huge amount of functionality with this one and is easy to use if needed.  

### Adobe Digital Enterprise Platform Document Services – Encryption  
Simple module to allow PDF documents to be encrypted and secured with either a password or private key.  If the end user has neither the private key or password then they will be unable to view the contents.  

## Communications

### Adobe Digital Enterprise Platform Document Services – Output 10.0  
Along with the Forms and Process Management modules this is the one I come across most often.  It’s another heavy weight module that delivers a lot of functionality and also shares some features with the Forms module.  However unlike Forms, Output is geared towards preparing forms for physical output rather than for being displayed on screen.  There have been some updates to Output in version 10.0 such as the ability to flatten interactive forms.  Key features in Output remain the assembly of PDF documents, setting print options, merging XML data into forms and outputting to PostScript.  

### Adobe Digital Enterprise Platform Document Services – Production Print  
I’ve not personally used this one but Product Print is geared production printing as the name suggests.  Like Output and Forms it enables combining forms designing in Designer with XML data.  In this case it is often to personalise the form (e.g. add the customers name).  Only needed if you require printing on a industrial scale.  Worth noting that this module doesn’t install with the rest of Document Services and instead has its own installation process.  

### Adobe Digital Enterprise Platform Document Services – PDF Generator 10.0  
This module has a number of common use cases as it allows a large range of file formats to be converted into PDF documents and vice-versa.  Very useful if, for example, your process allows a user to upload a Word document but you want to convert this to a PDF document in your process.  Similarly you can convert PDF documents into HTML and a range of other formats including images.  


## Content Management

### Connectors for ECM  
As the name suggests this module provides access from within your processes to third party Enterprise Content Management (ECM) systems.  Currently these include:  

*   Adobe Digital Enterprise Platform Document Services - Connector for EMC® Documentum® 10.0
*   Adobe Digital Enterprise Platform Document Services - Connector for IBM ® FileNet 10.0
*   Adobe Digital Enterprise Platform Document Services - Connector for IBM ® Content Manager 10.0
*   Adobe Digital Enterprise Platform Document Services - Connector for Microsoft®SharePoint® (2007 and 2010) 10.0