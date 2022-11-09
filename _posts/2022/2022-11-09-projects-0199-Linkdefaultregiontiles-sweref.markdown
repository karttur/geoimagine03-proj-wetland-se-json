---
layout: article
title: 0199-Linkdefaultregiontiles-sweref.json
categories: sewetland
excerpt:  Link Sweden national boundary to project default tiles
tags:: 
    - 0199-Linkdefaultregiontiles-sweref
date: 2022-11-09
modified: 2022-11-09
comments: true
share: true
---

# 0199 Linkdefaultregiontiles sweref (projects)

##  Link Sweden national boundary to project default tiles

The json command file <span class='file'>0199-Linkdefaultregiontiles-sweref.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
