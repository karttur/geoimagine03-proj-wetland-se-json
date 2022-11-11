---
layout: article
title: 0190_MosaicAdjacentTiles_metria-DEM_10m-min.json
categories: sewetland
excerpt:  Create min DEM virtual overlap mosaics for each original tile
tags:: 
    - 0190_MosaicAdjacentTiles_metria-DEM_10m-min
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0190 MosaicAdjacentTiles metria DEM 10m min (projects)

##  Create min DEM virtual overlap mosaics for each original tile

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
      "overwrite": false,
      "parameters": {
        "tr_xres": 10,
        "tr_yres": 10,
        "resample": "near",
        "asscript": true
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
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
