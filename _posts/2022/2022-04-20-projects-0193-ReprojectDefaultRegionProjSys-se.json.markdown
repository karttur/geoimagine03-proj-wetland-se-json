---
layout: article
title: 0193-ReprojectDefaultRegionProjSys-se.json
categories: projects
excerpt:  Import Sweden national boundaries by reprojection from system default **
tags:: 
    - 0193-ReprojectDefaultRegionProjSys-se.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0193 ReprojectDefaultRegionProjSys se.json (projects)

##  Import Sweden national boundaries by reprojection from system default **

The json command file <span class='file'>0193-ReprojectDefaultRegionProjSys-se.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
