---
id: 51
title: 'Helioviewer.org update: Improved movie quality'
date: 2010-12-29T19:53:00+00:00
author: keith
layout: post
guid: http://helioviewer.nascom.nasa.gov/blog/?p=51
permalink: /2010/12/29/helioviewer-org-update-improved-movie-quality/
enclosure:
  - |
    https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-before.mp4
    3579320
    video/mp4
    
  - |
    https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after.mp4
    9609574
    video/mp4
    
  - |
    https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after-hq.mp4
    95393376
    video/mp4
    
categories:
  - Development
  - General
  - Helioviewer.org
  - Movies
---
Helioviewer.org has been updated this morning to include some recent improvement to the movie generation process. The result of this update is that the quality of the movies that you see on Helioviewer.org has been greatly improved.

While Helioviewer.org has offered High-definition [H.264](http://en.wikipedia.org/wiki/H.264/MPEG-4_AVC "H.264 on Wikipedia") movies for several months now (encoded using the excellent [x264](http://x264.nl/) library), the amount of compression used was fairly high. The result of this was very small file sizes (around 1-5MB), but some noticeable compression artifacts; the effect of which was especially noticeable for larger movies.

For example, the below movie was generated on Helioviewer.org several days ago:

<p style="text-align: center;">
  <video id="wp_mep_1" width="640" height="384" poster="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-before-poster.png" controls="controls" preload="none" > <source src="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-before.mp4" type="video/mp4" /> </video>
</p>

<p style="text-align: center;">
  <strong>Example 1: In-browser movie before update (<a href="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-before.mp4">download video</a>)<br /> </strong>
</p>

A number of changes were made to the H.264 encoding parameters in order to improve the quality, for example, whereas movies were previously generated using a <span style="text-decoration: line-through;">constant</span> variable bit-rate (-b 2048K), the newer movies use a different rate-control method called &#8220;[Constant Ratefactor (CRF)](http://mewiki.project357.com/wiki/X264_Settings#crf)&#8221; in order to achieve a desired level of quality.

Here is an example of a movie created for viewing in the browser using the new code:

<p style="text-align: center;">
  <video id="wp_mep_2" width="640" height="384" poster="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after-poster.png" controls="controls" preload="none" > <source src="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after.mp4" type="video/mp4" /> </video>
</p>

<p style="text-align: center;">
  <strong> </strong><strong>Example 2: </strong><strong>In-browser movie after update (<a href="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after.mp4">download video</a>)<br /> </strong>
</p>

<p style="text-align: left;">
  What&#8217;s more, the &#8220;high-quality&#8221; download option is now much higher quality than ever before. Previously, when users clicked on the link below in the in-browser movie that says &#8220;<em>Click here to download a high-quality version</em>&#8220;, what they got was actually the same movie that was already playing in their browser, but packed in a container format compatible with the user&#8217;s operating system. With the update this morning, however, the high-quality download link now points to a separate and visibly higher-quality movie from what is shown in the browser. The high-quality option available now is actually a <a href="http://en.wikipedia.org/wiki/Lossless_data_compression lossless">lossless</a> movie, with respect to the underlying <a href="http://wiki.helioviewer.org/wiki/JPEG_2000">JPEG 2000</a> data archive used by Helioviewer.org.
</p>

<p style="text-align: center;">
  <video id="wp_mep_3" width="640" height="384" poster="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after-hq-poster.png" controls="controls" preload="none" > <source src="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after-hq.mp4" type="video/mp4" /> </video>
</p>

<p style="text-align: center;">
  <strong>Example 3: </strong><strong>High quality movie after update (<a href="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after-hq.mp4">download video</a>)<br /> </strong>
</p>

<p style="text-align: center;">
  (<strong>Note: </strong>If you are having trouble viewing the above video, you can download an MP4 version directly from <a href="https://helioviewer-project.github.io/images/uploads/2010/12/helioviewer.org-after-hq.mp4">here</a>.)
</p>

Of course, nothing comes for free, and that is true in the case of these improvements as well. The improvements made to quality come at the cost of increased movie filesize. For the standard-quality movie that is shown directly in the browser, the filesize has increased from by a factor of around 1.5-10x with the largest files around 50MB each. The real behemoths, however, are the high-quality (lossless) movies which range from around 50-300MB. It&#8217;s a lot, but try watching a few of high-quality AIA movies and you won&#8217;t ever want to go back again. 🙂

**Update 2010/12/31:** Thanks to Dark_Shikari on #x264 for some help making sense of some of the many rate control options available when encoding using x264.

