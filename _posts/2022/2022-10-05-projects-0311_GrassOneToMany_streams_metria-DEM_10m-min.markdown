---
layout: article
title: 0311_GrassOneToMany_streams_metria-DEM_10m-min.json
categories: sewetland
excerpt:  Extract streams from DEM
tags:: 
    - 0311_GrassOneToMany_streams_metria-DEM_10m-min
date: 2022-10-05
modified: 2022-10-05
comments: true
share: true
---

# 0311 GrassOneToMany streams metria DEM 10m min (projects)

##  Extract streams from DEM

The json command file <span class='file'>0311_GrassOneToMany_streams_metria-DEM_10m-min.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "GrassOnetoManyTiles",
      "version": "1.3",
      "overwrite": true,
      "dryrun": false,
      "verbose": 1,
      "parameters": {
        "asscript": true,
        "mosaic": true,
        "regionlayer": "DEM",
        "subparameter": [
          {
            "g.region": {
              "raster": "DEM"
            }
          },

          {
            "r.stream.extract": {
              "elevation": "DEM",
              "threshold": 500,
              "mexp": 1.2,
              "stream_length": 4,
              "stream_rast": "extractstream",
              "memory": 4000,
              "overwrite": true
            },

            "r.mapcalc": {
              "\"depressedstream ": " if((extractstream>0),1,null())\"",
              "overwrite": true
            }
          },

          {
            "r.out.gdal": {
              "flags": "f",
              "type": "Byte",
              "input": "depressedstream",
              "output": "stream-rast"
            }
          }
        ]
      },
      "srcpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "sewetland",
        "hdr": "tif"
      },
      "srccomp": [
        {
          "*": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "min-10m"
          }
        }
      ],
      "dstcopy": [
        {
          "stream-rast": {
            "source": "copy",
            "product": "copy",
            "content": "terrain",
            "layerid": "stream-rast",
            "prefix": "stream-rast",
            "suffix": "v01-min10m",
            "cellnull": -999,
            "celltype": "Byte",
            "dataunit": "boolean class",
            "measure": "N"
          }
        }
      ]
    }
  ]
}
```
