---
layout: article
title: 0122_BBoxTiledRawData_slu-diken.json
categories: projects
excerpt:  Create vector bounding boxes for the 1 m ditch tiles
tags:: 
    - 0122_BBoxTiledRawData_slu-diken.json
date: 2022-04-21
modified: 2022-04-21
comments: true
share: true
---

# 0122 BBoxTiledRawData slu diken.json (projects)

##  Create vector bounding boxes for the 1 m ditch tiles

The json command file <span class='file'>0122_BBoxTiledRawData_slu-diken.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "srcdir": "DOWNLOADS/skogsstyrelsen/opendata/DikenRaster_1m/image",
        "dstdir": "DOWNLOADS/skogsstyrelsen/opendata/DikenRaster_1m/tiles"
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "shp"
      }
    }
  ]
}
```
