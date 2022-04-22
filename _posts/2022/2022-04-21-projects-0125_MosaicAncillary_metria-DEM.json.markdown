---
layout: article
title: 0125_MosaicAncillary_metria-DEM.json
categories: projects
excerpt:  Mosaic DEM 
tags:: 
    - 0125_MosaicAncillary_metria-DEM.json
date: 2022-04-21
modified: 2022-04-21
comments: true
share: true
---

# 0125 MosaicAncillary metria DEM.json (projects)

##  Mosaic DEM 

The json command file <span class='file'>0125_MosaicAncillary_metria-DEM.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "MosaicAncillary",
      "overwrite": false,
      "parameters": {
        "pattern": "",
        "nonpattern": "density",
        "getlist": "oswalk",
        "srcdir": "DOWNLOADS/Metria/DEM2m/data"
      },
      "srcpath": {
        "volume": "Arctic2021",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "Arctic2021",
        "hdr": "vrt"
      },
      "dstcomp": [
        {
          "DEM": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "raw"
          }
        }
      ]
    }
  ]
}
```
