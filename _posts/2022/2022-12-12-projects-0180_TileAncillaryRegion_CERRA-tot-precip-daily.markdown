---
layout: article
title: 0180_TileAncillaryRegion_CERRA-tot-precip-daily.json
categories: sewetland
excerpt:  tile CERRA climate data 
tags:: 
    - 0180_TileAncillaryRegion_CERRA-tot-precip-daily
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0180 TileAncillaryRegion CERRA tot precip daily (projects)

##  tile CERRA climate data 

The json command file <span class='file'>0180_TileAncillaryRegion_CERRA-tot-precip-daily.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "TileAncillaryRegion",
      "version": "1.3",
      "overwrite": false,
      "parameters": {
        "src_defregid": "europe",
        "tr_xres": 5500,
        "tr_yres": 5500,
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
          "precip": {
            "source": "c3s",
            "product": "cerra",
            "content": "precip",
            "layerid": "tot-precip-kgm2",
            "prefix": "tot-precip-kgm2",
            "suffix": "v2022"
          }
        }
      ],
      "dstcopy": [
        {
          "precip": {
            "srccomp": "precip_tot-precip-kgm2"
          }
        }
      ]
    }
  ]
}
```
