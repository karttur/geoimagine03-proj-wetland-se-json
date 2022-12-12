---
layout: article
title: 0115-download-Metria-VMI.json
categories: sewetland
excerpt:  download Metria Svenska Vatmarksinventeringen (VMI) 
tags:: 
    - 0115-download-Metria-VMI
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0115 download Metria VMI (projects)

##  download Metria Svenska Vatmarksinventeringen (VMI) 

The json command file <span class='file'>0115-download-Metria-VMI.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "path": "DOWNLOADS/Metria/VMI/Metria-Svenska_VMI.txt",
        "datadir": "DOWNLOADS/Metria/VMI/data"
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
