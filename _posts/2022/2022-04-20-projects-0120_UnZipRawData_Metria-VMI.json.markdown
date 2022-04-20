---
layout: article
title: 0120_UnZipRawData_Metria-VMI.json
categories: projects
excerpt:  Unzip Metria VMI datasets 
tags:: 
    - 0120_UnZipRawData_Metria-VMI.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0120 UnZipRawData Metria VMI.json (projects)

##  Unzip Metria VMI datasets 

The json command file <span class='file'>0120_UnZipRawData_Metria-VMI.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
        "volume": "GeoImg2021",
        "hdr": "zip"
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "*"
      }
    }
  ]
}
```
