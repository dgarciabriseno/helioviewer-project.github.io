---
title: Helioprojective Mouse Coordinates
date: 2023-08-25T00:00:00-05:00
author: Daniel Garcia Briseno & Jack Ireland
layout: post
permalink: /2023/08/28/MouseCoords/
categories:
  - General
---

## Coordinates are returning to Helioviewer!
 
Knowing the position of the mouse pointer in a solar coordinate system when using Helioviewer.org has been widely requested by users.
 
We have been working on this for some time and we're happy to announce that coordinates are back on Helioviewer. Users can show the mouse position in helioprojective Cartesian or radial coordinates. *The mouse position provided by Helioviewer.org approximates the true position*. While we do believe the coordinates returned to be reasonably accurate, there may be cases where the displayed mouse coordinate is incorrect. Users are encouraged to use other tools for work that requires more accuracy.
 
We tested the veracity of the Helioviewer.org mouse position using [sunpy](https://sunpy.org/), a free and open-source Python package for solar physics data analysis that has a sophisticated and well-tested coordinate framework.
 
The image below shows the mouse pointer hovering over a sunspot. Helioviewer.org shows the coordinate position as (-593, -264) arcseconds.
![Image of the mouse hovering over a sunspot on helioviewer with the top bar showing coordinates (-593, -264) arcseconds](/images/uploads/2023/hv_mouse.jpg)
 
If we take the Helioviewer.org coordinate position, and use [sunpy](https://sunpy.org/) to plot that position on the same data (red dot), we get the following image:
![Image of the same sunspot and coordinates plotted with sunpy](/images/uploads/2023/sunpy_mouse.jpg)
 
The red dot in the _sunpy_ image is in approximately the same position as the location of the mouse in the Helioviewer.org image above.
