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
# users

Available model fields.

On this model you can `GET`, `POST`, `PUT` or `DELETE`

Follow [this guide](/xentinel/crud) for generic CRUD Operations

|Field|Type|Required|Default|Index|
|---|---|---|---|---|
|username|String|`false`|`none`|`unique`|
|userId|ObjectID|`true`|`none`|`true`|
|password|String|`false`|`none`|`true`|
|email|String|`false`|`none`|`unique`|
|active|Boolean|`false`|`true`|`false`|
|defaultCity|ObjectID|`false`|`none`|`false`|
|information.avatar|String|`true`|`none`|`false`|
|information.name|String|`true`|`none`|`true`|
|information.lastName|String|`true`|`none`|`true`|
|information.male|Boolean|`true`|`true`|`false`|
|information.phone|String|`true`|`none`|`unique`|
|information.mobilePhone|String|`true`|`none`|`unique`|
|information.country|ObjectID|`true`|`none`|`false`|
|information.state|ObjectID|`true`|`none`|`false`|
|information.city|ObjectID|`true`|`none`|`false`|
|information.street|String|`true`|`none`|`true`|
|information.outsideNumber|String|`true`|`none`|`true`|
|information.insideNumber|String|`false`|`none`|`true`|
|information.neighborhood|String|`true`|`none`|`true`|
|information.zipCode|String|`true`|`none`|`true`|
|information.location.lat|String|`true`|`none`|`false`|
|information.location.lng|String|`true`|`none`|`false`|
|security.expirePassword|Boolean|`false`|`true`|`false`|
|security.notifyPasswordExpires|Boolean|`false`|`true`|`false`|
|security.contactByPhone|Boolean|`false`|`true`|`false`|
|security.contactByEmail|Boolean|`false`|`true`|`false`|
|security.sendTips|Boolean|`false`|`true`|`false`|
|roles|Array|`false`|`none`|`false`|
|permissions|Array|`false`|`none`|`false`|
|acceptLocation|Boolean|`false`|`none`|`false`|
|acceptTerms|Boolean|`false`|`none`|`false`|
|subscribeNewsLetter|Boolean|`false`|`none`|`false`|
|accountLevel|Number|`false`|`none`|`false`|
|createdAt|Date|`false`|`now() `|`true`|
|userType|Number|`false`|`2`|`false`|
|visibility|Number|`false`|`3`|`true`|
|subUsers|Array|`false`|`none`|`false`|
|subscribers|Array|`false`|`none`|`false`|
|owner|Array|`false`|`none`|`false`|
|locale|String|`false`|`es`|`false`|
|_id|ObjectID|`false`|`none`|`false`|
