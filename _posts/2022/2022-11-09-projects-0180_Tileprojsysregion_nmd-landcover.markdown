---
layout: article
title: 0180_Tileprojsysregion_nmd-landcover.json
categories: sewetland
excerpt:  tile Metria NMD landcover to sweref 
tags:: 
    - 0180_Tileprojsysregion_nmd-landcover
date: 2022-11-09
modified: 2022-11-09
comments: true
share: true
---

# 0180 Tileprojsysregion nmd landcover (projects)

##  tile Metria NMD landcover to sweref 

The json command file <span class='file'>0180_Tileprojsysregion_nmd-landcover.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "timestep": "singleyear",
    "startyear": 2018,
    "endyear": 2018
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
        "resample": "near",
        "asscript": true
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
          "nmdbas": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-base",
            "prefix": "nmd-base",
            "suffix": "v1-1"
          }
        },
        {
          "nmdbete": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-bete",
            "prefix": "nmd-bete",
            "suffix": "v1"
          }
        },
        {
          "nmdkraftledning": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-kraftled",
            "prefix": "nmd-kraftled",
            "suffix": "v1"
          }
        },
        {
          "nmdanlagda": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-anlagda-ytor",
            "prefix": "nmd-anlagda-ytor",
            "suffix": "v1"
          }
        },
        {
          "nmdfjaellskog": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-fjaellskog",
            "prefix": "nmd-fjaellskog",
            "suffix": "v1"
          }
        }
      ],
      "dstcopy": [
        {
          "nmdbas": {
            "srccomp": "landcover-nmd-base"
          }
        },
        {
          "nmdbete": {
            "srccomp": "landcover-nmd-bete"
          }
        },
        {
          "nmdkraftledning": {
            "srccomp": "landcover-nmd-kraftled"
          }
        },
        {
          "nmdanlagda": {
            "srccomp": "landcover-nmd-anlagda-ytor"
          }
        },
        {
          "nmdfjaellskog": {
            "srccomp": "landcover-nmd-fjaellskog"
          }
        }
      ]
    }
  ]
}
```
