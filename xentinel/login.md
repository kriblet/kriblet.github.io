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

#Login

To login we must send POST with 2 required parameters.

[Login Example](#example)

### Parameters

| Name | Type | Required | Description | 
|:--|:-------|:------|:---------------------|
| u | String | `true` | Contains the username |
| p | String | `true` | Contains the password |

### Result
User Object and Token


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