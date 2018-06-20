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
# alertsTypes

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|userId|ObjectID|`false`|`none`|`false`|
|name|String|`true`|`none`|`unique`|
|properties|Array|`false`|`none`|`false`|
|related|Array|`false`|`none`|`false`|
|createdAt|Date|`false`|`now() `|`true`|
|visibility|Number|`false`|`4`|`true`|
|_id|ObjectID|`false`|`none`|`false`|
