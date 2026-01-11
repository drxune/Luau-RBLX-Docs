# Mouse | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Mouse
Scraped: 2026-01-11T02:42:16.491126Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- Mouse
- BasePart
- PlayerMouse
- PluginMouse
- UserInputService
- ContextActionService
- Player:GetMouse()
- Players.LocalPlayer
- LocalScript
- Tool.Equipped
- Icon
- TargetFilter
- Hit
- Target
- TargetSurface
- WorldRoot:Raycast()
- Plugins
- Plugin:GetMouse()
- UserInputService.MouseBehavior
- UserInputService.MouseDeltaSensitivity
- Button1Down
- BindAction
- Mouse.TargetFilter
- Tools
- Mouse.Target
- Mouse.UnitRay
- Workspace.CurrentCamera
- Mouse.Hit
- Mouse.Origin
- GuiButton
- UserInputService.MouseIconEnabled
- UserInputService.MouseIcon
- Mouse.Icon
- MouseEnter
- MouseLeave
- MouseButton1Down
- mouse
- BasePart.BrickColor
- Character
- CFrame
- X()
- Y()
- ViewSizeX()
- ViewSizeY()
- Move()
- ContextActionService:BindAction()
- UserInputService.InputChanged
- Position
- InputObject
- Mouse.Y
- Changed
- GetPropertyChangedSignal
- Mouse.Move
- Mouse.X
- Tool
- local player
- mouse's target
- Mouse.WheelForward
- HopperBin
- Mouse.WheelBackward
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Mouse](/docs/reference/engine/classes/Mouse)

English

Feedback

Engine Class

Mouse

Legacy object that contains members useful for pointer input.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Hit](#Hit):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [hit](#hit):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [Icon](#Icon):ContentId |
| [IconContent](#IconContent):[Content](/docs/reference/engine/datatypes/Content) |
| [Origin](#Origin):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Target](#Target):[BasePart](/docs/reference/engine/classes/BasePart) |
| [target](#target):[BasePart](/docs/reference/engine/classes/BasePart)  Deprecated |
| [TargetFilter](#TargetFilter):[Instance](/docs/reference/engine/datatypes/Instance) |
| [TargetSurface](#TargetSurface):[Enum.NormalId](/docs/reference/engine/enums/NormalId) |
| [UnitRay](#UnitRay):[Ray](/docs/reference/engine/datatypes/Ray) |
| [ViewSizeX](#ViewSizeX):[number](/docs/luau/numbers) |
| [ViewSizeY](#ViewSizeY):[number](/docs/luau/numbers) |
| [X](#X):[number](/docs/luau/numbers) |
| [Y](#Y):[number](/docs/luau/numbers) |

Events

|  |
| --- |
| [Button1Down](#Button1Down)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Button1Up](#Button1Up)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Button2Down](#Button2Down)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Button2Up](#Button2Up)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Idle](#Idle)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [KeyDown](#KeyDown)(key: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [keyDown](#keyDown)(key: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [KeyUp](#KeyUp)(key: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [Move](#Move)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WheelBackward](#WheelBackward)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WheelForward](#WheelForward)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[PlayerMouse](/docs/reference/engine/classes/PlayerMouse), [PluginMouse](/docs/reference/engine/classes/PluginMouse)

Mouse has been superseded by [UserInputService](/docs/reference/engine/classes/UserInputService) and
[ContextActionService](/docs/reference/engine/classes/ContextActionService), which cover a broader scope, are more feature
rich, and support cross-platform patterns better. It remains supported
because of its widespread use, but you should strongly consider using these
alternatives.

The Mouse object houses various API for pointers, primarily for buttons
and raycasting. It can be accessed through [Player:GetMouse()](/docs/reference/engine/classes/Player#GetMouse) called on
the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) in a [LocalScript](/docs/reference/engine/classes/LocalScript). It is also passed by
the [Tool.Equipped](/docs/reference/engine/classes/Tool#Equipped) event.

* It is most notable for the [Icon](/docs/reference/engine/classes/Mouse#Icon) property, which changes
  the cursor's appearance.
* It continually raycasts the screen mouse position into the 3D world using
  the [TargetFilter](/docs/reference/engine/classes/Mouse#TargetFilter) property, storing the results of
  the raycast in the [Hit](/docs/reference/engine/classes/Mouse#Hit), [Target](/docs/reference/engine/classes/Mouse#Target), and
  [TargetSurface](/docs/reference/engine/classes/Mouse#TargetSurface) properties. These can be useful
  for simple cases, but [WorldRoot:Raycast()](/docs/reference/engine/classes/WorldRoot#Raycast) should be used in more
  complicated [raycasting](/docs/workspace/raycasting) scenarios.
* [Plugins](/docs/reference/engine/classes/Plugin) can use [Plugin:GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse) to get a
  [PluginMouse](/docs/reference/engine/classes/PluginMouse), which behaves similarly.

```
-- From a LocalScript:



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



-- Setting the mouse icon



mouse.Icon = "rbxasset://SystemCursors/Wait"
```

Note:

* This object does not control/restrict pointer movement. For this, see
  [UserInputService.MouseBehavior](/docs/reference/engine/classes/UserInputService#MouseBehavior) and
  [UserInputService.MouseDeltaSensitivity](/docs/reference/engine/classes/UserInputService#MouseDeltaSensitivity).
* If two functions are connected to same input event, such as
  [Button1Down](/docs/reference/engine/classes/Mouse#Button1Down), both functions will run when the
  event fires. There is no concept of sinking/passing input, as events don't
  support this behavior. However, [ContextActionService](/docs/reference/engine/classes/ContextActionService) does have this
  behavior through [BindAction](/docs/reference/engine/classes/ContextActionService#BindAction).
* While a mouse may not be available on all platforms, Mouse will still
  function on mobile (touch) and console (gamepad), which don't typically have
  mice or pointer hardware. For explicit cross-platform behaviors, use
  [UserInputService](/docs/reference/engine/classes/UserInputService) and [ContextActionService](/docs/reference/engine/classes/ContextActionService).

  See [Input and Camera](/docs/input) for more information on
  customizing inputs in your experience.

---

API Reference

Properties

Hit

Read Only

Not Replicated

Read Parallel

The [CFrame](/docs/reference/engine/datatypes/CFrame) of the mouse's position in 3D space.

Mouse.Hit:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property indicates [CFrame](/docs/reference/engine/datatypes/CFrame) of the mouse's position in 3D
space. Note that [Mouse.TargetFilter](/docs/reference/engine/classes/Mouse#TargetFilter) and its descendants will be
ignored.

Developers can get obtain the position of Hit like so:

```
local position = mouse.Hit.Position
```

Hit is often used by [Tools](/docs/reference/engine/classes/Tool) to fire a weapon towards the mouse
in third person.

Developers looking for the [BasePart](/docs/reference/engine/classes/BasePart) the mouse is pointing at
should use [Mouse.Target](/docs/reference/engine/classes/Mouse#Target).

#### How is Mouse.Hit calculated?

The position of the Hit CFrame is calculated as the point of intersection
between the mouse's internal [Ray](/docs/reference/engine/datatypes/Ray) (an extended version of
[Mouse.UnitRay](/docs/reference/engine/classes/Mouse#UnitRay)) and an object in 3D space (such as a part).

The orientation of the Hit CFrame corresponds with the direction of the
[Mouse.UnitRay](/docs/reference/engine/classes/Mouse#UnitRay).

```
local unitRayDirection = mouse.UnitRay.Direction



local mouseHitDirection = mouse.Hit.lookVector



-- unitRayDirection ≈ mouseHitDirection



-- the vectors are approximately equal
```

Note, the roll of the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) is not used when
calculating the orientation of the Hit [CFrame](/docs/reference/engine/datatypes/CFrame).

The mouse's internal ray extends for 1,000 studs. If the mouse is not
pointing at an object in 3D space (for example when pointing at the sky),
this property will be 1,000 studs away from the
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera).

Code Samples

Mouse.Hit Laser Beam

The code in this sample, when placed inside a LocalScript within
StarterPlayerScripts will draw a red laser beam between the character's head
and [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) at all times.

Note, this beam will pass directly through obstructions in third person as the
Mouse's raycasting is done from the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) not the
head.

```
local Players = game:GetService("Players")



local RunService = game:GetService("RunService")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local beam = Instance.new("Beam")



beam.Segments = 1



beam.Width0 = 0.2



beam.Width1 = 0.2



beam.Color = ColorSequence.new(Color3.new(1, 0, 0))



beam.FaceCamera = true



local attachment0 = Instance.new("Attachment")



local attachment1 = Instance.new("Attachment")



beam.Attachment0 = attachment0



beam.Attachment1 = attachment1



beam.Parent = workspace.Terrain



attachment0.Parent = workspace.Terrain



attachment1.Parent = workspace.Terrain



local function onRenderStep()



local character = player.Character



if not character then



beam.Enabled = false



return



end



local head = character:FindFirstChild("Head")



if not head then



beam.Enabled = false



return



end



beam.Enabled = true



local origin = head.Position



local finish = mouse.Hit.Position



attachment0.Position = origin



attachment1.Position = finish



end



RunService.RenderStepped:Connect(onRenderStep)
```

Mouse Origin vs Mouse Hit vs CurrentCamera Position

The code below visualizes the difference between [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Mouse.Origin](/docs/reference/engine/classes/Mouse#Origin). In order to do this, the code uses the
[Vector3](/docs/reference/engine/datatypes/Vector3) positions of the hit and origin [CFrame](/docs/reference/engine/datatypes/CFrame) values
using .p.

The difference is that the origin is "where the mouse came from" (its origin)
and the hit is the position where the mouse hits (is when the player presses
their mouse).

This example also visualizes that the mouse origin is very similar to the
position of the CurrentCamera by printing the magnitude (distance) between
the two positions.

```
local Players = game:GetService("Players")



local Workspace = game:GetService("Workspace")



local player = Players.LocalPlayer



local camera = Workspace.CurrentCamera



local mouse = player:GetMouse()



local camPos = camera.CFrame.Position



local function onButton1Down()



print("Mouse.Hit:", mouse.Hit.Position)



print("camPos:", camPos)



print("Mouse.Origin:", mouse.Origin.Position)



print("Magnitude:", (mouse.Origin.Position - camPos).Magnitude)



end



mouse.Button1Down:Connect(onButton1Down)
```

Provide feedback

---

hit

Deprecated

Show details

---

Icon

Read Parallel

The content ID of the image used as the [Mouse](/docs/reference/engine/classes/Mouse) icon.

Mouse.Icon:ContentId

Icon is a property that determines the image used as the pointer. If
blank, a default arrow is used. While the cursor hovers over a
[GuiButton](/docs/reference/engine/classes/GuiButton), this property is temporarily ignored.

To hide the cursor entirely, do not use a transparent image –
instead, set [UserInputService.MouseIconEnabled](/docs/reference/engine/classes/UserInputService#MouseIconEnabled) to false.

For getting/setting the user mouse icon in experiences, you should use
[UserInputService.MouseIcon](/docs/reference/engine/classes/UserInputService#MouseIcon). [Mouse.Icon](/docs/reference/engine/classes/Mouse#Icon) will be deprecated
after the new API for plugins to set the mouse cursor is released.

##### Designing a Cursor

The following guidelines may prove useful when creating your own mouse
cursors:

* The dimensions of the image used determines the size of the cursor.
* The dimensions of the image should not exceed 256 pixels on any axis.
* The center of the image is where mouse inputs are issued.
* The default mouse image is 64x64 pixels, with the mouse taking up 17x24
  pixels of space.

##### System Cursors

When using a [PluginMouse](/docs/reference/engine/classes/PluginMouse) retrieved from [Plugin:GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse),
you can use the following icons similar to your system's default cursors,
such as hands, arrows, I-beams, etc. You can use these with GUI events
like [MouseEnter](/docs/reference/engine/classes/GuiObject#MouseEnter),
[MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave), and
[MouseButton1Down](/docs/reference/engine/classes/GuiButton#MouseButton1Down) to provide a
consistent Studio experience when interacting with certain kinds of GUI
components. Note that these only work for Studio plugins; they will not
work for other [Mouse](/docs/reference/engine/classes/Mouse) objects.

| Look\* | Asset | Suggested Use |
| --- | --- | --- |
|  | rbxasset://SystemCursors/Arrow | Default clicking and selection. |
|  | rbxasset://SystemCursors/PointingHand | Hovering over an active link/button. |
|  | rbxasset://SystemCursors/OpenHand | Hovering over a draggable item. |
|  | rbxasset://SystemCursors/ClosedHand | Dragging an item. |
|  | rbxasset://SystemCursors/IBeam | Hovering in a text field. |
|  | rbxasset://SystemCursors/SizeNS | Hovering over a vertical resize handle. |
|  | rbxasset://SystemCursors/SizeEW | Hovering over a horizontal resize handle. |
|  | rbxasset://SystemCursors/SizeNESW | Hovering over a corner resize handle. |
|  | rbxasset://SystemCursors/SizeNWSE | Hovering over a corner resize handle. |
|  | rbxasset://SystemCursors/SizeAll | Hovering over a multi-direction resize handle. |
|  | rbxasset://SystemCursors/SplitNS | Hovering over a vertical "split" handle. |
|  | rbxasset://SystemCursors/SplitEW | Hovering over a horizontal "split" handle. |
|  | rbxasset://SystemCursors/Forbidden | Hovering over a locked/forbidden item. |
|  | rbxasset://SystemCursors/Wait | Indicating an action is in progress. |
|  | rbxasset://SystemCursors/Busy | Indicating the system is busy. |
|  | rbxasset://SystemCursors/Cross | Hovering over a pinpoint selection area. |

\* These appearances are approximations — the actual look is dependent on your operating system.

Code Samples

Dragon Mouse Icon

This example changes the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) mouse icon to look like
a dragon image.

```
local Players = game:GetService("Players")



local mouse = Players.LocalPlayer:GetMouse()



mouse.Icon = "http://www.roblox.com/asset?id=163023520"
```

Provide feedback

---

IconContent

Read Parallel

The content of the image used as the [Mouse](/docs/reference/engine/classes/Mouse) icon. Only supports
asset URIs.

Mouse.IconContent:[Content](/docs/reference/engine/datatypes/Content)

Icon is a property that determines the image used as the pointer. If
blank, a default arrow is used. While the cursor hovers over a
[GuiButton](/docs/reference/engine/classes/GuiButton), this property is temporarily ignored. This property
only supports asset URIs.

To hide the cursor entirely, do not use a transparent image –
instead, set [UserInputService.MouseIconEnabled](/docs/reference/engine/classes/UserInputService#MouseIconEnabled) to false.

For getting/setting the user mouse icon in experiences, you should use
[UserInputService.MouseIcon](/docs/reference/engine/classes/UserInputService#MouseIcon). [Mouse.Icon](/docs/reference/engine/classes/Mouse#Icon) will be deprecated
after the new API for plugins to set the mouse cursor is released.

##### Designing a Cursor

The following guidelines may prove useful when creating your own mouse
cursors:

* The dimensions of the image used determines the size of the cursor.
* The dimensions of the image should not exceed 256 pixels on any axis.
* The center of the image is where mouse inputs are issued.
* The default mouse image is 64x64 pixels, with the mouse taking up 17x24
  pixels of space.

##### System Cursors

When using a [PluginMouse](/docs/reference/engine/classes/PluginMouse) retrieved from [Plugin:GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse),
you can use the following icons similar to your system's default cursors,
such as hands, arrows, I-beams, etc. You can use these with GUI events
like [MouseEnter](/docs/reference/engine/classes/GuiObject#MouseEnter),
[MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave), and
[MouseButton1Down](/docs/reference/engine/classes/GuiButton#MouseButton1Down) to provide a
consistent Studio experience when interacting with certain kinds of GUI
components. Note that these only work for Studio plugins; they will not
work for other [Mouse](/docs/reference/engine/classes/Mouse) objects.

| Look\* | Asset | Suggested Use |
| --- | --- | --- |
|  | rbxasset://SystemCursors/Arrow | Default clicking and selection. |
|  | rbxasset://SystemCursors/PointingHand | Hovering over an active link/button. |
|  | rbxasset://SystemCursors/OpenHand | Hovering over a draggable item. |
|  | rbxasset://SystemCursors/ClosedHand | Dragging an item. |
|  | rbxasset://SystemCursors/IBeam | Hovering in a text field. |
|  | rbxasset://SystemCursors/SizeNS | Hovering over a vertical resize handle. |
|  | rbxasset://SystemCursors/SizeEW | Hovering over a horizontal resize handle. |
|  | rbxasset://SystemCursors/SizeNESW | Hovering over a corner resize handle. |
|  | rbxasset://SystemCursors/SizeNWSE | Hovering over a corner resize handle. |
|  | rbxasset://SystemCursors/SizeAll | Hovering over a multi-direction resize handle. |
|  | rbxasset://SystemCursors/SplitNS | Hovering over a vertical "split" handle. |
|  | rbxasset://SystemCursors/SplitEW | Hovering over a horizontal "split" handle. |
|  | rbxasset://SystemCursors/Forbidden | Hovering over a locked/forbidden item. |
|  | rbxasset://SystemCursors/Wait | Indicating an action is in progress. |
|  | rbxasset://SystemCursors/Busy | Indicating the system is busy. |
|  | rbxasset://SystemCursors/Cross | Hovering over a pinpoint selection area. |

\* These appearances are approximations — the actual look is dependent on your operating system.

Code Samples

Dragon Mouse Icon

This example changes the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) mouse icon to look like
a dragon image.

```
local Players = game:GetService("Players")



local mouse = Players.LocalPlayer:GetMouse()



mouse.Icon = "http://www.roblox.com/asset?id=163023520"
```

Provide feedback

---

Origin

Read Only

Not Replicated

Read Parallel

A [CFrame](/docs/reference/engine/datatypes/CFrame) positioned at the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) and
oriented toward the mouse's 3D position.

Mouse.Origin:[CFrame](/docs/reference/engine/datatypes/CFrame)

The origin [Mouse](/docs/reference/engine/classes/Mouse) property is a [CFrame](/docs/reference/engine/datatypes/CFrame) indicating where
the mouse originated from. It is positioned at the
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) and oriented toward the mouse's 3D
position.

[Mouse.UnitRay](/docs/reference/engine/classes/Mouse#UnitRay) starts at the same position as Origin, and extends
for a stud in the same direction.

```
local unitRay = mouse.UnitRay



local origin = mouse.Origin



-- unitRay.Direction = origin.p



-- unitRay.Direction ≈ origin.lookVector
```

For the position of the [Mouse](/docs/reference/engine/classes/Mouse) in 3D space, see [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit).

Code Samples

Mouse Origin vs Mouse Hit vs CurrentCamera Position

The code below visualizes the difference between [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Mouse.Origin](/docs/reference/engine/classes/Mouse#Origin). In order to do this, the code uses the
[Vector3](/docs/reference/engine/datatypes/Vector3) positions of the hit and origin [CFrame](/docs/reference/engine/datatypes/CFrame) values
using .p.

The difference is that the origin is "where the mouse came from" (its origin)
and the hit is the position where the mouse hits (is when the player presses
their mouse).

This example also visualizes that the mouse origin is very similar to the
position of the CurrentCamera by printing the magnitude (distance) between
the two positions.

```
local Players = game:GetService("Players")



local Workspace = game:GetService("Workspace")



local player = Players.LocalPlayer



local camera = Workspace.CurrentCamera



local mouse = player:GetMouse()



local camPos = camera.CFrame.Position



local function onButton1Down()



print("Mouse.Hit:", mouse.Hit.Position)



print("camPos:", camPos)



print("Mouse.Origin:", mouse.Origin.Position)



print("Magnitude:", (mouse.Origin.Position - camPos).Magnitude)



end



mouse.Button1Down:Connect(onButton1Down)
```

Provide feedback

---

Target

Read Only

Not Replicated

Read Parallel

The object in 3D space the [mouse](/docs/reference/engine/classes/Mouse) is pointing to.

Mouse.Target:[BasePart](/docs/reference/engine/classes/BasePart)

The object in 3D space the [mouse](/docs/reference/engine/classes/Mouse) is pointing to.

Note:

* If [Mouse.TargetFilter](/docs/reference/engine/classes/Mouse#TargetFilter) has been set, the target filter and its
  descendants will be ignored.
* When the mouse is not pointing at a [BasePart](/docs/reference/engine/classes/BasePart), for example when
  it is pointing at the sky, Target will be nil.
* Developers looking for the position of the mouse in 3D space should use
  [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit).

Code Samples

Color Randomizer Tool

The following code sample, when placed in StarterPlayerScripts will create a
tool in the player's backpack that, once equipped, will change the
[BasePart.BrickColor](/docs/reference/engine/classes/BasePart#BrickColor) of every BasePart the player clicks on.

```
local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



local backpack = localPlayer:WaitForChild("Backpack")



local tool = Instance.new("Tool")



tool.RequiresHandle = false



tool.CanBeDropped = false



tool.Parent = backpack



tool.Equipped:Connect(function(mouse)



mouse.Button1Down:Connect(function()



if mouse.Target and mouse.Target.Parent then



mouse.Target.BrickColor = BrickColor.random()



end



end)



end)
```

Provide feedback

---

target

Deprecated

Show details

---

TargetFilter

Read Parallel

Determines an object (and its descendants) to be ignored when determining
[Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) and [Mouse.Target](/docs/reference/engine/classes/Mouse#Target).

Mouse.TargetFilter:[Instance](/docs/reference/engine/datatypes/Instance)

This property determines an object to be ignored by the mouse when
calculating [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) and [Mouse.Target](/docs/reference/engine/classes/Mouse#Target). The descendants of
the object are also ignored, so it is possible to ignore multiple objects
so long as they are a descendant of the object to which this property is
set. This property is useful when filtering models containing special
effects or decorations that should not affect [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) or
[Mouse.Target](/docs/reference/engine/classes/Mouse#Target).

This property can be set to any [Instance](/docs/reference/engine/classes/Instance) or nil, for example:

```
local Players = game:GetService("Players")



local Workspace = game:GetService("Workspace")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



mouse.TargetFilter = Workspace.Model
```

Note that the [Character](/docs/reference/engine/classes/Player#Character) of the
[Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) is ignored by the mouse automatically.

Provide feedback

---

TargetSurface

Read Only

Not Replicated

Read Parallel

Indicates the [Enum.NormalId](/docs/reference/engine/enums/NormalId) of the [BasePart](/docs/reference/engine/classes/BasePart) surface at which the
mouse is pointing.

Mouse.TargetSurface:[Enum.NormalId](/docs/reference/engine/enums/NormalId)

This property indicates the [Enum.NormalId](/docs/reference/engine/enums/NormalId) of the [BasePart](/docs/reference/engine/classes/BasePart)
surface at which the mouse is pointing. This property is derived from the
world position of mouse ([Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit)) and the part toward which the
mouse is pointing ([Mouse.Target](/docs/reference/engine/classes/Mouse#Target)).

This property isn't meaningful when the mouse is not pointing at a part,
for example when the mouse is pointing at the sky. At the moment, this
property is set to 'Right' under these circumstances. Before using this
property, check that the mouse's target is not nil.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



-- Check that there exists a part at which the mouse is pointing



if mouse.Target then



print("The mouse is pointing to the " .. mouse.TargetSurface.Name .. " side of " .. mouse.Target.Name)



else



print("The mouse is not pointing at anything.")



end
```

Code Samples

Surface Randomizer

The code in this sample, when placed in a LocalScript inside
StarterPlayerScripts will set the surface of any BasePart clicked on to a
random surface.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local surfaceTypes = {



Enum.SurfaceType.Smooth,



Enum.SurfaceType.Glue,



Enum.SurfaceType.Weld,



Enum.SurfaceType.Studs,



Enum.SurfaceType.Inlet,



Enum.SurfaceType.Universal,



Enum.SurfaceType.Hinge,



Enum.SurfaceType.Motor,



}



local function onMouseClick()



-- make sure the mouse is pointing at a part



local target = mouse.Target



if not target then



return



end



local surfaceType = surfaceTypes[math.random(1, #surfaceTypes)]



local surface = mouse.TargetSurface



local propertyName = surface.Name .. "Surface"



mouse.Target[propertyName] = surfaceType



end



mouse.Button1Down:Connect(onMouseClick)
```

Provide feedback

---

UnitRay

Read Only

Not Replicated

Read Parallel

A [Ray](/docs/reference/engine/datatypes/Ray) directed towards the mouse's world position, originating
from the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) world position.

Mouse.UnitRay:[Ray](/docs/reference/engine/datatypes/Ray)

The UnitRay property is a [Ray](/docs/reference/engine/datatypes/Ray) directed toward the mouse's
position in 3D space (described by [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit)). It originates from
the [CFrame](/docs/reference/engine/classes/Camera#CFrame) of the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera).
Like all unit rays, it has a distance of 1.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



print(mouse.UnitRay.Direction.Magnitude) -- Always 1
```

Provide feedback

---

ViewSizeX

Read Only

Not Replicated

Read Parallel

Describes the width of the game window in pixels.

Mouse.ViewSizeX:[number](/docs/luau/numbers)

The ViewSizeX property describes the horizontal component of the game
window's size in pixels.

Code Samples

Normalized Mouse Position

This code sample shows how you can create a [Vector2](/docs/reference/engine/datatypes/Vector2) representing
the Mouse object's position on screen ([X()](/docs/reference/engine/classes/Mouse#X) and
[Y()](/docs/reference/engine/classes/Mouse#Y)) and the size of the screen itself
([ViewSizeX()](/docs/reference/engine/classes/Mouse#ViewSizeX) and [ViewSizeY()](/docs/reference/engine/classes/Mouse#ViewSizeY)).
Using these, you can normalize the position of the mouse on-screen such that
the top-left just under the topbar maps to (0, 0) and the bottom-right maps to
(1, 1). This normalized position is calculated and printed as the mouse moves
using the [Move()](/docs/reference/engine/classes/Mouse#Move) event.

```
local Players = game:GetService("Players")



-- Note: You should use ContextActionService or UserInputService instead of



-- the Mouse object for accomplishing this task.



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local function onMouseMove()



-- Construct Vector2 objects for the mouse's position and screen size



local position = Vector2.new(mouse.X, mouse.Y)



local size = Vector2.new(mouse.ViewSizeX, mouse.ViewSizeY)



-- A normalized position will map the top left (just under the topbar)



-- to (0, 0) the bottom right to (1, 1), and the center to (0.5, 0.5).



-- This is calculated by dividing the position by the total size.



local normalizedPosition = position / size



print(normalizedPosition)



end



mouse.Move:Connect(onMouseMove)
```

Provide feedback

---

ViewSizeY

Read Only

Not Replicated

Read Parallel

Describes the height of the game window in pixels.

Mouse.ViewSizeY:[number](/docs/luau/numbers)

The ViewSizeY property describes the vertical component of the game
window's size in pixels. This length includes the space used by the
topbar.

Code Samples

Normalized Mouse Position

This code sample shows how you can create a [Vector2](/docs/reference/engine/datatypes/Vector2) representing
the Mouse object's position on screen ([X()](/docs/reference/engine/classes/Mouse#X) and
[Y()](/docs/reference/engine/classes/Mouse#Y)) and the size of the screen itself
([ViewSizeX()](/docs/reference/engine/classes/Mouse#ViewSizeX) and [ViewSizeY()](/docs/reference/engine/classes/Mouse#ViewSizeY)).
Using these, you can normalize the position of the mouse on-screen such that
the top-left just under the topbar maps to (0, 0) and the bottom-right maps to
(1, 1). This normalized position is calculated and printed as the mouse moves
using the [Move()](/docs/reference/engine/classes/Mouse#Move) event.

```
local Players = game:GetService("Players")



-- Note: You should use ContextActionService or UserInputService instead of



-- the Mouse object for accomplishing this task.



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local function onMouseMove()



-- Construct Vector2 objects for the mouse's position and screen size



local position = Vector2.new(mouse.X, mouse.Y)



local size = Vector2.new(mouse.ViewSizeX, mouse.ViewSizeY)



-- A normalized position will map the top left (just under the topbar)



-- to (0, 0) the bottom right to (1, 1), and the center to (0.5, 0.5).



-- This is calculated by dividing the position by the total size.



local normalizedPosition = position / size



print(normalizedPosition)



end



mouse.Move:Connect(onMouseMove)
```

Provide feedback

---

X

Read Only

Not Replicated

Read Parallel

Describes the X (horizontal) component of the mouse's position on the
screen.

Mouse.X:[number](/docs/luau/numbers)

When detecting changes in the mouse's position on-screen, it is
recommended that you use [ContextActionService:BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction) with
[Enum.UserInputType.MouseMovement](/docs/reference/engine/enums/UserInputType#MouseMovement) or
[UserInputService.InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged), which both describe the position of
the mouse using the [Position](/docs/reference/engine/classes/InputObject#Position) (a
[Vector3](/docs/reference/engine/datatypes/Vector3)) of an [InputObject](/docs/reference/engine/classes/InputObject), instead of using this and
related properties.

The X property describes the horizontal component of the mouse's position
on the screen. The position is measured in pixels relative to the top left
corner, under the topbar. This property can be used in conjunction with
[Mouse.Y](/docs/reference/engine/classes/Mouse#Y) to produce a [Vector2](/docs/reference/engine/datatypes/Vector2) representing the mouse's
position:

```
local position = Vector2.new(mouse.X, mouse.Y)
```

This property does not fire [Changed](/docs/reference/engine/classes/Object#Changed) or the signal
returned from
[GetPropertyChangedSignal](/docs/reference/engine/classes/Object#GetPropertyChangedSignal). Use
the [Mouse.Move](/docs/reference/engine/classes/Mouse#Move) event instead.

Code Samples

Normalized Mouse Position

This code sample shows how you can create a [Vector2](/docs/reference/engine/datatypes/Vector2) representing
the Mouse object's position on screen ([X()](/docs/reference/engine/classes/Mouse#X) and
[Y()](/docs/reference/engine/classes/Mouse#Y)) and the size of the screen itself
([ViewSizeX()](/docs/reference/engine/classes/Mouse#ViewSizeX) and [ViewSizeY()](/docs/reference/engine/classes/Mouse#ViewSizeY)).
Using these, you can normalize the position of the mouse on-screen such that
the top-left just under the topbar maps to (0, 0) and the bottom-right maps to
(1, 1). This normalized position is calculated and printed as the mouse moves
using the [Move()](/docs/reference/engine/classes/Mouse#Move) event.

```
local Players = game:GetService("Players")



-- Note: You should use ContextActionService or UserInputService instead of



-- the Mouse object for accomplishing this task.



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local function onMouseMove()



-- Construct Vector2 objects for the mouse's position and screen size



local position = Vector2.new(mouse.X, mouse.Y)



local size = Vector2.new(mouse.ViewSizeX, mouse.ViewSizeY)



-- A normalized position will map the top left (just under the topbar)



-- to (0, 0) the bottom right to (1, 1), and the center to (0.5, 0.5).



-- This is calculated by dividing the position by the total size.



local normalizedPosition = position / size



print(normalizedPosition)



end



mouse.Move:Connect(onMouseMove)
```

Provide feedback

---

Y

Read Only

Not Replicated

Read Parallel

Describes the Y (vertical) component of the mouse's screen position.

Mouse.Y:[number](/docs/luau/numbers)

When detecting changes in the mouse's position on-screen, it is
recommended that you use [ContextActionService:BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction) with
[Enum.UserInputType.MouseMovement](/docs/reference/engine/enums/UserInputType#MouseMovement) or
[UserInputService.InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged), which both describe the position of
the mouse using the [Position](/docs/reference/engine/classes/InputObject#Position) (a
[Vector3](/docs/reference/engine/datatypes/Vector3)) of an [InputObject](/docs/reference/engine/classes/InputObject), instead of using this and
related properties.

The Y property describes the vertical component of the mouse's position on
the screen. The position is measured in pixels relative to the top left
corner, under the topbar. This property can be used in conjunction with
[Mouse.X](/docs/reference/engine/classes/Mouse#X) to produce a [Vector2](/docs/reference/engine/datatypes/Vector2) representing the mouse's
position:

```
local position = Vector2.new(mouse.X, mouse.Y)
```

This property does not fire [Changed](/docs/reference/engine/classes/Object#Changed) or the signal
returned from
[GetPropertyChangedSignal](/docs/reference/engine/classes/Object#GetPropertyChangedSignal). Use
the [Mouse.Move](/docs/reference/engine/classes/Mouse#Move) event instead.

Code Samples

Normalized Mouse Position

This code sample shows how you can create a [Vector2](/docs/reference/engine/datatypes/Vector2) representing
the Mouse object's position on screen ([X()](/docs/reference/engine/classes/Mouse#X) and
[Y()](/docs/reference/engine/classes/Mouse#Y)) and the size of the screen itself
([ViewSizeX()](/docs/reference/engine/classes/Mouse#ViewSizeX) and [ViewSizeY()](/docs/reference/engine/classes/Mouse#ViewSizeY)).
Using these, you can normalize the position of the mouse on-screen such that
the top-left just under the topbar maps to (0, 0) and the bottom-right maps to
(1, 1). This normalized position is calculated and printed as the mouse moves
using the [Move()](/docs/reference/engine/classes/Mouse#Move) event.

```
local Players = game:GetService("Players")



-- Note: You should use ContextActionService or UserInputService instead of



-- the Mouse object for accomplishing this task.



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local function onMouseMove()



-- Construct Vector2 objects for the mouse's position and screen size



local position = Vector2.new(mouse.X, mouse.Y)



local size = Vector2.new(mouse.ViewSizeX, mouse.ViewSizeY)



-- A normalized position will map the top left (just under the topbar)



-- to (0, 0) the bottom right to (1, 1), and the center to (0.5, 0.5).



-- This is calculated by dividing the position by the total size.



local normalizedPosition = position / size



print(normalizedPosition)



end



mouse.Move:Connect(onMouseMove)
```

Provide feedback

---

Events

Button1Down

Fires when the left mouse button is pressed.

Mouse.Button1Down():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the player presses their left mouse button. Note
that this can be accessed from a [Tool](/docs/reference/engine/classes/Tool); for example, when placed in
a [LocalScript](/docs/reference/engine/classes/LocalScript), the code below prints Button1Down whenever the
left mouse button is pressed.

```
local tool = script.Parent  -- Make sure this is a Tool object



tool.Equipped:Connect(function(mouse)



mouse.Button1Down:Connect(function()



print("Button1Down")



end)



end)
```

You can find out the position of the mouse in world space and if it's
pointing at any [BasePart](/docs/reference/engine/classes/BasePart) using the [Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Target](/docs/reference/engine/classes/Mouse#Target) properties.

Provide feedback

---

Button1Up

Fires when the left mouse button is released.

Mouse.Button1Up():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the player releases their left mouse button. Note
that this can be accessed from a [Tool](/docs/reference/engine/classes/Tool); for example, when placed in
a [LocalScript](/docs/reference/engine/classes/LocalScript), the code below prints Button1Up whenever the left
mouse button is released.

```
local tool = script.Parent  -- Make sure this is a Tool object



tool.Equipped:Connect(function(mouse)



mouse.Button1Up:Connect(function()



print("Button1Up")



end)



end)
```

You can find out the position of the mouse in world space and if it's
pointing at any [BasePart](/docs/reference/engine/classes/BasePart) using the [Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Target](/docs/reference/engine/classes/Mouse#Target) properties.

Provide feedback

---

Button2Down

Fires when the right mouse button is pressed.

Mouse.Button2Down():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the player presses their right mouse button. Note
that this can be accessed from a [Tool](/docs/reference/engine/classes/Tool); for example, when placed in
a [LocalScript](/docs/reference/engine/classes/LocalScript), the code below prints Button2Down whenever the
right mouse button is pressed.

```
local tool = script.Parent  -- Make sure this is a Tool object



tool.Equipped:Connect(function(mouse)



mouse.Button2Down:Connect(function()



print("Button2Down")



end)



end)
```

You can find out the position of the mouse in world space and if it's
pointing at any [BasePart](/docs/reference/engine/classes/BasePart) using the [Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Target](/docs/reference/engine/classes/Mouse#Target) properties.

Provide feedback

---

Button2Up

Fired when the right mouse button is released.

Mouse.Button2Up():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the player releases their right mouse button. Note
that this can be accessed from a [Tool](/docs/reference/engine/classes/Tool); for example, when placed in
a [LocalScript](/docs/reference/engine/classes/LocalScript), the code below prints Button2Up whenever the
right mouse button is released.

```
local tool = script.Parent  -- Make sure this is a Tool object



tool.Equipped:Connect(function(mouse)



mouse.Button2Up:Connect(function()



print("Button2Up")



end)



end)
```

You can find out the position of the mouse in world space and if it's
pointing at any [BasePart](/docs/reference/engine/classes/BasePart) using the [Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Target](/docs/reference/engine/classes/Mouse#Target) properties.

Provide feedback

---

Idle

Fired during every heartbeat that the mouse isn't being passed to another
mouse event.

Mouse.Idle():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fired during every heartbeat that the mouse isn't being passed to another
mouse event.

Note, this event should not be used to determine when the mouse is still.
As it fires every heartbeat it will fire between [Mouse.Move](/docs/reference/engine/classes/Mouse#Move)
events.

For information on how to obtain the [Mouse](/docs/reference/engine/classes/Mouse) object, please see the
[Mouse](/docs/reference/engine/classes/Mouse) page.

Developers can find out the position of the mouse in world-space, and if
it is pointing at any [BasePart](/docs/reference/engine/classes/BasePart) using the [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Mouse.Target](/docs/reference/engine/classes/Mouse#Target) properties.

Note, developers are recommended to use [UserInputService](/docs/reference/engine/classes/UserInputService) instead
of the [Mouse](/docs/reference/engine/classes/Mouse) object in new work.

Code Samples

Mouse.Idle

This example demonstrates how mouse events are passed during each frame

```
local Players = game:GetService("Players")



local RunService = game:GetService("RunService")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local events = {



"Button1Down",



"Button1Up",



"Button2Down",



"Button2Up",



"Idle",



"Move",



"WheelBackward",



"WheelForward",



"KeyDown",



"KeyUp",



}



local currentEvent



local frame = 0



local function processInput()



frame = frame + 1



print("Frame", frame, "- mouse event was passed to", currentEvent)



end



for _, event in pairs(events) do



mouse[event]:Connect(function()



currentEvent = event



end)



end



RunService:BindToRenderStep("ProcessInput", Enum.RenderPriority.Input.Value, processInput)
```

Provide feedback

---

KeyDown

Deprecated

Show details

---

keyDown

Deprecated

Show details

---

KeyUp

Deprecated

Show details

---

Move

Fired when the mouse is moved.

Mouse.Move():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fired when the mouse is moved.

Note, this event is fired when the mouse's position is updated, therefore
it will fire repeatedly while being moved.

For information on how to obtain the [Mouse](/docs/reference/engine/classes/Mouse) object, please see the
[Mouse](/docs/reference/engine/classes/Mouse) page.

Developers can find out the position of the mouse in world-space, and if
it is pointing at any [BasePart](/docs/reference/engine/classes/BasePart) using the [Mouse.Hit](/docs/reference/engine/classes/Mouse#Hit) and
[Mouse.Target](/docs/reference/engine/classes/Mouse#Target) properties.

```
mouse.Move:Connect(function()



local position = mouse.Hit.p



local target = mouse.Target



print(target, position)



end)
```

Note, developers are recommended to use [UserInputService](/docs/reference/engine/classes/UserInputService) instead
of the [Mouse](/docs/reference/engine/classes/Mouse) object in new work.

Code Samples

Move Parts with the Mouse

The example below allows the [local player](/docs/reference/engine/classes/Players#LocalPlayer) to move
parts with their mouse.

When the player presses their left mouse button over a part, that part is the
[mouse's target](/docs/reference/engine/classes/Mouse#Target) and becomes the *point*. Until the player
releases their left mouse button, that part will move to the mouse's world
position when the player moves their mouse.

Note that the [Mouse.TargetFilter](/docs/reference/engine/classes/Mouse#TargetFilter) property allows the code to ignore
the part being moved when determining the mouse's world position.

The code should work as expected when placed in a LocalScript.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local point



local down



local function selectPart()



if mouse.Target and not mouse.Target.Locked then



point = mouse.Target



mouse.TargetFilter = point



down = true



end



end



local function movePart()



if down and point then



local posX, posY, posZ = mouse.Hit.X, mouse.Hit.Y, mouse.Hit.Z



point.Position = Vector3.new(posX, posY, posZ)



end



end



local function deselectPart()



down = false



point = nil



mouse.TargetFilter = nil



end



mouse.Button1Down:Connect(selectPart)



mouse.Button1Up:Connect(deselectPart)



mouse.Move:Connect(movePart)
```

Provide feedback

---

WheelBackward

Fires when the mouse wheel is scrolled backwards.

Mouse.WheelBackward():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

The WheelBackward event fires when the mouse wheel is scrolled backwards.
Possible uses for this event include toggling a gun's scope in a first
person shooter (FPS) or zooming the player's camera.

This can be used alongside the scrolling forward event,
[Mouse.WheelForward](/docs/reference/engine/classes/Mouse#WheelForward).

For information on how to obtain the [Mouse](/docs/reference/engine/classes/Mouse) object, please see the
[Mouse](/docs/reference/engine/classes/Mouse) page.

Note, developers are recommended to use [UserInputService](/docs/reference/engine/classes/UserInputService) instead
of the [Mouse](/docs/reference/engine/classes/Mouse) object in new work.

Code Samples

Mouse.WheelBackward

The below example assumes that you have already got the player's mouse (and
set it as a variable named 'mouse'), whether by use of a [Tool](/docs/reference/engine/classes/Tool),
[HopperBin](/docs/reference/engine/classes/HopperBin) or the [Player:GetMouse()](/docs/reference/engine/classes/Player#GetMouse) method. It will print
"Wheel went backwards!" when the player scrolls backwards.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local function onWheelBackward()



print("Wheel went backwards!")



end



mouse.WheelBackward:Connect(onWheelBackward)
```

Provide feedback

---

WheelForward

Fires when the mouse wheel is scrolled forwards.

Mouse.WheelForward():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

The WheelForward event fires when the mouse wheel is scrolled forwards.
Possible uses for this event include toggling a gun's scope in a first
person shooter (FPS) or zooming the player's camera.

This can be used alongside the scrolling backward event,
[Mouse.WheelBackward](/docs/reference/engine/classes/Mouse#WheelBackward).

For information on how to obtain the [Mouse](/docs/reference/engine/classes/Mouse) object, please see the
[Mouse](/docs/reference/engine/classes/Mouse) page.

Note, developers are recommended to use [UserInputService](/docs/reference/engine/classes/UserInputService) instead
of the [Mouse](/docs/reference/engine/classes/Mouse) object in new work.

Code Samples

Mouse.WheelForward

The below example assumes that you have already got the player's mouse (and
set it as a variable named 'mouse'), whether by use of a Tool, HopperBin
or the [Player:GetMouse()](/docs/reference/engine/classes/Player#GetMouse) method. It will print "Wheel went forward!"
when the player scrolls forwards.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local function onWheelForward()



print("Wheel went forward!")



end



mouse.WheelForward:Connect(onWheelForward)
```

Provide feedback

---