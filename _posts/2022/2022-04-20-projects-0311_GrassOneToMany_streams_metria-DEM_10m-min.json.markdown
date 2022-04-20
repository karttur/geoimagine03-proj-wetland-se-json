---
layout: article
title: 0311_GrassOneToMany_streams_metria-DEM_10m-min.json
categories: projects
excerpt: 
tags:: 
    - 0311_GrassOneToMany_streams_metria-DEM_10m-min.json
date: 2022-04-20
modified: 2022-04-20
comments: true
share: true
---

# 0311 GrassOneToMany streams metria DEM 10m min.json (projects)

## 

The json command file <span class='file'>0311_GrassOneToMany_streams_metria-DEM_10m-min.json</span> is part of Karttur's GeoImagine project <span class='project'>projects</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
            "r.watershed": {
              "flags": "a",
              "elevation": "DEM",
              "accumulation": "MFDupstream",
              "drainage": "MFDflowdir",
              "stream": "MFDstream",
              "threshold": 1000,
              "memory": 4000,
              "overwrite": true
            }
          },
          {
            "r.stream.extract": {
              "elevation": "DEM",
              "accumulation": "MFDupstream",
              "threshold": 1000,
              "mexp": 1.2,
              "stream_length": 4,
              "stream_rast": "extractstream",
              "stream_vector": "extractstreamvect",
              "direction": "extractflowdir",
              "memory": "4000",
              "overwrite": true
            }
          },
          {
            "r.out.gdal": {
              "flags": "f",
              "input": "extractstream",
              "output": "stream-rast"
            }
          }
        ]
      },
      "srcpath": {
        "volume": "Arctic2021",
        "hdr": "tif"
      },
      "dstpath": {
        "volume": "Arctic2021",
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
            "suffix": "v01-pfpf-hydrdem4+4-90m",
            "cellnull": -999,
            "celltype": "Int16",
            "dataunit": "boolean class",
            "measure": "N"
          }
        }
      ]
    }
  ]
}
```
