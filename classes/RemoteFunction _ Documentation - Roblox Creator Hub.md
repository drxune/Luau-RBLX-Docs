# RemoteFunction | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RemoteFunction
Scraped: 2026-01-11T02:37:57.688977Z

## Inherits
- Instance
- RemoteFunction
- Player
- Object
- RemoteFunction:InvokeClient()
- RemoteFunction:InvokeServer()
- ReplicatedStorage
- Workspace
- Tool
- RemoteEvent
- BaseParts
- Models
- OnClientInvoke
- Script
- InvokeClient()
- RemoteEvent:FireClient()
- OnServerInvoke
- LocalScript
- RemoteEvent:FireServer()
- InvokeServer()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [RemoteFunction](/docs/reference/engine/classes/RemoteFunction)

English

Feedback

Engine Class

![RemoteFunction](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/RemoteFunction-Dark.webp)RemoteFunction

An object which facilitates synchronous, two-way communication across the
client-server boundary. Scripts invoking a [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) yield until
they receive a response from the recipient.

---

Summary

Methods

|  |
| --- |
| [InvokeClient](#InvokeClient)(player: [Player](/docs/reference/engine/classes/Player),arguments: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |
| [InvokeServer](#InvokeServer)(arguments: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |

Callbacks

|  |
| --- |
| [OnClientInvoke](#OnClientInvoke)(arguments: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |
| [OnServerInvoke](#OnServerInvoke)(player: [Player](/docs/reference/engine/classes/Player),arguments: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The RemoteFunction object facilitates synchronous, two-way communication
across the [client-server](/docs/projects/client-server) boundary. You
can use it to define a custom callback function and invoke it manually by
calling [RemoteFunction:InvokeClient()](/docs/reference/engine/classes/RemoteFunction#InvokeClient) or
[RemoteFunction:InvokeServer()](/docs/reference/engine/classes/RemoteFunction#InvokeServer). The code invoking the function
yields until it receives a response from the recipient.

In order for both the server and clients to access a [RemoteFunction](/docs/reference/engine/classes/RemoteFunction)
instance, it must be in a place where both sides can see it, such as
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage), although in some cases it's appropriate to store it
in [Workspace](/docs/reference/engine/classes/Workspace) or inside a [Tool](/docs/reference/engine/classes/Tool).

If the result is not needed, it is recommended that you use a
[RemoteEvent](/docs/reference/engine/classes/RemoteEvent) instead, since its call is asynchronous and doesn't need
to wait for a response to continue execution. See
[Remote Events and Callbacks](/docs/scripting/events/remote) for code
samples and further details on [RemoteFunction](/docs/reference/engine/classes/RemoteFunction).

#### Streaming Precautions

Note that if an invoked [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) creates an instance on the
server, there is no guarantee that it exists on the client when the function
returns. This is particularly important in places where instance
[streaming](/docs/workspace/streaming) is enabled and when the created
instances are [BaseParts](/docs/reference/engine/classes/BasePart) or [Models](/docs/reference/engine/classes/Model), since parts
that are far away from the player's character may not be streamed to the
client, and models that are [Atomic](/docs/reference/engine/enums/ModelStreamingMode) depend on whether
their parts are streamed. Even if a model is
[Persistent](/docs/reference/engine/enums/ModelStreamingMode), there may be some delay between the
creation of the model and when it is replicated to the client.

#### Parameter Limitations

Any type of Roblox object such as an [Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), or
others can be passed as a parameter when a [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) is invoked,
as well as Luau types such as numbers, strings, and booleans, although you
should carefully explore the
[limitations](/docs/scripting/events/remote#argument-limitations).

---

API Reference

Methods

InvokeClient

Yields

Invokes the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) which in turn calls the
[OnClientInvoke](/docs/reference/engine/classes/RemoteFunction#OnClientInvoke) callback.

RemoteFunction:InvokeClient(

player:[Player](/docs/reference/engine/classes/Player), arguments:[Tuple](/docs/luau/tuples)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) associated with the client to invoke. |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to the [OnClientInvoke](/docs/reference/engine/classes/RemoteFunction#OnClientInvoke) callback. |

Returns

[Tuple](/docs/luau/tuples)

Values returned from the
[OnClientInvoke](/docs/reference/engine/classes/RemoteFunction#OnClientInvoke) callback.

Invokes the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) which in turn calls the
[OnClientInvoke](/docs/reference/engine/classes/RemoteFunction#OnClientInvoke) callback. Since this
method is used to communicate from the server to a client, it will only
work when used in a [Script](/docs/reference/engine/classes/Script).

Any type of Roblox object such as an [Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), or
others can be passed as a parameter to
[InvokeClient()](/docs/reference/engine/classes/RemoteFunction#InvokeClient), as well as Luau
types such as numbers, strings, and booleans, although you should
carefully explore the
[limitations](/docs/scripting/events/remote#argument-limitations).

See [Remote Events and Callbacks](/docs/scripting/events/remote) for
code samples and further details on [RemoteFunction](/docs/reference/engine/classes/RemoteFunction).

#### Warning

In practice, the server does not often invoke the client, as clients
typically do not have information that the server doesn't have, and
actions that only a client can take, such as displaying a GUI, typically
do not require a callback. As such, [RemoteEvent:FireClient()](/docs/reference/engine/classes/RemoteEvent#FireClient) is
recommended as an asynchronous method that doesn't need to wait for a
response to continue execution.

If you legitimately need to invoke a client from the server, note the
following risks:

* If the client throws an error, the server throws the error too.
* If the client disconnects while it's being invoked,
  [InvokeClient()](/docs/reference/engine/classes/RemoteFunction#InvokeClient) throws an error.
* If the client doesn't return a value, the server yields forever.

Provide feedback

---

InvokeServer

Yields

Invokes the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) which in turn calls the
[OnServerInvoke](/docs/reference/engine/classes/RemoteFunction#OnServerInvoke) callback.

RemoteFunction:InvokeServer(arguments:[Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to the [OnServerInvoke](/docs/reference/engine/classes/RemoteFunction#OnServerInvoke) callback. |

Returns

[Tuple](/docs/luau/tuples)

Values returned from the
[OnServerInvoke](/docs/reference/engine/classes/RemoteFunction#OnServerInvoke) callback.

Invokes the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) which in turn calls the
[OnServerInvoke](/docs/reference/engine/classes/RemoteFunction#OnServerInvoke) callback. Since this
method is used to communicate from a client to the server, it will only
work when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

If a returned result is not needed, it's recommended to use
[RemoteEvent:FireServer()](/docs/reference/engine/classes/RemoteEvent#FireServer) instead, as its call is asynchronous and
doesn't need to wait for a response to continue execution.

Any type of Roblox object such as an [Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), or
others can be passed as a parameter to
[InvokeServer()](/docs/reference/engine/classes/RemoteFunction#InvokeServer), as well as Luau
types such as numbers, strings, and booleans, although you should
carefully explore the
[limitations](/docs/scripting/events/remote#argument-limitations).

See [Remote Events and Callbacks](/docs/scripting/events/remote) for
code samples and further details on [RemoteFunction](/docs/reference/engine/classes/RemoteFunction).

Provide feedback

---

Callbacks

OnClientInvoke

Callback for when the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) is invoked with
[InvokeClient()](/docs/reference/engine/classes/RemoteFunction#InvokeClient).

RemoteFunction.OnClientInvoke(arguments:[Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [InvokeClient()](/docs/reference/engine/classes/RemoteFunction#InvokeClient). |

Returns

[Tuple](/docs/luau/tuples)

Values returned by the callback function.

This callback is called when the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) is invoked with
[InvokeClient()](/docs/reference/engine/classes/RemoteFunction#InvokeClient). When the bound
function returns, the returned values are sent back to the calling server.

See [Remote Events and Callbacks](/docs/scripting/events/remote) for
code samples and further details on
[OnClientInvoke](/docs/reference/engine/classes/RemoteFunction#OnClientInvoke).

Provide feedback

---

OnServerInvoke

Callback for when the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) is invoked with
[InvokeServer()](/docs/reference/engine/classes/RemoteFunction#InvokeServer).

RemoteFunction.OnServerInvoke(

player:[Player](/docs/reference/engine/classes/Player), arguments:[Tuple](/docs/luau/tuples)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) associated with the client that the [InvokeServer()](/docs/reference/engine/classes/RemoteFunction#InvokeServer) call originates from. |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [InvokeServer()](/docs/reference/engine/classes/RemoteFunction#InvokeServer). |

Returns

[Tuple](/docs/luau/tuples)

Values returned by the callback function.

This callback is called when the [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) is invoked with
[InvokeServer()](/docs/reference/engine/classes/RemoteFunction#InvokeServer). When the bound
function returns, the returned values are sent back to the calling client.

See [Remote Events and Callbacks](/docs/scripting/events/remote) for
code samples and further details on
[OnServerInvoke](/docs/reference/engine/classes/RemoteFunction#OnServerInvoke).

Provide feedback

---