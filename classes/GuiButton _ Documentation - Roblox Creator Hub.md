# GuiButton | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GuiButton
Scraped: 2026-01-11T02:28:23.347286Z

## Tags
- Not Creatable

## Inherits
- GuiObject
- GuiButton
- HapticEffect
- InputObject
- GuiBase2d
- Instance
- Object
- ImageButton
- TextButton
- AutoButtonColor
- Modal
- Activated
- Mouse
- HoverImage
- PressedImage
- Image
- LocalScript
- Script
- RunContext
- MouseButton1Down
- MouseButton1Up
- MouseButton1Click
- MouseButton2Down
- MouseButton2Up
- MouseButton2Click
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiObject](/docs/reference/engine/classes/GuiObject)
6. /
7. [GuiButton](/docs/reference/engine/classes/GuiButton)

English

Feedback

Engine Class

GuiButton

An abstract class for interactive 2D user interface elements.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [AutoButtonColor](#AutoButtonColor):[boolean](/docs/luau/booleans) |
| [HoverHapticEffect](#HoverHapticEffect):[HapticEffect](/docs/reference/engine/classes/HapticEffect) |
| [Modal](#Modal):[boolean](/docs/luau/booleans) |
| [PressHapticEffect](#PressHapticEffect):[HapticEffect](/docs/reference/engine/classes/HapticEffect) |
| [Selected](#Selected):[boolean](/docs/luau/booleans) |
| [Style](#Style):[Enum.ButtonStyle](/docs/reference/engine/enums/ButtonStyle) |

Events

|  |
| --- |
| [Activated](#Activated)(inputObject: [InputObject](/docs/reference/engine/classes/InputObject),clickCount: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton1Click](#MouseButton1Click)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton1Down](#MouseButton1Down)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton1Up](#MouseButton1Up)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton2Click](#MouseButton2Click)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton2Down](#MouseButton2Down)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseButton2Up](#MouseButton2Up)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [SecondaryActivated](#SecondaryActivated)(inputObject: [InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[ImageButton](/docs/reference/engine/classes/ImageButton), [TextButton](/docs/reference/engine/classes/TextButton)

[GuiButton](/docs/reference/engine/classes/GuiButton) is an abstract class that inherits from [GuiObject](/docs/reference/engine/classes/GuiObject).
It is the base class for the interactive, clickable [ImageButton](/docs/reference/engine/classes/ImageButton) and
[TextButton](/docs/reference/engine/classes/TextButton) objects. This class also defines several properties for
interactive behavior, namely [AutoButtonColor](/docs/reference/engine/classes/GuiButton#AutoButtonColor)
and [Modal](/docs/reference/engine/classes/GuiButton#Modal).

The most important event of a [GuiButton](/docs/reference/engine/classes/GuiButton) is
[Activated](/docs/reference/engine/classes/GuiButton#Activated), a multi-platform event that fires
when the button is activated. When using a mouse, this means clicking the
button and releasing with the cursor still over the UI object. For touch, the
same applies but with a touch instead of button press. Finally, for gamepads,
[Activated](/docs/reference/engine/classes/GuiButton#Activated) fires if a [GuiButton](/docs/reference/engine/classes/GuiButton) is selected
when the A button is pressed and released. In short, this event is very
useful for multi-platform user interface programming as it provides a nice
general interface for a single user input.

---

API Reference

Properties

AutoButtonColor

Read Parallel

Determines whether the button automatically changes color when the mouse
hovers over or clicks on it.

GuiButton.AutoButtonColor:[boolean](/docs/luau/booleans)

This property determines whether the button automatically changes color
when the user's [Mouse](/docs/reference/engine/classes/Mouse) hovers over or clicks on it. If true, the
button will automatically change color when the mouse hovers over or
clicks on it. If false, the button will not change.

If you would like to customize how a button changes when the user's mouse
hovers over or clicks on it, consider using an [ImageButton](/docs/reference/engine/classes/ImageButton) and
changing the element's [HoverImage](/docs/reference/engine/classes/ImageButton#HoverImage) and
[PressedImage](/docs/reference/engine/classes/ImageButton#PressedImage).

Please note that this property will not have an effect on an
[ImageButton](/docs/reference/engine/classes/ImageButton) if its [Image](/docs/reference/engine/classes/ImageButton#Image) property is set
to an image. Additionally, this property will not affect an
[ImageButton](/docs/reference/engine/classes/ImageButton) on mouse hover when its
[HoverImage](/docs/reference/engine/classes/ImageButton#HoverImage) is not nil, nor on mouse click
if its [PressedImage](/docs/reference/engine/classes/ImageButton#PressedImage) is not nil.

Provide feedback

---

HoverHapticEffect

Read Parallel

A [HapticEffect](/docs/reference/engine/classes/HapticEffect) instance that will play when the [GuiButton](/docs/reference/engine/classes/GuiButton)
is being hovered.

GuiButton.HoverHapticEffect:[HapticEffect](/docs/reference/engine/classes/HapticEffect)

A [HapticEffect](/docs/reference/engine/classes/HapticEffect) instance that will play when the [GuiButton](/docs/reference/engine/classes/GuiButton)
is being hovered.

Provide feedback

---

Modal

Read Parallel

If true while the GUI element is visible, the mouse will not be locked
unless the right mouse button is down.

GuiButton.Modal:[boolean](/docs/luau/booleans)

If true while the GUI element is visible, the mouse will not be locked
unless the right mouse button is down.

Provide feedback

---

PressHapticEffect

Read Parallel

A [HapticEffect](/docs/reference/engine/classes/HapticEffect) instance that will play when the [GuiButton](/docs/reference/engine/classes/GuiButton)
is being pressed.

GuiButton.PressHapticEffect:[HapticEffect](/docs/reference/engine/classes/HapticEffect)

A [HapticEffect](/docs/reference/engine/classes/HapticEffect) instance that will play when the [GuiButton](/docs/reference/engine/classes/GuiButton)
is being pressed.

Provide feedback

---

Selected

Read Parallel

A boolean property which indicates whether the object has been selected.

GuiButton.Selected:[boolean](/docs/luau/booleans)

A boolean property which indicates whether the object has been selected.

Provide feedback

---

Style

Read Parallel

Sets the style of the [GuiButton](/docs/reference/engine/classes/GuiButton) based on a list of pre-determined
styles.

GuiButton.Style:[Enum.ButtonStyle](/docs/reference/engine/enums/ButtonStyle)

Sets the style of the [GuiButton](/docs/reference/engine/classes/GuiButton) based on a list of pre-determined
styles.

Provide feedback

---

Events

Activated

Fires when the button is activated.

GuiButton.Activated(

inputObject:[InputObject](/docs/reference/engine/classes/InputObject), clickCount:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| inputObject:[InputObject](/docs/reference/engine/classes/InputObject) |
| clickCount:[number](/docs/luau/numbers) |

Fires when the button is activated. As this event doesn't fire on the
server, it should only be used in a [LocalScript](/docs/reference/engine/classes/LocalScript), or in a
[Script](/docs/reference/engine/classes/Script) with [RunContext](/docs/reference/engine/classes/Script#RunContext) of
[Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client).

Provide feedback

---

MouseButton1Click

Fires when the user's mouse fully left clicks the [GuiButton](/docs/reference/engine/classes/GuiButton).

GuiButton.MouseButton1Click():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the user's mouse fully left clicks the
[GuiButton](/docs/reference/engine/classes/GuiButton).

In regards to clicking, the mouse must be in bounds of the
[GuiButton](/docs/reference/engine/classes/GuiButton) and the mouse button must be pressed down and up again
before this event fires. If the mouse leaves the bounds of the
[GuiButton](/docs/reference/engine/classes/GuiButton) and is released, the event will not fire. If you would
like to avoid this limitation, you can use
[MouseButton1Down](/docs/reference/engine/classes/GuiButton#MouseButton1Down) and
[MouseButton1Up](/docs/reference/engine/classes/GuiButton#MouseButton1Up); these events are similar
but will fire whenever the user presses their left mouse button down or
up, respectively.

Provide feedback

---

MouseButton1Down

Fires when the user presses their left mouse button down on the
[GuiButton](/docs/reference/engine/classes/GuiButton).

GuiButton.MouseButton1Down(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels. |

This event fires when the user presses their left mouse button down on the
[GuiButton](/docs/reference/engine/classes/GuiButton).

For an event requiring the user to press and release their left mouse
on a [GuiButton](/docs/reference/engine/classes/GuiButton) in order for the event to fire, consider using
[MouseButton1Click](/docs/reference/engine/classes/GuiButton#MouseButton1Click).

Provide feedback

---

MouseButton1Up

Fires when the user releases their left mouse button off of the
[GuiButton](/docs/reference/engine/classes/GuiButton).

GuiButton.MouseButton1Up(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels. |

This event fires when the user releases their left mouse button off of the
[GuiButton](/docs/reference/engine/classes/GuiButton).

For an event requiring the user to press and release their left mouse
on a [GuiButton](/docs/reference/engine/classes/GuiButton) in order for the event to fire, consider using
[MouseButton1Click](/docs/reference/engine/classes/GuiButton#MouseButton1Click).

Provide feedback

---

MouseButton2Click

Fires when the user's mouse fully right clicks the [GuiButton](/docs/reference/engine/classes/GuiButton).

GuiButton.MouseButton2Click():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the user's mouse fully right clicks the
[GuiButton](/docs/reference/engine/classes/GuiButton).

In regards to clicking, the mouse must be in bounds of the
[GuiButton](/docs/reference/engine/classes/GuiButton) and the mouse button must be pressed down and up again
before this event fires. If the mouse leaves the bounds of the
[GuiButton](/docs/reference/engine/classes/GuiButton) and is released, the event will not fire. If you would
like to avoid this limitation, you can use
[MouseButton2Down](/docs/reference/engine/classes/GuiButton#MouseButton2Down) and
[MouseButton2Up](/docs/reference/engine/classes/GuiButton#MouseButton2Up); these events are similar
but will fire whenever the user presses their right mouse button down or
up, respectively.

Provide feedback

---

MouseButton2Down

Fires when the user presses their right mouse button down on the
[GuiButton](/docs/reference/engine/classes/GuiButton).

GuiButton.MouseButton2Down(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels. |

This event fires when the user presses their right mouse button down on
the [GuiButton](/docs/reference/engine/classes/GuiButton).

For an event requiring the user to press and release their right mouse
on a [GuiButton](/docs/reference/engine/classes/GuiButton) in order for the event to fire, consider using
[MouseButton2Click](/docs/reference/engine/classes/GuiButton#MouseButton2Click).

Provide feedback

---

MouseButton2Up

Fires when the user releases their right mouse button off of the
[GuiButton](/docs/reference/engine/classes/GuiButton).

GuiButton.MouseButton2Up(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels. |

This event fires when the user releases their right mouse button off of
the [GuiButton](/docs/reference/engine/classes/GuiButton).

For an event requiring the user to press and release their right mouse
on a [GuiButton](/docs/reference/engine/classes/GuiButton) in order for the event to fire, consider using
[MouseButton2Click](/docs/reference/engine/classes/GuiButton#MouseButton2Click).

Provide feedback

---

SecondaryActivated

GuiButton.SecondaryActivated(inputObject:[InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| inputObject:[InputObject](/docs/reference/engine/classes/InputObject) |

Provide feedback

---