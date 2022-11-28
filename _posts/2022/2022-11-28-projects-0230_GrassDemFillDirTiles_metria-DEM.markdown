---
layout: article
title: 0230_GrassDemFillDirTiles_metria-DEM.json
categories: sewetland
excerpt:  Fill single pits and peaks (adjacent to streams)
tags:: 
    - 0230_GrassDemFillDirTiles_metria-DEM
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0230 GrassDemFillDirTiles metria DEM (projects)

##  Fill single pits and peaks (adjacent to streams)

The json command file <span class='file'>0230_GrassDemFillDirTiles_metria-DEM.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "GrassDemFillDirTiles",
      "version": "1.3",
      "overwrite": true,
      "parameters": {
        "singlewatershed" :false,
        "tileoverlap": 200,
        "asscript": true,
        "superimpose": true,
        "pitsize": 1,
        "pitquery": "",
        "peaks": true,
        "peakquery": "nbupmax >= 500 AND nbupq3 >= 250",
        "mosaic": true
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
          "dem": {
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
          "dem": {
            "source": "copy",
            "product": "copy",
            "content": "copy",
            "layerid": "copy",
            "prefix": "copy",
            "suffix": "pfpf-mean-10m"
          }
        }
      ]
    }
  ]
}
```
