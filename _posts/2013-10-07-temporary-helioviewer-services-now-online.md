---
id: 1237
title: Temporary Helioviewer services now online
date: 2013-10-07T16:20:19+00:00
author: jack
layout: post
guid: http://blog.helioviewer.org/?p=1237
permalink: /2013/10/07/temporary-helioviewer-services-now-online/
categories:
  - General
---
Our colleagues at the [Space Influences Data Center (SIDC)](http://sidc.be/) at the [Royal Observatory of Belgium](http://www.observatory.be/) have kindly brought a Helioviewer server online at <http://swhv.oma.be/helioviewer/>. The webpage provides AIA 171 and 304 images taken once every 10 minutes. PROBA2-SWAP images (at full cadence) are also provided.

Users of JHelioviewer on Mac OS X can also use the Helioviewer server at SIDC to stream movies. Go to your JHelioviewer directory and look for the subdirectory &#8220;Settings&#8221;. Add these lines to the _user.properties_ file:

> API.dataSources.path=http\://swhv.oma.be/helioviewer/api/?action\=getDataSources&verbose\=true&enable\=[PROBA2]  
> API.jp2images.path=http\://swhv.oma.be/helioviewer/api/  
> API.jp2series.path=http\://swhv.oma.be/helioviewer/api/ 

Many thanks to our colleagues at the Royal Observatory of Belgium for providing their resources in support of the Helioviewer Project.

