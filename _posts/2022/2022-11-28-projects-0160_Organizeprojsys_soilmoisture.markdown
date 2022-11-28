---
layout: article
title: 0160_Organizeprojsys_soilmoisture.json
categories: sewetland
excerpt:  Import soilmoisture products 
tags:: 
    - 0160_Organizeprojsys_soilmoisture
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0160 Organizeprojsys soilmoisture (projects)

##  Import soilmoisture products 

The json command file <span class='file'>0160_Organizeprojsys_soilmoisture.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "importcode": "tif",
        "epsg": "3006",
        "orgid": "SLU",
        "dsname": "soilmositure",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.skogsstyrelsen.se/sjalvservice/karttjanster/geodatatjanster/ftp/",
        "metaurl": "https://www.slu.se/institutioner/skogens-ekologi-skotsel/forskning2/markfuktighetskartor/",
        "title": "Markfuktighetsindex SLU",
        "label": "Markfuktighetsindex SLU"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srcraw": [
        {
          "soilmositure": {
            "datadir": "DOWNLOADS/skogsstyrelsen/SLUMarkfuktighetskarta",
            "datafile": "SLUMarkfuktighetskarta",
            "title": "soilmoisture_slu-ml_sweref_0_v01-2021",
            "label": "soilmoisture_slu-ml_sweref_0_v01-2021"
          }
        },
        {
          "soilmositureklassad": {
            "datadir": "DOWNLOADS/skogsstyrelsen/SLUMarkfuktighetskartaKlassad",
            "datafile": "SLUMarkfuktighetKlassad",
            "title": "soilmoisture-classes_slu-ml_sweref_0_v01-2021",
            "label": "soilmoisture-classes_slu-ml_sweref_0_v01-2021"
          }
        }
      ],
      "dstcomp": [
        {
          "soilmositure": {
            "source": "slu",
            "product": "slu-ml",
            "content": "sm-percent",
            "layerid": "soilmoisture",
            "prefix": "soilmoisture",
            "suffix": "v01-2021-2m",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "index",
            "celltype": "Byte",
            "cellnull": 255,
            "measure": "R",
            "masked": "N"
          },
          "soilmositureklassad": {
            "source": "slu",
            "product": "slu-ml",
            "content": "sm-class",
            "layerid": "soilmoistureclasses",
            "prefix": "soilmoistureclasses",
            "suffix": "v01-2021-2m",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "classes",
            "celltype": "Byte",
            "cellnull": 255,
            "measure": "O",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
