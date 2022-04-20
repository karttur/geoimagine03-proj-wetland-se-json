---
layout: article
title: 0199-Linkdefaultregiontiles-sweref.json
categories: projects
excerpt:  Link Sweden national boundary to project default tiles
tags:: 
    - 0199-Linkdefaultregiontiles-sweref.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0199 Linkdefaultregiontiles sweref.json (projects)

##  Link Sweden national boundary to project default tiles

The json command file <span class='file'>0199-Linkdefaultregiontiles-sweref.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "LinkDefaultRegionTiles",
      "overwrite": true,
      "version": "0.9",
      "parameters": {
        "defregmask": "global",
        "regioncat": "global",
        "srcepsgL": "3006",
        "onlyregionsfullywithinsystem": false
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
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@100m"
          }
        }
      ]
    }
  ]
}
```
