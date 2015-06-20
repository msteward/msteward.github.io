---
layout: post
title: ASDoc - wading through the errors
date: '2011-03-29T04:40:00.000-07:00'
author: Michael Steward
tags:
- Adobe Flex
modified_time: '2012-03-03T11:38:26.073-08:00'
blogger_id: tag:blogger.com,1999:blog-8669861761761330438.post-438142796823706574
blogger_orig_url: http://www.michaelsteward.com/2011/03/asdoc-wading-through-errors.html
---

ASDoc is a nightmare. What should have been a simple task turned into a day of trawling the net trying to find the cause of the seemingly endless errors preventing me from running it. Eventually I got it working so here's a short post explaining the pitfalls I faced.  

* Include the Flex libraries in your -library-path argument (i.e. flex.swc, rpc.swc, framework.swc, utilities.swc). Without this I was getting errors from asdoc not being able to find some of the standard classes.
* Check your code! Some of the errors I was getting were actually problems that just weren't throwing errors (some of my event dispatching classes were not extending EventDispatcher, this threw lots of errors whenever asdoc encountered dispatchEvent )
* Give your -source-path as the root of your application but use -doc-sources to list only those folders you actually want documenting

For reference here is my very simple ANT script for generating my ASDocs:  

{% highlight xml %}  
<project name="ASDoc Build Script" default="main" >  

<!--  
 Read in the properties file which contains the locations  
 for all paths referred to here  
 -->  
 <property file="asdoc.properties" />  

<!--  
 Main Target:  
 Cleans and compiles ASDocs with a log  
 -->  
 <target name="main" depends="clean, log, create-docs" />  

<!--  
 Delete and recreate the asdoc output directory  
 -->  
 <target name="clean" >  
 <delete dir="${output.dir}" />  
 <mkdir dir="${output.dir}" />  
 </target>  

<!--  
 Run asdoc.exe on the source documents passing all required  
 parameters to asdoc  
 -->  
 <target name="create-docs" >  
 <exec executable="${asdoc.exe}" failonerror="true" >  
 <arg line="-source-path '${root_src}' " />  
 <arg line="-doc-sources '${framework_src}' '${actionscripts_src}' " />  
 <arg line="-library-path '${irmds_library.dir}' '${flex_library.dir}'" />  

<arg line="-main-title '${main.title}'" />  
 <arg line="-window-title '${window.title}'" />  
 <arg line="-output '${output.dir}'" />  
 </exec>  
 </target>  

<!--  
 Write out a log file  
 -->  
 <target name="log" >  
 <record name="${output.dir}/asdoc-log.txt" action="start" append="true" />  
 </target>  
</project>  

{% endhighlight %} 