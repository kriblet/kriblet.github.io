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
# vehicles

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|name|String|`true`|`none`|`unique`|
|alias|String|`false`|`none`|`unique`|
|licensePlate|String|`true`|`none`|`unique`|
|brand|String|`true`|`none`|`true`|
|model|String|`true`|`none`|`true`|
|year|String|`true`|`none`|`true`|
|vin|String|`true`|`none`|`unique`|
|performance|Number|`false`|`none`|`false`|
|gasTank|Number|`false`|`none`|`false`|
|vehicleType|Number|`true`|`none`|`false`|
|deviceId|ObjectID|`false`|`none`|`false`|
|userId|ObjectID|`false`|`none`|`false`|
|entityTypeId|ObjectID|`false`|`none`|`false`|
|createdAt|Date|`false`|`now() `|`false`|
|nextPaymentAt|Date|`false`|`none`|`false`|
|active|Boolean|`false`|`none`|`false`|
|color|String|`true`|`none`|`false`|
|userAccess|Array|`false`|`none`|`false`|
|visibility|Number|`false`|`3`|`true`|
|engineStatus|Boolean|`false`|`true`|`false`|
|activeShutdown|Boolean|`false`|`true`|`false`|
|accConnected|Boolean|`false`|`true`|`false`|
|_id|ObjectID|`false`|`none`|`false`|
