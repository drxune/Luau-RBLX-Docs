# InputObject | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/InputObject
Scraped: 2026-01-11T02:37:48.747742Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- InputObject
- UserInputType
- UserInputState
- Position
- Delta
- KeyCode
- Changed
- UserInputService.InputBegan
- UserInputService
- GuiObject
- Object.Changed
- UserInputService.InputChanged
- GuiObject.InputChanged
- InputBegan
- InputChanged
- GetMouseDelta()
- InputObjects
- GetMouseLocation()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [InputObject](/docs/reference/engine/classes/InputObject)

English

Feedback

Engine Class

InputObject

An object created when an input begins that describes a particular user input.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Delta](#Delta):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [KeyCode](#KeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [UserInputState](#UserInputState):[Enum.UserInputState](/docs/reference/engine/enums/UserInputState) |
| [UserInputType](#UserInputType):[Enum.UserInputType](/docs/reference/engine/enums/UserInputType) |

Methods

|  |
| --- |
| [IsModifierKeyDown](#IsModifierKeyDown)(modifierKey: [Enum.ModifierKey](/docs/reference/engine/enums/ModifierKey)):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An InputObject represents a single user input, such as mouse movement,
touches, key presses and more. It is created when an input begins.

The properties of this object vary according the
[UserInputType](/docs/reference/engine/classes/InputObject#UserInputType). Each kind of input will
undergo various changes to its
[UserInputState](/docs/reference/engine/classes/InputObject#UserInputState). During the lifetime of an
input, other properties which further describe the input may change, such as
[Position](/docs/reference/engine/classes/InputObject#Position) and [Delta](/docs/reference/engine/classes/InputObject#Delta).
Keyboard and gamepad button presses will have the
[KeyCode](/docs/reference/engine/classes/InputObject#KeyCode) property set.

Once created at the beginning of an input, the same object persists and is
updated until the input ends. As a result, you can track the object's changes
using the [Changed](/docs/reference/engine/classes/Object#Changed) event as the user changes the input
in question. You can also place these objects into a list of active inputs
track and interact with the object after it's creation by an event such as
[UserInputService.InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan). This is mostly useful for touch events,
as each touch point will have a separate InputObject.

See also [UserInputService](/docs/reference/engine/classes/UserInputService) whose events and functions often use
InputObject, and [GuiObject](/docs/reference/engine/classes/GuiObject) whose events related to user input use
InputObject.

---

API Reference

Properties

Delta

Read Parallel

A [Vector3](/docs/reference/engine/datatypes/Vector3) describing the delta between input movements.

InputObject.Delta:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) describing the delta (change) between input
movements.

This is useful when used with the input's
[Position](/docs/reference/engine/classes/InputObject#Position) to track the position and movement
of the user's input, such as when you're creating custom movement or
camera scripts. Consider tracking input object changes using the
[Object.Changed](/docs/reference/engine/classes/Object#Changed) event or when user input changes via events such as
[UserInputService.InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged) and [GuiObject.InputChanged](/docs/reference/engine/classes/GuiObject#InputChanged).

Note that an [InputObject](/docs/reference/engine/classes/InputObject) corresponding to
[Enum.UserInputType.MouseButton1](/docs/reference/engine/enums/UserInputType#MouseButton1) (left click) and
[Enum.UserInputType.MouseButton2](/docs/reference/engine/enums/UserInputType#MouseButton2) (right click) supplied from an
[InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan) callback will not have its
[Delta](/docs/reference/engine/classes/InputObject#Delta) or [Position](/docs/reference/engine/classes/InputObject#Position)
updated once created, except for when the mouse input ends. In order to
get updated deltas for mouse inputs, you must instead reference an
[InputObject](/docs/reference/engine/classes/InputObject) from an
[InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged) callback, or call
[GetMouseDelta()](/docs/reference/engine/classes/UserInputService#GetMouseDelta). However, any
[InputObjects](/docs/reference/engine/classes/InputObject) corresponding to touch inputs will have
their delta and position updated every frame throughout their lifetime.

Provide feedback

---

KeyCode

Read Parallel

Contains an Enum that describes the kind of input used.

InputObject.KeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Contains a [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) enum that describes what kind of input was used.
For types of input like keyboard, this describes what key was pressed. For
inputs like the mouse, this provides no additional information.

Provide feedback

---

Position

Read Parallel

A [Vector3](/docs/reference/engine/datatypes/Vector3) describing the positional value of this input.

InputObject.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) describing the positional value of this input.

For mouse and touch input, this is the screen position of the mouse/touch,
described in the X and Y components. The inset applied to GUI
elements (such as from the top bar) is accounted for in the position. For
the mouse wheel input, the Z component describes whether the wheel was
moved forward (1), backwards (-1), or not at all (0).

Note that an [InputObject](/docs/reference/engine/classes/InputObject) corresponding to
[Enum.UserInputType.MouseButton1](/docs/reference/engine/enums/UserInputType#MouseButton1) (left click) and
[Enum.UserInputType.MouseButton2](/docs/reference/engine/enums/UserInputType#MouseButton2) (right click) supplied from an
[InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan) callback will not have its
[Delta](/docs/reference/engine/classes/InputObject#Delta) or [Position](/docs/reference/engine/classes/InputObject#Position)
updated once created, except for when the mouse input ends. In order to
get updated positions for mouse inputs, you must instead reference an
[InputObject](/docs/reference/engine/classes/InputObject) from an
[InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged) callback, or call
[GetMouseLocation()](/docs/reference/engine/classes/UserInputService#GetMouseLocation). However,
any [InputObjects](/docs/reference/engine/classes/InputObject) corresponding to touch inputs will
have their delta and position updated every frame throughout their
lifetime.

Provide feedback

---

UserInputState

Read Parallel

Describes the state of an input being performed, following a specific flow
depending on the [UserInputType](/docs/reference/engine/classes/InputObject#UserInputType).

InputObject.UserInputState:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)

This property describes the state of an input being performed, following a
specific flow depending on the
[UserInputType](/docs/reference/engine/classes/InputObject#UserInputType). It uses the enum of the
same name, [Enum.UserInputState](/docs/reference/engine/enums/UserInputState).

Provide feedback

---

UserInputType

Read Parallel

Describes the kind of input being performed (mouse, keyboard, gamepad,
touch, etc.).

InputObject.UserInputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)

This property describes the kind of input this [InputObject](/docs/reference/engine/classes/InputObject)
represents, such as mouse, keyboard, touch, or gamepad input. It uses the
enum of the same name, [Enum.UserInputType](/docs/reference/engine/enums/UserInputType).

Provide feedback

---

Methods

IsModifierKeyDown

Returns whether the passed in modifier key is down.

InputObject:IsModifierKeyDown(modifierKey:[Enum.ModifierKey](/docs/reference/engine/enums/ModifierKey)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| modifierKey:[Enum.ModifierKey](/docs/reference/engine/enums/ModifierKey) |

Returns

[boolean](/docs/luau/booleans)

true if the passed in modifierKey is being held down; false
otherwise.

Returns true if the passed in modifierKey such as
[Shift](/docs/reference/engine/enums/ModifierKey) is being held down.

Provide feedback

---