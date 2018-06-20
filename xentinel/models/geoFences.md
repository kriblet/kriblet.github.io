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
# geoFences

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|name|String|`true`|`none`|`false`|
|userId|ObjectID|`true`|`none`|`true`|
|loc.type|String|`false`|`none`|`false`|
|loc.coordinates|Array|`false`|`none`|`false`|
|color|String|`true`|`none`|`false`|
|userAccess|Array|`false`|`none`|`false`|
|createdAt|Date|`false`|`now() `|`true`|
|visibility|Number|`false`|`3`|`true`|
|_id|ObjectID|`false`|`none`|`false`|
