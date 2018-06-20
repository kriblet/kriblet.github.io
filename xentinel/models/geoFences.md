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
|name|String|`true`||`false`|
|userId|ObjectID|`true`||`true`|
|loc.type|String|`false`||`false`|
|loc.coordinates|Array|`false`||`false`|
|color|String|`true`||`false`|
|userAccess|Array|`false`||`false`|
|createdAt|Date|`false`|Default now() |`true`|
|visibility|Number|`false`|Default 3|`true`|
|_id|ObjectID|`false`||`false`|
