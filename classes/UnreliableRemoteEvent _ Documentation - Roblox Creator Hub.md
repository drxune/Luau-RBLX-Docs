# UnreliableRemoteEvent | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UnreliableRemoteEvent
Scraped: 2026-01-11T02:32:30.525861Z

## Inherits
- BaseRemoteEvent
- UnreliableRemoteEvent
- Player
- Instance
- Object
- RemoteEvent
- ReplicatedStorage
- Workspace
- Tool
- FireServer()
- RemoteEvents
- UnreliableRemoteEvents
- OnClientEvent
- FireClient()
- Script
- OnServerEvent
- LocalScript
- FireAllClients()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BaseRemoteEvent](/docs/reference/engine/classes/BaseRemoteEvent)
6. /
7. [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent)

English

Feedback

Engine Class

![UnreliableRemoteEvent](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UnreliableRemoteEvent-Dark.webp)UnreliableRemoteEvent

An object which facilitates asynchronous, unordered and unreliable, one-way
communication across the client-server boundary. Scripts firing a
[UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) do not yield.

---

Summary

Methods

|  |
| --- |
| [FireAllClients](#FireAllClients)(arguments: [Tuple](/docs/luau/tuples)):() |
| [FireClient](#FireClient)(player: [Player](/docs/reference/engine/classes/Player),arguments: [Tuple](/docs/luau/tuples)):() |
| [FireServer](#FireServer)(arguments: [Tuple](/docs/luau/tuples)):() |

Events

|  |
| --- |
| [OnClientEvent](#OnClientEvent)(arguments: [Tuple](/docs/luau/tuples)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [OnServerEvent](#OnServerEvent)(player: [Player](/docs/reference/engine/classes/Player),arguments: [Tuple](/docs/luau/tuples)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The UnreliableRemoteEvent object is a variant of the [RemoteEvent](/docs/reference/engine/classes/RemoteEvent)
object. It facilitates asynchronous, unordered and unreliable, one-way
communication across the [client-server](/docs/projects/client-server)
boundary without yielding for a response. This communication can be directed
from one client to the server, from the server to a specific client, or from
the server to all clients.

In order for both the server and clients to access a
[UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) instance, it must be in a place where both sides
can see it, such as [ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage), although in some cases it's
appropriate to store it in [Workspace](/docs/reference/engine/classes/Workspace) or inside a [Tool](/docs/reference/engine/classes/Tool).

[UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) is best used for ephemeral events, including
effects that are only relevant for a short time, or for replicating
continuously changing data. These events are not resent if they are lost and
they do not wait for previously fired events to arrive before being processed,
potentially resulting in reduced latency and network traffic. When you need
ordering and reliability, use a [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instead.

If no connected listener exists to handle an event, you might see a
Remote event invocation discarded error in the log to indicate that the
event was discarded and that you need to implement either OnClientEvent or
OnServerEvent.

#### Throttling

Remote events are subject to rate limits when sent from the client to the
server with the [FireServer()](/docs/reference/engine/classes/RemoteEvent#FireServer) method.
[RemoteEvents](/docs/reference/engine/classes/RemoteEvent) and
[UnreliableRemoteEvents](/docs/reference/engine/classes/UnreliableRemoteEvent) both have a limit of
approximately 500 requests per second, per client. This limit is shared
among all remote events of the same type. To avoid throttling and latency
issues, limit recurring remote events whenever possible.

#### Parameter limitations

Any type of Roblox object ([Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), etc.) can be
passed as a parameter when an [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) is fired, as well
as Luau types such as numbers, strings, and booleans, although you should
carefully explore the
[limitations](/docs/scripting/events/remote#argument-limitations).

Events with payloads larger than 1000 bytes are dropped. When this happens in
Studio, a log message in the [Output](/docs/studio/output) window
indicates the number of bytes the event went over.

Like all events, the [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) methods encode and compress
certain object types, such as buffers, which shrinks the payload size and can
make it difficult to verify whether you are under the limit prior to firing
the event. If you frequently reach this limit, consider whether a standard
[RemoteEvent](/docs/reference/engine/classes/RemoteEvent) is the better fit for your use case.

---

API Reference

Methods

FireAllClients

Fires the [OnClientEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnClientEvent) event
for all connected clients. Has a 1000 byte limit to the payload of the
event. Events with larger payloads are dropped.

UnreliableRemoteEvent:FireAllClients(arguments:[Tuple](/docs/luau/tuples)):()

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to all [OnClientEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnClientEvent) events connected to the same [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent). |

Returns

()

Fires the [OnClientEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnClientEvent) event
for all connected clients. Unlike
[FireClient()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireClient), this event does
not take a target [Player](/docs/reference/engine/classes/Player) as the first argument, since it fires to
multiple clients. Since this method is used to communicate from the server
to clients, it only works when used in a [Script](/docs/reference/engine/classes/Script).

Provide feedback

---

FireClient

Fires the [OnClientEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnClientEvent) event
for a specific client. Has a 1000 byte limit to the payload of the event.
Events with larger payloads are dropped.

UnreliableRemoteEvent:FireClient(

player:[Player](/docs/reference/engine/classes/Player), arguments:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The client of the [Player](/docs/reference/engine/classes/Player) to fire the event to. |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to [OnClientEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnClientEvent) events connected to the same [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent). |

Returns

()

Fires the [OnClientEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnClientEvent) event
for the specific client in the required [Player](/docs/reference/engine/classes/Player) argument. Since
this method is used to communicate from the server to a client, it only
works when used in a [Script](/docs/reference/engine/classes/Script).

Provide feedback

---

FireServer

Fires the [OnServerEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnServerEvent) event
on the server from one connected client. Has a 1000 byte limit to the
payload of the event. Events with larger payloads are dropped.

UnreliableRemoteEvent:FireServer(arguments:[Tuple](/docs/luau/tuples)):()

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to [OnServerEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnServerEvent) events connected to the same [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent). |

Returns

()

Fires the [OnServerEvent](/docs/reference/engine/classes/UnreliableRemoteEvent#OnServerEvent) event
on the server from one connected client. Connected events receive the
[Player](/docs/reference/engine/classes/Player) argument of the firing client. Since this method is used to
communicate from a client to the server, it only works when used in a
client script.

Provide feedback

---

Events

OnClientEvent

Fires from a [LocalScript](/docs/reference/engine/classes/LocalScript) when either
[FireClient()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireClient) or
[FireAllClients()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireAllClients) is called
on the same [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) instance from a [Script](/docs/reference/engine/classes/Script),
although this firing is not guaranteed even if one of the above methods
are called. This can occur due to packet loss or to maintain optimal
engine performance.

UnreliableRemoteEvent.OnClientEvent(arguments:[Tuple](/docs/luau/tuples)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [FireClient()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireClient) or [FireAllClients()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireAllClients). |

Fires from a [LocalScript](/docs/reference/engine/classes/LocalScript) when either
[FireClient()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireClient) or
[FireAllClients()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireAllClients) is called
on the same [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) instance from a [Script](/docs/reference/engine/classes/Script),
although this firing is not guaranteed even if one of the above methods
are called. This can occur due to packet loss or to maintain optimal
engine performance.

Also note that it is not guaranteed that the order of events will match
the order of [FireClient()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireClient) or
[FireAllClients()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireAllClients) calls.

Provide feedback

---

OnServerEvent

Fires from a [Script](/docs/reference/engine/classes/Script) when
[FireServer()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireServer) is called on the
same [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) instance from a [LocalScript](/docs/reference/engine/classes/LocalScript),
although this firing is not guaranteed even if the above methods is
called. This can occur due to packet loss or to maintain optimal engine
performance.

UnreliableRemoteEvent.OnServerEvent(

player:[Player](/docs/reference/engine/classes/Player), arguments:[Tuple](/docs/luau/tuples)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) associated with the client that the [FireServer()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireServer) call originates from. |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [FireServer()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireServer). |

Fires from a [Script](/docs/reference/engine/classes/Script) when
[FireServer()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireServer) is called on the
same [UnreliableRemoteEvent](/docs/reference/engine/classes/UnreliableRemoteEvent) instance from a [LocalScript](/docs/reference/engine/classes/LocalScript),
although this firing is not guaranteed even if the above methods is
called. This can occur due to packet loss or to maintain optimal engine
performance.

Also note that it is not guaranteed that the order of events will match
the order of [FireServer()](/docs/reference/engine/classes/UnreliableRemoteEvent#FireServer)
calls.

Provide feedback

---