---
title: Helioprojective Mouse Coordinates
date: 2023-08-25T00:00:00-05:00
author: Daniel Garcia-Briseno
layout: post
permalink: /2023/08/28/MouseCoords/
categories:
  - General
---

## Coordinates are returning to Helioviewer!

The ability to see where your mouse is on the sun has been heavily requested by Helioviewer users.

This has been in the works for some time and we're happy to announce that mouse coordinates are back on Helioviewer.

![Image of the mouse hovering over a sunspot on helioviewer with the top bar showing coordinates (-593, -264) arcseconds](/images/uploads/2023/hv_mouse.jpg)

To ensure a reasonable accuracy of these coordinates, we used [sunpy](https://sunpy.org/) to plot the coordinates provided by Helioviewer.
![Image of the same sunspot and coordinates plotted with sunpy](/images/uploads/2023/sunpy_mouse.jpg)

### Disclaimer!
These coordinates are provided as approximations. While we do believe them to be reasonably accurate, there may be cases where the computed coordinate is incorrect. Always double check your coordinates if you are doing any kind of scientific analysis.
