# Actor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Actor
Scraped: 2026-01-11T02:33:56.982612Z

## Inherits
- Model
- Actor
- PVInstance
- Instance
- Object
- SendMessage()
- BindToMessage()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Model](/docs/reference/engine/classes/Model)
6. /
7. [Actor](/docs/reference/engine/classes/Actor)

English

Feedback

Engine Class

![Actor](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Actor-Dark.webp)Actor

An [Actor](/docs/reference/engine/classes/Actor) is a container for code that can be safely split into its own
thread.

---

Summary

Methods

|  |
| --- |
| [BindToMessage](#BindToMessage)(topic: [string](/docs/luau/strings),function: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [BindToMessageParallel](#BindToMessageParallel)(topic: [string](/docs/luau/strings),function: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [SendMessage](#SendMessage)(topic: [string](/docs/luau/strings),message: [Tuple](/docs/luau/tuples)):() |

Inherited Members

26 inherited from [Model](/docs/reference/engine/classes/Model)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An [Actor](/docs/reference/engine/classes/Actor) is a container for code that can be safely split into its own
thread using [task.desynchronize()](/docs/reference/engine/libraries/task#desynchronize). It should also contain the
instances used by its scripts.

To learn more about using multiple Actors to optimize script performance, see
[Parallel Luau](/docs/scripting/multithreading).

---

API Reference

Methods

BindToMessage

Write Parallel

Binds a Luau callback to a message with the specified topic.

Actor:BindToMessage(

topic:[string](/docs/luau/strings), function:[function](/docs/luau/functions)

):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| topic:[string](/docs/luau/strings)  The topic used to identify the type of message. |
| function:[function](/docs/luau/functions) |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

This connection object may be used to disconnect the Luau callback
from receiving messages.

This method is used to bind a Luau callback to a message with the
specified topic. When a message is sent (using
[SendMessage()](/docs/reference/engine/classes/Actor#SendMessage)) to the topic specified the
provided callback will be called in a *serial* execution context.

Multiple Luau callbacks may be bound to a single actor and even to a
single message topic.

Note: Only the scripts which are descendants of an Actor may bind to its
messages.

```
local actor = script:GetActor()



-- Print out a message when a greeting message is sent to the Actor



-- this script is a descendant of.



local connection = actor:BindToMessage("Greeting", function(message)



print("Received Greeting Message:", message)



end)
```

Provide feedback

---

BindToMessageParallel

Write Parallel

Binds a Luau callback to a message with the specified topic.

Actor:BindToMessageParallel(

topic:[string](/docs/luau/strings), function:[function](/docs/luau/functions)

):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| topic:[string](/docs/luau/strings)  The topic used to identify the type of message. |
| function:[function](/docs/luau/functions) |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

This connection object may be used to disconnect the Luau callback
from receiving messages.

This method is used to bind a Luau callback to a message with the
specified topic. When a message is sent (using
[SendMessage()](/docs/reference/engine/classes/Actor#SendMessage)) to the topic specified the
provided callback will be called in a *parallel* execution context.

Multiple Luau callbacks may be bound to a single actor and even to a
single message topic.

Note: Only the scripts which are descendants of an Actor may bind to its
messages.

```
local actor = script:GetActor()



-- Print out a message when a greeting message is sent to the Actor



-- this script is a descendant of.



local connection = actor:BindToMessageParallel("Greeting", function(message)



print("Received Greeting Message:", message)



end)
```

Provide feedback

---

SendMessage

Write Parallel

Sends a message to an Actor.

Actor:SendMessage(

topic:[string](/docs/luau/strings), message:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| topic:[string](/docs/luau/strings)  The topic used to identify the message being sent. |
| message:[Tuple](/docs/luau/tuples)  The contents of the message to send to the Actor. |

Returns

()

Sends a message to an Actor. Messages are sent asynchronously, so the
sender will not block or yield when calling the
[SendMessage()](/docs/reference/engine/classes/Actor#SendMessage) method.

Since a single Actor may receive different kinds of messages, a topic
parameter is used to distinguish between various kinds of messages.

See [BindToMessage()](/docs/reference/engine/classes/Actor#BindToMessage) for details on receiving
a message sent using [SendMessage()](/docs/reference/engine/classes/Actor#SendMessage).

```
-- Assume `actor` is a local variable referring to an Actor instance



actor:SendMessage("Greeting", "Hello World")
```

Provide feedback

---