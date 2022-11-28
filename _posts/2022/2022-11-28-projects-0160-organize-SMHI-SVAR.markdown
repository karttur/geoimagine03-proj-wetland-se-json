---
layout: article
title: 0160-organize-SMHI-SVAR.json
categories: sewetland
excerpt:  Organize SMHI SVAR data 
tags:: 
    - 0160-organize-SMHI-SVAR
date: 2022-11-28
modified: 2022-11-28
comments: true
share: true
---

# 0160 organize SMHI SVAR (projects)

##  Organize SMHI SVAR data 

The json command file <span class='file'>0160-organize-SMHI-SVAR.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "importcode": "shp",
        "epsg": "3006",
        "orgid": "SMHI",
        "dsname": "SVAR",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 SMHI SVAR",
        "label": "SWEREF99 Svenskt VattenArkriv"
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "shp"
      },
      "srcraw": [
        {
          "aro": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "aro_y_2016_3",
            "datalayer": "aro_y_2016_3",
            "title": "Avrinningsomraden",
            "label": "SWEREF99 Avrinningsomraden SMHI"
          }
        },
        {
          "haro": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "Haro_y_2016_3",
            "datalayer": "Haro_y_2016_3",
            "title": "Huvudavrinningsomraden",
            "label": "SWEREF99 Huvudavrinningsomraden SMHI"
          }
        },
        {
          "vy": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "vy_y_2016_3",
            "datalayer": "by_y_2016_3",
            "title": "Vattenytor",
            "label": "SWEREF99 Vattenytor SMHI"
          }
        },
        {
          "vd-l": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "vd_l_2016_3",
            "datalayer": "vd_l_2016_3",
            "title": "Vattendrag",
            "label": "SWEREF99 Vattendrag linjer SMHI"
          }
        },
        {
          "Havsomr": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "Havsomr_y_2016_3",
            "datalayer": "Havsomr_y_2016_3",
            "title": "Havsomraaden",
            "label": "SWEREF99 Havsomraaden SMHI"
          }
        },
        {
          "sj-p": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "sj_p_2016",
            "datalayer": "sj_p_2016",
            "title": "Sjoepunkter",
            "label": "SWEREF99 Sjoepunkter SMHI"
          }
        },
        {
          "RW-LW-VARO": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "RW_LW_VARO_2016_3c",
            "datalayer": "RW_LW_VARO_2016_3c",
            "title": "Kopplade delavrinningsomraden",
            "label": "SWEREF99 Kopplade delavrinningsomraden SMHI"
          }
        },
        {
          "CW-VARO": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "CW_VARO_2016_3c",
            "datalayer": "CW_VARO_2016_3c",
            "title": "Kopplade kustvattenomraden",
            "label": "SWEREF99 Kopplade kustvattenomraden SMHI"
          }
        },
        {
          "hydnet": {
            "datadir": "DOWNLOADS/SMHI/SVAR/data",
            "datafile": "Hyd_grundnat_SMHI_2020",
            "datalayer": "Hyd_grundnat_SMHI_2020",
            "title": "hydro stations",
            "label": "SWEREF99 hydrologiska maetstationer SMHI"
          }
        }
      ],
      "dstcomp": [
        {
          "aro": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "aro",
            "prefix": "aro",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "haro": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "haro",
            "prefix": "haro",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "vy": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "vy",
            "prefix": "vy",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "vd-l": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "vd-l",
            "prefix": "vd-l",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "line",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "Havsomr": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "havsomr",
            "prefix": "havsomr",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "sj-p": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "sj-p",
            "prefix": "sj-p",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "point",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "RW-LW-VARO": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "rw-lr-varo",
            "prefix": "rw-lr-varo",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "CW-VARO": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "cw-varo",
            "prefix": "cw-varo",
            "suffix": "v2016-3",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "hydnet": {
            "source": "smhi",
            "product": "svar",
            "content": "hydro",
            "layerid": "stations",
            "prefix": "stations",
            "suffix": "v2020",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "point",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
