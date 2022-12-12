---
layout: article
title: 0160-OrganizeNetCDFetGRIB-E-OBS_1950-1964.json
categories: sewetland
excerpt:  Organize E-OBS climate data 1950 - 1964 
tags:: 
    - 0160-OrganizeNetCDFetGRIB-E-OBS_1950-1964
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0160 OrganizeNetCDFetGRIB E OBS 1950 1964 (projects)

##  Organize E-OBS climate data 1950 - 1964 

The json command file <span class='file'>0160-OrganizeNetCDFetGRIB-E-OBS_1950-1964.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur-cerra-europe",
    "tractid": "karttur-cerra-europe",
    "siteid": "*",
    "plotid": "*",
    "system": "ancillary"
  },
  "period": {
    "timestep": "D",
    "startyear": 1950,
    "startmonth": 1,
    "startday": 1,
    "endyear": 1964,
    "endmonth": 12,
    "endday": 31
  },
  "process": [
    {
      "processid": "OrganizeNetCDFetGRIB",
      "overwrite": false,
      "parameters": {
        "importcode": "netcdf",
        "epsg": "3006",
        "orgid": "ECA&D",
        "dsname": "E-OBS",
        "dsversion": "v26",
        "accessdate": "20221124",
        "regionid": "europe",
        "regioncat": "europe",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "E-OBS daily total precipitation",
        "label": "E-OBS daily total precipitation"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "nc"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srcraw": [
        {
          "p-tot": {
            "datadir": "DOWNLOADS/E-OBS/RR/data",
            "datafile": "rr_ens_mean_0.1deg_reg_1950-1964_v26.0e",
            "datalayer": "rr",
            "title": "E-OBS daily total precipitation",
            "label": "E-OBS daily total precipitation"
          }
        }
      ],
      "dstcomp": [
        {
          "p-tot": {
            "source": "e-obs",
            "product": "climate",
            "content": "precip",
            "layerid": "rr",
            "prefix": "rr",
            "suffix": "v26",
            "scalefac": 0.1,
            "offsetadd": 0,
            "dataunit": "mm",
            "celltype": "Float32",
            "cellnull": -9999,
            "measure": "R",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
