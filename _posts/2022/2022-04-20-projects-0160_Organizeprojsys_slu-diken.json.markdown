---
layout: article
title: 0160_Organizeprojsys_slu-diken.json
categories: projects
excerpt:  Import 1 m ditch tiles 
tags:: 
    - 0160_Organizeprojsys_slu-diken.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0160 Organizeprojsys slu diken.json (projects)

##  Import 1 m ditch tiles 

The json command file <span class='file'>0160_Organizeprojsys_slu-diken.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
        "dsname": "diken1m",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 diken 1m SLU",
        "label": "SWEREF99 diken 1m SLU"
      },
      "srcpath": {
        "volume": "Ancillary",
        "hdr": "vrt"
      },
      "dstpath": {
        "volume": "Ancillary",
        "hdr": "vrt"
      },
      "srcraw": [
        {
          "diken": {
            "datadir": "ancillary/SLU/region/diken/global/0",
            "datafile": "diken1m_diken_global_0_v01-2021-full",
            "datalayer": "diken",
            "title": "diken1m_diken_sweref_0_v01-2021-full",
            "label": "diken1m_diken_sweref_0_v01-2021-full"
          }
        }
      ],
      "dstcomp": [
        {
          "diken": {
            "source": "SLU",
            "product": "diken",
            "content": "diken",
            "layerid": "diken1m",
            "prefix": "diken1m",
            "suffix": "v01-2021",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boolean",
            "celltype": "Byte",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
