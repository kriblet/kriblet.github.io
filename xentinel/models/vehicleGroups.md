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
# vehicleGroups

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|userId|ObjectID|`true`|`none`|`false`|
|name|String|`true`|`none`|`false`|
|description|String|`true`|`none`|`false`|
|entities|Array|`false`|`none`|`false`|
|validAt|Date|`false`|`none`|`false`|
|createdAt|Date|`false`|`now() `|`false`|
|userAccess|Array|`false`|`none`|`false`|
|visibility|Number|`false`|`3`|`true`|
|_id|ObjectID|`false`|`none`|`false`|
