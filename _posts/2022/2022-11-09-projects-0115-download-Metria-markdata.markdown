---
layout: article
title: 0115-download-Metria-markdata.json
categories: sewetland
excerpt:  Download Metria land cover (NMD) 
tags:: 
    - 0115-download-Metria-markdata
date: 2022-11-09
modified: 2022-11-09
comments: true
share: true
---

# 0115 download Metria markdata (projects)

##  Download Metria land cover (NMD) 

The json command file <span class='file'>0115-download-Metria-markdata.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "volume": "sewetland"
      },
      "dstpath": {
        "volume": "sewetland"
      }
    }
  ]
}
```
