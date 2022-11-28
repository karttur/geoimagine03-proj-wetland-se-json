---
layout: article
title: 0115-download-lantmateriet-FTP.json
categories: sewetland
excerpt:  FTP Download Lantmateriet vector data 
tags:: 
    - 0115-download-lantmateriet-FTP
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0115 download lantmateriet FTP (projects)

##  FTP Download Lantmateriet vector data 

The json command file <span class='file'>0115-download-lantmateriet-FTP.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "FtpAncillary",
      "overwrite": false,
      "parameters": {
        "downloadcode": "filelist",
        "path": "/Volumes/sewetland/DOWNLOADS/lantmateriet/lantmateriet_ftp.txt",
        "datadir": "DOWNLOADS/lantmateriet",
        "host": "download-opendata.lantmateriet.se",
        "port": 21,
        "encryptation": "normal",
        "logontype": "normal",
        "user": "thomas.gumbricht",
        "password": "co6-l4G-67a-tI7"
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
