---
layout: article
title: 0180_TileAncillaryRegion_ERA5-climate.json
categories: sewetland
excerpt:  tile ERA5 climate data 
tags:: 
    -  0180_TileAncillaryRegion_ERA5-climate
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

#  0180 TileAncillaryRegion ERA5 climate (projects)

##  tile ERA5 climate data 

The json command file <span class='file'>0180_TileAncillaryRegion_ERA5-climate.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur-sweref",
    "tractid": "karttur-sweref",
    "siteid": "*",
    "plotid": "*",
    "system": "sweref"
  },
  "period": {
    "timestep": "M",
    "startyear": 1950,
    "startmonth": 1,
    "startday": 1,
    "endyear": 2020,
    "endmonth": 12,
    "endday": 31
  },
  "process": [
    {
      "processid": "TileAncillaryRegion",
      "version": "1.3",
      "overwrite": false,
      "parameters": {
        "src_defregid": "global",
        "tr_xres": 10000,
        "tr_yres": 10000,
        "resample": "near",
        "asscript": true
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srccomp": [
        {
          "precip": {
            "source": "c3s",
            "product": "era5",
            "content": "precip",
            "layerid": "tot-precip-m-m",
            "prefix": "tot-precip-m-m",
            "suffix": "v2022-r-fill8px"
          }
        }
      ],
      "dstcopy": [
        {
          "precip": {
            "srccomp": "precip_tot-precip-m-m"
          }
        }
      ]
    },
    {
      "processid": "TileAncillaryRegion",
      "version": "1.3",
      "overwrite": false,
      "parameters": {
        "src_defregid": "global",
        "tr_xres": 10000,
        "tr_yres": 10000,
        "resample": "near",
        "asscript": true
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srccomp": [
        {
          "temp": {
            "source": "c3s",
            "product": "era5",
            "content": "airtemp",
            "layerid": "temperature@2m",
            "prefix": "temperature@2m",
            "suffix": "v2022-r-fill8px"
          }
        }
      ],
      "dstcopy": [
        {
          "temp": {
            "srccomp": "airtemp_temperature@2m"
          }
        }
      ]
    }
  ]
}
```
