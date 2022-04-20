---
layout: article
title: 0115-download-SMHI-SVAR.json
categories: projects
excerpt:  Download SMHI SVAR data 
tags:: 
    - 0115-download-SMHI-SVAR.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0115 download SMHI SVAR.json (projects)

##  Download SMHI SVAR data 

The json command file <span class='file'>0115-download-SMHI-SVAR.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "DownloadAncillary",
      "overwrite": false,
      "parameters": {
        "downloadcode": "filelist",
        "path": "DOWNLOADS/SMHI/SVAR/SMHI-SVAR-Svenskt_vattenarkiv.txt",
        "datadir": "DOWNLOADS/SMHI/SVAR/data"
      },
      "srcpath": {
        "volume": "GeoImg2021"
      },
      "dstpath": {
        "volume": "GeoImg2021"
      }
    }
  ]
}
```
