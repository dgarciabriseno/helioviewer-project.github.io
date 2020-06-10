---
id: 1403
title: Warning concerning Helioviewer.org Movie and Screenshot Histories
date: 2016-09-23T15:18:30+00:00
author: jack
layout: post
guid: http://blog.helioviewer.org/?p=1403
permalink: /2016/09/23/warning-concerning-helioviewer-org-movie-and-screenshot-histories/
categories:
  - Helioviewer.org
  - News
---
Helioviewer.org is moving to using [HTTPS](https://en.wikipedia.org/wiki/HTTPS) instead of [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol).  This means that <span class="_Tgc">all communications between your browser and helioviewer.org are encrypted. The switch to using HTTPS only will happen on September 30th.  An unfortunate side effect of this is that your helioviewer.org movie and screenshot histories will be lost.  This is due to security features in your browser, which are explained below.<br /> </span>

Helioviewer.org uses the HTML5 [LocalStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) property to store your links to the movies on your computer.  [LocalStorage](https://en.wikipedia.org/wiki/Web_storage) does not allow data from a regular HTTP page (for example <http://htmlui.com>{.}) to be accessed by pages served from its HTTPS version (for example, <https://htmlui.com>{.}, and vice versa.  This is done to improve security; for example, you want to isolate values created during a secure session from unsecured sessions.  The practical effect of this security is that when we switch to using HTTPS, the histories created when helioviewer.org was using HTTP cannot be accessed by your web browser when helioviewer.org starts to use HTTPS.  So your movie and screenshot histories will not be viewable in helioviewer.org.

The switch to using HTTPS does not affect any movie links to helioviewer.org.  If you have a link for example, <http://helioviewer.org/?movieId=KSJd5> , then the server will automatically switch to using the secure version, <https://helioviewer.org/?movieId=KSJd5> .  Please make a note of any movie links you want to keep a hold of.

We apologize for any inconvenience this may cause.  If you have questions concerning the change from HTTP to HTTPS, please let us know.


