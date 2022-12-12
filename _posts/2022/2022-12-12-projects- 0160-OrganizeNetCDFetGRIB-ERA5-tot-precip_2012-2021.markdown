---
layout: article
title: 0160-OrganizeNetCDFetGRIB-ERA5-tot-precip_2012-2021.json
categories: sewetland
excerpt:  Organize ERA monthly climate data; precipitation 2012-2021 
tags:: 
    -  0160-OrganizeNetCDFetGRIB-ERA5-tot-precip_2012-2021
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

#  0160 OrganizeNetCDFetGRIB ERA5 tot precip 2012 2021 (projects)

##  Organize ERA monthly climate data; precipitation 2012-2021 

The json command file <span class='file'>0160-OrganizeNetCDFetGRIB-ERA5-tot-precip_2012-2021.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "startyear": 2012,
    "startmonth": 1,
    "startday": 1,
    "endyear": 2021,
    "endmonth": 12,
    "endday": 31
  },
  "process": [
    {
      "processid": "OrganizeNetCDFetGRIB",
      "overwrite": false,
      "parameters": {
        "importcode": "grib",
        "epsg": "-9999",
        "orgid": "C3S",
        "dsname": "precip",
        "dsversion": "1.0",
        "accessdate": "20221124",
        "regionid": "global",
        "regioncat": "global",
        "dataurl": "https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=overview",
        "metaurl": "https://confluence.ecmwf.int/display/CKB/ERA5%3A+data+documentation",
        "title": "ERA5 Total precipitation",
        "label": "ERA5 climate reanlysis monthly total precipitation"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "grib"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srcraw": [
        {
          "precip": {
            "datadir": "DOWNLOADS/ERA5/tot-p",
            "datafile": "precip_2012-2021",
            "datalayer": "precip",
            "title": "ERA5 global monthly total precipitation reanalysis",
            "label": "ERA5 global monthly total precipitation reanalysis"
          }
        }
      ],
      "dstcomp": [
        {
          "precip": {
            "source": "c3s",
            "product": "era5",
            "content": "precip",
            "layerid": "tot-precip-m-m",
            "prefix": "tot-precip-m-m",
            "suffix": "v2022",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "m",
            "celltype": "Float64",
            "cellnull": 9999,
            "measure": "R",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
