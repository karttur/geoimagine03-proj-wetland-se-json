---
layout: article
title: 0160-organize-Metria-markfuktighetsindex.json
categories: sewetland
excerpt:  organize Metria soil moisture (markfuktighetsindex) 
tags:: 
    - 0160-organize-Metria-markfuktighetsindex
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0160 organize Metria markfuktighetsindex (projects)

##  organize Metria soil moisture (markfuktighetsindex) 

The json command file <span class='file'>0160-organize-Metria-markfuktighetsindex.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "OrganizeProjSysData",
      "overwrite": false,
      "parameters": {
        "importcode": "ige",
        "epsg": "3006",
        "orgid": "Metria",
        "dsname": "markfuktighetsindex",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 Metria markfuktighetsindex",
        "label": "SWEREF99 Metria markfuktighetsindex"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "img",
        "dat": "ige"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srcraw": [
        {
          "markfuktighetsindex": {
            "datadir": "DOWNLOADS/Metria/markdata/data/Markfuktighetsindex_NMD_Sverige",
            "datafile": "Markfuktighetsindex_NMD",
            "datalayer": "Markfuktighetsindex_NMD",
            "title": "Markfuktighetsindex NMD 2018",
            "label": "Markfuktighetsindex NMD 2018"
          }
        }
      ],
      "dstcomp": [
        {
          "markfuktighetsindex": {
            "source": "metria",
            "product": "markfuktighetsindex",
            "content": "soilmoisture",
            "layerid": "soilmoisture-nmd",
            "prefix": "soilmoisture-nmd",
            "suffix": "v1-10m",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "idnex",
            "celltype": "Float32",
            "cellnull": -3.40282e+38,
            "measure": "I",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
