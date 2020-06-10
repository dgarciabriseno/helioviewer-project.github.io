---
id: 1460
title: Improved AIA 304 images coming soon!
date: 2019-09-09T21:34:42+00:00
author: jack
layout: post
guid: http://blog.helioviewer.org/?p=1460
permalink: /2019/09/09/improved-aia-304-images-coming-soon/
categories:
  - General
---
Over years, the response of detectors can change.&nbsp; This can lead to changes in the images captured by those detectors.&nbsp; This is especially apparent in the AIA 304 channel, where images are much darker now than they once were.&nbsp; For example, here is a relatively recent AIA 304 image of the Sun.

<a href="https://blog.helioviewer.org/?attachment_id=1465" rel="attachment wp-att-1465"><img class="aligncenter size-medium wp-image-1465" src="https://helioviewer-project.github.io/images/uploads/2019/09/2018_09_09_15_18_13_AIA_3041-600x316.png" alt="" width="600" height="316" srcset="http://blog.helioviewer.org/wp-content/uploads/2019/09/2018_09_09_15_18_13_AIA_3041-600x316.png 600w, http://blog.helioviewer.org/wp-content/uploads/2019/09/2018_09_09_15_18_13_AIA_3041-768x405.png 768w, http://blog.helioviewer.org/wp-content/uploads/2019/09/2018_09_09_15_18_13_AIA_3041.png 1420w" sizes="(max-width: 600px) 100vw, 600px" /></a>and here is an image of the Sun from the same telescope taken seven years earlier

<a href="https://blog.helioviewer.org/?attachment_id=1466" rel="attachment wp-att-1466"><img class="aligncenter size-medium wp-image-1466" src="https://helioviewer-project.github.io/images/uploads/2019/09/2011_09_09_15_18_13_AIA_304-600x316.png" alt="" width="600" height="316" srcset="http://blog.helioviewer.org/wp-content/uploads/2019/09/2011_09_09_15_18_13_AIA_304-600x316.png 600w, http://blog.helioviewer.org/wp-content/uploads/2019/09/2011_09_09_15_18_13_AIA_304-768x405.png 768w, http://blog.helioviewer.org/wp-content/uploads/2019/09/2011_09_09_15_18_13_AIA_304.png 1420w" sizes="(max-width: 600px) 100vw, 600px" /></a>As you can tell, this image is much brighter.

We can partially compensate for the degradation of the detector by comparing how images looked earlier in the lifetime of AIA to how they look now, and calculate compensation factors that return at least some of the dynamic range to the more recent images.

In the next couple of days we will start including these compensation factors into our AIA 304 images.&nbsp; With these compensation factors, the first image above changes to this:

<a href="https://blog.helioviewer.org/?attachment_id=1467" rel="attachment wp-att-1467"><img class="aligncenter size-medium wp-image-1467" src="https://helioviewer-project.github.io/images/uploads/2019/09/2018_09_09_15_18_13_AIA_304-600x316.png" alt="" width="600" height="316" srcset="http://blog.helioviewer.org/wp-content/uploads/2019/09/2018_09_09_15_18_13_AIA_304-600x316.png 600w, http://blog.helioviewer.org/wp-content/uploads/2019/09/2018_09_09_15_18_13_AIA_304-768x405.png 768w, http://blog.helioviewer.org/wp-content/uploads/2019/09/2018_09_09_15_18_13_AIA_304.png 1420w" sizes="(max-width: 600px) 100vw, 600px" /></a>

As you can tell, the overall sense of brightness is much closer to that of the second (pre-degradation) image than the first degraded image.

Screenshots and movies that use AIA 304 will automatically include these compensation factors.&nbsp; This fix also answers [a long-standing feature request](https://github.com/Helioviewer-Project/helioviewer.org/issues/136) logged by a user.&nbsp; Other AIA measurements have also suffered some degradation over time, but not as much as AIA 304.&nbsp; Over the next few weeks we will roll out changes to images of other AIA data, but these will be not nearly as noticeable as the change to AIA 304.

Please let us know what you think!

