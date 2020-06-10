---
id: 800
title: Helioviewer.org 2.3.0 Released
date: 2012-04-02T20:26:13+00:00
author: keith
layout: post
guid: http://blog.helioviewer.org/?p=800
permalink: /2012/04/02/helioviewer-org-2-3-0-released/
categories:
  - General
  - Helioviewer.org
  - Releases
---
A new version of Helioviewer.org has been released including better movie customization, support for embedding Helioviewer.org in remote sites, and a number of performance and bug fixes.

<p style="text-align: center;">
  <a href="https://helioviewer-project.github.io/images/uploads/2012/04/Helioviewer_230_movie_settings.png"><img class="aligncenter  wp-image-801" title="Helioviewer.org 2.3.0 Movie Settings" src="https://helioviewer-project.github.io/images/uploads/2012/04/Helioviewer_230_movie_settings-1024x618.png" alt="Screenshot showing new movie settings added in Helioviewer.org 2.3.0." width="614" height="371" srcset="http://blog.helioviewer.org/wp-content/uploads/2012/04/Helioviewer_230_movie_settings-1024x618.png 1024w, http://blog.helioviewer.org/wp-content/uploads/2012/04/Helioviewer_230_movie_settings-300x181.png 300w, http://blog.helioviewer.org/wp-content/uploads/2012/04/Helioviewer_230_movie_settings.png 1193w" sizes="(max-width: 614px) 100vw, 614px" /></a>
</p>

Support has been added for embedding Helioviewer.org into third-party websites, and JSONP support makes it easier for new versions of the front-end to be created which interact with the main Helioviewer.org back-end. Similarly, the front-end has been rewritten to allow for easier creation of custom front-end clients without having to re-implement a tiling system, etc.

[<img class="aligncenter size-full wp-image-802" title="Helioviewer.org 2.3.0 settings" src="https://helioviewer-project.github.io/images/uploads/2012/04/helioviewer_230_settings.png" alt="New configuration options added in Helioviewer.org 2.3.0." width="405" height="266" srcset="http://blog.helioviewer.org/wp-content/uploads/2012/04/helioviewer_230_settings.png 405w, http://blog.helioviewer.org/wp-content/uploads/2012/04/helioviewer_230_settings-300x197.png 300w" sizes="(max-width: 405px) 100vw, 405px" />](https://helioviewer-project.github.io/images/uploads/2012/04/helioviewer_230_settings.png)

The back-end movie queuing system has been ported from Ruby to PHP to allow for better integration with the rest of the back-end, and the movies table structure has been modified for improved time estimation and similarity searching. Additional options (frame-rate and movie length) are offered to allow users further control over the movies they create and the duration option has been moved to a more obvious location.

Let us know what you think, or if you have any suggestions. Feedback is always welcome.

**RELEASE NOTES:**

[Helioviewer.2.3.0](https://launchpad.net/helioviewer.org/+milestone/2.3.0) includes several new features to give users more control over how the site behaves. Let us know what you think, or if you have any suggestions. Feedback is always welcome.

_**New features:**_

* JSONP support  
* Added option display date from last visit when returning to Helioviewer.org  
* Added setting to automatically update images every 5 minutes  
* Added support for embedding Helioviewer.org in other websites  
* Added support for specifying frame-rate or duration during movie creation  
* Added support for PROBA-2 SWAP data  
* Created an installer diagnostic script  
* Added support for tracking custom events in Google Analytics  
* Movie and screenshot selection rectangle preserved during visit  
* Data availability information included in getDateSources response

_**Bug fixes:**_

* Fixed [bug #691356](https://bugs.launchpad.net/helioviewer.org/+bug/691356) JPX Summary file does not exist  
* Fixed [bug #783497](https://bugs.launchpad.net/helioviewer.org/+bug/783497) Port Helioqueuer to PHP  
* Fixed [bug #903360](https://bugs.launchpad.net/helioviewer.org/+bug/903360) Error occurs for certain layer orders when attempting to create AIA/LASCO  
* Fixed [bug #925542](https://bugs.launchpad.net/helioviewer.org/+bug/925542) The minimum width of the display window is too big  
* Fixed [bug #624857](https://bugs.launchpad.net/helioviewer.org/+bug/624857) After clicking &#8220;clear history&#8221; unfinished requests are still processed, and download links displayed  
* Fixed [bug #885795](https://bugs.launchpad.net/helioviewer.org/+bug/885795) Add image attribution to about dialog  
* Fixed [bug #888269](https://bugs.launchpad.net/helioviewer.org/+bug/888269) Attempt to normalize movie frame-rate instead of duration when possible  
* Fixed [bug #909795](https://bugs.launchpad.net/helioviewer.org/+bug/909795) Normalize date strings for API requests  
* Fixed [bug #909897](https://bugs.launchpad.net/helioviewer.org/+bug/909897) Mark movies that have not finished in less than x hours as Error  
* Fixed [bug #930628](https://bugs.launchpad.net/helioviewer.org/+bug/930628) Improve movie creation time estimation  
* Fixed [bug #942547](https://bugs.launchpad.net/helioviewer.org/+bug/942547) Validate value for dsun before attempting to process in front-side  
* Fixed [bug #609219](https://bugs.launchpad.net/helioviewer.org/+bug/609219) API should return an error message when an invalid parameter is specified in a request  
* Fixed [bug #783481](https://bugs.launchpad.net/helioviewer.org/+bug/783481) Report mouse coordinates immediately upon activation  
* Fixed [bug #787744](https://bugs.launchpad.net/helioviewer.org/+bug/787744) Add a checkSettings method to the UserSettings class to verify user settings integrity  
* Fixed [bug #876707](https://bugs.launchpad.net/helioviewer.org/+bug/876707) Included creation_time in FFmpeg metadata for mp4/webm movies  
* Fixed [bug #789515](https://bugs.launchpad.net/helioviewer.org/+bug/789515) Reduce filesize of WebM movies

_**Library updates:**_

* Flowplayer (3.2.7 => 3.2.8)  
* jQuery (1.7.0 => 1.7.2)  
* jQuery UI (1.8.16 => 1.8.18)  
* jQuery.JSON (2.2 => 2.3)  
* jQuery imgAreaSelect (0.9.5 => 0.9.8)

