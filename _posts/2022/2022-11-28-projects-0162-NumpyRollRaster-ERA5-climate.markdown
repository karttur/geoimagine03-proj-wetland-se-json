---
layout: article
title: 0162-NumpyRollRaster-ERA5-climate.json
categories: sewetland
excerpt:  project ERA5 climate data to 180 W
tags:: 
    - 0162-NumpyRollRaster-ERA5-climate
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0162 NumpyRollRaster ERA5 climate (projects)

##  project ERA5 climate data to 180 W

The json command file <span class='file'>0162-NumpyRollRaster-ERA5-climate.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "NumpyRollRaster",
      "overwrite": false,
      "parameters": {
        "rollcolumns": 1800,
        "rollrows": 0
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
            "suffix": "v2022"
          }
        }
      ],
      "dstcopy": [
        {
          "temp": {
            "srccomp": "airtemp_temperature@2m",
            "suffix": "v2022-r"
          }
        }
      ]
    }
  ]
}
```
