---
id: 1292
title: Temporary replacement Helioviewer services now available.
date: 2014-10-07T16:32:48+00:00
author: jack
layout: post
guid: http://blog.helioviewer.org/?p=1292
permalink: /2014/10/07/temporary-replacement-helioviewer-services-now-available/
categories:
  - General
---
Colleagues at the [Institut d&#8217;Astrophysique Spatiale](http://www.ias.u-psud.fr/) in France have graciously stepped in to provide Helioviewer services while Helioviewer Project servers are undergoing maintenance. 

To use the web client, please go to <http://helioviewer.ias.u-psud.fr/helioviewer/>. Note that the &#8220;Upload Video to YouTube&#8221; function is not available from this site.

To use JHelioviewer, please add the following lines to your JHelioviewer/Settings/user.properties file

_API.jp2series.path=http\://helioviewer.ias.u-psud.fr/helioviewer/api/index.php  
API.dataSources.path=http\://helioviewer.ias.u-psud.fr/helioviewer/api/?action\=getDataSources&verbose\=true  
default.remote.path=jpip\://helioviewer.ias.u-psud.fr\:8080  
API.event.path=http\://helioviewer.ias.u-psud.fr/helioviewer/api/  
display.laf=com.sun.java.swing.plaf.gtk.GTKLookAndFeel  
default.httpRemote.path=http\://helioviewer.ias.u-psud.fr/helioviewer/jp2/  
API.jp2images.path=http\://helioviewer.ias.u-psud.fr/helioviewer/api/index.php  
default.server=ias_

We thank the [Institut d&#8217;Astrophysique Spatiale](http://www.ias.u-psud.fr/) for volunteering their services while Helioviewer Project servers are undergoing maintenance.

