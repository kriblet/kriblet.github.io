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
|username|String|`false`||`unique`|
|userId|ObjectID|`true`||`true`|
|password|String|`false`||`true`|
|email|String|`false`||`unique`|
|active|Boolean|`false`|Default true|`false`|
|defaultCity|ObjectID|`false`||`false`|
|information.avatar|String|`true`||`false`|
|information.name|String|`true`||`true`|
|information.lastName|String|`true`||`true`|
|information.male|Boolean|`true`|Default true|`false`|
|information.phone|String|`true`||`unique`|
|information.mobilePhone|String|`true`||`unique`|
|information.country|ObjectID|`true`||`false`|
|information.state|ObjectID|`true`||`false`|
|information.city|ObjectID|`true`||`false`|
|information.street|String|`true`||`true`|
|information.outsideNumber|String|`true`||`true`|
|information.insideNumber|String|`false`||`true`|
|information.neighborhood|String|`true`||`true`|
|information.zipCode|String|`true`||`true`|
|information.location.lat|String|`true`||`false`|
|information.location.lng|String|`true`||`false`|
|security.expirePassword|Boolean|`false`|Default true|`false`|
|security.notifyPasswordExpires|Boolean|`false`|Default true|`false`|
|security.contactByPhone|Boolean|`false`|Default true|`false`|
|security.contactByEmail|Boolean|`false`|Default true|`false`|
|security.sendTips|Boolean|`false`|Default true|`false`|
|roles|Array|`false`||`false`|
|permissions|Array|`false`||`false`|
|acceptLocation|Boolean|`false`||`false`|
|acceptTerms|Boolean|`false`||`false`|
|subscribeNewsLetter|Boolean|`false`||`false`|
|accountLevel|Number|`false`||`false`|
|createdAt|Date|`false`|Default now() |`true`|
|userType|Number|`false`|Default 2|`false`|
|visibility|Number|`false`|Default 3|`true`|
|subUsers|Array|`false`||`false`|
|subscribers|Array|`false`||`false`|
|owner|Array|`false`||`false`|
|locale|String|`false`|Default es|`false`|
|_id|ObjectID|`false`||`false`|
