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

# Conventions

## Responses
All responses structure from our api are the same.


| Name | Type | Description | 
|---|---|---|
| isValid | Boolean | Returns `true` when is a success response |
| data | Object | Contains the data from the request |
| hasMessages | Boolean | Returns `true` when response has messages |
| message | String | Contains the message when `hasMessages` is `true` |
| error | Object | Contains all error information when `isValid` is `false` |

## Required Headers
Haders must contain the following information:

Headers set
| Name | Type | Description | 
|---|---|---|
| x-application-id | String | Contains your ClientID provided by Xentinel |
| x-xen-session | String | Contains your session `token` provided by Xentinel API Login endpoint |
| Content-Type | String | Contains the data type sent `application/json; charset=UTF-8;` |


Example Javascript
```js
var headers = {
    "x-application-id": "clientID", //provided by Xentinel
    "x-xen-session": "LoggerUserToken", //provided by Xentinel Auth Service
    'Content-Type' : 'application/json; charset=UTF-8' // Required
};
``` 

## Expected Body Parameter

To communicate with our api, some requests must be coded in base64 format, for example:


Parameters
| Name | Type | Description | 
|---|---|---|---|
| value | String | Contains base64 representation of `contract` type of the endpoint |

 
 ### Get Example
 ```js
// Get example with AngularJs
dataFactory.doGet = function (url) {
    headers["x-xen-session"] = user.token;
    return $http({
        method:'GET',
        url: url,
        headers: headers
    });
};
```
### Clean Get Example
```js
// Get by id example with AngularJs
dataFactory.doGetId = function (url,id) {
    headers["x-xen-session"] = user.token;
    return $http({
        method:'GET',
        url: url + id,
        headers: headers
    });
};
```

### Post example

Please verify how the field `userId` is attached to the data object before converting it into base64 and send it to the server.

```js
// Post example with AngularJs
dataFactory.doPost = function (url,data) {
    headers["x-xen-session"] = user.token;
    if (app.user && data)
        data.userId = app.user._id;

    var dataToSend = "";
    if (data){
        var b64Data = utf8_to_b64(JSON.stringify(data));
        dataToSend = {
            value: b64Data
        }
    }
    return $http({
        method:'POST',
        url: url,
        data: dataToSend,
        headers: headers
    });
};

```

### Clean Post Example
```js
// Clean Post example with AngularJs
dataFactory.doCleanPost = function (url,data) {
    var headers = {
        "x-application-id": app._id,
        "x-xen-session": app.user.token,
        "Content-Type": undefined
    };
    return $http({
        method:'POST',
        url: url,
        data: data,
        headers: headers
    });
};
```

### Put Example

Please verify how the field `updateUserId` is attached to the data object before converting it into base64 and send it to the server.

```js

// Put example with AngularJs
dataFactory.doPut = function (url,data) {
    headers["x-xen-session"] = app.user.token;
    var dataToSend = "";
    if (data){
        if (app.user && data) {
            data.updateUserId = app.user._id;
        }
        var b64Data = utf8_to_b64(JSON.stringify(data));
        dataToSend = {
            value: b64Data
        }; 
        if (data._id){
            if (url.substr(url.length -1) !== '/'){
                url += '/';
            }
            url += data._id;
        }

    }
    return $http({
        method:'PUT',
        url: url,
        data: dataToSend,
        headers: headers
    });
};
```

### Clean Put Example

```js
// Clean Put example with AngularJs
dataFactory.doCleanPut = function (url,data) {
    headers["x-xen-session"] = app.user.token;
    var dataToSend = "";
    if (data){
        var b64Data = utf8_to_b64(JSON.stringify(data));
        dataToSend = {
            value: b64Data
        }
    }
    return $http({
        method:'PUT',
        url: url,
        data: dataToSend,
        headers: headers
    });
};

```

### Delete Example
```js
// Delete example with AngularJs
dataFactory.doDelete = function (url,data) {
    headers["x-xen-session"] = app.user.token;
    var dataToSend = "";
    if (data){
        var b64Data = utf8_to_b64(JSON.stringify(data));
        dataToSend = {
            value: b64Data
        };
        if (data._id){
            if (url.substr(url.length -1) !== '/'){
                url += '/';
            }
            url += data._id;
        }
    }
    return $http({
        method:'DELETE',
        url: url,
        data: dataToSend,
        headers: headers
    });
};
 ```