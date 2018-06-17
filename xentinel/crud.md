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

Please note: All Xentinel API endpoints are highly secured by our Auth System. You need a ClientID & token ALWAYS.

Please see [Available Models](/xentinel/models) that can be accessed thru Generic CRUD

All responsability is charged in the programmer. Each model has his own functionality please use it wisely.

All returned data is user scope.

### URL Convention

All models are available thru URL `https://stage.api.xentinel.io/:MODEL`, replace `:MODEL` for the desired public model. 

## Test Endpoint
`https://test.api.xentinel.io`

## Production Endpoint
`https://api.xentinel.io`


## Get

Generic way to obtain data, that data can show within a list or within an object.

### Get List

All lists data are paginated, please aware that you can not request more than 50 items at once. Api is validated to return `max 50 items`.


Get parameters available.

| Parameter | Type | Description | Example |
|---|---|---|---|
|q|`Json`|JSON.parse(q). Query filter in `mongoose` style. See [Mongoose Documentation](http://mongoosejs.com/docs/4.x/docs/queries.html) | `https://stage.api.xentinel.io/users/?skip=0&limit=1&q={"_id":"exampleMongoID"}` |
|limit|`integer`|Limit the api to return 1~50 items in the list|`https://stage.api.xentinel.io/users/limit=10`|
|skip|`integer`|Skips N quantity of records, available for pagination|`https://stage.api.xentinel.io/users/?skip=10&limit=10`|
|fields|`string`|Desired Model fields separated by comma|`https://stage.api.xentinel.io/users/?fields=_id,name,lastName`| 
|populate|`json`|JSON.parse(populate). Recursive. Please see [Mongoose Populate](http://mongoosejs.com/docs/populate.html)|`https://stage.api.xentinel.io/users/?populate=[{"path":"roles","model":"roles"}]`|
|sort|`json` or `string`|Sorts the result data into desired fields|`https://stage.api.xentinel.io/users/?sort="createdAt somethingElse"` or `https://stage.api.xentinel.io/users/?sort={"createdAt":1,"somethingElse":1}`|


###
 Get By ID

URL Convention `https://stage.api.xentinel.io/:MODEL/:ID`, replace `:MODEL` for the desired model, and replace `:ID` for the specific mongo id.

## Post

## Put

## Delete