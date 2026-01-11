# MessagingService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MessagingService
Scraped: 2026-01-11T02:27:52.454221Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- MessagingService
- Object
- MessagingService:PublishAsync()
- MessagingService:SubscribeAsync()
- ancestry changes
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MessagingService](/docs/reference/engine/classes/MessagingService)

English

Feedback

Engine Class

![MessagingService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/MessagingService-Dark.webp)MessagingService

Allows servers of the same experience to communicate with each other.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [PublishAsync](#PublishAsync)(topic: [string](/docs/luau/strings),message: Variant):() |
| [SubscribeAsync](#SubscribeAsync)(topic: [string](/docs/luau/strings),callback: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

MessagingService allows servers of the same experience to communicate with
each other in real time (less than 1 second) using topics. Topics are
developer‑defined strings (1–80 characters) that servers use to send and
receive messages.

Delivery is best effort and not guaranteed. Make sure to architect your
experience so delivery failures are not critical.

[Cross-Server Messaging](/docs/cloud-services/cross-server-messaging)
explores how to communicate between servers in greater detail.

If you want to publish ad-hoc messages to live game servers, or publish across
experiences, you can use the
[Open Cloud APIs](/docs/cloud/guides/usage-messaging).

#### Limitations

Note that these limits are subject to change.

| Limit | Maximum |
| --- | --- |
| **Size of message** | 1kB |
| **Messages sent per game server** | 600 + 240 \* (number of players in this game server) per minute |
| **Messages received per topic** | (40 + 80 \* number of servers) per minute |
| **Messages received for entire game** | (400 + 200 \* number of servers) per minute |
| **Subscriptions allowed per game server** | 20 + 8 \* (number of players in this game server) |
| **Subscribe requests per game server** | 240 requests per minute |

---

API Reference

Methods

PublishAsync

Yields

Invokes the supplied callback whenever a message is pushed to the topic.

MessagingService:PublishAsync(

topic:[string](/docs/luau/strings), message:Variant

):()

Parameters

|  |
| --- |
| topic:[string](/docs/luau/strings)  Determines where the message is sent. |
| message:Variant  The data to include in the message. |

Returns

()

This function sends the provided message to all subscribers to the topic,
triggering their registered callbacks to be invoked.

Yields until the message is received by the backend.

Provide feedback

---

SubscribeAsync

Yields

Begins listening to the given topic.

MessagingService:SubscribeAsync(

topic:[string](/docs/luau/strings), callback:[function](/docs/luau/functions)

):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| topic:[string](/docs/luau/strings)  Determines where to listen for messages. |
| callback:[function](/docs/luau/functions)  Function to be invoked whenever a message is received. |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Connection that can be used to unsubscribe from the topic.

This function registers a callback to begin listening to the given topic.
The callback is invoked when a topic receives a message. It can be called
multiple times for the same topic.

#### Callback

The callback is invoked with a single argument, a table with the following
entries:

| Field | Summary |
| --- | --- |
| **Data** | Developer supplied payload |
| **Sent** | Unix time in seconds at which the message was sent |

It yields until the subscription is properly registered and returns a
connection object.

To unsubscribe, call [Disconnect()](/docs/reference/engine/datatypes/RBXScriptConnection) on the
returned object. Once called, the callback should never be invoked.
Killing the script containing the connections also causes the underlying
connect to be unsubscribed.

See also [MessagingService:PublishAsync()](/docs/reference/engine/classes/MessagingService#PublishAsync) which sends the provided
message to all subscribers to the topic, triggering their registered
callbacks to be invoked.

Code Samples

Subscribing to Cross Server Messages

This example demonstrates how to use [MessagingService:SubscribeAsync()](/docs/reference/engine/classes/MessagingService#SubscribeAsync)
to listen to a topic for cross-server chat within a game universe.

When a player joins, the example subscribes to the topic
*player-<player.UserId>*. When a message is sent with this topic, the
connected callback executes and prints *Received message for <player.Name">*.
It also disconnects the connection when the player's
[ancestry changes](/docs/reference/engine/classes/Player#AncestryChanged).

In order for this to work as expected it must be placed in a server Script.

```
local MessagingService = game:GetService("MessagingService")



local Players = game:GetService("Players")



local function onPlayerAdded(player)



--subscribe to the topic



local topic = "player-" .. player.UserId



local connection = MessagingService:SubscribeAsync(topic, function(message)



print("Received message for", player.Name, message.Data)



end)



player.AncestryChanged:Connect(function()



-- unsubscribe from the topic



connection:Disconnect()



end)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---