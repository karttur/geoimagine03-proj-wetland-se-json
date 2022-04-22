---
layout: article
title: 0160-organize-Metria-VMI_replace.json
categories: projects
excerpt:  Organize Metria VMI 
tags:: 
    - 0160-organize-Metria-VMI_replace.json
date: 2022-04-21
modified: 2022-04-21
comments: true
share: true
---

# 0160 organize Metria VMI replace.json (projects)

##  Organize Metria VMI 

The json command file <span class='file'>0160-organize-Metria-VMI_replace.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
        "orgid": "Metria",
        "dsname": "VMI",
        "dsversion": "1.0",
        "accessdate": "20220122",
        "regionid": "sweref",
        "regioncat": "sweref",
        "dataurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "metaurl": "https://www.lantmateriet.se/en/maps-and-geographic-information/open-geodata/",
        "title": "SWEREF99 Metria VMI",
        "label": "SWEREF99 Swedish vetland inventory",
        "replacestr": "@",
        "replacetag": "county"
      },
      "srcpath": {
        "volume": "GeoImg2021",
        "hdr": "shp"
      },
      "dstpath": {
        "volume": "GeoImg2021",
        "hdr": "shp"
      },
      "county": {
        "type": "location",
        "replace": [
          {
            "AB": {
              "src": [
                {
                  "datafile": "AB_Stockholm",
                  "datalayer": "AB_Stockholm",
                  "title": "AB Stockholm",
                  "label": "AB Stockholm"
                }
              ],
              "dst": [
                {
                  "layerid": "AB",
                  "prefix": "AB"
                }
              ]
            },
            "AC": {
              "src": [
                {
                  "datafile": "AC_Vasterbotten",
                  "datalayer": "AC_Vasterbotten",
                  "title": "AC Vaesterbotten",
                  "label": "AC Vaesterbotten"
                }
              ],
              "dst": [
                {
                  "layerid": "AC",
                  "prefix": "AC"
                }
              ]
            },
            "BD": {
              "src": [
                {
                  "datafile": "BD_Norrbotten",
                  "datalayer": "BD_Norrbotten",
                  "title": "BD Norrbotten",
                  "label": "BD Norrbotten"
                }
              ],
              "dst": [
                {
                  "layerid": "BD",
                  "prefix": "BD"
                }
              ]
            },
            "C": {
              "src": [
                {
                  "datafile": "C_Uppsala",
                  "datalayer": "C_Uppsala",
                  "title": "C Uppsala",
                  "label": "C Uppsala"
                }
              ],
              "dst": [
                {
                  "layerid": "C",
                  "prefix": "C"
                }
              ]
            },
            "D": {
              "src": [
                {
                  "datafile": "D_Södermanland",
                  "datalayer": "D_Södermanland",
                  "title": "D Soedermanland",
                  "label": "D Soedermanland"
                }
              ],
              "dst": [
                {
                  "layerid": "D",
                  "prefix": "D"
                }
              ]
            },
            "E": {
              "src": [
                {
                  "datafile": "E_Östergötland",
                  "datalayer": "E_Östergötland",
                  "title": "E Oestergoetland",
                  "label": "E Oestergoetland"
                }
              ],
              "dst": [
                {
                  "layerid": "E",
                  "prefix": "E"
                }
              ]
            },
            "F": {
              "src": [
                {
                  "datafile": "F_Jönköping",
                  "datalayer": "F_Jönköping",
                  "title": "F Joenkoeping",
                  "label": "F Joenkoeping"
                }
              ],
              "dst": [
                {
                  "layerid": "F",
                  "prefix": "F"
                }
              ]
            },
            "G": {
              "src": [
                {
                  "datafile": "G_Kronoberg",
                  "datalayer": "G_Kronoberg",
                  "title": "G Kronoberg",
                  "label": "G_Kronoberg"
                }
              ],
              "dst": [
                {
                  "layerid": "G",
                  "prefix": "G"
                }
              ]
            },
            "H": {
              "src": [
                {
                  "datafile": "H_Kalmar",
                  "datalayer": "H_Kalmar",
                  "title": "H Kalmar",
                  "label": "H Kalmar"
                }
              ],
              "dst": [
                {
                  "layerid": "H",
                  "prefix": "H"
                }
              ]
            },
            "I": {
              "src": [
                {
                  "datafile": "I_Gotland",
                  "datalayer": "I_Gotland",
                  "title": "I Gotland",
                  "label": "I Gotland"
                }
              ],
              "dst": [
                {
                  "layerid": "I",
                  "prefix": "I"
                }
              ]
            },
            "K": {
              "src": [
                {
                  "datafile": "K_Blekinge",
                  "datalayer": "K_Blekinge",
                  "title": "K Blekinge",
                  "label": "K Blekinge"
                }
              ],
              "dst": [
                {
                  "layerid": "K",
                  "prefix": "K"
                }
              ]
            },
            "M": {
              "src": [
                {
                  "datafile": "M_Skåne",
                  "datalayer": "M_Skåne",
                  "title": "M Skaane",
                  "label": "M Skaane"
                }
              ],
              "dst": [
                {
                  "layerid": "M",
                  "prefix": "M"
                }
              ]
            },
            "N": {
              "src": [
                {
                  "datafile": "N_Halland",
                  "datalayer": "N_Halland",
                  "title": "N Halland",
                  "label": "N Halland"
                }
              ],
              "dst": [
                {
                  "layerid": "N",
                  "prefix": "N"
                }
              ]
            },
            "O": {
              "src": [
                {
                  "datafile": "O_VastraGotaland",
                  "datalayer": "O_VastraGotaland",
                  "title": "O VastraGotaland",
                  "label": "O VastraGotaland"
                }
              ],
              "dst": [
                {
                  "layerid": "O",
                  "prefix": "O"
                }
              ]
            },
            "S": {
              "src": [
                {
                  "datafile": "S_Värmland",
                  "datalayer": "S_Värmland",
                  "title": "S Vaermland",
                  "label": "S Vaermland"
                }
              ],
              "dst": [
                {
                  "layerid": "S",
                  "prefix": "S"
                }
              ]
            },
            "T": {
              "src": [
                {
                  "datafile": "T_Örebro",
                  "datalayer": "T_Örebro",
                  "title": "T Oerebro",
                  "label": "T Oerebro"
                }
              ],
              "dst": [
                {
                  "layerid": "T",
                  "prefix": "T"
                }
              ]
            },
            "U": {
              "src": [
                {
                  "datafile": "U_Västmanland",
                  "datalayer": "U_Västmanland",
                  "title": "U Vaestmanland",
                  "label": "U Vaestmanland"
                }
              ],
              "dst": [
                {
                  "layerid": "U",
                  "prefix": "U"
                }
              ]
            },
            "W": {
              "src": [
                {
                  "datafile": "W_Dalarna",
                  "datalayer": "W_Dalarna",
                  "title": "W Dalarna",
                  "label": "W Dalarna"
                }
              ],
              "dst": [
                {
                  "layerid": "W",
                  "prefix": "W"
                }
              ]
            },
            "X": {
              "src": [
                {
                  "datafile": "X_Gävleborg",
                  "datalayer": "X_Gävleborg",
                  "title": "X Gaevleborg",
                  "label": "X Gaevleborg"
                }
              ],
              "dst": [
                {
                  "layerid": "X",
                  "prefix": "X"
                }
              ]
            },
            "Y": {
              "src": [
                {
                  "datafile": "Y_Västernorrland",
                  "datalayer": "Y_Västernorrland",
                  "title": "Y Vaesternorrland",
                  "label": "Y Vaesternorrland"
                }
              ],
              "dst": [
                {
                  "layerid": "Y",
                  "prefix": "Y"
                }
              ]
            },
            "Z": {
              "src": [
                {
                  "datafile": "Z_Jämtland",
                  "datalayer": "Z_Jämtland",
                  "title": "Z Jaemtland",
                  "label": "Z Jaemtland"
                }
              ],
              "dst": [
                {
                  "layerid": "Z",
                  "prefix": "Z"
                }
              ]
            }
          }
        ]
      },
      "srcraw": [
        {
          "pt": {
            "datadir": "DOWNLOADS/Metria/VMI/data",
            "datafile": "@_VMI_Punkter",
            "datalayer": "@_VMI_Punkter",
            "title": "VMI @ points",
            "label": "SWEREF99 Metria wetland inventory @ points"
          }
        },
        {
          "poly": {
            "datadir": "DOWNLOADS/Metria/VMI/data",
            "datafile": "@_VMI_Ytor",
            "datalayer": "@_VMI_Ytor",
            "title": "VMI @ polygons",
            "label": "SWEREF99 Metria wetland inventory @ polys"
          }
        }
      ],
      "dstcomp": [
        {
          "pt": {
            "source": "metria",
            "product": "vmi",
            "content": "wetland",
            "layerid": "VMI-@-pt",
            "prefix": "VMI-@-pt",
            "suffix": "v0pt",
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
          "poly": {
            "source": "metria",
            "product": "vmi",
            "content": "wetland",
            "layerid": "VMI-@-poly",
            "prefix": "VMI-@-poly",
            "suffix": "v0poly",
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
