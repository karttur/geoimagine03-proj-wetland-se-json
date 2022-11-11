---
layout: article
title: 0180_TileProjSysRegion_metria-DEM_10m-mean.json
categories: sewetland
excerpt:  Tile DEM to sweref while resampling to m average resolution 
tags:: 
    - 0180_TileProjSysRegion_metria-DEM_10m-mean
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0180 TileProjSysRegion metria DEM 10m mean (projects)

##  Tile DEM to sweref while resampling to m average resolution 

The json command file <span class='file'>0180_TileProjSysRegion_metria-DEM_10m-mean.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
          "dem_mean-10m": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "raw"
          }
        }
      ],
      "dstcopy": [
        {
          "dem_mean-10m": {
            "srccomp": "dem_dem2m",
            "suffix": "mean-10m"
          }
        }
      ]
    }
  ]
}
```
