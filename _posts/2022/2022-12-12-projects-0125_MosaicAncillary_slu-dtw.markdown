---
layout: article
title: 0125_MosaicAncillary_slu-dtw.json
categories: sewetland
excerpt:  Mosaic depth to water tiles 
tags:: 
    - 0125_MosaicAncillary_slu-dtw
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0125 MosaicAncillary slu dtw (projects)

##  Mosaic depth to water tiles 

The json command file <span class='file'>0125_MosaicAncillary_slu-dtw.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "ancillary"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "MosaicAncillary",
      "overwrite": false,
      "parameters": {
        "getlist": "oswalk",
        "srcdir": "DOWNLOADS/skogsstyrelsen/SLUMarkfuktighet-DTW/images"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "vrt"
      },
      "dstcomp": [
        {
          "dtw": {
            "source": "SLU",
            "product": "slu-soilmoisture",
            "content": "soilmoisture",
            "layerid": "dtw",
            "prefix": "dtw",
            "suffix": "v01-2020"
          }
        }
      ]
    }
  ]
}
```
