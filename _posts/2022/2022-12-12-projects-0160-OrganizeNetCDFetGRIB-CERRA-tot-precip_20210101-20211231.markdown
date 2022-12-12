---
layout: article
title: 0160-OrganizeNetCDFetGRIB-CERRA-tot-precip_20210101-20211231.json
categories: sewetland
excerpt: 
tags:: 
    - 0160-OrganizeNetCDFetGRIB-CERRA-tot-precip_20210101-20211231
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0160 OrganizeNetCDFetGRIB CERRA tot precip 20210101 20211231 (projects)

## 

The json command file <span class='file'>0160-OrganizeNetCDFetGRIB-CERRA-tot-precip_20210101-20211231.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur-cerra-europe",
    "tractid": "karttur-cerra-europe",
    "siteid": "*",
    "plotid": "*",
    "system": "ancillary"
  },
  "period": {
    "timestep": "D",
    "startyear": 2021,
    "startmonth": 1,
    "startday": 1,
    "endyear": 2021,
    "endmonth": 12,
    "endday": 31
  },
  "process": [
    {
      "processid": "OrganizeNetCDFetGRIB",
      "overwrite": false,
      "parameters": {
        "importcode": "grib",
        "epsg": "3006",
        "orgid": "CERRA",
        "dsname": "p-tot",
        "dsversion": "1.0",
        "accessdate": "20221124",
        "regionid": "europe",
        "regioncat": "europe",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "CERRA daily total precipitation reanalysis",
        "label": "CERRA daily total precipitation reanalysis"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "grib"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srcraw": [
        {
          "p-tot": {
            "datadir": "DOWNLOADS/CERRA/tot-p",
            "datafile": "tot-p_cerra_europe_20210101-20211231_0",
            "datalayer": "p-tot",
            "title": "CERRA daily total precipitation reanalysis",
            "label": "CERRA daily total precipitation reanalysis"
          }
        }
      ],
      "dstcomp": [
        {
          "p-tot": {
            "source": "c3s",
            "product": "cerra",
            "content": "precip",
            "layerid": "tot-precip-kg*m-2",
            "prefix": "tot-precip-kg*m-2",
            "suffix": "v2022",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "kg/(m^2*s)",
            "celltype": "Float64",
            "cellnull": -32767,
            "measure": "R",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
