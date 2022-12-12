---
layout: article
title: 0165-fillnodata-ERA5-climate.json
categories: sewetland
excerpt:  fillnodata ERA3 climate data
tags:: 
    - 0165-fillnodata-ERA5-climate
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0165 fillnodata ERA5 climate (projects)

##  fillnodata ERA3 climate data

The json command file <span class='file'>0165-fillnodata-ERA5-climate.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "timestep": "M",
    "startyear": 1950,
    "startmonth": 1,
    "startday": 1,
    "endyear": 2021,
    "endmonth": 12,
    "endday": 31
  },
  "process": [
    {
      "processid": "fillnodataregion",
      "overwrite": true,
      "parameters": {
        "max_distance": 8
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
            "suffix": "v2022-r"
          }
        },
        {
          "temp": {
            "source": "c3s",
            "product": "era5",
            "content": "airtemp",
            "layerid": "temperature@2m",
            "prefix": "temperature@2m",
            "suffix": "v2022-r"
          }
        }
      ],
      "dstcopy": [
        {
          "precip": {
            "srccomp": "precip_tot-precip-m-m",
            "suffix": "v2022-r-fill8px"
          }
        },
        {
          "temp": {
            "srccomp": "airtemp_temperature@2m",
            "suffix": "v2022-r-fill8px"
          }
        }
      ]
    }
  ]
}
```
