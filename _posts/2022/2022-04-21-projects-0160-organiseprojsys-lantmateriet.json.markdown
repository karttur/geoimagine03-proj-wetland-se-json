---
layout: article
title: 0160-organiseprojsys-lantmateriet.json
categories: projects
excerpt: 
tags:: 
    - 0160-organiseprojsys-lantmateriet.json
date: 2022-04-21
modified: 2022-04-21
comments: true
share: true
---

# 0160 organiseprojsys lantmateriet.json (projects)

## 

The json command file <span class='file'>0160-organiseprojsys-lantmateriet.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "orgid": "lantmateriet",
        "dsname": "rutnaet",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 overskitskarta",
        "label": "SWEREF99 grid oversiktskarta"
      },
      "srcpath": {
        "volume": "Ancillary",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "Ancillary",
        "hdr": "shp"
      },
      "srcraw": [
        {
          "rutnaet": {
            "datadir": "DOWNLOADS/lantmateriet/ok_riks_Sweref_99_TM_shape/oversikt/riks",
            "datafile": "rutnat",
            "datalayer": "rutnat",
            "title": "SWEREF99 grid system",
            "label": "SWEREF99 grid system"
          }
        },
        {
          "naturreservat": {
            "datadir": "DOWNLOADS/lantmateriet/ok_riks_Sweref_99_TM_shape/oversikt/riks",
            "datafile": "nv_riks",
            "datalayer": "nv_riks",
            "title": "SWEREF99 naturreservat",
            "label": "SWEREF99 naturreservat"
          }
        },
        {
          "naturreservat-mindre": {
            "datadir": "DOWNLOADS/lantmateriet/ok_riks_Sweref_99_TM_shape/oversikt/riks",
            "datafile": "ns_riks",
            "datalayer": "ns_riks",
            "title": "SWEREF99 naturreservat mindre",
            "label": "SWEREF99 naturreservat mindre"
          }
        },
        {
          "fagelskyddsomrade": {
            "datadir": "DOWNLOADS/lantmateriet/ok_riks_Sweref_99_TM_shape/oversikt/riks",
            "datafile": "nl_riks",
            "datalayer": "nl_riks",
            "title": "SWEREF99 fagelskyddsomrade",
            "label": "SWEREF99 fagelskyddsomrade"
          }
        },
        {
          "fagelskyddsomrade2": {
            "datadir": "DOWNLOADS/lantmateriet/ok_riks_Sweref_99_TM_shape/oversikt/riks",
            "datafile": "nd_riks",
            "datalayer": "nd_riks",
            "title": "SWEREF99 fagelskyddsomrade",
            "label": "SWEREF99 fagelskyddsomrade"
          }
        },
        {
          "marktaecke": {
            "datadir": "DOWNLOADS/lantmateriet/ok_riks_Sweref_99_TM_shape/oversikt/riks",
            "datafile": "my_riks",
            "datalayer": "my_riks",
            "title": "SWEREF99 markyta markttaecke",
            "label": "SWEREF99 markyta markttaecke"
          }
        },
        {
          "sjoar": {
            "datadir": "DOWNLOADS/lantmateriet/ok_riks_Sweref_99_TM_shape/oversikt/riks",
            "datafile": "ms_riks",
            "datalayer": "ms_riks",
            "title": "SWEREF99 markyta sjoar",
            "label": "SWEREF99 markyta sjoar"
          }
        }
      ],
      "dstcomp": [
        {
          "rutnaet": {
            "source": "lantmateriet",
            "product": "sweref",
            "content": "rutnat",
            "layerid": "rutnat",
            "prefix": "grid",
            "suffix": "riks",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "grid",
            "celltype": "vector",
            "cellnull": -32767,
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "naturreservat": {
            "source": "lantmateriet",
            "product": "oversikt",
            "content": "naturskydd",
            "layerid": "naturereservat",
            "prefix": "naturereservat",
            "suffix": "riks",
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
          "naturreservat-mindre": {
            "source": "lantmateriet",
            "product": "oversikt",
            "content": "naturskydd",
            "layerid": "naturereservat-mindre",
            "prefix": "naturereservat-mindre",
            "suffix": "riks",
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
          "fagelskyddsomrade": {
            "source": "lantmateriet",
            "product": "oversikt",
            "content": "naturskydd",
            "layerid": "fagelskyddsomrade",
            "prefix": "fagelskyddsomrade",
            "suffix": "riks",
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
          "fagelskyddsomrade2": {
            "source": "lantmateriet",
            "product": "oversikt",
            "content": "naturskydd",
            "layerid": "fagelskyddsomrade2",
            "prefix": "fagelskyddsomrade2",
            "suffix": "riks",
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
          "marktaecke": {
            "source": "lantmateriet",
            "product": "oversikt",
            "content": "markyta",
            "layerid": "marktaecke",
            "prefix": "marktaecke",
            "suffix": "riks",
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
          "sjoar": {
            "source": "lantmateriet",
            "product": "oversikt",
            "content": "markyta",
            "layerid": "sjoar",
            "prefix": "sjoar",
            "suffix": "riks",
            "scalefac": 1,
            "offsetadd": 0,
            "dataunit": "boundary",
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
