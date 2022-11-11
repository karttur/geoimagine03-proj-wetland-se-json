---
layout: article
title: 0180_TileProjSysRegion_nmd-soilmoisture.json
categories: sewetland
excerpt:  tile Metria NMD soilmoisture to sweref 
tags:: 
    - 0180_TileProjSysRegion_nmd-soilmoisture
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0180 TileProjSysRegion nmd soilmoisture (projects)

##  tile Metria NMD soilmoisture to sweref 

The json command file <span class='file'>0180_TileProjSysRegion_nmd-soilmoisture.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "timestep": "singleyear",
    "startyear": 2018,
    "endyear": 2018
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
        "dstnodata": -3.40282e+38,
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
          "nmd-soilmoisture": {
            "source": "metria",
            "product": "markfuktighetsindex",
            "content": "soilmoisture",
            "layerid": "soilmoisture-nmd",
            "prefix": "soilmoisture-nmd",
            "suffix": "v1-10m",
            "cellnull": -3.40282e+38
          }
        }
      ],
      "dstcopy": [
        {
          "nmd-soilmoisture": {
            "srccomp": "sm-percent_soilmositre",
            "suffix": "v01-2021-10m-mean"
          }
        }
      ]
    }
  ]
}
```
