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
|userId|ObjectID|`false`||`false`|
|name.common|String|`false`||`unique`|
|name.official|String|`false`||`false`|
|name.native|Mixed|`false`||`false`|
|tld|Array|`false`||`false`|
|cca2|String|`false`||`unique`|
|ccn3|String|`false`||`unique`|
|cca3|String|`false`||`unique`|
|cioc|String|`false`||`false`|
|currency|Array|`false`||`false`|
|callingCode|Array|`false`||`false`|
|capital|String|`false`||`false`|
|altSpellings|Array|`false`||`false`|
|region|String|`false`||`false`|
|subregion|String|`false`||`false`|
|languages|Mixed|`false`||`false`|
|translations|Mixed|`false`||`false`|
|latlng|Array|`false`||`false`|
|location.lat|String|`false`||`false`|
|location.lng|String|`false`||`false`|
|demonym|String|`false`||`false`|
|landlocked|Boolean|`false`||`false`|
|borders|Array|`false`||`false`|
|area|Number|`false`||`false`|
|active|Boolean|`false`||`false`|
|visibility|Number|`false`|Default 4|`true`|
|_id|ObjectID|`false`||`false`|
