---
layout: article
title: 0230_GrassDemFillDirTiles_metria-DEM.json
categories: projects
excerpt:  Fill single pits and peaks (adjacent to streams)
tags:: 
    - 0230_GrassDemFillDirTiles_metria-DEM.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0230 GrassDemFillDirTiles metria DEM.json (projects)

##  Fill single pits and peaks (adjacent to streams)

The json command file <span class='file'>0230_GrassDemFillDirTiles_metria-DEM.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
        "volume": "Arctic2021",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "Arctic2021",
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
            "suffix": "raw"
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
            "suffix": "pfpf-2m"
          }
        }
      ]
    }
  ]
}
```
