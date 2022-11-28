---
layout: article
title: 0180_TileProjSysRegion_CERRA-tot-precip-daily.json
categories: sewetland
excerpt:  tile CERRA climate data 
tags:: 
    - 0180_TileProjSysRegion_CERRA-tot-precip-daily
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0180 TileProjSysRegion CERRA tot precip daily (projects)

##  tile CERRA climate data 

The json command file <span class='file'>0180_TileProjSysRegion_CERRA-tot-precip-daily.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "timestep": "D",
    "startyear": 2020,
    "startmonth": 1,
    "startday": 1,
    "endyear": 2020,
    "endmonth": 1,
    "endday": 31
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
        "resample": "near",
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
          "p-tot": {
            "source": "cerra",
            "product": "climate",
            "content": "precip",
            "layerid": "p-tot",
            "prefix": "p-tot",
            "suffix": "v2022"
          }
        }
      ],
      "dstcopy": [
        {
          "p-tot": {
            "srccomp": "precip_p-tot"
          }
        }
      ]
    }
  ]
}
```
