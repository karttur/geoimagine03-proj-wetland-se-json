---
layout: article
title: 0125_MosaicAncillary_slu-diken-05m.json
categories: sewetland
excerpt:  Mosaic 0.5 m ditch tiles 
tags:: 
    - 0125_MosaicAncillary_slu-diken-05m
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0125 MosaicAncillary slu diken 05m (projects)

##  Mosaic 0.5 m ditch tiles 

The json command file <span class='file'>0125_MosaicAncillary_slu-diken-05m.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "srcdir": "DOWNLOADS/skogsstyrelsen/DikenRaster_05m/image"
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
          "dikesraster1m": {
            "source": "SLU",
            "product": "slu-dem-ml",
            "content": "diken",
            "layerid": "diken1m",
            "prefix": "diken05m",
            "suffix": "v01-2021"
          }
        }
      ]
    }
  ]
}
```
