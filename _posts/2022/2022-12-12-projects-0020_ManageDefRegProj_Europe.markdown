---
layout: article
title: 0020_ManageDefRegProj_Europe.json
categories: sewetland
excerpt:  Create a new user project and region for this data
tags:: 
    - 0020_ManageDefRegProj_Europe
date: 2022-12-12
modified: 2022-12-12
comments: true
share: true
---

# 0020 ManageDefRegProj Europe (projects)

##  Create a new user project and region for this data

The json command file <span class='file'>0020_ManageDefRegProj_Europe.json</span> is part of Karttur's GeoImagine project [<span class='project'>SwedenWetlands</span>](https://karttur.github.io/geoimagine03-proj-wetland-se/index.html). For details on the commands see the blog on [Framework Processes](https://karttur.github.io/geoimagine03-docs-procpack/).

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "system"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "ManageDefRegProj",
      "overwrite": false,
      "parameters": {
        "defaultregion": "europe",
        "tractid": "karttur-cerra-europe",
        "tractname": "Karttur CERRA Europe",
        "projid": "karttur-cerra-europe",
        "projname": "Karttur CERRA Europe",
        "tracttitle": "Karttur CERRA Europe",
        "tractlabel": "Karttur CERRA Europe",
        "projtitle": "Karttur CERRA Europe",
        "projlabel": "Karttur CERRA Europe"
      }
    }
  ]
}
```
