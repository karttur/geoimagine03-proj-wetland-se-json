---
layout: article
title: 0180_Tileprojsysregion_metria-DEM_10m-mean.json
categories: projects
excerpt:  tile to 10 m average of 25 cells
tags:: 
    - 0180_Tileprojsysregion_metria-DEM_10m-mean.json
date: 2022-04-21
modified: 2022-04-21
comments: true
share: true
---

# 0180 Tileprojsysregion metria DEM 10m mean.json (projects)

##  tile to 10 m average of 25 cells

The json command file <span class='file'>0180_Tileprojsysregion_metria-DEM_10m-mean.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "volume": "Arctic2021",
        "hdr": "vrt"
      },
      "dstpath": {
        "volume": "Arctic2021",
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
