---
title: SentinelJs
description: SentinelJs Documentation
---


# Handshake service

__Path:__ /api/v1.0/auth/handshake  
__Method:__ POST  
__Description:__ Handshake service for users login

### Request body
|media type| data type | description |
|-------|--------|---------|
|application/json| HandshakeModel (JSON)| Handshake model|

### Response body
|media type| data type | description |
|-------|--------|---------|
|application/json| AccountMaskedModel (JSON)| Full name masked |


### Example

#### Request

```
POST /api/v1.0/auth/handshake
Content-Type: application/json
Accept: application/json

{
	"account": "..."
}
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": {
		"fullName": "A******* B***** C*****"
	}
}
```

## Models

### Handshake model

| name | type | description |
|-------|--------|---------|
| account | String | User account number |

### Account masked model

| name | type | description |
|-------|--------|---------|
| fullName | String | Full name masked |


# Auth service

__Path:__ /api/v1.0/auth/login  
__Method:__ POST  
__Description:__ Login service for users

### Request body
|media type| data type | description |
|-------|--------|---------|
|application/json| LoginModel (JSON)| Login model |

### Response body
|media type| data type | description |
|-------|--------|---------|
|application/json| TokenModel (JSON)| Token for user logged model |


### Example

#### Request

```
POST /api/v1.0/auth/login
Content-Type: application/json
Accept: application/json

{
	"account": "...",
	"confirm": "..."
}
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": {
		"token": "..."
	}
}
```

## Models

### Login model

| name | type | description |
|-------|--------|---------|
| account | String | User account number |
| confirm | Boolean | User must confirm that it is his account |

## Token model
| name | type | description |
|-------|--------|---------|
| token | String | Access token |

# Balance service

__Path:__ /api/v1.0/account/balance  
__Method:__ GET   
__Description:__ Balance service for accounts

### Request headers
| name| type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Response body
|media type| data type | description |
|-------|--------|---------|
|application/json| BbalanceModel (JSON)| Balance model|


### Example

#### Request

```
GET /api/v1.0/account/balance
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": {
		"_id": "...",
		"amount": "..."
		"expirationAt": "...",
		"balanceAt": "...",
		"isDept": "...",
		"payment": {
			"_id": "...",
			"amount": "...",
			"receiptId": "...",
			"paymentAt": "..."
		}
	}
}
```

## Models

## Balance model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| amount | Double | Account balance amount |
| expirationAt | Date | Account balance expiration date |
| balanceAt | Date | Account balance date |
| isDept | Boolean | Account has debit |
| payment (Optional) | PaymentModel | The last payment if there was |

## Payment model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| amount | Double | Payment amount |
| receiptId | Integer | Receipt identifier |
| paymentAt | Date | Payment date |

# Payments service

__Path:__ /api/v1.0/account/payments  
__Method:__ GET   
__Description:__ Last payments service for accounts

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Payments list (Array)| Last payments |


### Example

#### Request

```
GET /api/v1.0/account/payments
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": [
		{
		"_id": "...",
		"id": "...",
		"amount": "..."
		"paymentAt: "..."
	},
	{
		"_id": "...",
		"id": "...",
		"amount": "..."
		"paymentAt: "..."
	},
	...
	]
}
```

## Models

## Payment model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| id | Integer | Payment identifier |
| amount | Double | Payment amount |
| paymentAt | Date | Payment date |


# Receipts service

__Path:__ /api/v1.0/account/receipts  
__Method:__ GET   
__Description:__ Last receipts service for accounts

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Receipts list (Array)| Last receipts |


### Example

#### Request

```
GET /api/v1.0/account/receipts
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": [
		{
			"_id": "...",
			"id": "...",
			"amount": "..."
			"consumption": "...",
			"measurementUnit": "...",
			"previousDept": "...",
			"totalAmount": "...",
			"registerAt: "...",
			"expirationAt: "...",
			"periodsOwed": "...",
			"isCanceled": "...",
			"details": [
				{
						"_id": "...",
						"id": "...",
						"nature": "..."
						"quantity": "...",
						"description": "...",
						"unitPrice": "...",
						"amount": "..."
				},
				{
					"_id": "...",
					"id": "...",
					"nature": "..."
					"quantity": "...",
					"description": "...",
					"unitPrice": "...",
					"amount": "..."
				},
				...
			]
	},
	{
		"_id": "...",
		"id": "...",
		"amount": "..."
		"consumption": "...",
		"measurementUnit": "...",
		"previousDept": "...",
		"totalAmount": "...",
		"registerAt: "...",
		"expirationAt: "...",
		"periodsOwed": "...",
		"isCanceled": "...",
		"details": [
			{
					"_id": "...",
					"id": "...",
					"nature": "..."
					"quantity": "...",
					"description": "...",
					"unitPrice": "...",
					"amount": "..."
			},
			{
				"_id": "...",
				"id": "...",
				"nature": "..."
				"quantity": "...",
				"description": "...",
				"unitPrice": "...",
				"amount": "..."
			},
			...
		]
	},
	...
	]
}
```

## Models

## Receipts model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| id | Integer | Receipt identifier |
| amount | Double | Receipt amount |
| consumption | Double | Receipt consumption |
| measurementUnit | Double | Consumption measurement unit |
| previousDept | Double | Receipt previous dept |
| totalAmount | Double | Receipt amount + previoutDept |
| registerAt | Date | Register date |
| expirationAt | Date | Expiration date |
| details | Receipt details list (Array) | Receipt details |

## Receipt details model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| id | Integer | Detail identifier 
| nature | Boolean | debit (true) or credit (false) |
| quantity | Double | Detail quantity |
| description | Double | Description |
| unitPrice | Double | Detail unit price |
| amount | Double | Detail amount |

# Payment methods service

__Path:__ /api/v1.0/payment/methods  
__Method:__ GET   
__Description:__ Payment methods service for accounts

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Payment methods list (Array)| Payment methods |


### Example

#### Request

```
GET /api/v1.0/payment/methods
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": [
		{
			"_id": "...",
			"name": "...",
			"options": [
				{
					"_id": "...",
					"name": "...",
					"address": {
						"street: "...",
						"outsideNumber: "...",
						"insideNumber: "...",
						"zipCode: "...",
						"neighborhood: "...",
						"betweenStreet1: "...",
						"betweenStreet2: "...",
						"lot: "...",
						"square: "..."
					}
				},
				...
			]
	},
	...
	]
}
```

## Models

## Payment method category model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| name | String | Category name |
| options | Payment options list (Array) | Payment method options |

## Payment method option model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| name | Boolean | debit (true) or credit (false) |
| address | Address model (Optional) | Address |

## Address model
| name | type | description |
|-------|--------|---------|
| street | String | Street name |
| outsideNumber | String | Address outside number |
| insideNumber | String | Address inside number |
| zipCode | Integer | Address zipCode |
| neighborhood | String | Address neighborhood |
| betweenStreet1 | String | First between street |
| betweenStreet2 | String | Second between street |
| lot | String | Address lot |
| square | String | Address square |

# Complaint service

__Path:__ /api/v1.0/account/complaint  
__Method:__ POST   
__Description:__ Complaint service for accounts

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Request body
| media type | data type | description |
|-------|--------|---------|
| application/json | Complaint model | Complaint |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Complaint saved model | Complaint saved |


### Example

#### Request

```
POST /api/v1.0/account/complaint
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN

{
  "comment" : "..."
} 
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": {
		"newId": "..."
	}
}
```

## Models

## Complaint model
| name | type | description |
|-------|--------|---------|
| comment | String | Complaint comment |

## Complaint saved model
| name | type | description |
|-------|--------|---------|
| newId | String | Unique identifier |


# General leak service

__Path:__ /api/v1.0/leak/general
__Method:__ POST   
__Description:__ General leak service

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Request body
| media type | data type | description |
|-------|--------|---------|
| application/json | Leak model | Leak |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Leak saved model | Leak saved |


### Example

#### Request

```
POST /api/v1.0/leak/general
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN

{
	"type": "...",
	"address": "...",
  "comment" : "..."
} 
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": {
		"newId": "..."
	}
}
```

## Models

## Leak model
| name | type | description |
|-------|--------|---------|
| type | String | Leak type [water, drainage] |
| address | String | Leak address |
| comment | String | Leak comment |

## Leak saved model
| name | type | description |
|-------|--------|---------|
| newId | String | Unique identifier |


# Domestic leak service

__Path:__ /api/v1.0/leak/domestic
__Method:__ POST   
__Description:__ Domestic leak service

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Request body
| media type | data type | description |
|-------|--------|---------|
| application/json | Leak model | Leak |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Leak saved model | Leak saved |


### Example

#### Request

```
POST /api/v1.0/leak/general
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN

{
	"type": "...",
  "comment" : "..."
} 
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": {
		"newId": "..."
	}
}
```

## Models

## Leak model
| name | type | description |
|-------|--------|---------|
| type | String | Leak type [water, drainage, measurer] |
| comment | String | Leak comment |

## Leak saved model
| name | type | description |
|-------|--------|---------|
| newId | String | Unique identifier |

# Notes service

__Path:__ /api/v1.0/account/notes  
__Method:__ GET   
__Description:__ Notes service for accounts

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Notes list (Array)| Last notes |


### Example

#### Request

```
GET /api/v1.0/account/notes
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": [
		{
		"_id": "...",
		"title": "...",
		"description": "..."
		"image: "example.jpg",
		"url": "http://example.com"
	},
	{
		"_id": "...",
		"title": "...",
		"description": "..."
		"image: "example.jpg",
		"url": "http://example.com"
	},
	...
	]
}
```

## Models

## Note model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| title | String | Note title |
| description | String | Note description |
| image | String | Image name (See image service) |
| url | String | Note URL |

# Relays service

__Path:__ /api/v1.0/account/relays  
__Method:__ GET   
__Description:__ Relays service for accounts

### Request headers
| name | type | description |
|-------|--------|---------|
| Authorization | String | Access token |

### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Relays list (Array)| Last relays |


### Example

#### Request

```
GET /api/v1.0/account/relays
Content-Type: application/json
Accept: application/json
Authorization: $TOKEN
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": [
		{
		"_id": "...",
		"title": "...",
		"description": "..."
		"image: "example.jpg",
		"scheduledAt": "...",
		"endScheduledAt": "..."
	},
	{
		"_id": "...",
		"title": "...",
		"description": "..."
		"image: "example.jpg",
		"scheduledAt": "...",
		"endScheduledAt": "..."
	},
	...
	]
}
```

## Models

## Relay model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| title | String | Relay title |
| description | String | Relay description |
| image | String | Image name (See image service) |
| scheduledAt | Date | Relay scheduled start date |
| endScheduledAt | Date | Relay scheduled end date |

# Image service

__Path:__ /api/v1.0/multimedia/image/$IMAGE  
__Method:__ GET   
__Description:__ Image service

### Response body
| media type | data type | description |
|-------|--------|---------|
| image/jpeg | Image | Image |


### Example

#### Request

```
GET /api/v1.0/multimedia/image/example.jpg
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: image/jpeg
```

# Notification configuration service

__Path:__ /api/v1.0/account/notifications  
__Method:__ PUT  
__Description:__ Notification configuration service for accounts

### Request body
|media type| data type | description |
|-------|--------|---------|
|application/json| NotificationConfigModel (JSON)| Notification configuration model|

### Response body
|media type| data type | description |
|-------|--------|---------|
|application/json| UpdatedModel (JSON)| Updated model |


### Example

#### Request

```
PUT /api/v1.0/account/notifications
Content-Type: application/json
Accept: application/json

{
	"balanceExpires": true,
	"serviceCut": true,
	"suspended": true,
	"lackOfService": true
}
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": {
		"updated": true
	}
}
```

## Models

### Notification configuration model

| name | type | description |
|-------|--------|---------|
| balanceExpires | Boolean | Balance expires notification enabled |
| serviceCut | Boolean | Service cut notification enabled |
| suspended | Boolean | Account suspended notification enabled |
| lackOfService | Boolean | Lack of service notification enabled |


### Updated model

| name | type | description |
|-------|--------|---------|
| updated | Boolean | Model updated response |

# FAQs service

__Path:__ /api/v1.0/account/faqs  
__Method:__ GET   
__Description:__ FAQs service for accounts


### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | FAQs list (Array)| FAQs list |


### Example

#### Request

```
GET /api/v1.0/account/faqs
Content-Type: application/json
Accept: application/json
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": [
		{
			"_id": "...",
			"id": "...",
			"question": "...",
			"fbAnswer": "...",
			"waAnswer": "..."
		},
		{
			"_id": "...",
			"id": "...",
			"question": "...",
			"fbAnswer": "...",
			"waAnswer": "..."
		},
		...
	]
}
```

## Models

## FAQ model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| id | Integer | Chatbot identifier |
| question | String | FAQ question |
| fbAnswer | String | FAQ answer for Facebook |
| waAnswer | String | FAQ answer for WhatsApp |

# Organizations service

__Path:__ /api/v1.0/organizations  
__Method:__ GET   
__Description:__ Organizations service for accounts


### Response body
| media type | data type | description |
|-------|--------|---------|
| application/json | Organizations list (Array)| Organizations list |


### Example

#### Request

```
GET /api/v1.0/organizations
Content-Type: application/json
Accept: application/json
```

#### Response

```
HTTP/1.1 200 OK
Content-Type: application/json

{
	"status": "SUCCESS",
	"data": [
		{
			"_id": "...",
			"name": "...",
			"description": "...",
			"apiDomain": "..."
		},
		{
			"_id": "...",
			"name": "...",
			"description": "...",
			"apiDomain": "..."
		},
		...
	]
}
```

## Models

## Organization model
| name | type | description |
|-------|--------|---------|
| _id | String | Unique identifier |
| name | Integer | Organization name |
| description | String | Organization description |
| apiDomain | String | Organization API sub/domain |

# Online payment url format

__Format:__ $PROTOCOL://$HOST_NAME/pagar/$ACCOUNT?origen=$ORIGIN&emisor=$TRANSMITTER_ID&receptor=$RECEIVER_ID  
__Description:__ Online payment url format for accounts

### Example

```
https://sanluis.clariti.tech/pagar/00000195?origen=FB_MESSENGER&emisor=1901954919874040&receptor=363889730854449
```

## Parameters description

| name | type | description |
|-------|--------|---------|
| PROTOCOL | String | Service protocol (default: "https") |
| HOST_NAME | String | Organization's online payment hostname |
| ACCOUNT | String | User account number |
| ORIGIN | String | Origin service (available options: ["FB_MESSENGER", "WHATSAPP"]) |
| TRANSMITTER_ID | Number | Transmitter identifier |
| RECEIVER_ID | Number | Receiver identifier |

# Notifications

In order to create a new notification, in the microservices ecosystem there are events that can be triggered for an organization.

## Chat

Event: `chat-{organizationId}`

Replace organizationId for the desired organization `_id` field.

Example: `chat-5c476a722d4725048f696e8a`

## Parameters description

| name | type | description |
|-------|--------|---------|
| type | String | Notification type (guschat provided documentation)  |
| account | String | account to send the chat notification |
| channel | String | Channel to send the chat notification (guschat provided documentation) |
| sendAt | Instant | Optional. Defines the date & time to send the chat notification |



Example:
```java
JsonObject data = new JsonObject();

data.put("account", "1240");
data.put("type", "VRDS");
data.put("channel", "FB");

// optional parameter, when to send this notification, if its for later then its only saved in database
// if its supposed to send it now, its not saved in the database, until we get OK response from the provider.
data.put("sendAt", DateTime.now().toInstant());

// in case we want to send it later, in 15 min
// data.put("sendAt", DateTime.now().plusMinutes(15).toInstant());

// assuming we are in a verticle, we use the eventBus()
this.vertx.eventBus().send("chat-5c476a722d4725048f696e8a", data, messageAsyncResult -> {
    if (messageAsyncResult.succeeded()){
        //todo: Success handle
    }else{
        //todo: Error handle (notification is not saved if it was to send immediately)
    }
});

```


## Sms


Event: `sms-{organizationId}`

Replace organizationId for the desired organization `_id` field.

Example: `sms-5c476a722d4725048f696e8a`

## Parameters description

| name | type | description |
|-------|--------|---------|
| type | String | Notification type (anything you desire to identify)  |
| account | String | account to send the sms|
| message | String | Message to send as sms |
| cellphone | String | Cellphone to send the SMS |
| sendAt | Instant | Optional. Defines the date & time to send the SMS |



Example:
```java
JsonObject data = new JsonObject();

data.put("account", "1240");
data.put("type", "new_invoice");
data.put("message", "Dear Customer, you have a new invoice, available at https://claritibot.mx/path/to/invoice.pdf");
data.put("cellphone","6688112233");

// optional parameter, when to send this notification, if its for later then its only saved in database
// if its supposed to send it now, its not saved in the database, until we get OK response from the provider.
data.put("sendAt", DateTime.now().toInstant());


// in case we want to send it later, in 15 min
// data.put("sendAt", DateTime.now().plusMinutes(15).toInstant());


// assuming we are in a verticle, we use the eventBus()
this.vertx.eventBus().send("sms-5c476a722d4725048f696e8a", data, messageAsyncResult -> {
    if (messageAsyncResult.succeeded()){
        //todo: Success handle
    }else{
        //todo: Error handle (notification is not saved if it was to send immediately)
    }
});

```