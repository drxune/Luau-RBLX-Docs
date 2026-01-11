# InputBinding | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/InputBinding
Scraped: 2026-01-11T02:28:38.267644Z

## Inherits
- Object
- Instance
- InputBinding
- InputAction
- GuiButton
- GetState()
- StateChanged
- Type
- ReleasedThreshold
- PressedThreshold
- KeyCode
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [InputBinding](/docs/reference/engine/classes/InputBinding)

English

Feedback

Engine Class

![InputBinding](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/InputBinding-Dark.webp)InputBinding

Defines which hardware binding should trigger the parent [InputAction](/docs/reference/engine/classes/InputAction).

---

Summary

Properties

|  |
| --- |
| [Backward](#Backward):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [Down](#Down):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [Forward](#Forward):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [KeyCode](#KeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [Left](#Left):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [PressedThreshold](#PressedThreshold):[number](/docs/luau/numbers) |
| [ReleasedThreshold](#ReleasedThreshold):[number](/docs/luau/numbers) |
| [ResponseCurve](#ResponseCurve):[number](/docs/luau/numbers) |
| [Right](#Right):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [Scale](#Scale):[number](/docs/luau/numbers) |
| [UIButton](#UIButton):[GuiButton](/docs/reference/engine/classes/GuiButton) |
| [Up](#Up):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [Vector2Scale](#Vector2Scale):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Vector3Scale](#Vector3Scale):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An InputBinding defines which hardware binding should trigger the parent
[InputAction](/docs/reference/engine/classes/InputAction), for example a key press, gamepad button, or tap on a
touch‑enabled device. There can be multiple InputBinding instances parented
to an [InputAction](/docs/reference/engine/classes/InputAction).

---

API Reference

Properties

Backward

Read Parallel

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally
"backward" inputs to the parent [InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Backward:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally
"backward" inputs to [GetState()](/docs/reference/engine/classes/InputAction#GetState) and the
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) event of the parent
[InputAction](/docs/reference/engine/classes/InputAction). Only applies when the parent action's
[Type](/docs/reference/engine/classes/InputAction#Type) is [Direction3D](/docs/reference/engine/enums/InputActionType), in
which case the dispatched value will be a [Vector3](/docs/reference/engine/datatypes/Vector3) with its
[Z](/docs/reference/engine/datatypes/Vector3#Z) component between 0 and -1.

Provide feedback

---

Down

Read Parallel

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally "down"
inputs to the parent [InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Down:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally "down"
inputs to [GetState()](/docs/reference/engine/classes/InputAction#GetState) and the
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) event of the parent
[InputAction](/docs/reference/engine/classes/InputAction).

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction1D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a number
between 0 and -1.

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction2D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector2](/docs/reference/engine/datatypes/Vector2) with its [Y](/docs/reference/engine/datatypes/Vector2#Y) component between 0
and -1.

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction3D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector3](/docs/reference/engine/datatypes/Vector3) with its [Y](/docs/reference/engine/datatypes/Vector3#Y) component between 0
and -1.

Not applicable when the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Bool](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Forward

Read Parallel

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally
"forward" inputs to the parent [InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Forward:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally
"forward" inputs to [GetState()](/docs/reference/engine/classes/InputAction#GetState) and the
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) event of the parent
[InputAction](/docs/reference/engine/classes/InputAction). Only applies when the parent action's
[Type](/docs/reference/engine/classes/InputAction#Type) is [Direction3D](/docs/reference/engine/enums/InputActionType), in
which case the dispatched value will be a [Vector3](/docs/reference/engine/datatypes/Vector3) with its
[Z](/docs/reference/engine/datatypes/Vector3#Z) component between 0 and 1.

Provide feedback

---

KeyCode

Read Parallel

Specifies the [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) which triggers the parent
[InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.KeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Specifies the [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) which triggers the parent
[InputAction](/docs/reference/engine/classes/InputAction). The code type should match the input action's
[Type](/docs/reference/engine/classes/InputAction#Type), for example [Enum.KeyCode.E](/docs/reference/engine/enums/KeyCode#E) for an action
type of [Bool](/docs/reference/engine/enums/InputActionType) or [Enum.KeyCode.Thumbstick1](/docs/reference/engine/enums/KeyCode#Thumbstick1) for an
action type of [Direction2D](/docs/reference/engine/enums/InputActionType). Type mismatches will
either not fire the [InputAction](/docs/reference/engine/classes/InputAction) or the
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) event will receive a
converted value.

Provide feedback

---

Left

Read Parallel

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally "left"
inputs to the parent [InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Left:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally "left"
inputs to [GetState()](/docs/reference/engine/classes/InputAction#GetState) and the
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) event of the parent
[InputAction](/docs/reference/engine/classes/InputAction).

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction2D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector2](/docs/reference/engine/datatypes/Vector2) with its [X](/docs/reference/engine/datatypes/Vector2#X) component between 0
and -1.

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction3D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector3](/docs/reference/engine/datatypes/Vector3) with its [X](/docs/reference/engine/datatypes/Vector3#X) component between 0
and -1.

Not applicable when the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction1D](/docs/reference/engine/enums/InputActionType) or [Bool](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

PressedThreshold

Read Parallel

Numerical value above which to fire an [InputAction](/docs/reference/engine/classes/InputAction) with a
[Type](/docs/reference/engine/classes/InputAction#Type) of [Bool](/docs/reference/engine/enums/InputActionType).

InputBinding.PressedThreshold:[number](/docs/luau/numbers)

Numerical value above which to fire an [InputAction](/docs/reference/engine/classes/InputAction) with a
[Type](/docs/reference/engine/classes/InputAction#Type) of [Bool](/docs/reference/engine/enums/InputActionType), for example
when a gamepad trigger such as [Enum.KeyCode.ButtonL2](/docs/reference/engine/enums/KeyCode#ButtonL2) exceeds 0.5
(halfway pressed). Default is 0.5.

This property must be greater than or equal to
[ReleasedThreshold](/docs/reference/engine/classes/InputBinding#ReleasedThreshold) or else it will
be clamped to [ReleasedThreshold](/docs/reference/engine/classes/InputBinding#ReleasedThreshold).

Provide feedback

---

ReleasedThreshold

Read Parallel

Numerical value below which to fire an [InputAction](/docs/reference/engine/classes/InputAction) with a
[Type](/docs/reference/engine/classes/InputAction#Type) of [Bool](/docs/reference/engine/enums/InputActionType).

InputBinding.ReleasedThreshold:[number](/docs/luau/numbers)

Numerical value below which to fire an [InputAction](/docs/reference/engine/classes/InputAction) with a
[Type](/docs/reference/engine/classes/InputAction#Type) of [Bool](/docs/reference/engine/enums/InputActionType), for example
when a gamepad trigger such as [Enum.KeyCode.ButtonL2](/docs/reference/engine/enums/KeyCode#ButtonL2) falls below 0.5
(less than halfway pressed). Default is 0.2.

This property must be less than or equal to
[PressedThreshold](/docs/reference/engine/classes/InputBinding#PressedThreshold) or else it will be
clamped to [PressedThreshold](/docs/reference/engine/classes/InputBinding#PressedThreshold).

Provide feedback

---

ResponseCurve

Read Parallel

Numerical value to configure scaling for more precise thumbstick aiming.

InputBinding.ResponseCurve:[number](/docs/luau/numbers)

A numerical value to control the sensitivity of gamepad thumbstick input
by applying a quadratic response curve. Commonly used for camera control
to make small thumbstick inputs more precise, while ramping up quickly to
allow for large movements with higher magnitude input.

Ranges between 1 to 10, with higher values providing a more intense
curve. Default is 1, at which input is returned exactly as received.

Only applicable when the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction2D](/docs/reference/engine/enums/InputActionType) and the
[KeyCode](/docs/reference/engine/classes/InputBinding#KeyCode) is
[Thumbstick1](/docs/reference/engine/enums/KeyCode#Thumbstick1) or
[Thumbstick2](/docs/reference/engine/enums/KeyCode#Thumbstick2).

Provide feedback

---

Right

Read Parallel

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally
"right" inputs to the parent [InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Right:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally
"right" inputs to [GetState()](/docs/reference/engine/classes/InputAction#GetState) and the
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) event of the parent
[InputAction](/docs/reference/engine/classes/InputAction).

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction2D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector2](/docs/reference/engine/datatypes/Vector2) with its [X](/docs/reference/engine/datatypes/Vector2#X) component between 0
and 1.

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction3D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector3](/docs/reference/engine/datatypes/Vector3) with its [X](/docs/reference/engine/datatypes/Vector3#X) component between 0
and 1.

Not applicable when the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction1D](/docs/reference/engine/enums/InputActionType) or [Bool](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Scale

Read Parallel

Amount by which to linearly scale the values of a directional
[InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Scale:[number](/docs/luau/numbers)

Amount by which to linearly scale the values of an [InputAction](/docs/reference/engine/classes/InputAction)
with [Type](/docs/reference/engine/classes/InputAction#Type) of [Direction1D](/docs/reference/engine/enums/InputActionType),
[Direction2D](/docs/reference/engine/enums/InputActionType), or [Direction3D](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

UIButton

Read Parallel

Connects a [GuiButton](/docs/reference/engine/classes/GuiButton) to a boolean action.

InputBinding.UIButton:[GuiButton](/docs/reference/engine/classes/GuiButton)

[GuiButton](/docs/reference/engine/classes/GuiButton) to connect to a boolean action.

Provide feedback

---

Up

Read Parallel

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally "up"
inputs to the parent [InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Up:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Specifies an alternate [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for dispatching directionally "up"
inputs to [GetState()](/docs/reference/engine/classes/InputAction#GetState) and the
[StateChanged](/docs/reference/engine/classes/InputAction#StateChanged) event of the parent
[InputAction](/docs/reference/engine/classes/InputAction).

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction1D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a number
between 0 and 1.

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction2D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector2](/docs/reference/engine/datatypes/Vector2) with its [Y](/docs/reference/engine/datatypes/Vector2#Y) component between 0
and 1.

When the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Direction3D](/docs/reference/engine/enums/InputActionType), the dispatched value will be a
[Vector3](/docs/reference/engine/datatypes/Vector3) with its [Y](/docs/reference/engine/datatypes/Vector3#Y) component between 0
and 1.

Not applicable when the parent action's [Type](/docs/reference/engine/classes/InputAction#Type) is
[Bool](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Vector2Scale

Read Parallel

Amount by which to linearly scale the values of a two-directional
[InputAction](/docs/reference/engine/classes/InputAction).

InputBinding.Vector2Scale:[Vector2](/docs/reference/engine/datatypes/Vector2)

Amount by which to linearly scale the values of an [InputAction](/docs/reference/engine/classes/InputAction)
with [Type](/docs/reference/engine/classes/InputAction#Type) of [Direction2D](/docs/reference/engine/enums/InputActionType).

Provide feedback

---

Vector3Scale

Read Parallel

InputBinding.Vector3Scale:[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---