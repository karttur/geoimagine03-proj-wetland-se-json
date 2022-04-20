---
layout: article
title: 0115-download-Metria-markdata.json
categories: projects
excerpt:  Download Metria base layers 
tags:: 
    - 0115-download-Metria-markdata.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0115 download Metria markdata.json (projects)

##  Download Metria base layers 

The json command file <span class='file'>0115-download-Metria-markdata.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
        "path": "DOWNLOADS/Metria/markdata/Metria-Svenska_markdata.txt",
        "datadir": "DOWNLOADS/Metria/markdata/data"
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
