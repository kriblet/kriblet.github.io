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
|user|ObjectID|`true`|`none`|`true`|
|alertsConfig|ObjectID|`true`|`none`|`true`|
|vehicle|ObjectID|`true`|`none`|`true`|
|position|ObjectID|`true`|`none`|`true`|
|result|Mixed|`true`|`none`|`false`|
|validAt|Date|`false`|`now() `|`true`|
|sentAt|Date|`false`|`Wed Dec 31 1969 17:00:00 GMT-0700 (PST)`|`true`|
|readAt|Date|`false`|`none`|`true`|
|error.errorAt|Date|`false`|`none`|`true`|
|error.message|String|`false`|`none`|`true`|
|createdAt|Date|`false`|`now() `|`true`|
|visibility|Number|`false`|`3`|`true`|
|_id|ObjectID|`false`|`none`|`false`|
