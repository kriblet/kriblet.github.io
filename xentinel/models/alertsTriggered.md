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
# alertsTriggered

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|user|ObjectID|`true`||`true`|
|alertsConfig|ObjectID|`true`||`true`|
|vehicle|ObjectID|`true`||`true`|
|position|ObjectID|`true`||`true`|
|result|Mixed|`true`||`false`|
|validAt|Date|`false`|Default now() |`true`|
|sentAt|Date|`false`|Default Wed Dec 31 1969 17:00:00 GMT-0700 (PST)|`true`|
|readAt|Date|`false`||`true`|
|error.errorAt|Date|`false`||`true`|
|error.message|String|`false`||`true`|
|createdAt|Date|`false`|Default now() |`true`|
|visibility|Number|`false`|Default 3|`true`|
|_id|ObjectID|`false`||`false`|
