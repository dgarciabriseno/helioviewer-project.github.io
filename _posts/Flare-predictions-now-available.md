---
title: Flare predictions now available
date: 2023-04-10T12:00:00-05:00
author: Jack
layout: post
permalink: /2023/04/10/Flare-predictions-now-available/
categories:
  - General
---
Solar flare predictions provided by the  [Community Coordinated Modeling Center](https://ccmc.gsfc.nasa.gov/) (CCMC) are now available on helioviewer.org.

They can be found by clicking on _Data Sources > Features and Events > CCMC_.

![fp_where_to_find](https://user-images.githubusercontent.com/983575/231274256-875e4387-d833-4fca-a812-cb7803447258.png)

The CCMC is a multi-agency partnership enabling, supporting, and performing research and development for next-generation space science and space weather models. The CCMC [collects flare predictions](https://ccmc.gsfc.nasa.gov/scoreboards/flare/) based on a number of different algorithms and makes them available via an API and [their own browsing tools](https://iswa.gsfc.nasa.gov/IswaSystemWebApp/index.jsp?i_1=606&l_1=7&t_1=33&w_1=1721&h_1=865&s_1=0).

Each flare prediction shows the probability of GOES C, M and X flares
in the local area of the pin. 

![fp_pin](https://user-images.githubusercontent.com/983575/231274356-1d547859-bff8-4b33-a18d-238f89f58311.png)


Clicking on the pin itself pops up a window with a little more detail

![fp_popup](https://user-images.githubusercontent.com/983575/231274395-86ab2f0b-045c-4067-b5ed-1b4aba617f60.png)


Clicking on "View source data" brings up a larger window that shows the complete data associated with that particular flare prediction

![fp_view_source_data](https://user-images.githubusercontent.com/983575/231274461-b70a0e7d-ba8c-44a6-ab0c-9720bdc3e7fb.png)

You can also overlay features and events from the HEK. Here is [an example showing HEK Eruption, AMOS V1 REGIONS, and ASAP 1 REGIONS results overlaid on an AIA image](https://helioviewer.org/?date=2023-03-22T19:15:05.000Z&imageScale=2.42044088&centerX=-116.18116224&centerY=4.84088176&imageLayers=%5BSDO,AIA,171,1,100,0,60,1,2023-04-07T10:35:29.000Z.000Z.000Z%5D&eventLayers=%5BER,EruptionPatrol,1%5D,%5BFP,AMOS_v1_REGIONS;ASAP_1_REGIONS,1%5D&eventLabels=true&celestialBodies=%7B%22soho%22:%5B%22soho-mercury-tree-label%22,%22soho-venus-tree-label%22,%22soho-saturn-tree-label%22%5D,%22stereo_a%22:%5B%5D,%22stereo_b%22:%5B%5D%7D)

<img width="500" alt="Screen Shot 2023-04-11 at 16 18 16" src="https://user-images.githubusercontent.com/983575/231279903-5c4ce168-d9ce-47a2-abd5-0369338f64ab.png">


A small note about the display of flare prediction results. Since flares occur in active regions, the flare prediction pins wll often overlay each other
and other HEK information for active regions. Mousing over the result type you want will highlight the particular HEK or Flare Prediction pins shown.

For example, in this example, the mouse is over _HEK > Eruption > EruptionPatrol_ and only those results are shown:

<img width="500" alt="Screen Shot 2023-04-11 at 16 17 34" src="https://user-images.githubusercontent.com/983575/231279799-0af630cc-ca84-4349-b669-7e535748121e.png">

Similarly, we can show the ASAP 1 REGIONS results only by mousing-over _CCMC > Flare predictions > ASAP 1 REGIONS_ .

<img width="500" alt="Screen Shot 2023-04-11 at 16 18 00" src="https://user-images.githubusercontent.com/983575/231280301-597c51fe-0958-428d-a0e0-2056792a46bc.png">


If you have any questions or comments regarding flare predictions, please [send us an
email](mailto:HelioViewerDevelopment@nasa.onmicrosoft.com) or [file an
issue on the Helioviewer.org project page](https://github.com/Helioviewer-Project/helioviewer.org/issues).
