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

# Init positions history

This endpoint is made to start asking for position updates. 

Scoped to all devices from an user or a specific device.

To start getting updates you must use `init` endpoint.

## Endpoint
`https://api.xentinel.io/history/positions/init/:userId/:deviceId`

## Method
`GET`

## Path Parameters

|Parameter|Type|Required|Description|
|---|---|---|---|
|userId|`ObjectID`|`true`|User id who requires this information|
|deviceId|`ObjectID`|`false`|Device to get positions|

## Get Parameters

|Parameter|Type|Required|Default|Max|Description|
|limit|`number`|`false`|30|30|Number of positions returned of each device|
|skip|`number`|`false`|0||Number of positions skipped for pagination|
|limitV|`number`|`false`|10|10|Number of vehicles returned|
|skipV|`number`|`false`|0||Number of vehicles skipped for pagination|

## Headers
* `x-application-id`
* `x-xen-session`

## Response
```json
{
    "isValid": true,
    "type": 1,
    "data": {
        "items": {
            vehicleId: {
                "positions": [
                    {
                        "_id": ObjectId,
                        "deviceId": ObjectId,
                        "vehicleId": ObjectId,
                        "keyword": String,
                        "time": Number,
                        "date": Datetime,
                        "cellPhoneNumber": String,
                        "av": "A"|"V" (A=Valid,V=invalid),
                        "lat": Float,
                        "sn": "N"|"S" (N=North,S=South),
                        "lng": Float,
                        "ew": "W"|"E" (W=West,E=East),
                        "speed": Number,
                        "direction": Number,
                        "altitude": Number,
                        "accState": Number,
                        "doorState": Number,
                        "fuelSensor1": String("0.00%"),
                        "fuelSensor2": String("0.00%"),
                        "temperature": Number,
                        "location": [
                            Float(Longitude),
                            Float(Latitude)
                        ],
                        "satellites": Number(4> valid),
                        "original": String,
                        "battery": Number,
                        "stopTime": Number,
                        "createdAt": Datetime
                    }
                ]
            }
        },
        "totalCount": 1
    },
    "hasMessages": false,
    "message": ""
}
```

# Next position history

This endpoint is to follow updates from existent device, means returns less data.

## Endpoint
`https://api.xentinel.io/history/positions/next/:userId/:deviceId`

## Method
`GET`

## Path Parameters

|Parameter|Type|Required|Description|
|---|---|---|---|
|userId|`ObjectID`|`true`|User id who requires this information|
|deviceId|`ObjectID`|`false`|Device to get positions|

## Get Parameters

|Parameter|Type|Required|Default|Max|Description|
|lastPosition|`ObjectId`|`true`|`null`|`null`|From positionId to go on forward|
|limit|`number`|`false`|30|30|Number of positions returned of each device|
|skip|`number`|`false`|0||Number of positions skipped for pagination|
|limitV|`number`|`false`|10|10|Number of vehicles returned|
|skipV|`number`|`false`|0||Number of vehicles skipped for pagination|


## Headers
* `x-application-id`
* `x-xen-session`

## Response
```json
{
    "isValid": true,
    "type": 1,
    "data": {
        "items": {
            vehicleId: {
                "positions": [
                    {
                        "_id": ObjectId,
                        "deviceId": ObjectId,
                        "vehicleId": ObjectId,
                        "keyword": String,
                        "time": Number,
                        "date": Datetime,
                        "cellPhoneNumber": String,
                        "av": "A"|"V" (A=Valid,V=invalid),
                        "lat": Float,
                        "sn": "N"|"S" (N=North,S=South),
                        "lng": Float,
                        "ew": "W"|"E" (W=West,E=East),
                        "speed": Number,
                        "direction": Number,
                        "altitude": Number,
                        "accState": Number,
                        "doorState": Number,
                        "fuelSensor1": String("0.00%"),
                        "fuelSensor2": String("0.00%"),
                        "temperature": Number,
                        "location": [
                            Float(Longitude),
                            Float(Latitude)
                        ],
                        "satellites": Number(4> valid),
                        "original": String,
                        "battery": Number,
                        "stopTime": Number,
                        "createdAt": Datetime
                    }
                ]
            }
        },
        "totalCount": 1
    },
    "hasMessages": false,
    "message": ""
}
```