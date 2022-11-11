---
layout: article
title: 0122_BBoxTiledRawData_slu-diken-1m.json
categories: sewetland
excerpt:  Create vector bounding boxes for the 1 m ditch tiles 
tags:: 
    - 0122_BBoxTiledRawData_slu-diken-1m
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0122 BBoxTiledRawData slu diken 1m (projects)

##  Create vector bounding boxes for the 1 m ditch tiles 

The json command file <span class='file'>0122_BBoxTiledRawData_slu-diken-1m.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "BBoxTiledRawData",
      "dsversion": "1.3",
      "parameters": {
        "getlist": "oswalk",
        "srcdir": "DOWNLOADS/skogsstyrelsen/DikenRaster_1m/image",
        "dstdir": "DOWNLOADS/skogsstyrelsen/DikenRaster_1m/tiles"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "shp"
      }
    }
  ]
}
```
