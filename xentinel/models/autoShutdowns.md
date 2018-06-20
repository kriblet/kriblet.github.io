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
# autoShutdowns

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|name|String|`false`||`unique`|
|vehicleGroup|ObjectID|`false`||`true`|
|vehicles|Array|`false`||`false`|
|hours.begin.hour|Number|`false`||`false`|
|hours.begin.minute|Number|`false`||`false`|
|hours.final.hour|Number|`false`||`false`|
|hours.final.minute|Number|`false`||`false`|
|days.monday|Boolean|`false`||`false`|
|days.tuesday|Boolean|`false`||`false`|
|days.wednesday|Boolean|`false`||`false`|
|days.thursday|Boolean|`false`||`false`|
|days.friday|Boolean|`false`||`false`|
|days.saturday|Boolean|`false`||`false`|
|days.sunday|Boolean|`false`||`false`|
|visibility|Number|`false`|Default 3|`true`|
|createdAt|Date|`false`|Default now() |`true`|
|userId|ObjectID|`true`||`true`|
|userAccess|Array|`false`||`false`|
|active|Boolean|`false`|Default true|`false`|
|timeOffset|Number|`false`||`false`|
|_id|ObjectID|`false`||`false`|
