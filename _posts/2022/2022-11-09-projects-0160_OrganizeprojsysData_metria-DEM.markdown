---
layout: article
title: 0160_OrganizeprojsysData_metria-DEM.json
categories: sewetland
excerpt:  Import DEM tiles 
tags:: 
    - 0160_OrganizeprojsysData_metria-DEM
date: 2022-11-09
modified: 2022-11-09
comments: true
share: true
---

# 0160 OrganizeprojsysData metria DEM (projects)

##  Import DEM tiles 

The json command file <span class='file'>0160_OrganizeprojsysData_metria-DEM.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "timestep": "static"
  },
  "process": [
    {
      "processid": "OrganizeProjSysData",
      "overwrite": false,
      "parameters": {
        "importcode": "vrt",
        "epsg": "3006",
        "orgid": "Metria",
        "dsname": "dem2m",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 DEM 2m Metria",
        "label": "SWEREF99 DEM 2m Metria"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "vrt"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "vrt"
      },
      "srcraw": [
        {
          "dem": {
            "datadir": "ancillary/metria/region/dem/global/0",
            "datafile": "dem2m_dem_global_0_raw",
            "datalayer": "dem",
            "title": "dem2m_dem_global_0_raw",
            "label": "dem2m_dem_global_0_raw"
          }
        }
      ],
      "dstcomp": [
        {
          "dem": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "raw",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "masl",
            "celltype": "Float32",
            "cellnull": -999,
            "measure": "R",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
