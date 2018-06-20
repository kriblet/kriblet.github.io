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
# devices

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|name|String|`false`|`none`|`unique`|
|imei|String|`false`|`none`|`unique`|
|phone|String|`false`|`none`|`unique`|
|userId|ObjectID|`false`|`none`|`false`|
|lastSeen|Date|`false`|`none`|`false`|
|createdAt|Date|`false`|`now() `|`false`|
|attached|Boolean|`false`|`none`|`false`|
|active|Boolean|`false`|`none`|`false`|
|gmt|Number|`false`|`none`|`false`|
|visibility|Number|`false`|`3`|`true`|
|userAccess|Array|`false`|`none`|`false`|
|_id|ObjectID|`false`|`none`|`false`|
