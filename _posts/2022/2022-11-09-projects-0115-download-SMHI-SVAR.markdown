---
layout: article
title: 0115-download-SMHI-SVAR.json
categories: sewetland
excerpt:  Download SMHI SVAR data 
tags:: 
    - 0115-download-SMHI-SVAR
date: 2022-11-09
modified: 2022-11-09
comments: true
share: true
---

# 0115 download SMHI SVAR (projects)

##  Download SMHI SVAR data 

The json command file <span class='file'>0115-download-SMHI-SVAR.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "volume": "sewetland"
      },
      "dstpath": {
        "volume": "sewetland"
      }
    }
  ]
}
```
