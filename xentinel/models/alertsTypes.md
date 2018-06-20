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
|userId|ObjectID|`false`||`false`|
|name|String|`true`||`unique`|
|properties|Array|`false`||`false`|
|related|Array|`false`||`false`|
|createdAt|Date|`false`|Default now() |`true`|
|visibility|Number|`false`|Default 4|`true`|
|_id|ObjectID|`false`||`false`|
