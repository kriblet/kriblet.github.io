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
# permissions

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|name|String|`false`||`unique`|
|userId|ObjectID|`true`||`true`|
|function|ObjectID|`false`||`false`|
|actions|Array|`false`||`false`|
|visibility|Number|`false`|Default 4|`true`|
|_id|ObjectID|`false`||`false`|
