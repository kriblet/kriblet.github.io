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
# alertsConfigs

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|name|String|`true`||`false`|
|userId|ObjectID|`true`||`true`|
|alertsTypes|Array|`false`||`false`|
|vehicleGroupId|ObjectID|`false`||`true`|
|vehicleId|ObjectID|`false`||`true`|
|config|Mixed|`true`||`false`|
|expireMinutes|Number|`false`|Default 60|`false`|
|nextTriggerAt|Date|`false`|Default now() |`true`|
|lastTriggered.alertsTriggeredId|ObjectID|`false`||`true`|
|lastTriggered.triggeredAt|Date|`false`||`false`|
|hours|Array|`false`||`false`|
|days.monday|Boolean|`false`||`false`|
|days.tuesday|Boolean|`false`||`false`|
|days.wednesday|Boolean|`false`||`false`|
|days.thursday|Boolean|`false`||`false`|
|days.friday|Boolean|`false`||`false`|
|days.saturday|Boolean|`false`||`false`|
|days.sunday|Boolean|`false`||`false`|
|extraContacts.emails|Array|`false`||`false`|
|extraContacts.phones|Array|`false`||`false`|
|validAt|Date|`false`||`true`|
|createdAt|Date|`false`|Default now() |`true`|
|visibility|Number|`false`|Default 3|`true`|
|userAccess|Array|`false`||`false`|
|subscribers|Array|`false`||`false`|
|activeShutdown|Boolean|`false`||`false`|
|muted|Boolean|`false`||`false`|
|_id|ObjectID|`false`||`false`|
