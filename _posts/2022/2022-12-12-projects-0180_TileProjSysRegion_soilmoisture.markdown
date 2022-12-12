---
layout: article
title: 0180_TileProjSysRegion_soilmoisture.json
categories: sewetland
excerpt:  tile soilmoisture to sweref 
tags:: 
    - 0180_TileProjSysRegion_soilmoisture
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0180 TileProjSysRegion soilmoisture (projects)

##  tile soilmoisture to sweref 

The json command file <span class='file'>0180_TileProjSysRegion_soilmoisture.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "dstnodata": 255,
        "resample": "average",
        "asscript": true
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srccomp": [
        {
          "soilmoisture": {
            "source": "slu",
            "product": "slu-ml",
            "content": "sm-percent",
            "layerid": "soilmoisture",
            "prefix": "soilmoisture",
            "suffix": "v01-2021-2m",
            "cellnull": 255
          }
        },
        {
          "soilmoistureclasses": {
            "source": "slu",
            "product": "slu-ml",
            "content": "sm-class",
            "layerid": "soilmoistureclasses",
            "prefix": "soilmoistureclasses",
            "suffix": "v01-2021-2m",
            "cellnull": 255
          }
        }
      ],
      "dstcopy": [
        {
          "soilmoisture": {
            "srccomp": "sm-percent_soilmositre",
            "suffix": "v01-2021-10m-mean"
          }
        },
        {
          "soilmoistureclasses": {
            "srccomp": "sm-class_soilmoistureclasses",
            "suffix": "v01-2021-10m-mean"
          }
        }
      ]
    }
  ]
}
```
