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

# Security Check Status

This endpoint is made to check a token status.


|Endpoint|Http Method|Headers|Response|
|---|---|---|---|
|`https://api.xentinel.io/endpoint/security/checkStatus`|`POST`|`x-application-id` & `x-xen-session`|`{"isValid":Boolean,"type":Number,"data":{"_id":ObjectID,"username":String,"email":String,"userId":ObjectID,"locale":String,"owner":Array[ObjectID],"subscribers":Array[ObjectID],"subUsers":Array[ObjectID],"visibility":Number,"userType":Number,"createdAt":Datetime,"accountLevel":Number,"permissions":Array,"roles":Array,"security":{"sendTips":Boolean,"contactByEmail":Boolean,"contactByPhone":Boolean,"notifyPasswordExpires":Boolean,"expirePassword":Boolean},"information":{"name":String,"lastName":String,"phone":String,"mobilePhone":String,"country":ObjectID,"state":ObjectID,"city":ObjectID,"street":String,"outsideNumber":Number,"neighborhood":String,"zipCode":Number,"location":{"lat":Float,"lng":Float},"male":Boolean,"avatar":URI},"active":Boolean,"token":String},"hasMessages":Boolean,"message":String}`|