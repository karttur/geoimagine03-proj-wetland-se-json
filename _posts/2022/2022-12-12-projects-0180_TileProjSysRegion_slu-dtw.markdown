---
layout: article
title: 0180_TileProjSysRegion_slu-dtw.json
categories: sewetland
excerpt:  tile depth to water 
tags:: 
    - 0180_TileProjSysRegion_slu-dtw
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0180 TileProjSysRegion slu dtw (projects)

##  tile depth to water 

The json command file <span class='file'>0180_TileProjSysRegion_slu-dtw.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur-sweref",
    "tractid": "karttur-sweref",
    "siteid": "*",
    "plotid": "*",
    "system": "sweref"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "TileProjSysRegion",
      "version": "1.3",
      "overwrite": false,
      "parameters": {
        "src_defregid": "sweref",
        "tr_xres": 10,
        "tr_yres": 10,
        "dstnodata": -1,
        "resample": "average",
        "asscript": true
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "vrt"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srccomp": [
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
      ],
      "dstcopy": [
        {
          "dtw": {
            "srccomp": "soilmoisture-dtw",
            "suffix": "v01-2020-10m"
          }
        }
      ]
    }
  ]
}
```
