---
layout: article
title: 0180_Tileprojsysregion_slu-diken.json
categories: projects
excerpt:  tile 1 m ditch to sweref 
tags:: 
    - 0180_Tileprojsysregion_slu-diken.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0180 Tileprojsysregion slu diken.json (projects)

##  tile 1 m ditch to sweref 

The json command file <span class='file'>0180_Tileprojsysregion_slu-diken.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
        "tr_xres": 2,
        "tr_yres": 2,
        "dstnodata": 255,
        "resample": "near",
        "asscript": true
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "vrt"
      },
      "dstpath": {
        "volume": "GeoImg2021",
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
            "srccomp": "slu_diken1m"
          }
        }
      ]
    }
  ]
}
```
