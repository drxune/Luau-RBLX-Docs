# RemoteEvent | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RemoteEvent
Scraped: 2026-01-11T02:34:18.745867Z

## Inherits
- BaseRemoteEvent
- RemoteEvent
- Player
- Instance
- Object
- ReplicatedStorage
- Workspace
- Tool
- UnreliableRemoteEvents
- RemoteEvents
- RemoteFunction
- FireServer()
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
7. [RemoteEvent](/docs/reference/engine/classes/RemoteEvent)

English

Feedback

Engine Class

![RemoteEvent](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/RemoteEvent-Dark.webp)RemoteEvent

An object which facilitates asynchronous, one-way communication across the
client-server boundary. Scripts firing a [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) do not yield.

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

The RemoteEvent object facilitates asynchronous, one-way communication
across the [client-server](/docs/projects/client-server) boundary
without yielding for a response. This communication can be directed from one
client to the server, from the server to a specific client, or from the server
to all clients.

In order for both the server and clients to access a [RemoteEvent](/docs/reference/engine/classes/RemoteEvent)
instance, it must be in a place where both sides can see it, such as
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage), although in some cases it's appropriate to store it
in [Workspace](/docs/reference/engine/classes/Workspace) or inside a [Tool](/docs/reference/engine/classes/Tool).

If no connected listener exists to handle an event, you might see a
Remote event invocation discarded error in the log to indicate that the
event was discarded and that you need to implement either OnClientEvent or
OnServerEvent. Unlike [UnreliableRemoteEvents](/docs/reference/engine/classes/UnreliableRemoteEvent),
[RemoteEvents](/docs/reference/engine/classes/RemoteEvent) buffer a large number of events before
throwing this error.

If you need the result of the call, you should use a [RemoteFunction](/docs/reference/engine/classes/RemoteFunction)
instead. Otherwise a remote event is recommended since it will minimize
network traffic/latency and won't yield the script to wait for a response.

See [Remote events and callbacks](/docs/scripting/events/remote) for
code samples and further details.

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
passed as a parameter when a [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) is fired, as well as Luau
types such as numbers, strings, and booleans, although you should carefully
explore the
[limitations](/docs/scripting/events/remote#argument-limitations).

---

API Reference

Methods

FireAllClients

Fires the [OnClientEvent](/docs/reference/engine/classes/RemoteEvent#OnClientEvent) event for each
connected client.

RemoteEvent:FireAllClients(arguments:[Tuple](/docs/luau/tuples)):()

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to all [OnClientEvent](/docs/reference/engine/classes/RemoteEvent#OnClientEvent) events connected to the same [RemoteEvent](/docs/reference/engine/classes/RemoteEvent). |

Returns

()

Fires the [OnClientEvent](/docs/reference/engine/classes/RemoteEvent#OnClientEvent) event for each
connected client. Unlike [FireClient()](/docs/reference/engine/classes/RemoteEvent#FireClient),
this event does not take a target [Player](/docs/reference/engine/classes/Player) as the first argument,
since it fires to multiple clients. Since this method is used to
communicate from the server to clients, it only works when used in a
[Script](/docs/reference/engine/classes/Script).

Provide feedback

---

FireClient

Fires the [OnClientEvent](/docs/reference/engine/classes/RemoteEvent#OnClientEvent) event for a
specific client.

RemoteEvent:FireClient(

player:[Player](/docs/reference/engine/classes/Player), arguments:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The client of the [Player](/docs/reference/engine/classes/Player) to fire the event to. |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to [OnClientEvent](/docs/reference/engine/classes/RemoteEvent#OnClientEvent) events connected to the same [RemoteEvent](/docs/reference/engine/classes/RemoteEvent). |

Returns

()

Fires the [OnClientEvent](/docs/reference/engine/classes/RemoteEvent#OnClientEvent) event for the
specific client in the required [Player](/docs/reference/engine/classes/Player) argument. Since this method
is used to communicate from the server to a client, it only works when
used in a [Script](/docs/reference/engine/classes/Script).

Provide feedback

---

FireServer

Fires the [OnServerEvent](/docs/reference/engine/classes/RemoteEvent#OnServerEvent) event on the
server from one connected client.

RemoteEvent:FireServer(arguments:[Tuple](/docs/luau/tuples)):()

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to [OnServerEvent](/docs/reference/engine/classes/RemoteEvent#OnServerEvent) events connected to the same [RemoteEvent](/docs/reference/engine/classes/RemoteEvent). |

Returns

()

Fires the [OnServerEvent](/docs/reference/engine/classes/RemoteEvent#OnServerEvent) event on the
server from one client. Connected events receive the [Player](/docs/reference/engine/classes/Player)
argument of the firing client. Since this method is used to communicate
from a client to the server, it only works when used in a client script.

Provide feedback

---

Events

OnClientEvent

Fires from a [LocalScript](/docs/reference/engine/classes/LocalScript) when either
[FireClient()](/docs/reference/engine/classes/RemoteEvent#FireClient) or
[FireAllClients()](/docs/reference/engine/classes/RemoteEvent#FireAllClients) is called on the
same [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instance from a [Script](/docs/reference/engine/classes/Script).

RemoteEvent.OnClientEvent(arguments:[Tuple](/docs/luau/tuples)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [FireClient()](/docs/reference/engine/classes/RemoteEvent#FireClient) or [FireAllClients()](/docs/reference/engine/classes/RemoteEvent#FireAllClients). |

Fires from a [LocalScript](/docs/reference/engine/classes/LocalScript) when either
[FireClient()](/docs/reference/engine/classes/RemoteEvent#FireClient) or
[FireAllClients()](/docs/reference/engine/classes/RemoteEvent#FireAllClients) is called on the
same [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instance from a [Script](/docs/reference/engine/classes/Script).

See [Remote Events and Callbacks](/docs/scripting/events/remote) for
code samples and further details on
[OnClientEvent](/docs/reference/engine/classes/RemoteEvent#OnClientEvent).

Provide feedback

---

OnServerEvent

Fires from a [Script](/docs/reference/engine/classes/Script) when
[FireServer()](/docs/reference/engine/classes/RemoteEvent#FireServer) is called on the same
[RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instance from a [LocalScript](/docs/reference/engine/classes/LocalScript).

RemoteEvent.OnServerEvent(

player:[Player](/docs/reference/engine/classes/Player), arguments:[Tuple](/docs/luau/tuples)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) associated with the client that the [FireServer()](/docs/reference/engine/classes/RemoteEvent#FireServer) call originates from. |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [FireServer()](/docs/reference/engine/classes/RemoteEvent#FireServer). |

Fires from a [Script](/docs/reference/engine/classes/Script) when
[FireServer()](/docs/reference/engine/classes/RemoteEvent#FireServer) is called on the same
[RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instance from a [LocalScript](/docs/reference/engine/classes/LocalScript).

See [Remote Events and Callbacks](/docs/scripting/events/remote) for
code samples and further details on
[OnServerEvent](/docs/reference/engine/classes/RemoteEvent#OnServerEvent).

Provide feedback

---