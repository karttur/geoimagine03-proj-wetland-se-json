---
layout: article
title: 0190_MosaicAdjacentTiles_metria-DEM_10m-mean.json
categories: projects
excerpt: 
tags:: 
    - 0190_MosaicAdjacentTiles_metria-DEM_10m-mean.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0190 MosaicAdjacentTiles metria DEM 10m mean.json (projects)

## 

The json command file <span class='file'>0190_MosaicAdjacentTiles_metria-DEM_10m-mean.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "MosaicAdjacentTiles",
      "version": "1.3",
      "overwrite": false,
      "parameters": {
        "tr_xres": 2,
        "tr_yres": 2,
        "resample": "near",
        "asscript": true
      },
      "srcpath": {
        "volume": "Arctic2021",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "Arctic2021",
        "hdr": "vrt"
      },
      "srccomp": [
        {
          "dem_mean-10m": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "mean-10m"
          }
        }
      ],
      "dstcopy": [
        {
          "dem_mean-10m": {
            "srccomp": "dem_dem2m"
          }
        }
      ]
    }
  ]
}
```
