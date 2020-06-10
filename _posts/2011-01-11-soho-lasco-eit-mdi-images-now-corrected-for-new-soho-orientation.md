---
id: 33
title: SOHO LASCO, EIT, MDI images now corrected for new SOHO orientation
date: 2011-01-11T07:09:13+00:00
author: jack
layout: post
guid: http://helioviewer.nascom.nasa.gov/blog/?p=33
permalink: /2011/01/11/soho-lasco-eit-mdi-images-now-corrected-for-new-soho-orientation/
categories:
  - EIT
  - JP2Gen
  - LASCO
  - MDI
  - SOHO
---
Around 2010/10/29-30 the SOHO spacecraft changed flight operations so it is no longer constantly aligned with the rotation axis of the Sun. SOHO now points to ecliptic north, which makes an approximate seven degree angle with the equator of the Sun. SOHO will still flip 180 degrees in order to maintain optimal communication with the Earth, but the rotation will now flip the spacecraft relative to ecliptic north. The raw image data that SOHO takes therefore shows the new orientation. At the Helioviewer Project, we rotate the data so that solar north is towards the top of your screen and the rotation axis of the Sun is vertical (i.e., parallel to the left and right hand side of a rectangular screen). Our science data processing software &#8211; JP2Gen &#8211; now takes account of the new rotation of SOHO and rotates SOHO science data appropriately. This is done to maintain homogeneity with the existing images we already provide, and makes it easy to compare images from multiple telescopes.

