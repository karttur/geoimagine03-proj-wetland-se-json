---
layout: article
title: 0115-download-skogsstyrelsen-samverkan-FTP.json
categories: sewetland
excerpt:  download depth to groundwater from Skogsstyrelsen skogskartor account (older account that might no longer exist)
tags:: 
    - 0115-download-skogsstyrelsen-samverkan-FTP
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0115 download skogsstyrelsen samverkan FTP (projects)

##  download depth to groundwater from Skogsstyrelsen skogskartor account (older account that might no longer exist)

The json command file <span class='file'>0115-download-skogsstyrelsen-samverkan-FTP.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "downloadcode": "subdir",
        "host": "ftps://ftpsks.skogsstyrelsen.se",
        "port": 990,
        "encryptation": "normal",
        "logontype": "normal",
        "user": "Skogskartor",
        "password": "j6Jvj\t!x,",
        "path": "/Samverkan/Markfuktighet/",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata/markfuktighet-DTW"
      },
      "srcpath": {
        "volume": "ancillary"
      },
      "dstpath": {
        "volume": "ancillary"
      }
    }
  ]
}
```
