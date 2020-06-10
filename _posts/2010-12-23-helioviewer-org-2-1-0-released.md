---
id: 46
title: Helioviewer.org 2.1.0 Released
date: 2010-12-23T20:47:17+00:00
author: keith
layout: post
guid: http://helioviewer.nascom.nasa.gov/blog/?p=46
permalink: /2010/12/23/helioviewer-org-2-1-0-released/
categories:
  - Helioviewer.org
  - Releases
---
Helioviewer.org has been updated to include a number of new features and bug fixes. Although many of the features included in this release have already been available online for some time now, their performance and reliability has been greatly improved during the past several weeks.

[Try it out!](http://www.helioviewer.org) If you have any comments or suggestions, or run into any problems, [report a bug or feature request](http://bugs.launchpad.net/helioviewer.org).

Stayed tuned for some exciting new features next week 🙂

**RELEASE NOTES:**

[Helioviewer.org 2.1.0](https://launchpad.net/helioviewer.org/2.0/2.1.0) is a major release which includes many new features and a large number of bug fixes. Major features added include: full support for AIA images, on the fly movie and screenshot creation and a custom resource management and queuing system. Other changes include:

_**New features**:_

* Overhauled error back-end error handling  
* Support for HEK FRM/Event querying  
* PHP IMagick used in place of convert when available for better performance (See: http://valokuva.org/?p=40 for more information)  
* Custom FFmpeg wrapper used in place of PHPVideoToolkit  
* FirePHP support  
* Documentation for each back-end module now handled at the module level rather than globally  
* IE8 local storage support  
* Conversion from tile coordinates to spatial coordinates now handled on front-end  
* Removed dependencies on image archive directory structure  
* Added a JHelioviewer JNLP generation method so that users can easily jump from Helioviewer.org to JHelioviewer  
* Color of image layer timestamps now ranges on a scale from green (near requested time) to red (far from requested time). Absolute difference is used so that it does not matter whether actual image is ahead or behind requested one

_**Bug fixes**:_

* Fixed bug [#544338](https://bugs.launchpad.net/helioviewer.org/+bug/544338) Edge effects for tiles viewed at higher magnification  
* Fixed bug [#605412](https://bugs.launchpad.net/helioviewer.org/+bug/605412) Helioviewer-generated Flash movies degrade in quality as the movie progresses  
* Fixed bug [#614558](https://bugs.launchpad.net/helioviewer.org/+bug/614558) Use of IMagick#extentImage results in images with incorrect dimensions  
* Fixed bug [#619944](https://bugs.launchpad.net/helioviewer.org/+bug/619944) Movie history panel occasionally stays in viewport  
* Fixed bug [#312205](https://bugs.launchpad.net/helioviewer.org/+bug/312205) Sandbox dimensions are too large for C2 and C3 Images  
* Fixed bug [#383939](https://bugs.launchpad.net/helioviewer.org/+bug/383939) Disable tiling when layer is hidden  
* Fixed bug [#508723](https://bugs.launchpad.net/helioviewer.org/+bug/508723) Check to see if data exists for each source, or provide option to disable a data source  
* Fixed bug [#605398](https://bugs.launchpad.net/helioviewer.org/+bug/605398) Improve JPX request cadence optimization for non-evenly distributed data  
* Fixed bug [#605411](https://bugs.launchpad.net/helioviewer.org/+bug/605411) Fullscreen, etc. button tooltips are hidden by movie/screenshot creation dialogs  
* Fixed bug [#608265](https://bugs.launchpad.net/helioviewer.org/+bug/608265) Chrome appends .html on movies  
* Fixed bug [#610456](https://bugs.launchpad.net/helioviewer.org/+bug/610456) FITS header dialog not updated when image is changed  
* Fixed bug [#645836](https://bugs.launchpad.net/helioviewer.org/+bug/645836) shortcuts for time steps &#8220;<&#8221; or &#8220;>&#8221; not working  
* Fixed bug [#535645](https://bugs.launchpad.net/helioviewer.org/+bug/535645) Add link to uncompressed JavaScript and CSS for better &#8220;view source&#8221; function  
* Fixed bug [#544352](https://bugs.launchpad.net/helioviewer.org/+bug/544352) backfill JP2s from SOHO mission up to most recent  
* Fixed bug [#322857](https://bugs.launchpad.net/helioviewer.org/+bug/322857) Sandbox dimensions do not update right away when layers are removed  
* Fixed bug [#415455](https://bugs.launchpad.net/helioviewer.org/+bug/415455) helioviewer logo issues/request

_**Library updates**_:

* jQuery imgAreaSelect (0.8 => 0.9.2)  
* jQuery jGrowl (1.2.0 => 1.2.4)  
* jQuery qTip (1.0 r34 => 1.0 r54)
