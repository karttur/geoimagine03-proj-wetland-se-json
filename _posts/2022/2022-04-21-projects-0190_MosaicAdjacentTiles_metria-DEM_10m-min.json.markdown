---
layout: article
title: 0190_MosaicAdjacentTiles_metria-DEM_10m-min.json
categories: projects
excerpt: 
tags:: 
    - 0190_MosaicAdjacentTiles_metria-DEM_10m-min.json
date: 2022-04-21
modified: 2022-04-21
comments: true
share: true
---

# 0190 MosaicAdjacentTiles metria DEM 10m min.json (projects)

## 

The json command file <span class='file'>0190_MosaicAdjacentTiles_metria-DEM_10m-min.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "overwrite": true,
      "parameters": {
        "tr_xres": 10,
        "tr_yres": 10,
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
          "dem_min-10m": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "min-10m"
          }
        }
      ],
      "dstcopy": [
        {
          "dem_min-10m": {
            "srccomp": "dem_dem2m"
          }
        }
      ]
    }
  ]
}
```
