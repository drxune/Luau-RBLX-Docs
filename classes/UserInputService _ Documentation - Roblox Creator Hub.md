# UserInputService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UserInputService
Scraped: 2026-01-11T02:33:42.424275Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- UserInputService
- InputObject
- TextBox
- Object
- LocalScript
- ModuleScript
- Script
- RunContext
- GetDeviceAcceleration()
- DeviceAccelerationChanged
- GetConnectedGamepads()
- PreferredInput
- GetDeviceRotation()
- DeviceRotationChanged
- IsKeyDown()
- GetKeysPressed()
- GetMouseDelta
- GuiButton
- Modal
- Visible
- InputChanged
- Mouse
- GetMouseDelta()
- GetMouseLocation()
- ImageButton
- TextButton
- ProximityPrompt
- MouseIconEnabled
- MouseEnabled
- OnScreenKeyboardVisible
- OnScreenKeyboardSize
- OnScreenKeyboardPosition
- TouchStarted
- TouchMoved
- VRService
- AccelerometerEnabled
- GyroscopeEnabled
- DeviceGravityChanged
- TextBox:CaptureFocus()
- InputObjects
- GetStringForKeyCode()
- InputObject.KeyCode
- MouseBehavior
- MouseDeltaSensitivity
- GuiService:GetGuiInset()
- GuiObject
- SetNavigationGamepad()
- IsNavigationGamepad()
- ImageLabel
- GetImageForKeyCode()
- GamepadSupports()
- InputBinding
- InputActions
- GuiObjects
- GetNavigationGamepads()
- RecenterUserHeadCFrame()
- UserInputType
- Position
- GetDeviceGravity()
- Delta
- GamepadDisconnected
- GamepadConnected
- InputEnded
- ScrollingFrame
- InputBegan
- Humanoid.Jump
- JumpRequest
- GetLastInputType()
- TextBoxFocusReleased
- GetFocusedTextBox()
- TextBox.Focused
- TextBox.FocusLost
- GuiObject.Transparency
- TextBoxFocused
- TouchEnabled
- TouchEnded
- TouchTapInWorld
- WindowFocusReleased
- WindowFocused
- RemoteEvent
- ForceField
- StarterPlayerScripts
- ServerScriptService
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [UserInputService](/docs/reference/engine/classes/UserInputService)

English

Feedback

Engine Class

UserInputService

UserInputService is primarily used to detect the input types available on a
user's device, as well as detect input events.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [AccelerometerEnabled](#AccelerometerEnabled):[boolean](/docs/luau/booleans) |
| [GamepadEnabled](#GamepadEnabled):[boolean](/docs/luau/booleans) |
| [GyroscopeEnabled](#GyroscopeEnabled):[boolean](/docs/luau/booleans) |
| [KeyboardEnabled](#KeyboardEnabled):[boolean](/docs/luau/booleans) |
| [ModalEnabled](#ModalEnabled):[boolean](/docs/luau/booleans)  Deprecated |
| [MouseBehavior](#MouseBehavior):[Enum.MouseBehavior](/docs/reference/engine/enums/MouseBehavior) |
| [MouseDeltaSensitivity](#MouseDeltaSensitivity):[number](/docs/luau/numbers) |
| [MouseEnabled](#MouseEnabled):[boolean](/docs/luau/booleans) |
| [MouseIcon](#MouseIcon):ContentId |
| [MouseIconContent](#MouseIconContent):[Content](/docs/reference/engine/datatypes/Content) |
| [MouseIconEnabled](#MouseIconEnabled):[boolean](/docs/luau/booleans) |
| [OnScreenKeyboardPosition](#OnScreenKeyboardPosition):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [OnScreenKeyboardSize](#OnScreenKeyboardSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [OnScreenKeyboardVisible](#OnScreenKeyboardVisible):[boolean](/docs/luau/booleans) |
| [PreferredInput](#PreferredInput):[Enum.PreferredInput](/docs/reference/engine/enums/PreferredInput) |
| [TouchEnabled](#TouchEnabled):[boolean](/docs/luau/booleans) |
| [TouchScreenEnabled](#TouchScreenEnabled):[boolean](/docs/luau/booleans) |
| [UserHeadCFrame](#UserHeadCFrame):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [VREnabled](#VREnabled):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GamepadSupports](#GamepadSupports)(gamepadNum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),gamepadKeyCode: [Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):[boolean](/docs/luau/booleans) |
| [GetConnectedGamepads](#GetConnectedGamepads)():[Array](/docs/luau/tables#arrays) |
| [GetDeviceAcceleration](#GetDeviceAcceleration)():[InputObject](/docs/reference/engine/classes/InputObject) |
| [GetDeviceGravity](#GetDeviceGravity)():[InputObject](/docs/reference/engine/classes/InputObject) |
| [GetDeviceRotation](#GetDeviceRotation)():[Tuple](/docs/luau/tuples) |
| [GetFocusedTextBox](#GetFocusedTextBox)():[TextBox](/docs/reference/engine/classes/TextBox) |
| [GetGamepadConnected](#GetGamepadConnected)(gamepadNum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans) |
| [GetGamepadState](#GetGamepadState)(gamepadNum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):Instances |
| [GetImageForKeyCode](#GetImageForKeyCode)(keyCode: [Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):ContentId |
| [GetKeysPressed](#GetKeysPressed)():Instances |
| [GetLastInputType](#GetLastInputType)():[Enum.UserInputType](/docs/reference/engine/enums/UserInputType) |
| [GetMouseButtonsPressed](#GetMouseButtonsPressed)():Instances |
| [GetMouseDelta](#GetMouseDelta)():[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [GetMouseLocation](#GetMouseLocation)():[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [GetNavigationGamepads](#GetNavigationGamepads)():[Array](/docs/luau/tables#arrays) |
| [GetStringForKeyCode](#GetStringForKeyCode)(keyCode: [Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):[string](/docs/luau/strings) |
| [GetSupportedGamepadKeyCodes](#GetSupportedGamepadKeyCodes)(gamepadNum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[Array](/docs/luau/tables#arrays) |
| [GetUserCFrame](#GetUserCFrame)(type: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [IsGamepadButtonDown](#IsGamepadButtonDown)(gamepadNum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),gamepadKeyCode: [Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):[boolean](/docs/luau/booleans) |
| [IsKeyDown](#IsKeyDown)(keyCode: [Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):[boolean](/docs/luau/booleans) |
| [IsMouseButtonPressed](#IsMouseButtonPressed)(mouseButton: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans) |
| [IsNavigationGamepad](#IsNavigationGamepad)(gamepadEnum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans) |
| [RecenterUserHeadCFrame](#RecenterUserHeadCFrame)():() |
| [SetNavigationGamepad](#SetNavigationGamepad)(gamepadEnum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),enabled: [boolean](/docs/luau/booleans)):() |

Events

|  |
| --- |
| [DeviceAccelerationChanged](#DeviceAccelerationChanged)(acceleration: [InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DeviceGravityChanged](#DeviceGravityChanged)(gravity: [InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DeviceRotationChanged](#DeviceRotationChanged)(rotation: [InputObject](/docs/reference/engine/classes/InputObject),cframe: [CFrame](/docs/reference/engine/datatypes/CFrame)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GamepadConnected](#GamepadConnected)(gamepadNum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GamepadDisconnected](#GamepadDisconnected)(gamepadNum: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [InputBegan](#InputBegan)(input: [InputObject](/docs/reference/engine/classes/InputObject),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [InputChanged](#InputChanged)(input: [InputObject](/docs/reference/engine/classes/InputObject),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [InputEnded](#InputEnded)(input: [InputObject](/docs/reference/engine/classes/InputObject),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [JumpRequest](#JumpRequest)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [LastInputTypeChanged](#LastInputTypeChanged)(lastInputType: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PointerAction](#PointerAction)(wheel: [number](/docs/luau/numbers),pan: [Vector2](/docs/reference/engine/datatypes/Vector2),pinch: [number](/docs/luau/numbers),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TextBoxFocused](#TextBoxFocused)(textboxFocused: [TextBox](/docs/reference/engine/classes/TextBox)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TextBoxFocusReleased](#TextBoxFocusReleased)(textboxReleased: [TextBox](/docs/reference/engine/classes/TextBox)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchDrag](#TouchDrag)(dragDirection: [Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection),numberOfTouches: [number](/docs/luau/numbers),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchEnded](#TouchEnded)(touch: [InputObject](/docs/reference/engine/classes/InputObject),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchLongPress](#TouchLongPress)(touchPositions: [Array](/docs/luau/tables#arrays),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchMoved](#TouchMoved)(touch: [InputObject](/docs/reference/engine/classes/InputObject),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchPan](#TouchPan)(touchPositions: [Array](/docs/luau/tables#arrays),totalTranslation: [Vector2](/docs/reference/engine/datatypes/Vector2),velocity: [Vector2](/docs/reference/engine/datatypes/Vector2),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchPinch](#TouchPinch)(touchPositions: [Array](/docs/luau/tables#arrays),scale: [number](/docs/luau/numbers),velocity: [number](/docs/luau/numbers),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchRotate](#TouchRotate)(touchPositions: [Array](/docs/luau/tables#arrays),rotation: [number](/docs/luau/numbers),velocity: [number](/docs/luau/numbers),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchStarted](#TouchStarted)(touch: [InputObject](/docs/reference/engine/classes/InputObject),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchSwipe](#TouchSwipe)(swipeDirection: [Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection),numberOfTouches: [number](/docs/luau/numbers),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchTap](#TouchTap)(touchPositions: [Array](/docs/luau/tables#arrays),gameProcessedEvent: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchTapInWorld](#TouchTapInWorld)(position: [Vector2](/docs/reference/engine/datatypes/Vector2),processedByUI: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [UserCFrameChanged](#UserCFrameChanged)(type: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame),value: [CFrame](/docs/reference/engine/datatypes/CFrame)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [WindowFocused](#WindowFocused)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WindowFocusReleased](#WindowFocusReleased)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

UserInputService is primarily used to detect the input types available on a
user's device, as well as detect input events. It allows you to perform
different actions depending on the device and, in turn, provide the best
experience for the end user.

As this service is intended for client-side usage only, its properties,
methods, and events can only be used in a [LocalScript](/docs/reference/engine/classes/LocalScript), a
[ModuleScript](/docs/reference/engine/classes/ModuleScript) required by a [LocalScript](/docs/reference/engine/classes/LocalScript), or a [Script](/docs/reference/engine/classes/Script)
with [RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client).

---

API Reference

Properties

AccelerometerEnabled

Read Only

Not Replicated

Read Parallel

Describes whether the user's device has an accelerometer.

UserInputService.AccelerometerEnabled:[boolean](/docs/luau/booleans)

This property describes whether the user's device has an accelerometer, a
component found in most mobile devices that measures acceleration (change
in speed).

If the device has an enabled accelerometer, you can get its current
acceleration by using the
[GetDeviceAcceleration()](/docs/reference/engine/classes/UserInputService#GetDeviceAcceleration)
method or track when the device's acceleration changes through the
[DeviceAccelerationChanged](/docs/reference/engine/classes/UserInputService#DeviceAccelerationChanged)
event.

Code Samples

Move a Ball using the Accelerometer

This code adds a force on a part so that it falls in the direction of actual
gravity relative to the user's device. In order for this example to work as
expected, it must be placed in a [LocalScript](/docs/reference/engine/classes/LocalScript) and the user's device
must have an accelerometer.

```
local Workspace = game:GetService("Workspace")



local UserInputService = game:GetService("UserInputService")



local ball = script.Parent:WaitForChild("Ball")



local mass = ball:GetMass()



local gravityForce = ball:WaitForChild("GravityForce")



local function moveBall(gravity)



gravityForce.Force = gravity.Position * Workspace.Gravity * mass



end



if UserInputService.AccelerometerEnabled then



UserInputService.DeviceGravityChanged:Connect(moveBall)



end
```

Provide feedback

---

GamepadEnabled

Read Only

Not Replicated

Read Parallel

Describes whether the user's device has an available gamepad.

UserInputService.GamepadEnabled:[boolean](/docs/luau/booleans)

This property describes whether the user's device has an available
gamepad. If true, you can use gamepad‑related methods such as
[GetConnectedGamepads()](/docs/reference/engine/classes/UserInputService#GetConnectedGamepads).

For seamless cross-platform compatibility on mixed-input devices, see
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) which more
accurately reflects which input (mouse/keyboard, touch, gamepad, etc.) the
player is likely using as the primary input.

Provide feedback

---

GyroscopeEnabled

Read Only

Not Replicated

Read Parallel

Describes whether the user's device has a gyroscope.

UserInputService.GyroscopeEnabled:[boolean](/docs/luau/booleans)

This property describes whether the user's device has a gyroscope, a
component found in most mobile devices that detects orientation and
rotational speed.

If the device has a gyroscope, you can incorporate it into your experience
using the [GetDeviceRotation()](/docs/reference/engine/classes/UserInputService#GetDeviceRotation)
method or track when the device's rotation changes through the
[DeviceRotationChanged](/docs/reference/engine/classes/UserInputService#DeviceRotationChanged)
event.

Provide feedback

---

KeyboardEnabled

Read Only

Not Replicated

Read Parallel

Describes whether the user's device has a keyboard available.

UserInputService.KeyboardEnabled:[boolean](/docs/luau/booleans)

This property describes whether the user's device has a keyboard
available. If true, you can use key‑related methods such as
[IsKeyDown()](/docs/reference/engine/classes/UserInputService#IsKeyDown) or
[GetKeysPressed()](/docs/reference/engine/classes/UserInputService#GetKeysPressed).

For seamless cross-platform compatibility on mixed-input devices, see
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) which more
accurately reflects which input (mouse/keyboard, touch, gamepad, etc.) the
player is likely using as the primary input.

Provide feedback

---

ModalEnabled

Deprecated

Show details

---

MouseBehavior

Read Parallel

Determines whether the user's mouse can be moved freely or is locked.

UserInputService.MouseBehavior:[Enum.MouseBehavior](/docs/reference/engine/enums/MouseBehavior)

This property sets how the user's mouse behaves based on the
[Enum.MouseBehavior](/docs/reference/engine/enums/MouseBehavior) enum. It can be set to three values:

* [Enum.MouseBehavior.Default](/docs/reference/engine/enums/MouseBehavior#Default) — The mouse moves freely around the
  user's screen.
* [Enum.MouseBehavior.LockCenter](/docs/reference/engine/enums/MouseBehavior#LockCenter) — The mouse is locked and cannot
  move from the center of the user's screen.
* [Enum.MouseBehavior.LockCurrentPosition](/docs/reference/engine/enums/MouseBehavior#LockCurrentPosition) — The mouse is locked and
  cannot move from its current position on the user's screen at the time
  of locking.

The value of this property does not affect the sensitivity of events
tracking mouse movement. For example,
[GetMouseDelta](/docs/reference/engine/classes/UserInputService#GetMouseDelta) returns the same
[Vector2](/docs/reference/engine/datatypes/Vector2) screen position in pixels regardless of whether the
mouse is locked or able to move freely around the user's screen. As a
result, default scripts like those controlling the camera are not impacted
by this property.

This property is overridden if a [GuiButton](/docs/reference/engine/classes/GuiButton) with
[Modal](/docs/reference/engine/classes/GuiButton#Modal) enabled is [Visible](/docs/reference/engine/classes/GuiButton#Visible)
unless the player's right mouse button is down.

Note that if the mouse is locked,
[InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged) will still fire when
the player moves the mouse and will pass in the delta that the mouse
attempted to move by. Additionally, if the player is kicked from the
experience, the mouse will be forcefully unlocked.

Provide feedback

---

MouseDeltaSensitivity

Not Replicated

Read Parallel

Scales the delta (change) output of the user's [Mouse](/docs/reference/engine/classes/Mouse).

UserInputService.MouseDeltaSensitivity:[number](/docs/luau/numbers)

This property determines the sensitivity of the user's [Mouse](/docs/reference/engine/classes/Mouse). It
can be used to adjust the sensitivity of events tracking mouse movement,
such as [GetMouseDelta()](/docs/reference/engine/classes/UserInputService#GetMouseDelta).

This property does not affect the movement of the mouse icon, nor the
camera sensitivity that the user has selected for their client.

This property has a maximum value of 10 and a minimum value of 0. When
sensitivity is 0, events that track the mouse's movement will still fire
but all parameters and properties indicating the change in mouse position
will return 0.

Provide feedback

---

MouseEnabled

Read Only

Not Replicated

Read Parallel

Describes whether the user's device has a mouse available.

UserInputService.MouseEnabled:[boolean](/docs/luau/booleans)

This property describes whether the user's device has a mouse available.
If true, you can use mouse‑related methods such as
[GetMouseLocation()](/docs/reference/engine/classes/UserInputService#GetMouseLocation).

For seamless cross-platform compatibility on mixed-input devices, see
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) which more
accurately reflects which input (mouse/keyboard, touch, gamepad, etc.) the
player is likely using as the primary input.

Provide feedback

---

MouseIcon

Read Parallel

The content ID of the image for the user's mouse icon.

UserInputService.MouseIcon:ContentId

This property determines the content ID of the image for the user's mouse
icon. If blank, a default arrow pointer is used. While the cursor hovers
over certain UI objects such as an [ImageButton](/docs/reference/engine/classes/ImageButton),
[TextButton](/docs/reference/engine/classes/TextButton), [TextBox](/docs/reference/engine/classes/TextBox), or [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt), this
image will be overridden and temporarily ignored.

To hide the cursor entirely, do not use a transparent image; instead,
set [MouseIconEnabled](/docs/reference/engine/classes/UserInputService#MouseIconEnabled) to false.

Code Samples

Custom Mouse Icon

This example changes the user mouse icon to look like a dragon image.

```
local UserInputService = game:GetService("UserInputService")



-- In order to restore the cursor to what it was set to previously, it will need to be saved to a variable



local savedCursor = nil



local function setTemporaryCursor(cursor: string)



-- Only update the saved cursor if it's not currently saved



if not savedCursor then



savedCursor = UserInputService.MouseIcon



end



UserInputService.MouseIcon = cursor



end



local function clearTemporaryCursor()



-- Only restore the mouse cursor if there's a saved cursor to restore



if savedCursor then



UserInputService.MouseIcon = savedCursor



-- Don't restore the same cursor twice (might overwrite another script)



savedCursor = nil



end



end



setTemporaryCursor("http://www.roblox.com/asset?id=163023520")



print(UserInputService.MouseIcon)



clearTemporaryCursor()
```

Provide feedback

---

MouseIconContent

Read Parallel

The content ID of the image for the user's mouse icon. Only supports asset
URIs.

UserInputService.MouseIconContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines the content ID of the image for the user's mouse
icon. If blank, a default arrow pointer is used. While the cursor hovers
over certain UI objects such as an [ImageButton](/docs/reference/engine/classes/ImageButton),
[TextButton](/docs/reference/engine/classes/TextButton), [TextBox](/docs/reference/engine/classes/TextBox), or [ProximityPrompt](/docs/reference/engine/classes/ProximityPrompt), this
image will be overridden and temporarily ignored. Only asset URIs are
supported for this property.

To hide the cursor entirely, do not use a transparent image; instead,
set [MouseIconEnabled](/docs/reference/engine/classes/UserInputService#MouseIconEnabled) to false.

Code Samples

Custom Mouse Icon

This example changes the user mouse icon to look like a dragon image.

```
local UserInputService = game:GetService("UserInputService")



-- In order to restore the cursor to what it was set to previously, it will need to be saved to a variable



local savedCursor = nil



local function setTemporaryCursor(cursor: string)



-- Only update the saved cursor if it's not currently saved



if not savedCursor then



savedCursor = UserInputService.MouseIcon



end



UserInputService.MouseIcon = cursor



end



local function clearTemporaryCursor()



-- Only restore the mouse cursor if there's a saved cursor to restore



if savedCursor then



UserInputService.MouseIcon = savedCursor



-- Don't restore the same cursor twice (might overwrite another script)



savedCursor = nil



end



end



setTemporaryCursor("http://www.roblox.com/asset?id=163023520")



print(UserInputService.MouseIcon)



clearTemporaryCursor()
```

Provide feedback

---

MouseIconEnabled

Read Parallel

Determines whether the mouse icon is visible.

UserInputService.MouseIconEnabled:[boolean](/docs/luau/booleans)

This property determines whether the mouse icon is visible. To detect when
this property changes, you must listen to when the
[MouseEnabled](/docs/reference/engine/classes/UserInputService#MouseEnabled) property changes.

Provide feedback

---

OnScreenKeyboardPosition

Read Only

Not Replicated

Read Parallel

Determines the position of the on-screen keyboard.

UserInputService.OnScreenKeyboardPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property describes the position of the on-screen keyboard in pixels.
The keyboard's position is [Vector2.new(0, 0)](/docs/reference/engine/datatypes/Vector2) when it is
not visible.

See also
[OnScreenKeyboardVisible](/docs/reference/engine/classes/UserInputService#OnScreenKeyboardVisible)
and [OnScreenKeyboardSize](/docs/reference/engine/classes/UserInputService#OnScreenKeyboardSize).

Provide feedback

---

OnScreenKeyboardSize

Read Only

Not Replicated

Read Parallel

Determines the size of the on-screen keyboard.

UserInputService.OnScreenKeyboardSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property describes the size of the on-screen keyboard in pixels. The
keyboard's size is [Vector2.new(0, 0)](/docs/reference/engine/datatypes/Vector2) when it is not
visible.

See also
[OnScreenKeyboardVisible](/docs/reference/engine/classes/UserInputService#OnScreenKeyboardVisible)
and
[OnScreenKeyboardPosition](/docs/reference/engine/classes/UserInputService#OnScreenKeyboardPosition).

Provide feedback

---

OnScreenKeyboardVisible

Read Only

Not Replicated

Read Parallel

Describes whether an on-screen keyboard is currently visible on the user's
screen.

UserInputService.OnScreenKeyboardVisible:[boolean](/docs/luau/booleans)

This property describes whether an on-screen keyboard is currently visible
on the user's screen.

See also
[OnScreenKeyboardSize](/docs/reference/engine/classes/UserInputService#OnScreenKeyboardSize) and
[OnScreenKeyboardPosition](/docs/reference/engine/classes/UserInputService#OnScreenKeyboardPosition).

Provide feedback

---

PreferredInput

Read Only

Not Replicated

Read Parallel

Queries the primary input type a player is using, based on anticipated
user behavior.

UserInputService.PreferredInput:[Enum.PreferredInput](/docs/reference/engine/enums/PreferredInput)

This read-only property lets you query the primary input type a player
is likely using, based on anticipated user behavior, to ensure UI elements
like on‑screen buttons and menus work elegantly across devices. For
example, a touch‑enabled device assumes touch is the default input and
that touch buttons may appear for actions, but if a player connects an
additional bluetooth keyboard/mouse or gamepad, you can assume they want
to switch to that as the primary input type and possibly use touch as a
backup input for on‑screen UI.

The value of PreferredInput changes based on built‑in device inputs and
the player's most recent interaction with a connected gamepad or
keyboard/mouse. Examples include:

| Real-World Scenario | PreferredInput |
| --- | --- |
| Player is using a phone with no other connected input devices; no possibility of an input type change. | [Touch](/docs/reference/engine/enums/PreferredInput) |
| Player is using a mobile device with a bluetooth keyboard & mouse connected, but no gamepad is connected. | [KeyboardAndMouse](/docs/reference/engine/enums/PreferredInput) |
| Player is using a tablet with a bluetooth gamepad connected, but no keyboard or mouse is connected. | [Gamepad](/docs/reference/engine/enums/PreferredInput) |
| Player is using an Xbox or PlayStation with a bluetooth keyboard & mouse connected and has most recently interacted with the keyboard or mouse. | [KeyboardAndMouse](/docs/reference/engine/enums/PreferredInput) |
| Player is on a Windows or Mac PC with a gamepad connected and has most recently interacted with the gamepad. | [Gamepad](/docs/reference/engine/enums/PreferredInput) |

Code Samples

Preferred Input Detection

The following [LocalScript](/docs/reference/engine/classes/LocalScript) is a template for initially detecting the preferred input and responding to changes during gameplay.

```
local UserInputService = game:GetService("UserInputService")



local function preferredInputChanged()



local preferredInput = UserInputService.PreferredInput



if preferredInput == Enum.PreferredInput.Touch then



-- Player is on touch-enabled device with no other input types available/connected



print("Touch")



elseif preferredInput == Enum.PreferredInput.Gamepad then



-- Player has connected or most recently interacted with a gamepad



print("Gamepad")



elseif preferredInput == Enum.PreferredInput.KeyboardAndMouse then



-- Player has connected or most recently interacted with a keyboard or mouse



print("KeyboardAndMouse")



end



end



preferredInputChanged()



UserInputService:GetPropertyChangedSignal("PreferredInput"):Connect(function()



preferredInputChanged()



end)
```

Provide feedback

---

TouchEnabled

Read Only

Not Replicated

Read Parallel

Describes whether the user's device has a touch screen available.

UserInputService.TouchEnabled:[boolean](/docs/luau/booleans)

This property describes whether the user's device has a touch screen
available. If true, you can use touch‑related events such as
[TouchStarted](/docs/reference/engine/classes/UserInputService#TouchStarted) and
[TouchMoved](/docs/reference/engine/classes/UserInputService#TouchMoved).

For seamless cross-platform compatibility on mixed-input devices, see
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) which more
accurately reflects which input (mouse/keyboard, touch, gamepad, etc.) the
player is likely using as the primary input.

Provide feedback

---

TouchScreenEnabled

Read Only

Not Replicated

Roblox Script Security

Read Parallel

UserInputService.TouchScreenEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

UserHeadCFrame

Deprecated

Show details

---

VREnabled

Read Only

Not Replicated

Read Parallel

Indicates whether the user is using a virtual reality headset.

UserInputService.VREnabled:[boolean](/docs/luau/booleans)

This property describes whether the user is using a virtual reality (VR)
device. If true, you can use VR‑related properties, methods, and events
in [VRService](/docs/reference/engine/classes/VRService).

Provide feedback

---

Methods

GamepadSupports

Returns whether the given [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) gamepad supports a button
corresponding with the given [Enum.KeyCode](/docs/reference/engine/enums/KeyCode).

UserInputService:GamepadSupports(

gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), gamepadKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the gamepad. |
| gamepadKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)  The [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) of the button in question. |

Returns

[boolean](/docs/luau/booleans)

Whether the given gamepad supports a button corresponding with the
given [Enum.KeyCode](/docs/reference/engine/enums/KeyCode).

This method returns whether the given [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) gamepad
supports a button corresponding with the given [Enum.KeyCode](/docs/reference/engine/enums/KeyCode).

Provide feedback

---

GetConnectedGamepads

Returns an array of [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) gamepads currently connected.

UserInputService:GetConnectedGamepads():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of [UserInputTypes](/docs/reference/engine/enums/UserInputType) corresponding with the
gamepads connected to the user's device.

This method returns an array of [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) gamepads currently
connected. If no gamepads are connected, the array will be empty.

Alternatively to detecting all gamepads, the
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) property can be
used to more accurately reflect which input (mouse/keyboard, touch,
gamepad, etc.) the player is likely using as the primary input.

Provide feedback

---

GetDeviceAcceleration

Returns an [InputObject](/docs/reference/engine/classes/InputObject) that describes the device's current
acceleration.

UserInputService:GetDeviceAcceleration():[InputObject](/docs/reference/engine/classes/InputObject)

Returns

[InputObject](/docs/reference/engine/classes/InputObject)

This method returns an [InputObject](/docs/reference/engine/classes/InputObject) that describes the device's
current acceleration. For this to function, the user's device must have an
enabled accelerometer as queried through the
[AccelerometerEnabled](/docs/reference/engine/classes/UserInputService#AccelerometerEnabled)
property.

To track when the device's acceleration changes, use the
[DeviceAccelerationChanged](/docs/reference/engine/classes/UserInputService#DeviceAccelerationChanged)
event.

Code Samples

Output Device Acceleration

This example checks if a user's device has an enabled accelerometer and, if
true, it outputs the current acceleration.

```
local UserInputService = game:GetService("UserInputService")



if UserInputService.AccelerometerEnabled then



local acceleration = UserInputService:GetDeviceAcceleration().Position



print(acceleration)



else



warn("Cannot get device acceleration because device does not have an enabled accelerometer!")



end
```

Provide feedback

---

GetDeviceGravity

Returns an [InputObject](/docs/reference/engine/classes/InputObject) describing the device's current gravity
vector.

UserInputService:GetDeviceGravity():[InputObject](/docs/reference/engine/classes/InputObject)

Returns

[InputObject](/docs/reference/engine/classes/InputObject)

This method returns an [InputObject](/docs/reference/engine/classes/InputObject) describing the device's current
gravity vector. The vector is determined by the device's orientation
relative to the real-world force of gravity. For example:

* [Vector3.new(0, 0, -9.18)](/docs/reference/engine/datatypes/Vector3) if the device is perfectly
  upright (portrait)
* [Vector3.new(9.81, 0, 0)](/docs/reference/engine/datatypes/Vector3) if the left side of the
  device is pointing down
* [Vector3.new(0, -9.81, 0)](/docs/reference/engine/datatypes/Vector3) if the back of the device is
  pointing down

Gravity is only tracked for devices with an enabled gyroscope as queried
through [GyroscopeEnabled](/docs/reference/engine/classes/UserInputService#GyroscopeEnabled).

To track when the device's gravity changes, use the
[DeviceGravityChanged](/docs/reference/engine/classes/UserInputService#DeviceGravityChanged) event.

Code Samples

Moving Objects with the Gyroscope

This example implements a level where the bubble will move along the X and
Z axes depending on the device's current gryoscope position.

```
local UserInputService = game:GetService("UserInputService")



local bubble = script.Parent:WaitForChild("Bubble")



local camera = workspace.CurrentCamera



camera.CameraType = Enum.CameraType.Scriptable



camera.CFrame = CFrame.new(0, 20, 0) * CFrame.Angles(-math.pi / 2, 0, 0)



if UserInputService.GyroscopeEnabled then



-- Bind event to when gyroscope detects change



UserInputService.DeviceGravityChanged:Connect(function(accel)



-- Move the bubble in the world based on the gyroscope data



bubble.Position = Vector3.new(-8 * accel.Position.X, 1.8, -8 * accel.Position.Z)



end)



end
```

Provide feedback

---

GetDeviceRotation

Returns an [InputObject](/docs/reference/engine/classes/InputObject) and a [CFrame](/docs/reference/engine/datatypes/CFrame) describing the
device's current rotation vector.

UserInputService:GetDeviceRotation():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

A tuple containing two properties: The delta describing the amount of
rotation that last happened, and the [CFrame](/docs/reference/engine/datatypes/CFrame) of the device's
current rotation relative to its default reference frame.

This method returns an [InputObject](/docs/reference/engine/classes/InputObject) and a [CFrame](/docs/reference/engine/datatypes/CFrame)
describing the device's current rotation vector.

Device rotation is only tracked for devices with an enabled gyroscope as
queried through
[GyroscopeEnabled](/docs/reference/engine/classes/UserInputService#GyroscopeEnabled).

Code Samples

Output Device Rotation

This example checks if a user's device has an enabled gyroscope and, if
true, it outputs the device's current [CFrame](/docs/reference/engine/datatypes/CFrame).

```
local UserInputService = game:GetService("UserInputService")



if UserInputService.GyroscopeEnabled then



local _, cf = UserInputService:GetDeviceRotation()



print(cf)



else



warn("Cannot get device rotation because device does not have an enabled gyroscope!")



end
```

Provide feedback

---

GetFocusedTextBox

Returns the currently [TextBox](/docs/reference/engine/classes/TextBox) the client is currently focused on.

UserInputService:GetFocusedTextBox():[TextBox](/docs/reference/engine/classes/TextBox)

Returns

[TextBox](/docs/reference/engine/classes/TextBox)

This method returns the [TextBox](/docs/reference/engine/classes/TextBox) the client is currently focused
on. A [TextBox](/docs/reference/engine/classes/TextBox) can be manually selected by the user, or selection
can be forced using the [TextBox:CaptureFocus()](/docs/reference/engine/classes/TextBox#CaptureFocus) method. If no
[TextBox](/docs/reference/engine/classes/TextBox) is selected, this method will return nil.

Provide feedback

---

GetGamepadConnected

Returns whether a gamepad with the given [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) is
connected.

UserInputService:GetGamepadConnected(gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the gamepad in question. |

Returns

[boolean](/docs/luau/booleans)

Whether a gamepad associated with [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) is connected.

This method returns whether a gamepad with the given [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)
is connected.

Alternatively to detecting a specific gamepad by [Enum.UserInputType](/docs/reference/engine/enums/UserInputType), the
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) property can be
used to more accurately reflect which input (mouse/keyboard, touch,
gamepad, etc.) the player is likely using as the primary input.

Provide feedback

---

GetGamepadState

Returns an array of [InputObjects](/docs/reference/engine/classes/InputObject) for all available
inputs on the given gamepad, representing each input's last input state.

UserInputService:GetGamepadState(gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):Instances

Parameters

|  |
| --- |
| gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) corresponding with the gamepad in question. |

Returns

Instances

An array of [InputObjects](/docs/reference/engine/classes/InputObject) representing the current
state of all available inputs for the given gamepad.

This method returns an array of [InputObjects](/docs/reference/engine/classes/InputObject) for all
available inputs on the given [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) gamepad, representing
each input's last input state.

Provide feedback

---

GetImageForKeyCode

Returns an image for the requested [Enum.KeyCode](/docs/reference/engine/enums/KeyCode).

UserInputService:GetImageForKeyCode(keyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):ContentId

Parameters

|  |
| --- |
| keyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)  The [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for which to fetch the associated image. |

Returns

ContentId

The returned image asset ID.

This method takes the requested [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) and returns the associated
image for the currently connected gamepad device (limited to Xbox,
PlayStation, and Windows). This means that if the connected controller is
an Xbox One controller, the user sees Xbox assets. Similarly, if the
connected device is a PlayStation controller, the user sees PlayStation
assets. If you want to use custom assets, see
[GetStringForKeyCode()](/docs/reference/engine/classes/UserInputService#GetStringForKeyCode).

Code Samples

UserInputService - Get Image For KeyCode

This API returns the requested image for the given [Enum.KeyCode](/docs/reference/engine/enums/KeyCode).

```
local UserInputService = game:GetService("UserInputService")



local imageLabel = script.Parent



local key = Enum.KeyCode.ButtonA



local mappedIconImage = UserInputService:GetImageForKeyCode(key)



imageLabel.Image = mappedIconImage
```

Provide feedback

---

GetKeysPressed

Returns an array of [InputObjects](/docs/reference/engine/classes/InputObject) associated with the
[keys](/docs/reference/engine/enums/KeyCode) currently being pressed down.

UserInputService:GetKeysPressed():Instances

Returns

Instances

An array of [InputObjects](/docs/reference/engine/classes/InputObject) associated with the keys
currently being pressed.

This method returns an array of [InputObjects](/docs/reference/engine/classes/InputObject)
associated with the keys currently being pressed down. The array can be
iterated through to determine which keys are currently being pressed,
using the [InputObject.KeyCode](/docs/reference/engine/classes/InputObject#KeyCode) names or values.

To check if a specific key is being pressed, use
[IsKeyDown()](/docs/reference/engine/classes/UserInputService#IsKeyDown).

Provide feedback

---

GetLastInputType

Returns the [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) associated with the user's most recent
input.

UserInputService:GetLastInputType():[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)

Returns

[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)

The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) associated with the user's most recent input.

This method returns the [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) associated with the user's
most recent input. For example, if the user's previous input had been
pressing the A key, the returned [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) value
would be [Keyboard](/docs/reference/engine/enums/UserInputType).

For seamless cross-platform compatibility on mixed-input devices, see
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) which more
accurately reflects which input (mouse/keyboard, touch, gamepad, etc.) the
player is likely using as the primary input. GetLastInputType()
remains for advanced workflows or control schemes that rely on detecting
and responding to the player's specific most recent [Enum.UserInputType](/docs/reference/engine/enums/UserInputType).

Code Samples

Detect Last Input Type

This example gets the last [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) and outputs if it was keyboard
input.

```
local UserInputService = game:GetService("UserInputService")



if UserInputService:GetLastInputType() == Enum.UserInputType.Keyboard then



print("Most recent input was keyboard!")



end
```

Provide feedback

---

GetMouseButtonsPressed

Returns an array of [InputObjects](/docs/reference/engine/classes/InputObject) associated with the
mouse buttons currently being held down.

UserInputService:GetMouseButtonsPressed():Instances

Returns

Instances

An array of [InputObjects](/docs/reference/engine/classes/InputObject) corresponding to the
mouse buttons currently being currently held down.

This method returns an array of [InputObjects](/docs/reference/engine/classes/InputObject)
associated with the mouse buttons currently being held down. The array can
be iterated through to determine which buttons are currently being held,
using the [InputObject.KeyCode](/docs/reference/engine/classes/InputObject#KeyCode) names or values.

Mouse buttons that are tracked by this method include MouseButton1
(left), MouseButton2 (right), and MouseButton3 (middle).

If the user is not pressing any mouse button down when the method is
called, it will return an empty array.

Code Samples

Check Pressed Mouse Buttons

This example checks if the user pressed MouseButton1 (left), MouseButton2
(right), or both mouse buttons. This can be extended to behave differently
depending on which mouse buttons are pressed, including MouseButton3
(middle).

```
local UserInputService = game:GetService("UserInputService")



UserInputService.InputBegan:Connect(function(input, gameProcessedEvent)



-- Return an array of the pressed mouse buttons



local buttonsPressed = UserInputService:GetMouseButtonsPressed()



local m1, m2 = false, false



for _, button in buttonsPressed do



if button.UserInputType == Enum.UserInputType.MouseButton1 then



print("MouseButton1 pressed!")



m1 = true



end



if button.UserInputType == Enum.UserInputType.MouseButton2 then



print("MouseButton2 pressed!")



m2 = true



end



if m1 and m2 then



print("Both mouse buttons pressed!")



end



end



end)
```

Provide feedback

---

GetMouseDelta

Returns the change, in pixels, of the position of the player's
[Mouse](/docs/reference/engine/classes/Mouse) in the last rendered frame. Only works if the mouse is
locked.

UserInputService:GetMouseDelta():[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

Change in movement of the mouse.

This method returns the change, in pixels, of the position of the player's
[Mouse](/docs/reference/engine/classes/Mouse) in the last rendered frame, only if the mouse has been
locked using the [MouseBehavior](/docs/reference/engine/classes/UserInputService#MouseBehavior)
property; otherwise the returned [Vector2](/docs/reference/engine/datatypes/Vector2) values will be 0.

The sensitivity of the mouse, determined in the client's settings and
[MouseDeltaSensitivity](/docs/reference/engine/classes/UserInputService#MouseDeltaSensitivity), will
influence the result.

Code Samples

Getting Mouse Delta

The following example measures any mouse movement in pixels from the last
render step to the current render step. If the user has set their camera
sensitivity to be higher or lower than 1 in the experience's menu, it will
affect the returned value.

```
local RunService = game:GetService("RunService")



local UserInputService = game:GetService("UserInputService")



UserInputService.MouseBehavior = Enum.MouseBehavior.LockCenter



local function onRenderStep()



local delta = UserInputService:GetMouseDelta()



if delta ~= Vector2.new(0, 0) then



print("The mouse has moved", delta, "since the last step")



end



end



RunService:BindToRenderStep("MeasureMouseMovement", Enum.RenderPriority.Input.Value, onRenderStep)
```

Provide feedback

---

GetMouseLocation

Returns the current screen location of the player's [Mouse](/docs/reference/engine/classes/Mouse) relative
to the top-left corner of the screen.

UserInputService:GetMouseLocation():[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

A [Vector2](/docs/reference/engine/datatypes/Vector2) representing the current screen location of the
mouse, in pixels.

This method returns a [Vector2](/docs/reference/engine/datatypes/Vector2) representing the current screen
location of the player's [Mouse](/docs/reference/engine/classes/Mouse) in pixels relative to the top‑left
corner. This does not account for the [Enum.ScreenInsets](/docs/reference/engine/enums/ScreenInsets); to get the
top‑left and bottom‑right insets, call [GuiService:GetGuiInset()](/docs/reference/engine/classes/GuiService#GetGuiInset).

If the location of the mouse pointer is offscreen or the player's device
does not have a mouse, the returned value will be undetermined.

Provide feedback

---

GetNavigationGamepads

Returns an array of gamepads connected and enabled for [GuiObject](/docs/reference/engine/classes/GuiObject)
navigation in descending order of priority.

UserInputService:GetNavigationGamepads():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of [UserInputTypes](/docs/reference/engine/enums/UserInputType) that can be used for
navigation, in descending order of priority.

This method returns an array of gamepads that are connected and enabled
for [GuiObject](/docs/reference/engine/classes/GuiObject) navigation, but does not influence navigation
controls. This list is in descending order of priority, meaning it can be
iterated over to determine which gamepad should have navigation control.

See also
[SetNavigationGamepad()](/docs/reference/engine/classes/UserInputService#SetNavigationGamepad),
[IsNavigationGamepad()](/docs/reference/engine/classes/UserInputService#IsNavigationGamepad), and
[GetConnectedGamepads()](/docs/reference/engine/classes/UserInputService#GetConnectedGamepads).

Provide feedback

---

GetStringForKeyCode

Returns a string representing a key the user should press in order to
input a given [Enum.KeyCode](/docs/reference/engine/enums/KeyCode).

UserInputService:GetStringForKeyCode(keyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| keyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |

Returns

[string](/docs/luau/strings)

This method returns a string representing a key the user should press in
order to input a given [Enum.KeyCode](/docs/reference/engine/enums/KeyCode), keeping in mind their keyboard
layout. For key codes that require some modifier to be held, this method
returns the key to be pressed in addition to the modifier. See the
examples below for further explanation.

When using Roblox with a non‑QWERTY keyboard layout, key codes are mapped
to equivalent QWERTY positions. For example, pressing A on an
AZERTY keyboard results in [Enum.KeyCode.Q](/docs/reference/engine/enums/KeyCode#Q), potentially leading to
mismatched information on experience UI elements. This method solves the
issue by providing the actual key to be pressed while using non‑QWERTY
keyboard layouts.

| KeyCode | QWERTY Return | AZERTY Return |
| --- | --- | --- |
| [Enum.KeyCode.Q](/docs/reference/engine/enums/KeyCode#Q) | Q | A |
| [Enum.KeyCode.W](/docs/reference/engine/enums/KeyCode#W) | W | Z |
| [Enum.KeyCode.Equals](/docs/reference/engine/enums/KeyCode#Equals) | = | = |
| [Enum.KeyCode.At](/docs/reference/engine/enums/KeyCode#At) | 2 because @ is typed with Shift2 | É |

#### Gamepad Usage

GetStringForKeyCode() returns the string mapping for the [Enum.KeyCode](/docs/reference/engine/enums/KeyCode)
for the most recently connected gamepad. If the connected controller is
not supported, the method returns the default string conversion for the
requested key code.

The following example shows how you can map custom assets for
[ButtonA](/docs/reference/engine/enums/KeyCode#ButtonA):

```
local UserInputService = game:GetService("UserInputService")



local imageLabel = script.Parent



local key = Enum.KeyCode.ButtonA



local mappings = {



ButtonA = "rbxasset://BUTTON_A_ASSET", -- Replace with the desired ButtonA asset



ButtonCross = "rbxasset://BUTTON_CROSS_ASSET"  -- Replace with the desired ButtonCross asset



}



local mappedKey = UserInputService:GetStringForKeyCode(key)



local image = mappings[mappedKey]



imageLabel.Image = image
```

#### Gamepad Mappings

The directional pad key codes do not have any differences based on device.
[Enum.KeyCode.ButtonSelect](/docs/reference/engine/enums/KeyCode#ButtonSelect) has slightly different behavior in some cases.
Use both PlayStation mappings to ensure users see the correct buttons.

| KeyCode | PlayStation Return Value | Xbox Return Value |
| --- | --- | --- |
| [Enum.KeyCode.ButtonA](/docs/reference/engine/enums/KeyCode#ButtonA) | ButtonCross | ButtonA |
| [Enum.KeyCode.ButtonB](/docs/reference/engine/enums/KeyCode#ButtonB) | ButtonCircle | ButtonB |
| [Enum.KeyCode.ButtonX](/docs/reference/engine/enums/KeyCode#ButtonX) | ButtonSquare | ButtonX |
| [Enum.KeyCode.ButtonY](/docs/reference/engine/enums/KeyCode#ButtonY) | ButtonTriangle | ButtonY |
| [Enum.KeyCode.ButtonL1](/docs/reference/engine/enums/KeyCode#ButtonL1) | ButtonL1 | ButtonLB |
| [Enum.KeyCode.ButtonL2](/docs/reference/engine/enums/KeyCode#ButtonL2) | ButtonL2 | ButtonLT |
| [Enum.KeyCode.ButtonL3](/docs/reference/engine/enums/KeyCode#ButtonL3) | ButtonL3 | ButtonLS |
| [Enum.KeyCode.ButtonR1](/docs/reference/engine/enums/KeyCode#ButtonR1) | ButtonR1 | ButtonRB |
| [Enum.KeyCode.ButtonR2](/docs/reference/engine/enums/KeyCode#ButtonR2) | ButtonR2 | ButtonRT |
| [Enum.KeyCode.ButtonR3](/docs/reference/engine/enums/KeyCode#ButtonR3) | ButtonR3 | ButtonRS |
| [Enum.KeyCode.ButtonStart](/docs/reference/engine/enums/KeyCode#ButtonStart) | ButtonOptions | ButtonStart |
| [Enum.KeyCode.ButtonSelect](/docs/reference/engine/enums/KeyCode#ButtonSelect) | ButtonTouchpad and ButtonShare | ButtonSelect |

#### Legacy System Images

When using a [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) that may be better represented as an image,
such as for an [ImageLabel](/docs/reference/engine/classes/ImageLabel) in a user interface, you can use the
following legacy icons. However, it's recommended that you use
[GetImageForKeyCode()](/docs/reference/engine/classes/UserInputService#GetImageForKeyCode) as a
more modern, cross‑platform method to retrieve Xbox and PlayStation
controller icons.

| KeyCode | Asset ID |
| --- | --- |
| [Enum.KeyCode.ButtonX](/docs/reference/engine/enums/KeyCode#ButtonX) | rbxasset://textures/ui/Controls/xboxX.png |
| [Enum.KeyCode.ButtonY](/docs/reference/engine/enums/KeyCode#ButtonY) | rbxasset://textures/ui/Controls/xboxY.png |
| [Enum.KeyCode.ButtonA](/docs/reference/engine/enums/KeyCode#ButtonA) | rbxasset://textures/ui/Controls/xboxA.png |
| [Enum.KeyCode.ButtonB](/docs/reference/engine/enums/KeyCode#ButtonB) | rbxasset://textures/ui/Controls/xboxB.png |
| [Enum.KeyCode.DPadLeft](/docs/reference/engine/enums/KeyCode#DPadLeft) | rbxasset://textures/ui/Controls/dpadLeft.png |
| [Enum.KeyCode.DPadRight](/docs/reference/engine/enums/KeyCode#DPadRight) | rbxasset://textures/ui/Controls/dpadRight.png |
| [Enum.KeyCode.DPadUp](/docs/reference/engine/enums/KeyCode#DPadUp) | rbxasset://textures/ui/Controls/dpadUp.png |
| [Enum.KeyCode.DPadDown](/docs/reference/engine/enums/KeyCode#DPadDown) | rbxasset://textures/ui/Controls/dpadDown.png |
| [Enum.KeyCode.ButtonSelect](/docs/reference/engine/enums/KeyCode#ButtonSelect) | rbxasset://textures/ui/Controls/xboxView.png |
| [Enum.KeyCode.ButtonStart](/docs/reference/engine/enums/KeyCode#ButtonStart) | rbxasset://textures/ui/Controls/xboxmenu.png |
| [Enum.KeyCode.ButtonL1](/docs/reference/engine/enums/KeyCode#ButtonL1) | rbxasset://textures/ui/Controls/xboxLB.png |
| [Enum.KeyCode.ButtonR1](/docs/reference/engine/enums/KeyCode#ButtonR1) | rbxasset://textures/ui/Controls/xboxRB.png |
| [Enum.KeyCode.ButtonL2](/docs/reference/engine/enums/KeyCode#ButtonL2) | rbxasset://textures/ui/Controls/xboxLT.png |
| [Enum.KeyCode.ButtonR2](/docs/reference/engine/enums/KeyCode#ButtonR2) | rbxasset://textures/ui/Controls/xboxRT.png |
| [Enum.KeyCode.ButtonL3](/docs/reference/engine/enums/KeyCode#ButtonL3) | rbxasset://textures/ui/Controls/xboxLS.png |
| [Enum.KeyCode.ButtonR3](/docs/reference/engine/enums/KeyCode#ButtonR3) | rbxasset://textures/ui/Controls/xboxRS.png |
| [Enum.KeyCode.Thumbstick1](/docs/reference/engine/enums/KeyCode#Thumbstick1) | rbxasset://textures/ui/Controls/xboxLSDirectional.png |
| [Enum.KeyCode.Thumbstick2](/docs/reference/engine/enums/KeyCode#Thumbstick2) | rbxasset://textures/ui/Controls/xboxRSDirectional.png |
| [Enum.KeyCode.Backspace](/docs/reference/engine/enums/KeyCode#Backspace) | rbxasset://textures/ui/Controls/backspace.png |
| [Enum.KeyCode.Return](/docs/reference/engine/enums/KeyCode#Return) | rbxasset://textures/ui/Controls/return.png |
| [Enum.KeyCode.LeftShift](/docs/reference/engine/enums/KeyCode#LeftShift) | rbxasset://textures/ui/Controls/shift.png |
| [Enum.KeyCode.RightShift](/docs/reference/engine/enums/KeyCode#RightShift) | rbxasset://textures/ui/Controls/shift.png |
| [Enum.KeyCode.Tab](/docs/reference/engine/enums/KeyCode#Tab) | rbxasset://textures/ui/Controls/tab.png |
| [Enum.KeyCode.Quote](/docs/reference/engine/enums/KeyCode#Quote) | rbxasset://textures/ui/Controls/apostrophe.png |
| [Enum.KeyCode.Comma](/docs/reference/engine/enums/KeyCode#Comma) | rbxasset://textures/ui/Controls/comma.png |
| [Enum.KeyCode.Backquote](/docs/reference/engine/enums/KeyCode#Backquote) | rbxasset://textures/ui/Controls/graveaccent.png |
| [Enum.KeyCode.Period](/docs/reference/engine/enums/KeyCode#Period) | rbxasset://textures/ui/Controls/period.png |
| [Enum.KeyCode.Space](/docs/reference/engine/enums/KeyCode#Space) | rbxasset://textures/ui/Controls/spacebar.png |

Provide feedback

---

GetSupportedGamepadKeyCodes

Returns an array of [KeyCodes](/docs/reference/engine/enums/KeyCode) that the gamepad associated
with the given [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) supports.

UserInputService:GetSupportedGamepadKeyCodes(gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the gamepad. |

Returns

[Array](/docs/luau/tables#arrays)

An array of [KeyCodes](/docs/reference/engine/enums/KeyCode) supported by the given gamepad.

This method returns an array of [KeyCodes](/docs/reference/engine/enums/KeyCode) that the gamepad
associated with the given [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) supports. If called on a
non‑connected gamepad, returns an empty array.

To determine if a specific [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) is supported, use
[GamepadSupports()](/docs/reference/engine/classes/UserInputService#GamepadSupports).

Provide feedback

---

GetUserCFrame

Deprecated

Show details

---

IsGamepadButtonDown

Determines whether a particular button is pressed on a gamepad.

UserInputService:IsGamepadButtonDown(

gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), gamepadKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the given gamepad. |
| gamepadKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)  The [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) of the specified gamepad button. |

Returns

[boolean](/docs/luau/booleans)

Whether the specified button on the given gamepad is pressed is
pressed.

This method returns true if a particular button is pressed on a gamepad,
otherwise returns false.

See also [InputBinding](/docs/reference/engine/classes/InputBinding) as a way to hook gamepad and other input
interactions to [InputActions](/docs/reference/engine/classes/InputAction).

Provide feedback

---

IsKeyDown

Returns whether the given [key](/docs/reference/engine/enums/KeyCode) is currently held down.

UserInputService:IsKeyDown(keyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| keyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)  The [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) of the key. |

Returns

[boolean](/docs/luau/booleans)

Whether the specified key is being held down.

This method returns true if a particular key is pressed on a keyboard,
otherwise returns false.

See also [InputBinding](/docs/reference/engine/classes/InputBinding) as a way to hook key and other input
interactions to [InputActions](/docs/reference/engine/classes/InputAction).

Provide feedback

---

IsMouseButtonPressed

Returns whether the given mouse button is currently held down.

UserInputService:IsMouseButtonPressed(mouseButton:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| mouseButton:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the mouse button. |

Returns

[boolean](/docs/luau/booleans)

Whether the given mouse button is currently held down.

This method returns true if a particular mouse button is pressed,
otherwise returns false.

See also [InputBinding](/docs/reference/engine/classes/InputBinding) as a way to hook mouse button and other
input interactions to [InputActions](/docs/reference/engine/classes/InputAction).

Provide feedback

---

IsNavigationGamepad

Returns true if the specified gamepad is allowed to control navigation
and selection [GuiObjects](/docs/reference/engine/classes/GuiObject).

UserInputService:IsNavigationGamepad(gamepadEnum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| gamepadEnum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the specified gamepad. |

Returns

[boolean](/docs/luau/booleans)

Whether the specified gamepad is a navigation gamepad.

This method returns true if the specified gamepad is allowed to control
navigation and selection [GuiObjects](/docs/reference/engine/classes/GuiObject).

Use [SetNavigationGamepad()](/docs/reference/engine/classes/UserInputService#SetNavigationGamepad)
to set a navigation gamepad, or
[GetNavigationGamepads()](/docs/reference/engine/classes/UserInputService#GetNavigationGamepads)
to get a list of all navigation gamepads.

Provide feedback

---

RecenterUserHeadCFrame

Recenters the [CFrame](/docs/reference/engine/datatypes/CFrame) of the VR headset to the current
orientation of the headset worn by the user.

UserInputService:RecenterUserHeadCFrame():()

Returns

()

This method recenters the [CFrame](/docs/reference/engine/datatypes/CFrame) of the VR headset to the
current orientation of the headset worn by the user. This means that the
headset's current orientation is set to [CFrame.new()](/docs/reference/engine/datatypes/CFrame#new).

This method behaves identically to the [VRService](/docs/reference/engine/classes/VRService) method
[RecenterUserHeadCFrame()](/docs/reference/engine/classes/VRService#RecenterUserHeadCFrame).

Provide feedback

---

SetNavigationGamepad

Sets whether or not the specified gamepad can move the [GuiObject](/docs/reference/engine/classes/GuiObject)
navigator.

UserInputService:SetNavigationGamepad(

gamepadEnum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), enabled:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| gamepadEnum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the specified gamepad. |
| enabled:[boolean](/docs/luau/booleans)  Whether the specified gamepad can move the GUI navigator. |

Returns

()

This method sets whether the specified gamepad can move the
[GuiObject](/docs/reference/engine/classes/GuiObject) navigator.

Use [IsNavigationGamepad()](/docs/reference/engine/classes/UserInputService#IsNavigationGamepad)
to check if a specified gamepad is a set to be a navigation gamepad, or
[GetNavigationGamepads()](/docs/reference/engine/classes/UserInputService#GetNavigationGamepads)
to retrieve a list of all navigation gamepads.

Provide feedback

---

Events

DeviceAccelerationChanged

Fires when a user moves a device that has an accelerometer.

UserInputService.DeviceAccelerationChanged(acceleration:[InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| acceleration:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject), with a [UserInputType](/docs/reference/engine/classes/InputObject#UserInputType) of [Accelerometer](/docs/reference/engine/enums/UserInputType#Accelerometer) and [Position](/docs/reference/engine/classes/InputObject#Position) that shows the force of gravity on each local device axis. |

This event fires when a user moves a device that has an accelerometer, a
component found in most mobile devices that measures acceleration (change
in speed). To determine whether a user's device has an accelerometer
enabled, use
[AccelerometerEnabled](/docs/reference/engine/classes/UserInputService#AccelerometerEnabled).

This event can be used along with
[GetDeviceAcceleration()](/docs/reference/engine/classes/UserInputService#GetDeviceAcceleration)
to determine the current movement of a user's device.

Code Samples

Control Players Using the Accelerometer

This example uses the accelerometer to move the player character when a mobile
device is accelerated. The character will move along the axis that the device
was moved.

```
local UserInputService = game:GetService("UserInputService")



local Players = game:GetService("Players")



local SENSITIVITY = 0.2



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



local ready = true



local function changeAcceleration(acceleration)



if ready then



ready = false



local accel = acceleration.Position



if accel.Y >= SENSITIVITY then



humanoid.Jump = true



end



if accel.Z <= -SENSITIVITY then



humanoid:Move(Vector3.new(-1, 0, 0))



end



if accel.Z >= SENSITIVITY then



humanoid:Move(Vector3.new(1, 0, 0))



end



if accel.X <= -SENSITIVITY then



humanoid:Move(Vector3.new(0, 0, 1))



end



if accel.X >= SENSITIVITY then



humanoid:Move(Vector3.new(0, 0, -1))



end



task.wait(1)



ready = true



end



end



if UserInputService.AccelerometerEnabled then



UserInputService.DeviceAccelerationChanged:Connect(changeAcceleration)



end
```

Provide feedback

---

DeviceGravityChanged

Fires when the force of gravity changes on a device that has an enabled
accelerometer.

UserInputService.DeviceGravityChanged(gravity:[InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| gravity:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) with a [Position](/docs/reference/engine/classes/InputObject#Position) property that shows the force of gravity on each local device axis. This position can be used as a direction to determine the direction of gravity relative to the device. |

This event fires when the device's gravity [Vector3](/docs/reference/engine/datatypes/Vector3) changes on a
device that has an accelerometer. To determine whether a user's device has
an accelerometer enabled, use
[AccelerometerEnabled](/docs/reference/engine/classes/UserInputService#AccelerometerEnabled).

A device's gravity vector represent the force of gravity on each of the
device's X, Y, and Z axes. While gravity never changes, the
force it exerts on each axis changes when the device rotates and changes
orientation. The force value exerted on each axis is a unit vector ranging
from -1 to 1.

If the device has an enabled accelerometer, you can use the
[GetDeviceGravity()](/docs/reference/engine/classes/UserInputService#GetDeviceGravity) method to
get the current force of gravity on the user's device.

Code Samples

Move a Ball using the Accelerometer

This code adds a force on a part so that it falls in the direction of actual
gravity relative to the user's device. In order for this example to work as
expected, it must be placed in a [LocalScript](/docs/reference/engine/classes/LocalScript) and the user's device
must have an accelerometer.

```
local Workspace = game:GetService("Workspace")



local UserInputService = game:GetService("UserInputService")



local ball = script.Parent:WaitForChild("Ball")



local mass = ball:GetMass()



local gravityForce = ball:WaitForChild("GravityForce")



local function moveBall(gravity)



gravityForce.Force = gravity.Position * Workspace.Gravity * mass



end



if UserInputService.AccelerometerEnabled then



UserInputService.DeviceGravityChanged:Connect(moveBall)



end
```

Provide feedback

---

DeviceRotationChanged

Fires when a user rotates a device that has a gyroscope.

UserInputService.DeviceRotationChanged(

rotation:[InputObject](/docs/reference/engine/classes/InputObject), cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| rotation:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) providing info about the device's rotation. [Position](/docs/reference/engine/classes/InputObject#Position) represents the new rotation a [Vector3](/docs/reference/engine/datatypes/Vector3) positional value and [Delta](/docs/reference/engine/classes/InputObject#Delta) represents the change in rotation in a [Vector3](/docs/reference/engine/datatypes/Vector3) positional value. |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  A [CFrame](/docs/reference/engine/datatypes/CFrame) representing the device's current orientation. |

This event fires when a user rotates a device that has a gyroscope, a
component found in most mobile devices that detects orientation and
rotational speed. To check if a user's device has an enabled gyroscope,
use [GyroscopeEnabled](/docs/reference/engine/classes/UserInputService#GyroscopeEnabled).

To query the current device rotation, use the
[GetDeviceRotation()](/docs/reference/engine/classes/UserInputService#GetDeviceRotation) method.

Note that this event only fires when the Roblox client window is in focus.
Inputs will not be captured when the window is minimized.

Provide feedback

---

GamepadConnected

Fires when a gamepad is connected to the client.

UserInputService.GamepadConnected(gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the connected gamepad. |

This event fires when a gamepad is connected to the client. You can also
use [GetConnectedGamepads()](/docs/reference/engine/classes/UserInputService#GetConnectedGamepads)
to find the correct gamepad to use.

Alternatively, you can detect value changes to the
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) property which more
accurately reflects which input (mouse/keyboard, touch, gamepad, etc.) the
player is likely using as the primary input.

See also [GamepadDisconnected](/docs/reference/engine/classes/UserInputService#GamepadDisconnected).

Provide feedback

---

GamepadDisconnected

Fires when a gamepad is disconnected from the client.

UserInputService.GamepadDisconnected(gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| gamepadNum:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The[Enum.UserInputType](/docs/reference/engine/enums/UserInputType) of the disconnected gamepad. |

This event fires when a gamepad is disconnected from the client.

Alternatively, you can detect value changes to the
[PreferredInput](/docs/reference/engine/classes/UserInputService#PreferredInput) property which more
accurately reflects which input (mouse/keyboard, touch, gamepad, etc.) the
player is likely using as the primary input.

See also [GamepadConnected](/docs/reference/engine/classes/UserInputService#GamepadConnected).

Provide feedback

---

InputBegan

Fires when a user begins interacting with an input device such as a mouse
or gamepad.

UserInputService.InputBegan(

input:[InputObject](/docs/reference/engine/classes/InputObject), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| input:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) instance containing information about the user's input. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user begins interacting with an input device such
as a mouse or gamepad, such as when they first interact with a gamepad
button, although it does not capture mouse wheel movements. Can be used
along with [InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged) and
[InputEnded](/docs/reference/engine/classes/UserInputService#InputEnded) to track when user input
begins, changes, and ends.

See also [InputBinding](/docs/reference/engine/classes/InputBinding) as a way to hook input device interactions
to [InputActions](/docs/reference/engine/classes/InputAction).

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

InputChanged

Fires when a user changes how they're interacting with an input device
such as a mouse or gamepad.

UserInputService.InputChanged(

input:[InputObject](/docs/reference/engine/classes/InputObject), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| input:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) instance containing information about the user's input. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. To ignore events that are automatically handled by Roblox like scrolling in a [ScrollingFrame](/docs/reference/engine/classes/ScrollingFrame), check that gameProcessedEvent is false. |

This event fires when a user changes how they're interacting with an input
device such as a mouse or gamepad. Can be used along with
[InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan) and
[InputEnded](/docs/reference/engine/classes/UserInputService#InputEnded) to track when user input
begins, changes, and ends.

See also [InputBinding](/docs/reference/engine/classes/InputBinding) as a way to hook input device interactions
to [InputActions](/docs/reference/engine/classes/InputAction).

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

InputEnded

Fires when a user stops interacting with an input device such as a mouse
or gamepad.

UserInputService.InputEnded(

input:[InputObject](/docs/reference/engine/classes/InputObject), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| input:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) instance containing information about the user input. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user stops interacting with an input device such
as a mouse or gamepad, such as when they release a gamepad button. Can be
used along with [InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan) and
[InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged) to track when user
input begins, changes, and ends.

See also [InputBinding](/docs/reference/engine/classes/InputBinding) as a way to hook input device interactions
to [InputActions](/docs/reference/engine/classes/InputAction).

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

JumpRequest

Fires whenever the client makes a request for their character to jump.

UserInputService.JumpRequest():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when there is a jump request from the client, for example
when the client presses the spacebar or jump button on mobile. Default
behavior is to set the player's [Humanoid.Jump](/docs/reference/engine/classes/Humanoid#Jump) property to true
which makes the player's character jump.

Since this event fires multiple times for a single jump request, using a
[debounce](/docs/scripting/debounce) is recommended.

Code Samples

Disable Default Jumping

This code sample disables default jumping for the player's character by
setting the [Enum.HumanoidStateType.Jumping](/docs/reference/engine/enums/HumanoidStateType#Jumping) state to false and connects the
[JumpRequest](/docs/reference/engine/classes/UserInputService#JumpRequest) event for handling custom
behavior upon jump request.

```
local UserInputService = game:GetService("UserInputService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)



local processJumpRequest = false



local COOLDOWN_TIME = 0.5



local function jumpRequest()



if processJumpRequest == false then



processJumpRequest = true



-- Process custom jump request



print("Jump requested!")



-- Reset debounce variable after cooldown



task.wait(COOLDOWN_TIME)



processJumpRequest = false



end



end



UserInputService.JumpRequest:Connect(jumpRequest)
```

Provide feedback

---

LastInputTypeChanged

Fires whenever the client's [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) is changed.

UserInputService.LastInputTypeChanged(lastInputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| lastInputType:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  A [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) indicating the last input type. |

This event fires whenever the client's [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) is changed.

To get the value of the last input type, regardless of whether it has
changed, use the
[GetLastInputType()](/docs/reference/engine/classes/UserInputService#GetLastInputType) method.

Provide feedback

---

PointerAction

Fires when the user performs a specific pointer action.

UserInputService.PointerAction(

wheel:[number](/docs/luau/numbers), pan:[Vector2](/docs/reference/engine/datatypes/Vector2), pinch:[number](/docs/luau/numbers), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| wheel:[number](/docs/luau/numbers) |
| pan:[Vector2](/docs/reference/engine/datatypes/Vector2) |
| pinch:[number](/docs/luau/numbers) |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. |

This event fires when the user performs a specific pointer action
(wheel, pan, pitch).

Provide feedback

---

TextBoxFocused

Fires when the client focuses on a [TextBox](/docs/reference/engine/classes/TextBox).

UserInputService.TextBoxFocused(textboxFocused:[TextBox](/docs/reference/engine/classes/TextBox)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| textboxFocused:[TextBox](/docs/reference/engine/classes/TextBox)  The [TextBox](/docs/reference/engine/classes/TextBox) that gained focus. |

This event fires when the client gains focus on a [TextBox](/docs/reference/engine/classes/TextBox),
typically when a user clicks/taps it to begin inputting text. Also fires
if the [TextBox](/docs/reference/engine/classes/TextBox) is focused using [TextBox:CaptureFocus()](/docs/reference/engine/classes/TextBox#CaptureFocus).
Can be used alongside
[TextBoxFocusReleased](/docs/reference/engine/classes/UserInputService#TextBoxFocusReleased) to
track when a [TextBox](/docs/reference/engine/classes/TextBox) loses focus.

See also [GetFocusedTextBox()](/docs/reference/engine/classes/UserInputService#GetFocusedTextBox),
[TextBox.Focused](/docs/reference/engine/classes/TextBox#Focused), and [TextBox.FocusLost](/docs/reference/engine/classes/TextBox#FocusLost).

Code Samples

TextBox Modification on Focused and FocusReleased

This example adjusts the [GuiObject.Transparency](/docs/reference/engine/classes/GuiObject#Transparency) of [TextBox](/docs/reference/engine/classes/TextBox)
objects when they gain/lose focus.

```
local UserInputService = game:GetService("UserInputService")



local function textBoxFocused(textBox)



textBox.BackgroundTransparency = 0



end



local function textBoxFocusReleased(textBox)



textBox.BackgroundTransparency = 0.5



end



UserInputService.TextBoxFocused:Connect(textBoxFocused)



UserInputService.TextBoxFocusReleased:Connect(textBoxFocusReleased)
```

Provide feedback

---

TextBoxFocusReleased

Fires when the client loses focus on a [TextBox](/docs/reference/engine/classes/TextBox).

UserInputService.TextBoxFocusReleased(textboxReleased:[TextBox](/docs/reference/engine/classes/TextBox)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| textboxReleased:[TextBox](/docs/reference/engine/classes/TextBox)  The [TextBox](/docs/reference/engine/classes/TextBox) that lost focus. |

This event fires when the client loses focus on a [TextBox](/docs/reference/engine/classes/TextBox),
typically when a user stops text entry by pressing Enter or
clicking/touching elsewhere on the screen. Can be used alongside
[TextBoxFocused](/docs/reference/engine/classes/UserInputService#TextBoxFocused) to track when a
[TextBox](/docs/reference/engine/classes/TextBox) gains focus.

See also [GetFocusedTextBox()](/docs/reference/engine/classes/UserInputService#GetFocusedTextBox),
[TextBox.Focused](/docs/reference/engine/classes/TextBox#Focused), and [TextBox.FocusLost](/docs/reference/engine/classes/TextBox#FocusLost).

Code Samples

TextBox Modification on Focused and FocusReleased

This example adjusts the [GuiObject.Transparency](/docs/reference/engine/classes/GuiObject#Transparency) of [TextBox](/docs/reference/engine/classes/TextBox)
objects when they gain/lose focus.

```
local UserInputService = game:GetService("UserInputService")



local function textBoxFocused(textBox)



textBox.BackgroundTransparency = 0



end



local function textBoxFocusReleased(textBox)



textBox.BackgroundTransparency = 0.5



end



UserInputService.TextBoxFocused:Connect(textBoxFocused)



UserInputService.TextBoxFocusReleased:Connect(textBoxFocusReleased)
```

Provide feedback

---

TouchDrag

Fires when the user drags on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchDrag(

dragDirection:[Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection), numberOfTouches:[number](/docs/luau/numbers), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| dragDirection:[Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection)  The predominant drag direction for the event ([Up](/docs/reference/engine/enums/SwipeDirection), [Down](/docs/reference/engine/enums/SwipeDirection), [Left](/docs/reference/engine/enums/SwipeDirection), or [Right](/docs/reference/engine/enums/SwipeDirection)). |
| numberOfTouches:[number](/docs/luau/numbers)  Currently only supports one touch for a value of 1. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when the user drags on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchEnded

Fires when a user releases their finger from the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchEnded(

touch:[InputObject](/docs/reference/engine/classes/InputObject), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touch:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) instance containing information about the user's input. This is the same object throughout the lifetime of the touch, so comparing [InputObjects](/docs/reference/engine/classes/InputObject) when they are touch objects is valid to determine if it's the same finger. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user releases their finger from the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device. Can be paired
with [TouchStarted](/docs/reference/engine/classes/UserInputService#TouchStarted) to determine when
a user starts and stops touching the screen.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchLongPress

Fires when a user holds at least one finger for a short amount of time on
the screen of a [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchLongPress(

touchPositions:[Array](/docs/luau/tables#arrays), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  An array of [Vector2](/docs/reference/engine/datatypes/Vector2) objects indicating the position of the fingers involved in the gesture. |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  The [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) of the gesture. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user holds at least one finger for a short amount
of time on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchMoved

Fires when a user moves their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchMoved(

touch:[InputObject](/docs/reference/engine/classes/InputObject), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touch:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) instance containing information about the user's input. Note that its [Position](/docs/reference/engine/classes/InputObject#Position) is a [Vector3](/docs/reference/engine/datatypes/Vector3) but only includes X and Y coordinates (Z is always 0). |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user moves their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device, useful for
tracking whether a user is moving their finger on the screen and where
they're moving it. Can be paired with
[TouchStarted](/docs/reference/engine/classes/UserInputService#TouchStarted) and
[TouchEnded](/docs/reference/engine/classes/UserInputService#TouchEnded) to determine when a user
starts touching the screen, how their finger moves while touching it, and
when the they stop touching the screen.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchPan

Fires when the user drags at least one finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchPan(

touchPositions:[Array](/docs/luau/tables#arrays), totalTranslation:[Vector2](/docs/reference/engine/datatypes/Vector2), velocity:[Vector2](/docs/reference/engine/datatypes/Vector2), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  An array of [Vector2s](/docs/reference/engine/datatypes/Vector2) indicating the positions of the touches involved in the gesture. |
| totalTranslation:[Vector2](/docs/reference/engine/datatypes/Vector2)  The size of the pan gesture from start to end, in pixels. |
| velocity:[Vector2](/docs/reference/engine/datatypes/Vector2)  The speed of the pan gesture in pixels per second. |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  The [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) of the gesture. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when the user drags at least one finger on the screen of
a [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchPinch

Fires when a user performs a pinch gesture on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchPinch(

touchPositions:[Array](/docs/luau/tables#arrays), scale:[number](/docs/luau/numbers), velocity:[number](/docs/luau/numbers), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  An array of [Vector2s](/docs/reference/engine/datatypes/Vector2) indicating the screen position, in pixels, of the fingers involved in the pinch gesture. |
| scale:[number](/docs/luau/numbers)  The magnitude of the pinch from start to finish (in pixels) divided by the starting pinch positions. |
| velocity:[number](/docs/luau/numbers)  The speed of the pinch gesture in pixels per second. |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  The [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) of the gesture. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user performs a pinch gesture on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchRotate

Fires when a user rotates two fingers on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchRotate(

touchPositions:[Array](/docs/luau/tables#arrays), rotation:[number](/docs/luau/numbers), velocity:[number](/docs/luau/numbers), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  An array of [Vector2s](/docs/reference/engine/datatypes/Vector2) indicating the positions of the fingers involved in the gesture. |
| rotation:[number](/docs/luau/numbers)  The number of degree the gesture has rotated since the start of the gesture. |
| velocity:[number](/docs/luau/numbers)  The change in rotation (in degrees) divided by the duration of the change (in seconds). |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  The [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) of the gesture. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user rotates two fingers on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchStarted

Fires when a user places their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchStarted(

touch:[InputObject](/docs/reference/engine/classes/InputObject), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touch:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) instance, which contains information about the user's input. This is the same object throughout the lifetime of the touch, so comparing [InputObjects](/docs/reference/engine/classes/InputObject) when they are touch objects is valid to determine if it's the same finger. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user places their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device. Can be paired
with [TouchEnded](/docs/reference/engine/classes/UserInputService#TouchEnded) to determine when a
user starts and stops touching the screen.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchSwipe

Fires on a [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device when
a user places their finger(s) down on the screen, pans across the screen,
and lifts their finger(s) off with a certain speed of movement.

UserInputService.TouchSwipe(

swipeDirection:[Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection), numberOfTouches:[number](/docs/luau/numbers), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| swipeDirection:[Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection)  An [Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection) indicating the direction the user swiped. |
| numberOfTouches:[number](/docs/luau/numbers)  Number of touches involved in the swipe gesture. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires on a [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled)
device when a user places their finger(s) down on the screen, pans across
the screen, and lifts their finger(s) off with a certain speed of
movement.

For more precise tracking of touch input movement, use
[TouchMoved](/docs/reference/engine/classes/UserInputService#TouchMoved).

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchTap

Fires when a user taps their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.

UserInputService.TouchTap(

touchPositions:[Array](/docs/luau/tables#arrays), gameProcessedEvent:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  An array of [Vector2](/docs/reference/engine/datatypes/Vector2) objects indicating the position of the fingers involved in the tap gesture. |
| gameProcessedEvent:[boolean](/docs/luau/booleans)  Indicates whether the engine internally observed this input and acted on it. Generally this refers to UI processing, so if a button was touched or clicked from this input, gameProcessedEvent will be true. |

This event fires when a user taps their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device, regardless of
whether the user taps in the 3D world or on a [GuiObject](/docs/reference/engine/classes/GuiObject) element.
If you're looking for an event that only fires when the user taps in the
3D world, use [TouchTapInWorld](/docs/reference/engine/classes/UserInputService#TouchTapInWorld).

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

TouchTapInWorld

Fires when a user taps their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device and the tap
location is in the 3D world.

UserInputService.TouchTapInWorld(

position:[Vector2](/docs/reference/engine/datatypes/Vector2), processedByUI:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| position:[Vector2](/docs/reference/engine/datatypes/Vector2)  A [Vector2](/docs/reference/engine/datatypes/Vector2) indicating the position of the tap. |
| processedByUI:[boolean](/docs/luau/booleans)  Whether the user tapped a UI element. |

This event fires when a user taps their finger on the screen of a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device and the tap
location is in the 3D world rather than on a [GuiObject](/docs/reference/engine/classes/GuiObject) element.

Note that this event only fires when the Roblox client window is in focus.
It will not fire when the window is minimized.

Provide feedback

---

UserCFrameChanged

Deprecated

Show details

---

WindowFocused

Fires when the window of the Roblox client gains focus on the user's
screen.

UserInputService.WindowFocused():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the window of the Roblox client gains focus,
typically when it is maximized or actively opened by the user. Can be used
alongside [WindowFocusReleased](/docs/reference/engine/classes/UserInputService#WindowFocusReleased)
to track when the client loses focus on a user's screen.

Provide feedback

---

WindowFocusReleased

Fires when the window of the Roblox client loses focus on the user's
screen.

UserInputService.WindowFocusReleased():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the window of the Roblox client loses focus,
typically when it is minimized by the user. Can be used alongside
[WindowFocused](/docs/reference/engine/classes/UserInputService#WindowFocused) to track when the
client gains focus on a user's screen.

Code Samples

Window Focus Away Script (LocalScript)

The purpose of this code sample is to fire a server-side [RemoteEvent](/docs/reference/engine/classes/RemoteEvent)
to indicate when the player is "away" based on their client window being
minimized. When mimimized, the server creates a [ForceField](/docs/reference/engine/classes/ForceField) around the
player's character to shield them from damage.

The code below should be placed in a [LocalScript](/docs/reference/engine/classes/LocalScript) within
[StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts) with the intention of running it in conjunction
with the server-side [Script](/docs/reference/engine/classes/Script) that follows it.

```
local UserInputService = game:GetService("UserInputService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local awayEvent = ReplicatedStorage:WaitForChild("AwayEvent")



local function focusGained()



awayEvent:FireServer(false)



end



local function focusReleased()



awayEvent:FireServer(true)



end



UserInputService.WindowFocused:Connect(focusGained)



UserInputService.WindowFocusReleased:Connect(focusReleased)
```

Window Focus Away Script (Script)

The following [Script](/docs/reference/engine/classes/Script), placed within [ServerScriptService](/docs/reference/engine/classes/ServerScriptService),
completes the [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) connection triggered by the
[LocalScript](/docs/reference/engine/classes/LocalScript) above.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local awayEvent = Instance.new("RemoteEvent")



awayEvent.Name = "AwayEvent"



awayEvent.Parent = ReplicatedStorage



local function manageForceField(player, away)



if away then



local forceField = Instance.new("ForceField")



forceField.Parent = player.Character



else



local forceField = player.Character:FindFirstChildOfClass("ForceField")



if forceField then



forceField:Destroy()



end



end



end



awayEvent.OnServerEvent:Connect(manageForceField)
```

Provide feedback

---