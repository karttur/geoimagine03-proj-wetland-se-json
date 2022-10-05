---
layout: article
title: 0200_RenameDataset_slu-diken.json
categories: sewetland
excerpt:  Rename the 1 m ditch dataset 
tags:: 
    - 0200_RenameDataset_slu-diken
date: 2022-10-05
modified: 2022-10-05
comments: true
share: true
---

# 0200 RenameDataset slu diken (projects)

##  Rename the 1 m ditch dataset 

The json command file <span class='file'>0200_RenameDataset_slu-diken.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "RenameTileDataset",
      "version": "1.3",
      "overwrite": false,
      "parameters": {
        "asscript": false
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
          "diken": {
            "source": "slu",
            "product": "diken",
            "content": "diken",
            "layerid": "diken1m",
            "prefix": "diken1m",
            "suffix": "v01-2021"
          }
        }
      ],
      "dstcopy": [
        {
          "diken": {
            "srccomp": "slu_diken1m",
            "layerid": "diken1m",
            "suffix": "v01-2021-10m-sum"
          }
        }
      ]
    }
  ]
}
```
