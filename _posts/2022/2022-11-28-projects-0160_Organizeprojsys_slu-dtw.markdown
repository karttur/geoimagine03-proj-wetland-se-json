---
layout: article
title: 0160_Organizeprojsys_slu-dtw.json
categories: sewetland
excerpt:  Organise depth to water 
tags:: 
    - 0160_Organizeprojsys_slu-dtw
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0160 Organizeprojsys slu dtw (projects)

##  Organise depth to water 

The json command file <span class='file'>0160_Organizeprojsys_slu-dtw.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "OrganizeProjSysData",
      "overwrite": false,
      "parameters": {
        "importcode": "vrt",
        "epsg": "3006",
        "orgid": "SLU",
        "dsname": "dtw",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 depth to water SLU",
        "label": "SWEREF99 depth to water SLU"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "vrt"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "vrt"
      },
      "srcraw": [
        {
          "dtw": {
            "datadir": "ancillary/SLU/region/soilmoisture/global/0",
            "datafile": "dtw_slu-soilmoisture_global_0_v01-2020",
            "datalayer": "diken",
            "title": "SWEREF99 depth to water SLU",
            "label": "SWEREF99 depth to water SLU"
          }
        }
      ],
      "dstcomp": [
        {
          "dtw": {
            "source": "SLU",
            "product": "slu-soilmoisture",
            "content": "soilmoisture",
            "layerid": "dtw",
            "prefix": "dtw",
            "suffix": "v01-2020",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "cm",
            "celltype": "Int16",
            "cellnull": -1,
            "measure": "R",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
