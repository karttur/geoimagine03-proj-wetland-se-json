---
layout: article
title: 0193-ReprojectDefaultRegionProjSys-se.json
categories: sewetland
excerpt:  Import Sweden national boundaries by reprojection from system default **
tags:: 
    - 0193-ReprojectDefaultRegionProjSys-se
date: 2022-10-05
modified: 2022-10-05
comments: true
share: true
---

# 0193 ReprojectDefaultRegionProjSys se (projects)

##  Import Sweden national boundaries by reprojection from system default **

The json command file <span class='file'>0193-ReprojectDefaultRegionProjSys-se.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "startyear": 2014,
    "endyear": 2014
  },
  "process": [
    {
      "processid": "ReprojectDefaultRegionProjSys",
      "overwrite": false,
      "parameters": {
        "src_defregid": "se"
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "shp"
      },
      "srccomp": [
        {
          "se": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@100m"
          }
        }
      ],
      "dstcopy": [
        {
          "se": {
            "source": "copy",
            "product": "copy",
            "content": "copy",
            "layerid": "copy",
            "prefix": "copy",
            "suffix": "tol@100m"
          }
        }
      ]
    }
  ]
}
```
