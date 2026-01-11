# VRService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VRService
Scraped: 2026-01-11T02:36:12.399477Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- VRService
- VRService.UserCFrameChanged
- Camera.HeadScale
- VREnabled
- UserInputService:GetUserCFrame()
- UserInputService.UserCFrameChanged
- LocalScript
- Camera.HeadLocked
- VREnabled()
- GetUserCFrame()
- UserInputService
- UserCFrameChanged
- UserInputService:RecenterUserHeadCFrame()
- NavigationRequested
- GetUserCFrameEnabled()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [VRService](/docs/reference/engine/classes/VRService)

English

Feedback

Engine Class

![VRService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/VRService-Dark.webp)VRService

Service responsible for handling interactions between Roblox and Virtual
Reality (VR).

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [AutomaticScaling](#AutomaticScaling):[Enum.VRScaling](/docs/reference/engine/enums/VRScaling) |
| [AvatarGestures](#AvatarGestures):[boolean](/docs/luau/booleans) |
| [ControllerModels](#ControllerModels):[Enum.VRControllerModelMode](/docs/reference/engine/enums/VRControllerModelMode) |
| [FadeOutViewOnCollision](#FadeOutViewOnCollision):[boolean](/docs/luau/booleans) |
| [GuiInputUserCFrame](#GuiInputUserCFrame):[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) |
| [LaserPointer](#LaserPointer):[Enum.VRLaserPointerMode](/docs/reference/engine/enums/VRLaserPointerMode) |
| [ThirdPersonFollowCamEnabled](#ThirdPersonFollowCamEnabled):[boolean](/docs/luau/booleans) |
| [VREnabled](#VREnabled):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetTouchpadMode](#GetTouchpadMode)(pad: [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad)):[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode) |
| [GetUserCFrame](#GetUserCFrame)(type: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [GetUserCFrameEnabled](#GetUserCFrameEnabled)(type: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)):[boolean](/docs/luau/booleans) |
| [RecenterUserHeadCFrame](#RecenterUserHeadCFrame)():() |
| [RequestNavigation](#RequestNavigation)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),inputUserCFrame: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)):() |
| [SetTouchpadMode](#SetTouchpadMode)(pad: [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad),mode: [Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)):() |

Events

|  |
| --- |
| [NavigationRequested](#NavigationRequested)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),inputUserCFrame: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchpadModeChanged](#TouchpadModeChanged)(pad: [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad),mode: [Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [UserCFrameChanged](#UserCFrameChanged)(type: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame),value: [CFrame](/docs/reference/engine/datatypes/CFrame)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [UserCFrameEnabled](#UserCFrameEnabled)(type: [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame),enabled: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

VRService is responsible for handling interactions between Roblox and
Virtual Reality (VR). Its methods, properties, and events help you provide the
best experience for end users seeking to experience Roblox on VR devices.

See [VR Guidelines](/docs/production/publishing/vr-guidelines) for more
information on publishing an experience for VR devices.

Code Samples

VRService

The following example demonstrates how to get the [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) of the left controller and place a part at that point in real world space. The [CFrame](/docs/reference/engine/datatypes/CFrame) of the controller changes whenever the device moves, so you should update the necessary parts whenever [VRService.UserCFrameChanged](/docs/reference/engine/classes/VRService#UserCFrameChanged) fires.

```
local VRService = game:GetService("VRService")



local part = workspace.Part



local handOffset = VRService:GetUserCFrame(Enum.UserCFrame.LeftHand)



-- Account for headscale



handOffset = handOffset.Rotation + handOffset.Position * workspace.CurrentCamera.HeadScale



part.CFrame = workspace.CurrentCamera.CFrame * handOffset
```

---

API Reference

Properties

AutomaticScaling

Read Parallel

Automatically adjusts scaling in VR to align the player with their avatar.

VRService.AutomaticScaling:[Enum.VRScaling](/docs/reference/engine/enums/VRScaling)

When set to [Enum.VRScaling.World](/docs/reference/engine/enums/VRScaling#World), [Camera.HeadScale](/docs/reference/engine/classes/Camera#HeadScale) adjusts so
that the scale of the world is seen from the avatar's perspective. A
player with a small avatar will perceive the objects around them as larger
than a player with a large avatar will.

Provide feedback

---

AvatarGestures

Read Parallel

When true, a VR player will be able to animate their hands and head using
their controllers and headset.

VRService.AvatarGestures:[boolean](/docs/luau/booleans)

When set to true, a VR player will be able to animate their hands and head
using their controllers and headset.

This property must be set on the server.

Provide feedback

---

ControllerModels

Read Parallel

VRService.ControllerModels:[Enum.VRControllerModelMode](/docs/reference/engine/enums/VRControllerModelMode)

Provide feedback

---

FadeOutViewOnCollision

Read Parallel

When true, a VR player's view will fade to black when their head collides
with an object.

VRService.FadeOutViewOnCollision:[boolean](/docs/luau/booleans)

When true, a VR player's view fades to black when their head collides with
an object. This property prevents players from being able to see through
walls while in VR. The default value is true.

Provide feedback

---

GuiInputUserCFrame

Not Replicated

Read Parallel

Describes what [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) is responsible for input in VR.

VRService.GuiInputUserCFrame:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)

This property describes what [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) is responsible for input in
VR. For instance, if a VR headset is responsible, the value of this
property will be [Enum.UserCFrame.Head](/docs/reference/engine/enums/UserCFrame#Head).

To check if Roblox detects any VR devices, which would be responsible for
input in VR, you can check the [VREnabled](/docs/reference/engine/classes/VRService#VREnabled)
property.

Code Samples

VRService.GuiInputUserCFrame

This example checks if Roblox detects a VR device. If a VR device is detected,
this prints the name of the UserCFrame responsible for VR input. If not, this
example prints "No VR device detected!".

```
local VRService = game:GetService("VRService")



if VRService.VREnabled then



print(VRService.GuiInputUserCFrame.Name)



else



print("No VR device detected!")



end
```

Provide feedback

---

LaserPointer

Read Parallel

VRService.LaserPointer:[Enum.VRLaserPointerMode](/docs/reference/engine/enums/VRLaserPointerMode)

Provide feedback

---

ThirdPersonFollowCamEnabled

Read Only

Not Replicated

Read Parallel

VRService.ThirdPersonFollowCamEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

VREnabled

Read Only

Not Replicated

Read Parallel

Describes whether the user is using a virtual reality device.

VRService.VREnabled:[boolean](/docs/luau/booleans)

This property describes whether the user is using a virtual reality (VR)
device.

If a VR device is enabled, you can interact with its location and movement
through methods such as [UserInputService:GetUserCFrame()](/docs/reference/engine/classes/UserInputService#GetUserCFrame). You can
also react to VR device movement using the
[UserInputService.UserCFrameChanged](/docs/reference/engine/classes/UserInputService#UserCFrameChanged) event.

```
local UserInputService = game:GetService("UserInputService")



local isUsingVR = UserInputService.VREnabled



if isUsingVR then



print("User is using a VR headset!")



else



print("User is not using a VR headset!")



end
```

This property can only be used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

#### See Also

* [Camera.HeadLocked](/docs/reference/engine/classes/Camera#HeadLocked)
* [UserInputService:GetUserCFrame()](/docs/reference/engine/classes/UserInputService#GetUserCFrame)
* [UserInputService.UserCFrameChanged](/docs/reference/engine/classes/UserInputService#UserCFrameChanged)

Code Samples

VR Head Tracking

This example demonstrates how to implement a head tracking script that mirrors
the movement of a virtual reality (VR) headset (the user's actual head) to
their in-game character's head.

The example first check if the user is using a VR device by checking the value
of the [VREnabled()](/docs/reference/engine/classes/VRService#VREnabled) property. This example
only works if the user is using a VR headset.

To determine the initial [CFrame](/docs/reference/engine/datatypes/CFrame) of the character's head, the code
sample calls [GetUserCFrame()](/docs/reference/engine/classes/VRService#GetUserCFrame) and
passes [Enum.UserCFrame.Head](/docs/reference/engine/enums/UserCFrame#Head) as the argument.

To update the head's CFrame whenever the user's VR headset moves, the example
connects the [VRService.UserCFrameChanged](/docs/reference/engine/classes/VRService#UserCFrameChanged) event to the
*TrackHead()* function. When the event fires to indicate that a VR device
moved, TrackHead() checks if the headset moved. If the headset moved, the
function updates the CFrame of the character's head to the [CFrame](/docs/reference/engine/datatypes/CFrame)
*value* provided as an argument.

As the UserCFrame enum also tracks VR left and right hand devices, the concept
of VR device tracking can be expanded to other character bodyparts.

In order for the example to work as expected, it must be placed in a
LocalScript.

```
local VRService = game:GetService("VRService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.CharacterAdded:Wait()



local head = character:WaitForChild("Head")



local function TrackHead(inputType, value)



if inputType == Enum.UserCFrame.Head then



head.CFrame = value



end



end



if VRService.VREnabled then



-- Set the initial CFrame



head.CFrame = VRService:GetUserCFrame(Enum.UserCFrame.Head)



-- Track VR headset movement and mirror for character's head



VRService.UserCFrameChanged:Connect(TrackHead)



end
```

Provide feedback

---

Methods

GetTouchpadMode

Returns the VRTouchpadMode indicating the mode of a specified VRTouchpad.

VRService:GetTouchpadMode(pad:[Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad)):[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)

Parameters

|  |
| --- |
| pad:[Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad)  The specified [VRTouchpad](/docs/reference/engine/enums/VRTouchpad). |

Returns

[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)

The mode of the specified [VRTouchpad](/docs/reference/engine/enums/VRTouchpad).

This method returns the [Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode) indicating the mode of a
specified [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad). The returned mode indicates how the user
interacts with their touchpad to play the game.

This can also be used alongside the several [UserInputService](/docs/reference/engine/classes/UserInputService) VR
methods and events.

This method will only work when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService:GetTouchpadMode

This example retrieves and prints the name of the user's current
VRTouchpad.Left touchpad mode.

```
local VRService = game:GetService("VRService")



VRService:GetTouchpadMode(Enum.VRTouchpad.Left)
```

Provide feedback

---

GetUserCFrame

Returns a CFrame describing the position & orientation of a specified
virtual reality device as an offset from a point in real world space.

VRService:GetUserCFrame(type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)  The specified [UserCFrame](/docs/reference/engine/enums/UserCFrame). |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

This method returns a [CFrame](/docs/reference/engine/datatypes/CFrame) describing the position and
orientation of a specified virtual reality (VR) device as an offset from a
point in real world space. This method should be used when implementing VR
compatibility into a game to obtain and track the movement of a connected
VR device.

By using the method, developers can implement features such as
re-positioning the user's in-game character corresponding to the location
of a connected VR device. This can be done by changing the *CFrame* of the
user's in-game character to match the *CFrame* of the specified VR device
using the UserCFrame enum and *CFrame* value arguments passed by the
event.

[VRService](/docs/reference/engine/classes/VRService) also provides a
[UserCFrameChanged](/docs/reference/engine/classes/VRService#UserCFrameChanged) event that
automatically fires when the [CFrame](/docs/reference/engine/datatypes/CFrame) of connected VR device
changes, so long it is used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

This method will only work when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService:GetUserCFrame

This example positions a part at the player's left hand, assuming Camera.HeadLocked = true

```
local Workspace = game:GetService("Workspace")



local VRService = game:GetService("VRService")



local camera = Workspace.CurrentCamera



local part = script.Parent.Part



local handOffset = VRService:GetUserCFrame(Enum.UserCFrame.LeftHand)



-- Account for headscale



handOffset = handOffset.Rotation + handOffset.Position * camera.HeadScale



part.CFrame = camera.CFrame * handOffset
```

Provide feedback

---

GetUserCFrameEnabled

Returns true if the specified [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) is available to be
listened to.

VRService:GetUserCFrameEnabled(type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)  The specified type of VR device. |

Returns

[boolean](/docs/luau/booleans)

A boolean indicating whether the specified VR device is enabled
(true) or disabled (false).

This method returns true if the specified [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) virtual
reality device (VR) is available to be listened to. It can be used to
determine whether a specified VR device, such as [Enum.UserCFrame.Head](/docs/reference/engine/enums/UserCFrame#Head),
is connected to the user's game.

This can also be used alongside the several [UserInputService](/docs/reference/engine/classes/UserInputService) VR
methods and events.

This method will only work when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService:GetUserCFrameEnabled

This example indicates whether the UserCFrame.Head VR device is enabled or
disabled for the user. If the device is enabled, this prints "VR device is
enabled!". If the device is disabled, this prints "VR device is disabled!".

```
local VRService = game:GetService("VRService")



local isEnabled = VRService:GetUserCFrameEnabled(Enum.UserCFrame.Head)



if isEnabled then



print("VR device is enabled!")



else



print("VR device is disabled!")



end
```

Provide feedback

---

RecenterUserHeadCFrame

Re-centers the [CFrame](/docs/reference/engine/datatypes/CFrame) to the current location of the VR headset
being worn by the user.

VRService:RecenterUserHeadCFrame():()

Returns

()

This method re-centers the [CFrame](/docs/reference/engine/datatypes/CFrame) of the user's head to the
current location of the VR headset being worn by the user. It can be used
to ensure that the user's in-game head is positioned according to the
location of the user's VR headset.

This behaves identically to
[UserInputService:RecenterUserHeadCFrame()](/docs/reference/engine/classes/UserInputService#RecenterUserHeadCFrame).

This method will only work when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService:RecenterUserHeadCFrame

This example fires the function to recenter the CFrame of the user's head to
the current location of the VR headset being worn by the user.

```
local VRService = game:GetService("VRService")



VRService:RecenterUserHeadCFrame()
```

Provide feedback

---

RequestNavigation

Requests navigation to the specified [CFrame](/docs/reference/engine/datatypes/CFrame) using the specified
[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) as the origin for the visualizer parabola.

VRService:RequestNavigation(

cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), inputUserCFrame:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)

):()

Parameters

|  |
| --- |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  The specified [CFrame](/docs/reference/engine/datatypes/CFrame) coordinates. |
| inputUserCFrame:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)  The VR device for which the navigation is requested. |

Returns

()

This method requests navigation to the specified [CFrame](/docs/reference/engine/datatypes/CFrame) using
the specified [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) as the origin for the visualizer parabola.
It can be used to incorporate virtual reality (VR) into your game by
providing a means to visualize a navigation path from the user's VR device
to a destination.

[VRService](/docs/reference/engine/classes/VRService) has a similar event,
[NavigationRequested](/docs/reference/engine/classes/VRService#NavigationRequested), used to detect
such requests. This can also be used alongside the several
[UserInputService](/docs/reference/engine/classes/UserInputService) VR methods and events.

This method will only work when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService:RequestNavigation

This example requests navigation from the user's UserCFrame.Head
coordinates to the CFrame coordinates of a Part named
*NavigationDestination*.

*Note:* In order for this to work, a Part named *NavigationDestination* must
exist in the game's Workspace.

```
local VRService = game:GetService("VRService")



local destination = workspace:FindFirstChild("NavigationDestination")



VRService:RequestNavigation(Enum.UserCFrame.Head, destination.CFrame)
```

Provide feedback

---

SetTouchpadMode

Sets the mode of the specified [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad) to the specified
[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode).

VRService:SetTouchpadMode(

pad:[Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad), mode:[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)

):()

Parameters

|  |
| --- |
| pad:[Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad)  The specified [VRTouchpad](/docs/reference/engine/enums/VRTouchpad) you want to set the mode of. |
| mode:[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)  The mode you want to set the specified [VRTouchpad](/docs/reference/engine/enums/VRTouchpad) to. |

Returns

()

This method sets the mode of the specified [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad) to the
specified [Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode). It can be used to change the user's
virtual reality (VR) touchpad mode so that the user interacts with the
game differently using the touchpad.

This can also be used alongside the several [UserInputService](/docs/reference/engine/classes/UserInputService) VR
methods and events.

This method will only work when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService:SetTouchpadMode

This example sets the user's VRTouchpad.Left touchpad mode to
TouchMode.Touch. This means that the left touchpad is treated as ButtonB.

```
local VRService = game:GetService("VRService")



VRService:SetTouchpadMode(Enum.VRTouchpad.Left, Enum.VRTouchpadMode.Touch)
```

Provide feedback

---

Events

NavigationRequested

Fired when navigation is requested from [VRService](/docs/reference/engine/classes/VRService).

VRService.NavigationRequested(

cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), inputUserCFrame:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  The requested [CFrame](/docs/reference/engine/datatypes/CFrame) coordinates. |
| inputUserCFrame:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)  Indicates the VR device for which navigation is requested. |

This event fires when navigation is requested from [VRService](/docs/reference/engine/classes/VRService) for a
specified [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) VR device. It fires with a [CFrame](/docs/reference/engine/datatypes/CFrame)
coordinate and the specified [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) indicating the device
requesting the navigation.

This event can be used alongside [UserInputService](/docs/reference/engine/classes/UserInputService) service events
and methods.

Since this event fires locally, it can only be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService.NavigationRequested

This example prints the name of the UserCFrame VR device making the request,
and the CFrame coordinates passed.

```
local VRService = game:GetService("VRService")



VRService.NavigationRequested:Connect(function(cframe, inputUserCFrame)



print(inputUserCFrame.Name .. " made request with CFrame: " .. cframe)



end)
```

Provide feedback

---

TouchpadModeChanged

Fires if the [Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode) of a [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad) is changed.

VRService.TouchpadModeChanged(

pad:[Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad), mode:[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| pad:[Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad)  The touchpad that changed mode. |
| mode:[Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode)  The new mode. |

This event fires if the [Enum.VRTouchpadMode](/docs/reference/engine/enums/VRTouchpadMode) of a [Enum.VRTouchpad](/docs/reference/engine/enums/VRTouchpad) is
changed. You can use this event to track the states of VR touchpads
connected via the user's client.

This event can be used alongside [UserInputService](/docs/reference/engine/classes/UserInputService) service events
and methods.

Since this event fires locally, it can only be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService.TouchpadModeChanged

This example fires when the state of a VRTouchpad changes. It prints the name
of the Touchpad that changed, and the state that it changed to.

```
local VRService = game:GetService("VRService")



VRService.TouchpadModeChanged:Connect(function(pad, mode)



print(pad.Name .. " Touchpad changed to state: " .. mode.Name)



end)
```

Provide feedback

---

UserCFrameChanged

Fires when a [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) is changed.

VRService.UserCFrameChanged(

type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame), value:[CFrame](/docs/reference/engine/datatypes/CFrame)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)  The type of VR device that changed. |
| value:[CFrame](/docs/reference/engine/datatypes/CFrame)  The updated [CFrame](/docs/reference/engine/datatypes/CFrame) coordinates of the VR device after the change. |

This event fires when a [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) is changed, for instance when
the user moves a connected VR device. It can be used alongside
[GetUserCFrame()](/docs/reference/engine/classes/VRService#GetUserCFrame) to track the
[CFrame](/docs/reference/engine/datatypes/CFrame) coordinates of a VR device, and when it changes/moves.
It can also be used alongside [UserInputService](/docs/reference/engine/classes/UserInputService) service events and
methods.

Since this event fires locally, it can only be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService.UserCFrameChanged

This event fires when the user moves a connected VR device. When the event
fires, this prints the name of the VR device type that changed, and the
updated CFrame coordinates.

```
local VRService = game:GetService("VRService")



VRService.UserCFrameChanged:Connect(function(userCFrameType, cframeValue)



print(userCFrameType.Name .. " changed. Updated Frame: " .. tostring(cframeValue))



end)
```

Provide feedback

---

UserCFrameEnabled

Fires when a [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) is enabled or disabled.

VRService.UserCFrameEnabled(

type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame), enabled:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| type:[Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame)  The [UserCFrame](/docs/reference/engine/enums/UserCFrame) getting enabled or disabled. |
| enabled:[boolean](/docs/luau/booleans)  A boolean indicating whether the [UserCFrame](/docs/reference/engine/enums/UserCFrame) is enabled (true) or disabled (false). |

This event fires when a [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) is enabled or disabled. It can
be used alongside
[GetUserCFrameEnabled()](/docs/reference/engine/classes/VRService#GetUserCFrameEnabled) to track
whether a specified [UserCFrame](/docs/reference/engine/enums/UserCFrame) is enabled, and when its
state changes. It can also be used alongside [UserInputService](/docs/reference/engine/classes/UserInputService)
service events and methods.

Since this event fires locally, it can only be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

VRService.UserCFrameEnabled

This example fires when a UserCFrame changes state, printing the name of the
changed UserCFrame and whether it changed got enabled or disabled.

```
local VRService = game:GetService("VRService")



VRService.UserCFrameEnabled:Connect(function(type, enabled)



if enabled then



print(type.Name .. " got enabled!")



else



print(type.Name .. " got disabled!")



end



end)
```

Provide feedback

---