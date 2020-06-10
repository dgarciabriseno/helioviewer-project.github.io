---
id: 150
title: Improved scaling to AIA images.
date: 2011-02-01T21:37:11+00:00
author: jack
layout: post
guid: http://blog.helioviewer.org/?p=150
permalink: /2011/02/01/improved-scaling-to-aia-images/
categories:
  - AIA
  - JP2Gen
  - SDO
---
We recently changed the process of how we convert SDO-AIA science data into JPEG2000 images for use with the Helioviewer Project. The new process is now based on the scaling algorithms used to provide images for the Goddard Spaceflight Center&#8217;s SDO webpage. Images with the new scaling start from about 2011/01/31 02:00 &#8211; 04:00 UT onwards, depending on the _measurement_. The SDO-AIA 171 waveband shows the least difference between old and new scaling algorithms. All other wavebands show significant changes. We changed the scaling algorithms we use so that users are better able to see the structure and detail in these images without having to do any extra image processing themselves. We think the new images are a definite improvement, and we hope you like them too. Thanks to Leila Mays and Barbara Thompson of the SDO mission for their help in implementing the new scaling algorithms.

