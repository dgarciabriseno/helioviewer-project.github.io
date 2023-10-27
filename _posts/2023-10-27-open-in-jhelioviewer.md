---
title: Opening Videos in JHelioviewer
date: 2023-10-27T00:00:00-05:00
author: Daniel Garcia Briseno
layout: post
permalink: /2023/10/27/opening-movies-in-jhelioviewer
categories:
  - General
---

Helioviewer now supports opening helioviewer.org movies in [JHelioviewer](https://www.jhelioviewer.org/)!

## Background
This feature is enabled by [SAMP](https://www.ivoa.net/documents/SAMP/),
a standard by the International Virtual Observatory Alliance.
SAMP is a protocol that allows different applications to send messages to each other.
When JHelioviewer is running, it acts as a SAMP Hub and accepts requests to
load images specified in the SAMP message.

Helioviewer is able to communicate with JHelioviewer thanks to [sampjs](https://github.com/astrojs/sampjs),
a javascript library which implements the SAMP protocol, and library we developed called
[jhvrequest](https://www.npmjs.com/package/jhvrequest) which provides a clean
javascript interface for sending datasets to JHelioviewer.

Technically speaking, the mp4 video itself is not sent to JHelioviewer. Instead,
the list of the layers in the video and the video's timespan are sent to JHelioviewer
so that it can reconstruct the movie.

## Limitations
Currently videos containing XRT and GONG layers are not supported.

## How-To?
To open a movie in JHelioviewer, first have JHelioviewer running, then open one of your movies in [helioviewer.org](https://helioviewer.org).

In the bottom right of the video player window you will see an "Open In JHelioviewer" button.

![Video player window with JHelioviewer button](/images/uploads/2023/jhv-video.jpg)

If JHelioviewer is not running, the button will say "JHV is not open" and the button will not be clickable. Make sure to open JHelioviewer first.

When you click the button, JHelioviewer will display a notification asking if you'd like to accept the incoming request.

![SAMP Hub Security popup](/images/uploads/2023/security.jpg)

Click **Yes** to load the movie in JHelioviewer.
