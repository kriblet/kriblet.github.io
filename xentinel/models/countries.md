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
# countries

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|userId|ObjectID|`false`|`none`|`false`|
|name.common|String|`false`|`none`|`unique`|
|name.official|String|`false`|`none`|`false`|
|name.native|Mixed|`false`|`none`|`false`|
|tld|Array|`false`|`none`|`false`|
|cca2|String|`false`|`none`|`unique`|
|ccn3|String|`false`|`none`|`unique`|
|cca3|String|`false`|`none`|`unique`|
|cioc|String|`false`|`none`|`false`|
|currency|Array|`false`|`none`|`false`|
|callingCode|Array|`false`|`none`|`false`|
|capital|String|`false`|`none`|`false`|
|altSpellings|Array|`false`|`none`|`false`|
|region|String|`false`|`none`|`false`|
|subregion|String|`false`|`none`|`false`|
|languages|Mixed|`false`|`none`|`false`|
|translations|Mixed|`false`|`none`|`false`|
|latlng|Array|`false`|`none`|`false`|
|location.lat|String|`false`|`none`|`false`|
|location.lng|String|`false`|`none`|`false`|
|demonym|String|`false`|`none`|`false`|
|landlocked|Boolean|`false`|`none`|`false`|
|borders|Array|`false`|`none`|`false`|
|area|Number|`false`|`none`|`false`|
|active|Boolean|`false`|`none`|`false`|
|visibility|Number|`false`|`4`|`true`|
|_id|ObjectID|`false`|`none`|`false`|
