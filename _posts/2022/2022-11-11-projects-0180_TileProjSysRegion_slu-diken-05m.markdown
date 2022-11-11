---
layout: article
title: 0180_TileProjSysRegion_slu-diken-05m.json
categories: sewetland
excerpt:  tile 0.5 m ditch to sweref 
tags:: 
    - 0180_TileProjSysRegion_slu-diken-05m
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0180 TileProjSysRegion slu diken 05m (projects)

##  tile 0.5 m ditch to sweref 

The json command file <span class='file'>0180_TileProjSysRegion_slu-diken-05m.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "TileProjSysData",
      "version": "1.3",
      "overwrite": false,
      "parameters": {
        "src_defregid": "sweref",
        "tr_xres": 10,
        "tr_yres": 10,
        "dstnodata": 255,
        "resample": "sum",
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
          "diken": {
            "source": "slu",
            "product": "slu-dem-ml",
            "content": "diken",
            "layerid": "diken05m",
            "prefix": "diken05m",
            "suffix": "v01-2021",
            "cellnull": -32767
          }
        }
      ],
      "dstcopy": [
        {
          "diken": {
            "srccomp": "slu_diken05m",
            "suffix": "v01-2021-10m-sum"
          }
        }
      ]
    }
  ]
}
```
