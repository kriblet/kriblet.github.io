---
title: Xentinel
description: Xentinel API Documentation
layout: default
info:
    title: Xentinel
    description: Xentinel API Documentation
    favicon: /img/xentinel.png
    logo: /img/xentinel.png
---


# CRUD

Please see [Available Models](../models) that can be accessed thru Generic CRUD

All responsability is charged in the programmer. Each model has his own functionality please use it wisely.

All returned data is user scope.

### URL Convention

All models are available thru URL `https://stage.api.xentinel.io/:MODEL`, replace `:MODEL` for the desired public model. 

## Get

Generic way to obtain data, that data can show within a list or within an object.

### Get List

All lists data are paginated, please aware that you can not request more than 50 items at once. Api is validated to return `max 50 items`.

Get parameters available.

| Parameter | Type | Description | Example |
|---|---|---|---|
|q|`Json`|Query filter in `mongoose` style. See [Mongoose Documentation](http://mongoosejs.com/docs/4.x/docs/queries.html) | `https://stage.api.xentinel.io/users/?skip=0&limit=1&q={"_id":"exampleMongoID"}` |

### Get By ID

URL Convention `https://stage.api.xentinel.io/:MODEL/:ID`, replace `:MODEL` for the desired model, and replace `:ID` for the specific mongo id.

## Post

## Put

## Delete