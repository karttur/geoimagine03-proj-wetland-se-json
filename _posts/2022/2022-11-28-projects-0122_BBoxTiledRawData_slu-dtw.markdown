---
layout: article
title: 0122_BBoxTiledRawData_slu-dtw.json
categories: sewetland
excerpt:  Create vector bounding boxes for the depth to groundwater (dtw) tiles 
tags:: 
    - 0122_BBoxTiledRawData_slu-dtw
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0122 BBoxTiledRawData slu dtw (projects)

##  Create vector bounding boxes for the depth to groundwater (dtw) tiles 

The json command file <span class='file'>0122_BBoxTiledRawData_slu-dtw.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "srcdir": "DOWNLOADS/skogsstyrelsen/SLUMarkfuktighet-DTW/images",
        "dstdir": "DOWNLOADS/skogsstyrelsen/SLUMarkfuktighet-DTW/tiles"
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
