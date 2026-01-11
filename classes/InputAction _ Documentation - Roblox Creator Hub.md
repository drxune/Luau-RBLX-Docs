# InputAction | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/InputAction
Scraped: 2026-01-11T02:28:25.313531Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- InputAction
- InputBinding
- InputContext
- Type
- Pressed
- StateChanged
- Released
- InputAction.Type
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [InputAction](/docs/reference/engine/classes/InputAction)

English

Feedback

Engine Class

![InputAction](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/InputAction-Dark.webp)InputAction

Defines a gameplay action mechanic. These actions are then mapped to hardware
inputs using [InputBinding](/docs/reference/engine/classes/InputBinding).

---

Summary

Properties

|  |
| --- |
| [BoolState](#BoolState):[boolean](/docs/luau/booleans) |
| [Direction1DState](#Direction1DState):[number](/docs/luau/numbers) |
| [Direction2DState](#Direction2DState):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Direction3DState](#Direction3DState):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Type](#Type):[Enum.InputActionType](/docs/reference/engine/enums/InputActionType) |

Methods

|  |
| --- |
| [Fire](#Fire)(state: Variant):() |
| [GetState](#GetState)():Variant |

Events

|  |
| --- |
| [Pressed](#Pressed)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Released](#Released)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [StateChanged](#StateChanged)(value: Variant):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

InputAction defines a gameplay action mechanic such as "Jump," "Sprint," or
"Shoot." These actions are then mapped to hardware inputs using
[InputBinding](/docs/reference/engine/classes/InputBinding). An InputAction will check for its first ancestor type
of [InputContext](/docs/reference/engine/classes/InputContext) and register itself to that context (if there is no
ancestor context, it will be registered to a default context).

---

API Reference

Properties

BoolState

Read Only

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

InputAction.BoolState:[boolean](/docs/luau/booleans)

Provide feedback

---

Direction1DState

Read Only

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

Non-scriptable read-only property useful for debugging
[Direction1D](/docs/reference/engine/enums/InputActionType) input actions.

InputAction.Direction1DState:[number](/docs/luau/numbers)

A non-scriptable read-only property only visible in Studio, primarily
useful for debugging while testing an InputAction with
[Type](/docs/reference/engine/classes/InputAction#Type) of [Direction1D](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Direction2DState

Read Only

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

Non-scriptable read-only property useful for debugging
[Direction2D](/docs/reference/engine/enums/InputActionType) input actions.

InputAction.Direction2DState:[Vector2](/docs/reference/engine/datatypes/Vector2)

A non-scriptable read-only property only visible in Studio, primarily
useful for debugging while testing an InputAction with
[Type](/docs/reference/engine/classes/InputAction#Type) of [Direction2D](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Direction3DState

Read Only

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

Non-scriptable read-only property useful for debugging
[Direction3D](/docs/reference/engine/enums/InputActionType) input actions.

InputAction.Direction3DState:[Vector3](/docs/reference/engine/datatypes/Vector3)

A non-scriptable read-only property only visible in Studio, primarily
useful for debugging while testing an InputAction with
[Type](/docs/reference/engine/classes/InputAction#Type) of [Direction3D](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Enabled

Read Parallel

Determines if the InputAction is enabled or not.

InputAction.Enabled:[boolean](/docs/luau/booleans)

Determines if the InputAction is enabled or not. The action state will
be reset if this property is toggled to false.

Provide feedback

---

Type

Read Parallel

Specifies what type of input value the action is expecting.

InputAction.Type:[Enum.InputActionType](/docs/reference/engine/enums/InputActionType)

Specifies what type of input value the action is expecting. See
[Enum.InputActionType](/docs/reference/engine/enums/InputActionType) for more details.

Provide feedback

---

Methods

Fire

Updates the InputAction to the given state and fires the appropriate
signals.

InputAction:Fire(state:Variant):()

Parameters

|  |
| --- |
| state:Variant |

Returns

()

Updates the InputAction to the given state and fires the appropriate
signals. This method is most useful for script‑triggered "input" where the
passed state should trigger events like
[Pressed](/docs/reference/engine/classes/InputAction#Pressed) or
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) regardless of whether the
player triggered that state through normal inputs.

This method will only accept a state parameter that matches the
[Type](/docs/reference/engine/classes/InputAction#Type) and attempting to call it with a mismatched
type will cause an error, for example passing a state of 0.5 when the
[Type](/docs/reference/engine/classes/InputAction#Type) is [Bool](/docs/reference/engine/enums/InputActionType).

Note that this method follows the conditions of
[Pressed](/docs/reference/engine/classes/InputAction#Pressed),
[Released](/docs/reference/engine/classes/InputAction#Released), and
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged). For example, if you make
multiple consecutive calls to Fire() with a state of true,
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) will only fire on the first
state change and the subsequent calls to Fire() will do nothing.

Provide feedback

---

GetState

Write Parallel

Returns the current state of the [InputAction](/docs/reference/engine/classes/InputAction).

InputAction:GetState():Variant

Returns

Variant

The current state of [InputAction](/docs/reference/engine/classes/InputAction).

Returns the current state of the [InputAction](/docs/reference/engine/classes/InputAction), for example true
for an action with [Type](/docs/reference/engine/classes/InputAction#Type) set to
[Bool](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Events

Pressed

Fires only when the [InputAction.Type](/docs/reference/engine/classes/InputAction#Type) is set to
[Bool](/docs/reference/engine/enums/InputActionType) on a state transition from false to true.

InputAction.Pressed():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires only when the [Type](/docs/reference/engine/classes/InputAction#Type) is set to
[Bool](/docs/reference/engine/enums/InputActionType), and only when the state transitions from
false to true.

Provide feedback

---

Released

Fires only when the [InputAction.Type](/docs/reference/engine/classes/InputAction#Type) is set to
[Bool](/docs/reference/engine/enums/InputActionType) on a state transition from true to false.

InputAction.Released():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires only when the [Type](/docs/reference/engine/classes/InputAction#Type) is set to
[Bool](/docs/reference/engine/enums/InputActionType), and only when the state transitions from
true to false.

Provide feedback

---

StateChanged

Fires for all [Enum.InputActionType](/docs/reference/engine/enums/InputActionType) types whenever the state changes,
except if the state attempts to transition to the same state.

InputAction.StateChanged(value:Variant):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:Variant  The new state of the [InputAction](/docs/reference/engine/classes/InputAction). |

This event fires for all [Enum.InputActionType](/docs/reference/engine/enums/InputActionType) types whenever the state
changes, except if the state attempts to transition to the same state.

Provide feedback

---