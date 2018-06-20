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
|name|String|`true`|`none`|`false`|
|userId|ObjectID|`true`|`none`|`true`|
|alertsTypes|Array|`false`|`none`|`false`|
|vehicleGroupId|ObjectID|`false`|`none`|`true`|
|vehicleId|ObjectID|`false`|`none`|`true`|
|config|Mixed|`true`|`none`|`false`|
|expireMinutes|Number|`false`|`60`|`false`|
|nextTriggerAt|Date|`false`|`now() `|`true`|
|lastTriggered.alertsTriggeredId|ObjectID|`false`|`none`|`true`|
|lastTriggered.triggeredAt|Date|`false`|`none`|`false`|
|hours|Array|`false`|`none`|`false`|
|days.monday|Boolean|`false`|`none`|`false`|
|days.tuesday|Boolean|`false`|`none`|`false`|
|days.wednesday|Boolean|`false`|`none`|`false`|
|days.thursday|Boolean|`false`|`none`|`false`|
|days.friday|Boolean|`false`|`none`|`false`|
|days.saturday|Boolean|`false`|`none`|`false`|
|days.sunday|Boolean|`false`|`none`|`false`|
|extraContacts.emails|Array|`false`|`none`|`false`|
|extraContacts.phones|Array|`false`|`none`|`false`|
|validAt|Date|`false`|`none`|`true`|
|createdAt|Date|`false`|`now() `|`true`|
|visibility|Number|`false`|`3`|`true`|
|userAccess|Array|`false`|`none`|`false`|
|subscribers|Array|`false`|`none`|`false`|
|activeShutdown|Boolean|`false`|`none`|`false`|
|muted|Boolean|`false`|`none`|`false`|
|_id|ObjectID|`false`|`none`|`false`|
