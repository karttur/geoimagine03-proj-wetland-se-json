---
layout: article
title: 0120_UnZipRawData_SMHI-SVAR.json
categories: projects
excerpt:  UnZip SMHI SVAR data 
tags:: 
    - 0120_UnZipRawData_SMHI-SVAR.json
date: 2022-04-21
modified: 2022-04-21
comments: true
share: true
---

# 0120 UnZipRawData SMHI SVAR.json (projects)

##  UnZip SMHI SVAR data 

The json command file <span class='file'>0120_UnZipRawData_SMHI-SVAR.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "srcdir": "DOWNLOADS/SMHI/SVAR/data",
        "dstdir": "DOWNLOADS/SMHI/SVAR/data",
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
