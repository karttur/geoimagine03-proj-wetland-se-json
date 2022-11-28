---
layout: article
title: 0160-organize-Metria-NMD.json
categories: sewetland
excerpt:  Organize Metria NMD landcover 
tags:: 
    - 0160-organize-Metria-NMD
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0160 organize Metria NMD (projects)

##  Organize Metria NMD landcover 

The json command file <span class='file'>0160-organize-Metria-NMD.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
    "timestep": "singleyear",
    "startyear": 2018,
    "endyear": 2018
  },
  "process": [
    {
      "processid": "OrganizeProjSysData",
      "overwrite": false,
      "parameters": {
        "importcode": "shp",
        "epsg": "3006",
        "orgid": "Metria",
        "dsname": "VMI",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 Metria NMD",
        "label": "SWEREF99 Nationella Marktäckesdata"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srcraw": [
        {
          "nmdbas": {
            "datadir": "DOWNLOADS/Metria/markdata/data/NMD2018_basskikt_ogeneraliserad_Sverige_v1_1",
            "datafile": "nmd2018bas_ogeneraliserad_v1_1",
            "datalayer": "nmd2018bas_ogeneraliserad_v1_1",
            "title": "NMD 2018 bas v1.1",
            "label": "NMD 2018 bas v1.1"
          }
        },
        {
          "nmdbete": {
            "datadir": "DOWNLOADS/Metria/markdata/data/NMD_Tillaggsskikt_Markanvandning",
            "datafile": "NMD_markanv_bete_v1.tif",
            "datalayer": "NMD_markanv_bete_v1",
            "title": "NMD 2018 betesmark v1",
            "label": "NMD 2018 betesmark v1"
          }
        },
        {
          "nmdkraftledning": {
            "datadir": "DOWNLOADS/Metria/markdata/data/NMD_Tillaggsskikt_Markanvandning",
            "datafile": "NMD_markanv_kraftledning_v1.tif",
            "datalayer": "NMD_markanv_kraftledning_v1",
            "title": "NMD 2018 kraftledning v1",
            "label": "NMD 2018 kraftledning v1"
          }
        },
        {
          "nmdanlagda": {
            "datadir": "DOWNLOADS/Metria/markdata/data/NMD_Tillaggsskikt_Markanvandning",
            "datafile": "NMD_markanv_anlagda_omr_v1.tif",
            "datalayer": "NMD_markanv_anlagda_omr_v1_v1",
            "title": "NMD 2018 anlagda ytor v1",
            "label": "NMD 2018 anlagda ytor v1"
          }
        },
        {
          "nmdfjaellskog": {
            "datadir": "DOWNLOADS/Metria/markdata/data/NMD_Lag_fjallskog_v1_1",
            "datafile": "nmd_lag_fjallskog_v1_1.tif",
            "datalayer": "nmd_lag_fjallskog_v1_1",
            "title": "NMD 2018 laag fjaellskog v1",
            "label": "NMD 2018 laag fjaellskog v1"
          }
        }
      ],
      "dstcomp": [
        {
          "nmdbas": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-base",
            "prefix": "nmd-base",
            "suffix": "v1-1",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "class",
            "celltype": "UINT8",
            "cellnull": 0,
            "measure": "N",
            "masked": "N"
          }
        },

        {
          "nmdbete": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-bete",
            "prefix": "nmd-bete",
            "suffix": "v1",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "class",
            "celltype": "UINT8",
            "cellnull": 0,
            "measure": "N",
            "masked": "N"
          }
        },

        {
          "nmdkraftledning": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-kraftled",
            "prefix": "nmd-kraftled",
            "suffix": "v1",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "class",
            "celltype": "UINT8",
            "cellnull": 0,
            "measure": "N",
            "masked": "N"
          }
        },

        {
          "nmdanlagda": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-anlagda-ytor",
            "prefix": "nmd-anlagda-ytor",
            "suffix": "v1",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "class",
            "celltype": "UINT8",
            "cellnull": 0,
            "measure": "N",
            "masked": "N"
          }
        },

        {
          "nmdfjaellskog": {
            "source": "metria",
            "product": "nmd",
            "content": "landcover",
            "layerid": "nmd-fjaellskog",
            "prefix": "nmd-fjaellskog",
            "suffix": "v1",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "class",
            "celltype": "UINT8",
            "cellnull": 255,
            "measure": "N",
            "masked": "N"
          }
        }

      ]
    }
  ]
}
```
