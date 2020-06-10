---
id: 789
title: SDO data lag
date: 2012-04-02T13:54:54+00:00
author: jack
layout: post
guid: http://blog.helioviewer.org/?p=789
permalink: /2012/04/02/sdo-data-lag/
categories:
  - AIA
  - General
  - HMI
  - SDO
---
As you may have noticed, we are currently experiencing a lag in the availability of SDO images. The lag is happening upstream of Helioviewer. The Helioviewer Project provides images of scientific data. The science data is beamed down from the spacecraft , to a dedicated ground station (as [outlined here](https://helioviewer-project.github.io/2012/03/29/where-is-the-solar-dynamics-observatory-right-now/)) in New Mexico. The packets of data are first re-assembled to form the raw science data, and then have some corrections applied to yield data suitable for science applications. Data is constantly streaming off the spacecraft and being processed through this pipeline, which involves many different locations and institutions.

One of those science applications is visualization of the data. The Helioviewer Project takes that science data and converts those data to JPEG2000 images, which we then make available via [www.helioviewer.org](http://www.helioviewer.org) and [www.jhelioviewer.org](http://www.jhelioviewer.org). We have to have the science data available to make the JPEG2000 images.

As soon as new SDO-AIA and HMI images become available, we will make them available to you. We regret the interruption to the stream of SDO data. Other data-sets are unaffected, and are available as usual.

