# BindableEvent | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BindableEvent
Scraped: 2026-01-11T02:34:05.867981Z

## Inherits
- Object
- Instance
- BindableEvent
- BindableEvent:Fire()
- BindableEvents
- BindableFunction
- RemoteEvent
- Event
- Fire()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [BindableEvent](/docs/reference/engine/classes/BindableEvent)

English

Feedback

Engine Class

![BindableEvent](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BindableEvent-Dark.webp)BindableEvent

An object which enables custom events through asynchronous one-way
communication between scripts on the same side of the client-server boundary.
Scripts firing a [BindableEvent](/docs/reference/engine/classes/BindableEvent) do not yield.

---

Summary

Methods

|  |
| --- |
| [Fire](#Fire)(arguments: [Tuple](/docs/luau/tuples)):() |

Events

|  |
| --- |
| [Event](#Event)(arguments: [Tuple](/docs/luau/tuples)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BindableEvent object enables custom events through asynchronous
one-way communication between scripts on the same side of the
[client-server](/docs/projects/client-server) boundary. When you fire a
[BindableEvent](/docs/reference/engine/classes/BindableEvent) through the [BindableEvent:Fire()](/docs/reference/engine/classes/BindableEvent#Fire) method, the
firing script does not yield and the target function receives the passed
arguments with certain [limitations](#argument-limitations).
[BindableEvents](/docs/reference/engine/classes/BindableEvent) create threads of each connected
function, so even if one firing errors, others continue.

As an alternative for two-way communication between two scripts on the same
side of the client-server boundary, consider [BindableFunction](/docs/reference/engine/classes/BindableFunction).

As stated, [BindableEvents](/docs/reference/engine/classes/BindableEvent) do not allow for communication
between the server and clients. If you are looking for this functionality, use
a [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) as outlined in
[Remote Events and Callbacks](/docs/scripting/events/remote).

See [Bindable events and callbacks](/docs/scripting/events/bindable) for
code samples and further details on [BindableEvent](/docs/reference/engine/classes/BindableEvent).

#### Parameter Limitations

Any type of Roblox object such as an [Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), or
others can be passed as a parameter when a [BindableEvent](/docs/reference/engine/classes/BindableEvent) is fired, as
well as Luau types such as numbers, strings, and booleans, although you should
carefully explore the
[limitations](/docs/scripting/events/bindable#argument-limitations).

---

API Reference

Methods

Fire

Write Parallel

Fires the [BindableEvent](/docs/reference/engine/classes/BindableEvent) which in turn fires the
[Event](/docs/reference/engine/classes/BindableEvent#Event) event.

BindableEvent:Fire(arguments:[Tuple](/docs/luau/tuples)):()

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  Values to pass to [Event](/docs/reference/engine/classes/BindableEvent#Event) events connected to the same [BindableEvent](/docs/reference/engine/classes/BindableEvent). |

Returns

()

Fires the [BindableEvent](/docs/reference/engine/classes/BindableEvent) which in turn fires the
[Event](/docs/reference/engine/classes/BindableEvent#Event) event. This method does not yield, even
if no script has connected to the event, and even if a connected function
yields.

Any type of Roblox object such as an [Enum](/docs/reference/engine/datatypes/Enum), [Instance](/docs/reference/engine/classes/Instance), or
others can be passed as a parameter to
[Fire()](/docs/reference/engine/classes/BindableEvent#Fire), as well as Luau types such as
numbers, strings, and booleans, although you should carefully explore the
[limitations](/docs/scripting/events/bindable#argument-limitations).

See [Bindable events and callbacks](/docs/scripting/events/bindable)
for code samples and further details on
[Fire()](/docs/reference/engine/classes/BindableEvent#Fire).

Provide feedback

---

Events

Event

Fires when any script calls the [Fire()](/docs/reference/engine/classes/BindableEvent#Fire) method
on the same [BindableEvent](/docs/reference/engine/classes/BindableEvent) instance.

BindableEvent.Event(arguments:[Tuple](/docs/luau/tuples)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| arguments:[Tuple](/docs/luau/tuples)  The parameters sent through [Fire()](/docs/reference/engine/classes/BindableEvent#Fire). |

Fires when any script calls the [Fire()](/docs/reference/engine/classes/BindableEvent#Fire) method
on the same [BindableEvent](/docs/reference/engine/classes/BindableEvent) instance, using the same arguments as
parameters.

See [Bindable events and callbacks](/docs/scripting/events/bindable)
for code samples and further details on [Event](/docs/reference/engine/classes/BindableEvent#Event).

Provide feedback

---