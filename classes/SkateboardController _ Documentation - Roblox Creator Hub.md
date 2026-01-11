# SkateboardController | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SkateboardController
Scraped: 2026-01-11T02:28:01.597901Z

## Tags
- Not Replicated

## Inherits
- Controller
- SkateboardController
- Instance
- Object
- SkateboardPlatform
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Controller](/docs/reference/engine/classes/Controller)
6. /
7. [SkateboardController](/docs/reference/engine/classes/SkateboardController)

English

Feedback

Engine Class

SkateboardController

---

Summary

Properties

|  |
| --- |
| [Steer](#Steer):[number](/docs/luau/numbers) |
| [Throttle](#Throttle):[number](/docs/luau/numbers) |

Events

|  |
| --- |
| [AxisChanged](#AxisChanged)(axis: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

6 inherited from [Controller](/docs/reference/engine/classes/Controller)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A SkateboardController is an object responsible for translating PlayerActions
to movements with a [SkateboardPlatform](/docs/reference/engine/classes/SkateboardPlatform).

---

API Reference

Properties

Steer

Read Only

Not Replicated

Read Parallel

The direction of movement, tied to the keys A and D. Must be 1 (right), 0
(straight), or -1 (left). Will refresh back to 0 unless constantly set.

SkateboardController.Steer:[number](/docs/luau/numbers)

The direction of movement, tied to the keys A and D. Must be 1 (right), 0
(straight), or -1 (left). Will refresh back to 0 unless constantly set.

Provide feedback

---

Throttle

Read Only

Not Replicated

Read Parallel

The direction of movement, tied to the keys W and S. Must be an integer 1
(forward), 0 (null), or -1 (reverse). Will refresh back to 0 unless
constantly set.

SkateboardController.Throttle:[number](/docs/luau/numbers)

The direction of movement, tied to the keys W and S. Must be an integer 1
(forward), 0 (null), or -1 (reverse). Will refresh back to 0 unless
constantly set.

Provide feedback

---

Events

AxisChanged

Fired when any input state of the skateboard controller is updated.

SkateboardController.AxisChanged(axis:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| axis:[string](/docs/luau/strings) |

Fired when any input state of the skateboard controller is updated. The
axis is fired with either "Throttle" if the throttle state of the
skateboard was updated or "Steer" if the steering state of the
skateboard was updated.

Provide feedback

---