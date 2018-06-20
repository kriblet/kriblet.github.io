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
|userId|ObjectID|`true`||`false`|
|name|String|`true`||`false`|
|description|String|`true`||`false`|
|entities|Array|`false`||`false`|
|validAt|Date|`false`||`false`|
|createdAt|Date|`false`|Default now() |`false`|
|userAccess|Array|`false`||`false`|
|visibility|Number|`false`|Default 3|`true`|
|_id|ObjectID|`false`||`false`|
