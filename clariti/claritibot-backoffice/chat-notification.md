---
title: Claritibot-Backoffice
description: Claritibot-Backoffice API Documentation
layout: default
info:
    title: Claritibot-Backoffice
    description: Claritibot-Backoffice API Documentation
    favicon: /img/claritibot.png
    logo: /img/claritibot.png
---

# Overall

How to send chat notifications inside claritibot-backoffice ecosystem

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
