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
|name|String|`false`|`none`|`unique`|
|vehicleGroup|ObjectID|`false`|`none`|`true`|
|vehicles|Array|`false`|`none`|`false`|
|hours.begin.hour|Number|`false`|`none`|`false`|
|hours.begin.minute|Number|`false`|`none`|`false`|
|hours.final.hour|Number|`false`|`none`|`false`|
|hours.final.minute|Number|`false`|`none`|`false`|
|days.monday|Boolean|`false`|`none`|`false`|
|days.tuesday|Boolean|`false`|`none`|`false`|
|days.wednesday|Boolean|`false`|`none`|`false`|
|days.thursday|Boolean|`false`|`none`|`false`|
|days.friday|Boolean|`false`|`none`|`false`|
|days.saturday|Boolean|`false`|`none`|`false`|
|days.sunday|Boolean|`false`|`none`|`false`|
|visibility|Number|`false`|`3`|`true`|
|createdAt|Date|`false`|`now() `|`true`|
|userId|ObjectID|`true`|`none`|`true`|
|userAccess|Array|`false`|`none`|`false`|
|active|Boolean|`false`|`true`|`false`|
|timeOffset|Number|`false`|`none`|`false`|
|_id|ObjectID|`false`|`none`|`false`|
