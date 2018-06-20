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
|name|String|`false`||`unique`|
|imei|String|`false`||`unique`|
|phone|String|`false`||`unique`|
|userId|ObjectID|`false`||`false`|
|lastSeen|Date|`false`||`false`|
|createdAt|Date|`false`|Default now() |`false`|
|attached|Boolean|`false`||`false`|
|active|Boolean|`false`||`false`|
|gmt|Number|`false`||`false`|
|visibility|Number|`false`|Default 3|`true`|
|userAccess|Array|`false`||`false`|
|_id|ObjectID|`false`||`false`|
