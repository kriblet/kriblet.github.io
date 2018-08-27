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
# states

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|name|String|`false`|`none`|`true`|
|userId|ObjectID|`false`|`none`|`true`|
|country|ObjectID|`false`|`none`|`false`|
|location.lat|String|`false`|`none`|`false`|
|location.lng|String|`false`|`none`|`false`|
|visibility|Number|`false`|`4`|`true`|
|_id|ObjectID|`false`|`none`|`false`|
