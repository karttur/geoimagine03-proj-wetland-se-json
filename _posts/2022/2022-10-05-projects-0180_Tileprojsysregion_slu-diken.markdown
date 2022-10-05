---
layout: article
title: 0180_Tileprojsysregion_slu-diken.json
categories: sewetland
excerpt:  tile 1 m ditch to sweref 
tags:: 
    - 0180_Tileprojsysregion_slu-diken
date: 2022-10-05
modified: 2022-10-05
comments: true
share: true
---

# 0180 Tileprojsysregion slu diken (projects)

##  tile 1 m ditch to sweref 

The json command file <span class='file'>0180_Tileprojsysregion_slu-diken.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
            "product": "diken",
            "content": "diken",
            "layerid": "diken1m",
            "prefix": "diken1m",
            "suffix": "v01-2021",
            "cellnull": -32767
          }
        }
      ],
      "dstcopy": [
        {
          "diken": {
            "srccomp": "slu_diken1m",
            "suffix": "v01-2021-10m-sum"
          }
        }
      ]
    }
  ]
}
```
