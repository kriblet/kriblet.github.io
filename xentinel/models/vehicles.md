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
|name|String|`true`||`unique`|
|alias|String|`false`||`unique`|
|licensePlate|String|`true`||`unique`|
|brand|String|`true`||`true`|
|model|String|`true`||`true`|
|year|String|`true`||`true`|
|vin|String|`true`||`unique`|
|performance|Number|`false`||`false`|
|gasTank|Number|`false`||`false`|
|vehicleType|Number|`true`||`false`|
|deviceId|ObjectID|`false`||`false`|
|userId|ObjectID|`false`||`false`|
|entityTypeId|ObjectID|`false`||`false`|
|createdAt|Date|`false`|Default now() |`false`|
|nextPaymentAt|Date|`false`||`false`|
|active|Boolean|`false`||`false`|
|color|String|`true`||`false`|
|userAccess|Array|`false`||`false`|
|visibility|Number|`false`|Default 3|`true`|
|engineStatus|Boolean|`false`|Default true|`false`|
|activeShutdown|Boolean|`false`|Default true|`false`|
|accConnected|Boolean|`false`|Default true|`false`|
|_id|ObjectID|`false`||`false`|
