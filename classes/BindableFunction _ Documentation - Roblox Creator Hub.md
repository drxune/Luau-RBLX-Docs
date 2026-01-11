# BindableFunction | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BindableFunction
Scraped: 2026-01-11T02:36:16.089405Z

## Inherits
- Instance
- BindableFunction
- Object
- BindableFunction:Invoke()
- Invoke()
- BindableEvent
- BindableFunctions
- RemoteFunction
- OnInvoke
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [BindableFunction](/docs/reference/engine/classes/BindableFunction)

English

Feedback

Engine Class

![BindableFunction](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BindableFunction-Dark.webp)BindableFunction

An object which allows for synchronous two-way communication between scripts
on the same side of the client-server boundary. Scripts invoking a
[BindableFunction](/docs/reference/engine/classes/BindableFunction) yield until the corresponding callback is found.

---

Summary

Methods

|  |
| --- |
| [Invoke](#Invoke)(arguments: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |

Callbacks

|  |
| --- |
| [OnInvoke](#OnInvoke)(arguments: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BindableFunction object allows for synchronous two-way communication
between scripts on the same side of the
[client-server](/docs/projects/client-server) boundary. You can use it
to define a custom callback function and invoke it manually by calling
[BindableFunction:Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke). The code invoking the function yields
until the corresponding callback is found, and the callback receives the
arguments that you passed to [Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke). If
the callback was never set, the script that invokes it will not resume
execution.

As an alternative for one-way communication between two scripts on the same
side of the client-server boundary, consider [BindableEvent](/docs/reference/engine/classes/BindableEvent) which does
not yield for a return.

As stated, [BindableFunctions](/docs/reference/engine/classes/BindableFunction) do not allow for
communication between the server and clients. If you are looking for this
functionality, use a [RemoteFunction](/docs/reference/engine/classes/RemoteFunction) as outlined in
[Remote events and callbacks](/docs/scripting/events/remote).

See [Bindable events and callbacks](/docs/scripting/events/bindable) for
code samples and further details on [BindableFunction](/docs/reference/engine/classes/BindableFunction).

#### Parameter Limitations

Any type of Roblox object such as an [Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), or
others can be passed as a parameter when a [BindableFunction](/docs/reference/engine/classes/BindableFunction) is
invoked, as well as Luau types such as numbers, strings, and booleans,
although you should carefully explore the
[limitations](/docs/scripting/events/bindable#argument-limitations).

---

API Reference

Methods

Invoke

Yields

Invokes the [BindableFunction](/docs/reference/engine/classes/BindableFunction) which in turn calls the
[OnInvoke](/docs/reference/engine/classes/BindableFunction#OnInvoke) callback, returning any values
returned by the callback.

BindableFunction:Invoke(arguments:[Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to the [OnInvoke](/docs/reference/engine/classes/BindableFunction#OnInvoke) callback. |

Returns

[Tuple](/docs/luau/tuples)

Values returned from the [OnInvoke](/docs/reference/engine/classes/BindableFunction#OnInvoke)
callback.

Invokes the [BindableFunction](/docs/reference/engine/classes/BindableFunction) which in turn calls the
[OnInvoke](/docs/reference/engine/classes/BindableFunction#OnInvoke) callback, returning any values
returned by the callback. Invocations yield until the corresponding
callback is found, and if the callback was never set, the script that
invokes it will not resume execution.

Any type of Roblox object such as an [Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), or
others can be passed as a parameter to
[Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke), as well as Luau types such as
numbers, strings, and booleans, although you should carefully explore the
[limitations](/docs/scripting/events/bindable#argument-limitations).

Only one function can be bound to
[Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke) at a time. If you assign
multiple functions, only the last one assigned will be used.

See [Bindable events and callbacks](/docs/scripting/events/bindable)
for code samples and further details on
[Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke).

Provide feedback

---

Callbacks

OnInvoke

Callback for when the [BindableFunction](/docs/reference/engine/classes/BindableFunction) is invoked with
[Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke).

BindableFunction.OnInvoke(arguments:[Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke). |

Returns

[Tuple](/docs/luau/tuples)

Values returned by the callback function.

This callback is called when the [BindableFunction](/docs/reference/engine/classes/BindableFunction) is invoked with
[Invoke()](/docs/reference/engine/classes/BindableFunction#Invoke). It can be set multiple times
but cannot be called directly. Invocations will yield until this callback
is found and, if it is never set, the script that invoked it will not
resume execution.

See [Bindable events and callbacks](/docs/scripting/events/bindable)
for code samples and further details on
[OnInvoke](/docs/reference/engine/classes/BindableFunction#OnInvoke).

Provide feedback

---