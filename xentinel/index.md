---
title: Xentinel
description: Xentinel API Documentation
layout: post
test: Value
---
# Xentinel
<img src="/img/xentinel2.png" alt="Xentinel.io" width="100px"/>

## Overall
This is a GPS Tracking software light and powerful, made to support [xentinel.io](https://xentinel.io) platform

### Content
[Standard Communication Convention](#standard-communication-convention)
[Required Headers](#required-headers)
[Required Body and Examples](#required-body)
[Login](#login)

## Standard Communication Convention

### Required Headers
Haders must contain the following information:
```javascript
var headers = {
    "x-application-id": "clientID", //provided by Xentinel
    "x-xen-session": "LoggerUserToken", //provided by Xentinel Auth Service
    'Content-Type' : 'application/json; charset=UTF-8' // Required
};
``` 

### Required body

To communicate with our api, some requests must be coded in base64 format, for example:
 ```javascript

// Get example with AngularJs
dataFactory.doGet = function (url) {
    headers["x-xen-session"] = app.user.token;
    return $http({
        method:'GET',
        url: url,
        headers: headers
    });
};

// Get by id example with AngularJs
dataFactory.doGetId = function (url,id) {
    headers["x-xen-session"] = app.user.token;
    return $http({
        method:'GET',
        url: url + id,
        headers: headers
    });
};

// Post example with AngularJs
dataFactory.doPost = function (url,data) {
    headers["x-xen-session"] = app.user.token;
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

## Login

## Generic CRUD

## Public Models Available

## Special Endpoints

## Embedded Xentinel Map
