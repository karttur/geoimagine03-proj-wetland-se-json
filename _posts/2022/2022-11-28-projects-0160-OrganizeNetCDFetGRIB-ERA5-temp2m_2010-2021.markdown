---
layout: article
title: 0160-OrganizeNetCDFetGRIB-ERA5-temp2m_2010-2021.json
categories: sewetland
excerpt:  Organize ERA5 monthly climate data; temperature @ 2m 2010-2021 
tags:: 
    - 0160-OrganizeNetCDFetGRIB-ERA5-temp2m_2010-2021
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0160 OrganizeNetCDFetGRIB ERA5 temp2m 2010 2021 (projects)

##  Organize ERA5 monthly climate data; temperature @ 2m 2010-2021 

The json command file <span class='file'>0160-OrganizeNetCDFetGRIB-ERA5-temp2m_2010-2021.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "startyear": 2010,
    "startmonth": 1,
    "startday": 1,
    "endyear": 2011,
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
        "dsname": "climate",
        "dsversion": "1.0",
        "accessdate": "20221124",
        "regionid": "global",
        "regioncat": "global",
        "dataurl": "https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=overview",
        "metaurl": "https://confluence.ecmwf.int/display/CKB/ERA5%3A+data+documentation",
        "title": "ERA5 temperature",
        "label": "ERA5 climate reanlysis monthly average temperature @ 2m"
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
          "temp": {
            "datadir": "DOWNLOADS/ERA5/temperature_2m",
            "datafile": "temp_2010-2021",
            "datalayer": "temperature",
            "title": "ERA5 global monthly average temperautre (celsius) reanalysis",
            "label": "ERA5 global monthly average temperautre (celsius) reanalysis"
          }
        }
      ],
      "dstcomp": [
        {
          "temp": {
            "source": "c3s",
            "product": "era5",
            "content": "airtemp",
            "layerid": "temperature@2m",
            "prefix": "temperature@2m",
            "suffix": "v2022",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "K",
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
