---
id: 1158
title: 'NEW: Solar features and events from the Heliophysics Event Knowledgebase'
date: 2013-07-16T19:18:21+00:00
author: jack
layout: post
guid: http://blog.helioviewer.org/?p=1158
permalink: /2013/07/16/new-solar-features-and-events-from-the-heliophysics-event-knowledgebase/
categories:
  - General
  - HEK
  - Helioviewer.org
  - Releases
---
The Sun has many different features and events of great scientific interest. It&#8217;s useful to be able to catalog those features and measure their properties. By doing so, we can build up more knowledge about the Sun.

The [Heliophysics Event Knowledgebase](http://www.lmsal.com/hek/) (HEK) is one such catalog. The HEK collects and stores information about many different types of solar feature &#8211; active regions, flares, etc, from many different sources around the world. Each solar feature and event can be detected in different ways. Some features and events are detected by _people_ looking at the data, and some are detected by [specialized computer vision algorithms](http://solar.physics.montana.edu/sol_phys/fft/). 

We&#8217;ve taken the information in the HEK and designed a simple interface to allow you to find out what features and events occurred on the Sun at any given time. We&#8217;ve organized the information in the HEK by _feature/event_. You may need to reload helioviewer.org to get the latest version which includes the HEK.

[<img src="https://helioviewer-project.github.io/images/uploads/2013/07/HV-intro-Screenshot-from-2013-07-16-101837.png" alt="HV intro: Screenshot from 2013-07-16 10:18:37" width="281" height="461" class="aligncenter size-full wp-image-1161" sizes="(max-width: 281px) 100vw, 281px" />](https://helioviewer-project.github.io/images/uploads/2013/07/HV-intro-Screenshot-from-2013-07-16-101837.png)

The numbers at the end of each line tell you the total number of features/events of each type on the Sun at that time. You can select any combination of features and events you want (green tick marks), or you can select none. If you&#8217;ve selected a particular type of feature/event but the text is faded out, this means that there are none of those particular feature/events at the time you&#8217;ve requested. If you browse forward and backwards and time and those feature/events are in the HEK, helioviewer.org will display them.

We then break down the total number of features/events by _feature recognition method_. We do this because different feature recognition methods can give different results for the same feature/event type. You can select any combination of the available feature recognition methods, or you can select none. For example, the active regions on the Sun at this time were detected using two different feature recognition methods:

[<img src="https://helioviewer-project.github.io/images/uploads/2013/07/HV-Intro-Screenshot-from-2013-07-16-101905.png" alt="HV Intro: Screenshot from 2013-07-16 10:19:05" width="280" height="98" class="aligncenter size-full wp-image-1160" />](https://helioviewer-project.github.io/images/uploads/2013/07/HV-Intro-Screenshot-from-2013-07-16-101905.png)

The numbers at the end of each line tell you how many active regions were detected by [SPoCA](http://sdoatsidc.oma.be/web/sdoatsidc/SoftwareSPoCA) (a computer vision algorithm) and the [NOAA SWPC Observer](http://www.swpc.noaa.gov/) (people looking at the data).

Here&#8217;s a typical view of some AIA 304 data with the HEK features and events overplotted.

[<img src="https://helioviewer-project.github.io/images/uploads/2013/07/HV-Intro-Screenshot-from-2013-07-16-102931-1024x627.png" alt="HV Intro: Screenshot from 2013-07-16 10:29:31" width="640" height="392" class="aligncenter size-large wp-image-1164"  sizes="(max-width: 640px) 100vw, 640px" />](https://helioviewer-project.github.io/images/uploads/2013/07/HV-Intro-Screenshot-from-2013-07-16-102931.png)

Each of the marker pins corresponds to the feature/event detected by a feature recognition method. Clicking on them pulls up much more information on each individual event. Each of the marker pins also has a small label attached to it with an important piece of information concerning that feature/event. We&#8217;ve also extended the movie and screenshot capability so that your selected feature/event markers and labels appear in any movies and screenshots you make.

Finally, in the bottom left-hand corner of the viewer window you&#8217;ll see a small image of the Earth. This is the size of the Earth on the same scale as the solar and heliospheric images. This also appears in movies and screenshots of the Sun. Full information on using helioviewer.org can be found by clicking the [help link](http://wiki.helioviewer.org/wiki/Helioviewer.org_User_Guide_2.4.0) at the bottom of the helioviewer.org webpage.

The HEK is the result of much work by many different people around the world. We are happy to be able to present data from this great solar and heliospheric resource in Helioviewer.org.

