---
layout: article
title: 0125_MosaicAncillary_slu-diken.json
categories: sewetland
excerpt:  Mosaic 1 m ditch tiles 
tags:: 
    - 0125_MosaicAncillary_slu-diken
date: 2022-10-05
modified: 2022-10-05
comments: true
share: true
---

# 0125 MosaicAncillary slu diken (projects)

##  Mosaic 1 m ditch tiles 

The json command file <span class='file'>0125_MosaicAncillary_slu-diken.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "srcdir": "DOWNLOADS/skogsstyrelsen/opendata/DikenRaster_1m/image"
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
            "product": "diken",
            "content": "diken",
            "layerid": "diken1m",
            "prefix": "diken1m",
            "suffix": "v01-2021"
          }
        }
      ]
    }
  ]
}
```
