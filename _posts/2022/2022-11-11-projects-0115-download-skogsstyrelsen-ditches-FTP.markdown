---
layout: article
title: 0115-download-skogsstyrelsen-ditches-FTP.json
categories: sewetland
excerpt:  download ditches
tags:: 
    - 0115-download-skogsstyrelsen-ditches-FTP
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0115 download skogsstyrelsen ditches FTP (projects)

##  download ditches

The json command file <span class='file'>0115-download-skogsstyrelsen-ditches-FTP.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "port": 21,
        "encryptation": "normal",
        "logontype": "normal",
        "user": "SGD",
        "password": "0N!nd=I9EJ",
        "path": "/DikenRaster_1m",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata//DikenRaster_1m/"
      },
      "srcpath": {
        "volume": "ancillary"
      },
      "dstpath": {
        "volume": "ancillary"
      }
    },
    {
      "processid": "FtpAncillary",
      "overwrite": false,
      "parameters": {
        "downloadcode": "subdir",
        "host": "ftps://ftpsks.skogsstyrelsen.se",
        "port": 21,
        "encryptation": "normal",
        "logontype": "normal",
        "user": "SGD",
        "password": "0N!nd=I9EJ",
        "path": "/DikenRaster_05m",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata//DikenRaster_05m/"
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
