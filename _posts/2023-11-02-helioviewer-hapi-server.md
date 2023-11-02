---
title: HAPI with Helioviewer
date: 2023-11-02T00:00:00-05:00
author: Daniel Garcia Briseno
layout: post
permalink: /2023/11/02/hapi
categories:
  - General
---

Helioviewer supports HAPI for listing images and some image metadata.

[Helioviewer's HAPI interface](https://api.helioviewer.org/hapi/)

# What is HAPI?

[HAPI](https://hapi-server.github.io/) stands for Heliophysics Data Application Programmer’s Interface.
It is a modern API that makes it very simple to deliver time series data to applications.
You can interact with HAPI directly from the browser or within a programming language.

## Using HAPI

You could use the [HAPI Interface](https://api.helioviewer.org/hapi/) to browse
the image datasets available from Helioviewer.
(You could also do this on [Helioviewer.org](https://helioviewer.org) since all image datasets are retrievable with HAPI.)

Below are examples of using HAPI with Python and JavaScript.
You can find a list of officially supported clients [here](https://github.com/hapi-server/?q=client-&type=all).

If your desired language isn't supported, you can review the [API specification](https://github.com/hapi-server/data-specification)
to write a new client.

### With Python
```python
>>> from hapiclient import hapi
>>> data, meta = hapi(
...     "https://api.helioviewer.org/hapi/helioviewer/hapi",
...     "AIA_304",
...     "url",
...     "2023-01-01T00:00:00Z",
...     "2023-01-01T23:59:59Z"
... )
>>> print(data)
[(b'2023-01-01T00:00:05Z', 'https://helioviewer.org/jp2/AIA/2023/01/01/304/2023_01_01__00_00_05_129__SDO_AIA_AIA_304.jp2')
 (b'2023-01-01T00:00:41Z', 'https://helioviewer.org/jp2/AIA/2023/01/01/304/2023_01_01__00_00_41_131__SDO_AIA_AIA_304.jp2')
 (b'2023-01-01T00:01:17Z', 'https://helioviewer.org/jp2/AIA/2023/01/01/304/2023_01_01__00_01_17_130__SDO_AIA_AIA_304.jp2')
 ...
 (b'2023-01-01T23:58:17Z', 'https://helioviewer.org/jp2/AIA/2023/01/01/304/2023_01_01__23_58_17_132__SDO_AIA_AIA_304.jp2')
 (b'2023-01-01T23:58:53Z', 'https://helioviewer.org/jp2/AIA/2023/01/01/304/2023_01_01__23_58_53_131__SDO_AIA_AIA_304.jp2')
 (b'2023-01-01T23:59:29Z', 'https://helioviewer.org/jp2/AIA/2023/01/01/304/2023_01_01__23_59_29_140__SDO_AIA_AIA_304.jp2')]
```

### With JavaScript
```javascript
// Include hapi-0.0.1.js from https://github.com/hapi-server/client-javascript
// <script src="hapi-0.0.1.js"></script>
hapi("https://api.helioviewer.org/hapi/helioviewer/hapi",
     "AIA_304",
     "url",
     "2023-01-01T00:00:00Z",
     "2023-01-01T23:59:59Z",
     (data, meta) => {
        console.log(data);
     }
);
/**
 * {
 *  Time: ["2023-01-01T00:00:05Z", "2023-01-01T00:00:41Z"...]
 *  url: ["https://helioviewer.org/jp2/AIA/2023/01/01/304/2023_01_01__00_00_05_129__SDO_AIA_AIA_304.jp2"...]
 * }
 */
```