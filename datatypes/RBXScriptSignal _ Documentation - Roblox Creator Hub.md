# RBXScriptSignal | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/RBXScriptSignal
Scraped: 2026-01-11T02:42:09.860089Z
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

English

Feedback

Engine Data Type

RBXScriptSignal

An object that runs connected functions upon a specific occurrence.

---

Summary

Methods

|  |
| --- |
| [Connect](#Connect)(func: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [ConnectParallel](#ConnectParallel)(func: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [Once](#Once)(func: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [Wait](#Wait)():Variant |

The [RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) data type, more commonly known as an Event,
provides a way for user-defined functions, called listeners, to call when
something happens in the game. When an event happens, the
[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) fires and calls any listeners that are connected to
it. An [RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) may also pass arguments to each listener to
provide extra information about the event.

---

API Reference

Methods

Connect

Connects the given function to the event and returns an
[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) that represents it.

RBXScriptSignal:Connect(func:[function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| func:[function](/docs/luau/functions) |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Establishes a function to be called when the event fires. Returns an
[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) object associated with the connection.

Provide feedback

---

ConnectParallel

Connects the given function to the event and returns an
[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) that represents it.

RBXScriptSignal:ConnectParallel(func:[function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| func:[function](/docs/luau/functions) |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Establishes a function to be called when the event fires. Returns an
[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) object associated with the connection. When
the event fires, the signal callback is executed in a desynchronized
state. Using ConnectParallel is similar to, but more efficient than,
using Connect followed by a call to [task.desynchronize()](/docs/reference/engine/libraries/task#desynchronize) in
the signal handler.

Note: Scripts that connect in parallel must be rooted under an Actor.

Provide feedback

---

Once

Connects the given function to the event (for a single invocation) and
returns an [RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) that represents it.

RBXScriptSignal:Once(func:[function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| func:[function](/docs/luau/functions) |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Establishes a function to be called when the event fires. Returns an
[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) object associated with the connection. The
behavior of Once is similar to Connect. However, instead of allowing
multiple events to be received by the specified function, only the first
event will be delivered. Using Once also ensures that the connection to
the function will be automatically disconnected prior the function being
called.

Provide feedback

---

Wait

Yields the current thread until the signal fires and returns the arguments
provided by the signal.

RBXScriptSignal:Wait():Variant

Returns

Variant

Yields the current thread until the signal fires and returns the arguments
provided by the signal.

Provide feedback

---