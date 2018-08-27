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

# Near vehicles

To get the near vehicles we must send GET with 2 required parameters.
__URL:__ `/endpoint/vehicles/near/:lat/:lng`

[Example](#example)

### Parameters

| Name | Type | Required | Description | 
|:--|:-------|:------|:---------------------|
| lat | Double | `true` | Contains the latitude |
| lng | Double | `true` | Contains the longitude |

### Result
Vehicles list near to the location given


## Example
Near vehicles example AngularJs
```js
$dataFactory.doGet(app.apiPrefix + '/endpoint/vehicles/near/25.795507/-108.950868'})
    .success(function(result) {
        if (result.isValid) {
            var vehicles = result.data;
        } else {
            // Failed get see result.error / result.message
        }
    })
    .error(function(err){
        // Failed get see result.error / result.message
        console.error(err);
    });
```