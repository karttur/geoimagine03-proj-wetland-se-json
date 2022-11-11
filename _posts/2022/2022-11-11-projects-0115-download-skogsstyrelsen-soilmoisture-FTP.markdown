---
layout: article
title: 0115-download-skogsstyrelsen-soilmoisture-FTP.json
categories: sewetland
excerpt:  download soilmositure products
tags:: 
    - 0115-download-skogsstyrelsen-soilmoisture-FTP
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0115 download skogsstyrelsen soilmoisture FTP (projects)

##  download soilmositure products

The json command file <span class='file'>0115-download-skogsstyrelsen-soilmoisture-FTP.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "path": "/SLUMarkfuktighet/SLUMarkfuktighetskarta/",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata/SLUMarkfuktighetskarta/"
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
        "path": "/SLUMarkfuktighet/SLUMarkfuktighetskartaKlassad/",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata/SLUMarkfuktighetskartaKlassad/"
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
        "path": "/SLUMarkfuktighet/Streams/10ha",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata/SLUStreams10ha/"
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
        "path": "/SLUMarkfuktighet/Streams/2ha",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata/SLUStreams2ha/"
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
        "path": "/SLUMarkfuktighet/Streams/30ha",
        "datadir": "DOWNLOADS/skogsstyrelsen/opendata/SLUStreams30ha/"
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
