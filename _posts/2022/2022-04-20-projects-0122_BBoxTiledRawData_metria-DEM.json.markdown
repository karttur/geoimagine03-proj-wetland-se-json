---
layout: article
title: 0122_BBoxTiledRawData_metria-DEM.json
categories: projects
excerpt:  Create vector bounding boxes for the 2 m DEM tiles
tags:: 
    - 0122_BBoxTiledRawData_metria-DEM.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0122 BBoxTiledRawData metria DEM.json (projects)

##  Create vector bounding boxes for the 2 m DEM tiles

The json command file <span class='file'>0122_BBoxTiledRawData_metria-DEM.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "BBoxTiledRawData",
      "dsversion": "1.3",
      "parameters": {
        "getlist": "oswalk",
        "pattern": "",
        "nonpattern": "density",
        "srcdir": "DOWNLOADS/METRIA/DEM2m/data",
        "dstdir": "DOWNLOADS/METRIA/DEM2m/tiles"
      },
      "srcpath": {
        "volume": "Arctic2021",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "Arctic2021",
        "hdr": "shp"
      }
    }
  ]
}
```
