---
layout: article
title: 0312_GrassManyToMany_hydrodem_metria-DEM_10m-min.json
categories: sewetland
excerpt:  Combine min DEM and mean DEM to get well defined streams
tags:: 
    - 0312_GrassManyToMany_hydrodem_metria-DEM_10m-min
date: 2022-11-11
modified: 2022-11-11
comments: true
share: true
---

# 0312 GrassManyToMany hydrodem metria DEM 10m min (projects)

##  Combine min DEM and mean DEM to get well defined streams

The json command file <span class='file'>0312_GrassManyToMany_hydrodem_metria-DEM_10m-min.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

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
      "processid": "GrassManytoManyTiles",
      "version": "1.3",
      "overwrite": true,
      "dryrun": false,
      "verbose": 1,
      "parameters": {
        "asscript": true,
        "mosaic": true,
        "regionlayer": "mindem",
        "subparameter": [
          {
            "g.region": {
              "raster": "mindem"
            }
          },
          {
            "r.stream.extract": {
              "elevation": "mindem",
              "threshold": 500,
              "mexp": 1.2,
              "stream_length": 4,
              "stream_rast": "extractstream",
              "memory": 4000,
              "overwrite": true
            }
          },
          {
            "r.mapcalc": {
              "\"depressedstream ": " if((extractstream>0),1,null())\"",
              "overwrite": true
            }
          },
          {
            "r.mapcalc": {
              "\"streamdem ": " if( isnull(depressedstream),meandem,mindem)\"",
              "overwrite": true
            }
          },
          {
            "r.out.gdal": {
              "flags": "f",
              "type": "Byte",
              "nodata": 255,
              "input": "depressedstream",
              "output": "stream-rast"
            }
          },
          {
            "r.out.gdal": {
              "flags": "f",
              "nodata": -999,
              "input": "streamdem",
              "output": "stream-dem"
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
          "mindem": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "min-10m"
          },
          "meandem": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem2m",
            "prefix": "dem2m",
            "suffix": "mean-10m"
          }
        }
      ],
      "dstcomp": [
        {
          "stream-rast": {
            "source": "metria",
            "product": "dem",
            "content": "terrain",
            "layerid": "stream",
            "prefix": "stream",
            "suffix": "v01-min10m",
            "cellnull": 255,
            "celltype": "Byte",
            "dataunit": "boolean class",
            "measure": "N"
          },
          "stream-dem": {
            "source": "metria",
            "product": "dem",
            "content": "dem",
            "layerid": "dem10m",
            "prefix": "dem10m",
            "suffix": "v01-mean+minchannel",
            "cellnull": -999,
            "celltype": "Float32",
            "dataunit": "masl",
            "measure": "R"
          }
        }
      ]
    }
  ]
}
```
