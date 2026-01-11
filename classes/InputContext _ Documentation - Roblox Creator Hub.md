# InputContext | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/InputContext
Scraped: 2026-01-11T02:33:59.731664Z

## Inherits
- Object
- Instance
- InputContext
- InputActions
- Enabled
- Priority
- Sink
- InputAction
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [InputContext](/docs/reference/engine/classes/InputContext)

English

Feedback

Engine Class

![InputContext](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/InputContext-Dark.webp)InputContext

Collection of actions which holds related actions and defines how they
interact with other contexts/actions.

---

Summary

Properties

|  |
| --- |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Priority](#Priority):[number](/docs/luau/numbers) |
| [Sink](#Sink):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An InputContext is a collection of actions which holds related
[InputActions](/docs/reference/engine/classes/InputAction) and defines how they interact with other
contexts and actions. Nested InputContext instances will have no effect and
ordering/priority is managed through [Enabled](/docs/reference/engine/classes/InputContext#Enabled),
[Priority](/docs/reference/engine/classes/InputContext#Priority), and [Sink](/docs/reference/engine/classes/InputContext#Sink).

---

API Reference

Properties

Enabled

Read Parallel

Determines if this InputContext is enabled or not.

InputContext.Enabled:[boolean](/docs/luau/booleans)

Determines if this InputContext is enabled or not. When false, all of
the descendant actions of the context do not receive any signals except
when Enabled is toggled from true to false, in which case a final
"end" signal is triggered if a key is pressed or a two-directional input
is not zero.

Provide feedback

---

Priority

Read Parallel

The priority level at which the context should be run.

InputContext.Priority:[number](/docs/luau/numbers)

The priority level at which the context should be run (higher priority
InputContext instances run before lower ones).

Provide feedback

---

Sink

Read Parallel

Determines whether input bindings of lower priority will be processed.

InputContext.Sink:[boolean](/docs/luau/booleans)

When Sink is set to true, inputs will not be processed for connected
[InputAction](/docs/reference/engine/classes/InputAction) bindings within contexts of lower
[Priority](/docs/reference/engine/classes/InputContext#Priority). Contexts with the same priority
will receive the input.

For example, if multiple contexts contain an [InputAction](/docs/reference/engine/classes/InputAction) with a
binding to [Enum.KeyCode.E](/docs/reference/engine/enums/KeyCode#E) and a higher priority context has Sink set
to true, the lower priority contexts will not receive the input signal
for [Enum.KeyCode.E](/docs/reference/engine/enums/KeyCode#E) and will fire no events for it.

Provide feedback

---