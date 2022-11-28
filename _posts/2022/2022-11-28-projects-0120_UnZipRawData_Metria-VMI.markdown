---
layout: article
title: 0120_UnZipRawData_Metria-VMI.json
categories: sewetland
excerpt:  Unzip Metria VMI datasets 
tags:: 
    - 0120_UnZipRawData_Metria-VMI
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0120 UnZipRawData Metria VMI (projects)

##  Unzip Metria VMI datasets 

The json command file <span class='file'>0120_UnZipRawData_Metria-VMI.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "ancillary"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "UnZipRawData",
      "overwrite": false,
      "parameters": {
        "srcdir": "DOWNLOADS/Metria/VMI/data",
        "dstdir": "DOWNLOADS/Metria/VMI/data",
        "getlist": "oswalk",
        "pattern": "*",
        "zipreplace": ".*",
        "minlon": -180,
        "maxlon": 180,
        "minlat": -90,
        "maxlat": 90
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "zip"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "*"
      }
    }
  ]
}
```
