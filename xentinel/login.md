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

# Login

Login method to get a valid Token for the next 30 minutes, this token must be refreshed each 30 minutes.

[Login Example](#example)

## Endpoint

`https://api.xentinel.io/endpoint/security/login`

## Method

`POST`

### Post Parameters

| Name | Type | Required | Description | 
|:--|:-------|:------|:---------------------|
| u | String | `true` | Contains the username |
| p | String | `true` | Contains the password |

## Result

User Object and Token
```json
{
    "token": String,
    "_id": ObjectID,//user _id
    "username": String,
    "picture": String(uri),
    "userType": Number
} 
```


## Example
Login Example AngularJs
```js
$dataFactory.doPost(app.apiPrefix + '/endpoint/security/login', {u:$scope.usr, p:$scope.pwd})
    .success(function(result) {
        if (result.isValid) {
            var user = result.data;
            var token = user.token;
        } else {
            // Failed login see result.error / result.message
        }
    })
    .error(function(err){
        // Failed login see result.error / result.message
        console.error(err);
    });
```