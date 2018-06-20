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
# cities

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|userId|ObjectID|`false`||`false`|
|name|String|`false`||`true`|
|state|ObjectID|`false`||`false`|
|location.lat|String|`false`||`false`|
|location.lng|String|`false`||`false`|
|visibility|Number|`false`|Default 4|`true`|
|_id|ObjectID|`false`||`false`|
