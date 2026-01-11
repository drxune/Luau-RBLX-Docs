# Camera | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Camera
Scraped: 2026-01-11T02:40:28.445192Z

## Tags
- Not Replicated

## Inherits
- PVInstance
- Camera
- Instance
- Object
- Workspace
- Workspace.CurrentCamera
- CFrame
- CameraType
- CameraSubject
- FieldOfView
- Focus
- Cameras
- Folder
- Model
- CurrentCamera
- Humanoid
- BasePart
- Instances
- Humanoid.CameraOffset
- VehicleSeats
- GetRenderCFrame()
- RunService:BindToRenderStep()
- Tween
- ViewportSize
- PointLights
- VRService:GetUserCFrame()
- VRService:RecenterUserHeadCFrame()
- VRService.AutomaticScaling
- Humanoid.HeadScale
- NumberValue
- AbsoluteSize
- ScreenGui
- ScreenInsets
- DiagonalFieldOfView
- PreRender
- ViewportFrames
- BaseParts
- WorldRoot:Raycast()
- Terrain
- HeadLocked
- ViewportPointToRay()
- ViewportFrame
- GuiObject.AbsolutePosition
- ScreenPointToRay()
- WorldToViewportPoint()
- ScreenGui.IgnoreGuiInset
- WorldToScreenPoint()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PVInstance](/docs/reference/engine/classes/PVInstance)
6. /
7. [Camera](/docs/reference/engine/classes/Camera)

English

Feedback

Engine Class

![Camera](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Camera-Dark.webp)Camera

A class which defines a view of the 3D world.

Not Replicated

---

Summary

Properties

|  |
| --- |
| [CameraSubject](#CameraSubject):[Instance](/docs/reference/engine/datatypes/Instance) |
| [CameraType](#CameraType):[Enum.CameraType](/docs/reference/engine/enums/CameraType) |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [CoordinateFrame](#CoordinateFrame):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [DiagonalFieldOfView](#DiagonalFieldOfView):[number](/docs/luau/numbers) |
| [FieldOfView](#FieldOfView):[number](/docs/luau/numbers) |
| [FieldOfViewMode](#FieldOfViewMode):[Enum.FieldOfViewMode](/docs/reference/engine/enums/FieldOfViewMode) |
| [Focus](#Focus):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [focus](#focus):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [HeadLocked](#HeadLocked):[boolean](/docs/luau/booleans) |
| [HeadScale](#HeadScale):[number](/docs/luau/numbers) |
| [MaxAxisFieldOfView](#MaxAxisFieldOfView):[number](/docs/luau/numbers) |
| [NearPlaneZ](#NearPlaneZ):[number](/docs/luau/numbers) |
| [ViewportSize](#ViewportSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [VRTiltAndRollEnabled](#VRTiltAndRollEnabled):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetLargestCutoffDistance](#GetLargestCutoffDistance)(ignoreList: Instances):[number](/docs/luau/numbers)  Deprecated |
| [GetPanSpeed](#GetPanSpeed)():[number](/docs/luau/numbers)  Deprecated |
| [GetPartsObscuringTarget](#GetPartsObscuringTarget)(castPoints: [Array](/docs/luau/tables#arrays),ignoreList: Instances):Instances |
| [GetRenderCFrame](#GetRenderCFrame)():[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [GetRoll](#GetRoll)():[number](/docs/luau/numbers)  Deprecated |
| [GetTiltSpeed](#GetTiltSpeed)():[number](/docs/luau/numbers)  Deprecated |
| [Interpolate](#Interpolate)(endPos: [CFrame](/docs/reference/engine/datatypes/CFrame),endFocus: [CFrame](/docs/reference/engine/datatypes/CFrame),duration: [number](/docs/luau/numbers)):()  Deprecated |
| [PanUnits](#PanUnits)(units: [number](/docs/luau/numbers)):()  Deprecated |
| [ScreenPointToRay](#ScreenPointToRay)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),depth: [number](/docs/luau/numbers)):[Ray](/docs/reference/engine/datatypes/Ray) |
| [SetCameraPanMode](#SetCameraPanMode)(mode: [Enum.CameraPanMode](/docs/reference/engine/enums/CameraPanMode)):()  Deprecated |
| [SetRoll](#SetRoll)(rollAngle: [number](/docs/luau/numbers)):()  Deprecated |
| [TiltUnits](#TiltUnits)(units: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [ViewportPointToRay](#ViewportPointToRay)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),depth: [number](/docs/luau/numbers)):[Ray](/docs/reference/engine/datatypes/Ray) |
| [WorldToScreenPoint](#WorldToScreenPoint)(worldPoint: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Tuple](/docs/luau/tuples) |
| [WorldToViewportPoint](#WorldToViewportPoint)(worldPoint: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Tuple](/docs/luau/tuples) |
| [ZoomToExtents](#ZoomToExtents)(boundingBoxCFrame: [CFrame](/docs/reference/engine/datatypes/CFrame),boundingBoxSize: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |

Events

|  |
| --- |
| [InterpolationFinished](#InterpolationFinished)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Camera object defines a view of the 3D world. In a running experience,
each client has its own Camera object which resides in that client's local
[Workspace](/docs/reference/engine/classes/Workspace), accessible through the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera)
property.

The most important camera properties are:

* [CFrame](/docs/reference/engine/classes/Camera#CFrame) which represents the position and orientation
  of the camera.
* [CameraType](/docs/reference/engine/classes/Camera#CameraType) which is read by the experience's
  camera scripts and determines how the camera should update each frame.
* [CameraSubject](/docs/reference/engine/classes/Camera#CameraSubject) which is read by the experience's
  camera scripts and determines what object the camera should follow.
* [FieldOfView](/docs/reference/engine/classes/Camera#FieldOfView) which represents the visible extent
  of the observable world.
* [Focus](/docs/reference/engine/classes/Camera#Focus) which represents the point the camera is looking
  at. It's important this property is set, as certain visuals will be more
  detailed and will update more frequently depending on how close they are to
  the focus point.

See [Customizing the Camera](/docs/workspace/camera) for more
information on how to adjust and customize the camera's behavior.

#### Storing Multiple Cameras

Note that when changing [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) to a new
[Camera](/docs/reference/engine/classes/Camera), all other [Cameras](/docs/reference/engine/classes/Camera) directly descending from
[Workspace](/docs/reference/engine/classes/Workspace) will be destroyed. If you need to store multiple cameras and
swap between them on demand, it's recommended that you store them in a
[Folder](/docs/reference/engine/classes/Folder) or [Model](/docs/reference/engine/classes/Model) under [Workspace](/docs/reference/engine/classes/Workspace), inside which they
will remain even when [CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) is
changed.

---

API Reference

Properties

CameraSubject

Read Parallel

The [Humanoid](/docs/reference/engine/classes/Humanoid) or [BasePart](/docs/reference/engine/classes/BasePart) that is the [Camera](/docs/reference/engine/classes/Camera)
subject.

Camera.CameraSubject:[Instance](/docs/reference/engine/datatypes/Instance)

CameraSubject accepts a variety of [Instances](/docs/reference/engine/classes/Instance). The
default camera scripts respond differently to the available settings:

* By default, the camera scripts follow the local character's
  [Humanoid](/docs/reference/engine/classes/Humanoid), factoring in the humanoid's current state and
  [Humanoid.CameraOffset](/docs/reference/engine/classes/Humanoid#CameraOffset).
* When set to a [BasePart](/docs/reference/engine/classes/BasePart), the camera scripts follow its position,
  with a vertical offset in the case of [VehicleSeats](/docs/reference/engine/classes/VehicleSeat).

CameraSubject cannot be set to nil. Attempting to do so will revert it
to its previous value.

To restore CameraSubject to its default value, set it to the local
character's [Humanoid](/docs/reference/engine/classes/Humanoid):

```
local Players = game:GetService("Players")



local Workspace = game:GetService("Workspace")



local localPlayer = Players.LocalPlayer



local camera = Workspace.CurrentCamera



local function resetCameraSubject()



if camera and localPlayer.Character then



local humanoid = localPlayer.Character:FindFirstChildWhichIsA("Humanoid")



if humanoid then



camera.CameraSubject = humanoid



end



end



end
```

Provide feedback

---

CameraType

Read Parallel

Specifies the [Enum.CameraType](/docs/reference/engine/enums/CameraType) to be read by the camera scripts.

Camera.CameraType:[Enum.CameraType](/docs/reference/engine/enums/CameraType)

The default Roblox camera scripts have several built-in behaviors. Setting
this property toggles between the various [Enum.CameraType](/docs/reference/engine/enums/CameraType) behaviors.
Note that some camera types require a valid
[CameraSubject](/docs/reference/engine/classes/Camera#CameraSubject) to work correctly.

The default camera scripts will not move or update the camera if
CameraType is set to [Enum.CameraType.Scriptable](/docs/reference/engine/enums/CameraType#Scriptable). For more information
on positioning and orienting the camera manually, see
[CFrame](/docs/reference/engine/classes/Camera#CFrame).

For all CameraType settings except [Enum.CameraType.Scriptable](/docs/reference/engine/enums/CameraType#Scriptable), the
[CameraSubject](/docs/reference/engine/classes/Camera#CameraSubject) property represents the object
whose position the camera's [Focus](/docs/reference/engine/classes/Camera#Focus) is set to.

Provide feedback

---

CFrame

Read Parallel

The [CFrame](/docs/reference/engine/datatypes/CFrame) of the [Camera](/docs/reference/engine/classes/Camera), defining its position and
orientation in the 3D world.

Camera.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property is the [CFrame](/docs/reference/engine/datatypes/CFrame) of the [Camera](/docs/reference/engine/classes/Camera), defining its
position and orientation in the 3D world. Note that some transformations,
such as the rotation of the head when using VR devices, are not reflected
in this property, so you should use
[GetRenderCFrame()](/docs/reference/engine/classes/Camera#GetRenderCFrame) to obtain the "true"
[CFrame](/docs/reference/engine/datatypes/CFrame) of the camera.

You can move the camera by setting this property. However, the default
camera scripts also set it, so you should either:

* Set the camera [CameraType](/docs/reference/engine/classes/Camera#CameraType) to
  [Enum.CameraType.Scriptable](/docs/reference/engine/enums/CameraType#Scriptable) so that the default camera scripts will not
  update the camera's [CFrame](/docs/reference/engine/datatypes/CFrame). This method is simplest and
  recommended in most cases.
* Completely replace the default camera scripts with alternatives. This
  approach is only recommended if you do not need any default camera
  functionality.

The most intuitive way to position and orient the [Camera](/docs/reference/engine/classes/Camera) is by
using the [CFrame.lookAt()](/docs/reference/engine/datatypes/CFrame#lookAt) constructor. In the following
example, the [Camera](/docs/reference/engine/classes/Camera) is positioned at
[Vector3.new(0, 10, 0)](/docs/reference/engine/datatypes/Vector3#new) and is oriented to be looking towards
[Vector3.new(10, 0, 0)](/docs/reference/engine/datatypes/Vector3#new).

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



camera.CameraType = Enum.CameraType.Scriptable



local pos = Vector3.new(0, 10, 0)



local lookAtPos = Vector3.new(10, 0, 0)



Workspace.CurrentCamera.CFrame = CFrame.lookAt(pos, lookAtPos)
```

Although the camera can be placed in the manner demonstrated above, you
may want to animate it to move smoothly from one [CFrame](/docs/reference/engine/datatypes/CFrame) to
another. For this, you can either:

* Set the camera's position/orientation every frame with
  [RunService:BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep) and the [CFrame:Lerp()](/docs/reference/engine/datatypes/CFrame#Lerp)
  method.
* Create and play a [Tween](/docs/reference/engine/classes/Tween) that animates the position/orientation
  of the camera:

  ```
  local Players = game:GetService("Players")



  local TweenService = game:GetService("TweenService")



  local Workspace = game:GetService("Workspace")



  local camera = Workspace.CurrentCamera



  camera.CameraType = Enum.CameraType.Scriptable



  local player = Players.LocalPlayer



  local character = player.Character



  if not character or character.Parent == nil then



  character = player.CharacterAdded:Wait()



  end



  local pos = camera.CFrame * Vector3.new(0, 20, 0)



  local lookAtPos = character.PrimaryPart.Position



  local targetCFrame = CFrame.lookAt(pos, lookAtPos)



  local tween = TweenService:Create(camera, TweenInfo.new(2), {CFrame = targetCFrame})



  tween:Play()
  ```

Provide feedback

---

CoordinateFrame

Deprecated

Show details

---

DiagonalFieldOfView

Not Replicated

Read Parallel

Sets the angle of the camera's diagonal field of view.

Camera.DiagonalFieldOfView:[number](/docs/luau/numbers)

Sets how many degrees in the diagonal direction (from one corner of the
viewport to its opposite corner) the camera can view. See
[FieldOfView](/docs/reference/engine/classes/Camera#FieldOfView) for a more general explanation of
field of view.

Note that DiagonalFieldOfView represents the field of view that is
visible by the [Camera](/docs/reference/engine/classes/Camera) rendering into the fullscreen area which may
be occluded by notches or screen cutouts on some devices. See
[ViewportSize](/docs/reference/engine/classes/Camera#ViewportSize) for more information.

Provide feedback

---

FieldOfView

Read Parallel

Sets the angle of the camera's vertical field of view.

Camera.FieldOfView:[number](/docs/luau/numbers)

The FieldOfView (FOV) property sets how many degrees in the vertical
direction the camera can view. This property is clamped between 1 and
120 degrees and defaults at 70. Very low or very high fields of view
are not recommended as they can be disorientating to players.

Note that uniform scaling is enforced, meaning the vertical and horizontal
field of view are always related by the aspect ratio of the screen.

Suggested uses for FieldOfView include:

* Reducing FOV to give the impression of magnification, for example when
  using binoculars.
* Increasing FOV when the player is "sprinting" to give the impression of
  a lack of control.

Note that FieldOfView represents the field of view that is visible by
the [Camera](/docs/reference/engine/classes/Camera) rendering into the fullscreen area which may be
occluded by notches or screen cutouts on some devices. See
[ViewportSize](/docs/reference/engine/classes/Camera#ViewportSize) for more information.

Provide feedback

---

FieldOfViewMode

Read Parallel

Determines the FOV value of the [Camera](/docs/reference/engine/classes/Camera) that's invariant under
viewport size changes.

Camera.FieldOfViewMode:[Enum.FieldOfViewMode](/docs/reference/engine/enums/FieldOfViewMode)

The camera's [FieldOfView](/docs/reference/engine/classes/Camera#FieldOfView) (FOV) must be updated
to reflect [ViewportSize](/docs/reference/engine/classes/Camera#ViewportSize) changes. The value of
FieldOfViewMode determines which FOV value will be kept constant.

For example, when this property is set to [Enum.FieldOfViewMode.Vertical](/docs/reference/engine/enums/FieldOfViewMode#Vertical),
the horizontal FOV is updated when the viewport is resized, but the
vertical FOV is kept constant. If this property is set to
[Enum.FieldOfViewMode.Diagonal](/docs/reference/engine/enums/FieldOfViewMode#Diagonal), both horizontal and vertical FOV might be
changed to keep the diagonal FOV constant.

Provide feedback

---

Focus

Read Parallel

Sets the area in 3D space that is prioritized by Roblox's graphical
systems.

Camera.Focus:[CFrame](/docs/reference/engine/datatypes/CFrame)

Certain graphical operations the engine performs, such as updating
lighting, can take time or computational effort to complete. The camera's
Focus property tells the engine which area in 3D space to prioritize
when performing such operations. For example, dynamic lighting from
objects such as [PointLights](/docs/reference/engine/classes/PointLight) may not render at distances
far from the focus.

The default Roblox camera scripts automatically set Focus to follow the
[CameraSubject](/docs/reference/engine/classes/Camera#CameraSubject) (usually a [Humanoid](/docs/reference/engine/classes/Humanoid)).
However, Focus will not automatically update when
[CameraType](/docs/reference/engine/classes/Camera#CameraType) is set to
[Enum.CameraType.Scriptable](/docs/reference/engine/enums/CameraType#Scriptable) or when the default camera scripts are not
being used. In these cases, you should update Focus every frame, using
[RunService:BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep) method at the
[Enum.RenderPriority.Camera](/docs/reference/engine/enums/RenderPriority#Camera) priority.

Focus has no bearing on the position or orientation of the camera; see
[CFrame](/docs/reference/engine/classes/Camera#CFrame) for this.

Provide feedback

---

focus

Deprecated

Show details

---

HeadLocked

Read Parallel

Toggles whether the camera will automatically track the head motion of a
player using a VR device.

Camera.HeadLocked:[boolean](/docs/luau/booleans)

Toggles whether the camera will automatically track the head motion of a
player using a VR device. When true (default), the engine combines
[CFrame](/docs/reference/engine/classes/Camera#CFrame) with the [Enum.UserCFrame](/docs/reference/engine/enums/UserCFrame) of the user's head
to render the player's view with head tracking factored in. The view will
be rendered at the following [CFrame](/docs/reference/engine/datatypes/CFrame):

```
local UserInputService = game:GetService("UserInputService")



local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local headCFrame = UserInputService:GetUserCFrame(Enum.UserCFrame.Head)



headCFrame = headCFrame.Rotation + headCFrame.Position * camera.HeadScale



-- This will be equivalent to Camera:GetRenderCFrame()



local renderCFrame = camera.CFrame * headCFrame
```

It is recommended to not disable this property for the following
reasons:

* Players may experience motion sickness if an equivalent head tracking
  solution is not added.
* The Roblox Engine performs latency optimizations when HeadLocked is
  true.

##### See Also

* [VRService:GetUserCFrame()](/docs/reference/engine/classes/VRService#GetUserCFrame) which can be used to obtain the
  [CFrame](/docs/reference/engine/datatypes/CFrame) of the head.
* [VRService:RecenterUserHeadCFrame()](/docs/reference/engine/classes/VRService#RecenterUserHeadCFrame) which is used to recenter the
  head to the current position and orientation of the VR device.
* The [GetRenderCFrame()](/docs/reference/engine/classes/Camera#GetRenderCFrame) method which
  returns the [CFrame](/docs/reference/engine/classes/Camera#CFrame) combined with the
  [CFrame](/docs/reference/engine/datatypes/CFrame) of the user's head.

Provide feedback

---

HeadScale

Read Parallel

Sets the scale of the user's perspective of the world when using VR.

Camera.HeadScale:[number](/docs/luau/numbers)

HeadScale is the scale of the user's perspective of the world when using
VR.

The size of 1 stud in VR is 0.3 meters / HeadScale, meaning that larger
HeadScale values equate to the world looking smaller from the user's
perspective when using VR devices. For example, a part that's 1 stud tall
appears to be 0.6 meters tall to a VR player with a HeadScale of 0.5.

This property is automatically controlled by
[VRService.AutomaticScaling](/docs/reference/engine/classes/VRService#AutomaticScaling) to align the player's perspective with
the size of their avatar. If you intend to control HeadScale yourself or
use custom characters, toggle [VRService.AutomaticScaling](/docs/reference/engine/classes/VRService#AutomaticScaling) to
[Enum.VRScaling.Off](/docs/reference/engine/enums/VRScaling#Off).

This property should not be confused with [Humanoid.HeadScale](/docs/reference/engine/classes/Humanoid#HeadScale) which
is a [NumberValue](/docs/reference/engine/classes/NumberValue) parented to a [Humanoid](/docs/reference/engine/classes/Humanoid) to control its
scaling.

Provide feedback

---

MaxAxisFieldOfView

Not Replicated

Read Parallel

Sets the angle of the camera's field of view along the longest viewport
axis.

Camera.MaxAxisFieldOfView:[number](/docs/luau/numbers)

The MaxAxisFieldOfView property sets how many degrees along the longest
viewport axis the camera can view.

When the longest axis is the vertical axis, this property will behave
similar to the [FieldOfView](/docs/reference/engine/classes/Camera#FieldOfView) property. This is
generally the case when a device is in a portrait orientation. In a
landscape orientation, the longest axis will be the horizontal axis; in
this case, the property describes the horizontal field of view of the
[Camera](/docs/reference/engine/classes/Camera).

Provide feedback

---

NearPlaneZ

Read Only

Not Replicated

Read Parallel

Describes the negative Z offset, in studs, of the camera's near
clipping plane.

Camera.NearPlaneZ:[number](/docs/luau/numbers)

The NearPlaneZ property describes how far away the camera's near
clipping plane is, in studs. The near clipping plane is a geometric plane
that sits in front of the camera's [CFrame](/docs/reference/engine/classes/Camera#CFrame). Anything
between this plane and the camera will not render, creating a cutaway view
when viewing objects at very short distances. The value of NearPlaneZ
varies across different platforms and is currently always between -0.1
and -0.5.

![Diagram showing how the NearPlaneZ clips (does not render) 3D content between the plane and the camera.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/Camera/NearPlaneZ.jpg)

Provide feedback

---

ViewportSize

Read Only

Not Replicated

Read Parallel

The dimensions of the device safe area on a Roblox client.

Camera.ViewportSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

ViewportSize returns the dimensions of the device safe area on the
current screen. This area is a rectangle which includes the Roblox top bar
area but does not include any device notches or screen cutouts. The units
of ViewportSize are Roblox UI offset units which may be different from
native display pixels.

![Mobile device screen with cutout showing device safe area.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/Camera/DeviceSafeAreaVsFullscreen.png)

As noted above, ViewportSize is not equal to the fullscreen area size on
displays with cutouts or notches. To obtain the fullscreen area size on
all displays, you can query the
[AbsoluteSize](/docs/reference/engine/classes/ScreenGui#AbsoluteSize) property of a
[ScreenGui](/docs/reference/engine/classes/ScreenGui) with [ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) set to
[None](/docs/reference/engine/enums/ScreenInsets#None). See [Enum.ScreenInsets](/docs/reference/engine/enums/ScreenInsets) for a more
information about how screen areas are defined.

Finally, note that ViewportSize is not the actual viewport size the
camera uses for rendering (the camera renders in the fullscreen area).
Also, the [FieldOfView](/docs/reference/engine/classes/Camera#FieldOfView) and
[DiagonalFieldOfView](/docs/reference/engine/classes/Camera#DiagonalFieldOfView) properties are
based on the fullscreen area, not ViewportSize.

##### Camera Updates

Only the [Camera](/docs/reference/engine/classes/Camera) currently referred to by
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) has its ViewportSize updated each frame
during the [PreRender](/docs/reference/engine/classes/RunService#PreRender) step. The ViewportSize
of all other cameras in your experience won't be updated, including those
used for [ViewportFrames](/docs/reference/engine/classes/ViewportFrame).

Provide feedback

---

VRTiltAndRollEnabled

Read Parallel

Toggles whether to apply tilt and roll from the
[CFrame](/docs/reference/engine/classes/Camera#CFrame) property while the player is using a VR
device.

Camera.VRTiltAndRollEnabled:[boolean](/docs/luau/booleans)

This property toggles whether to apply tilt and roll from the
[CFrame](/docs/reference/engine/classes/Camera#CFrame) property while the player is using a VR
device.

To prevent motion sickness, the horizon should remain level. Tilting and
rolling the player's view while using a VR device can cause a disconnect
between the player's physical space and the virtual space they are
viewing. Changing the apparent downwards direction can cause players to
lose balance or experience dizziness.

For these reasons, it is generally advisable to leave this property
disabled, unless you have extensively tested your experience for these
effects. Even with tilt and roll enabled, you may want to ensure the
player always has a stable reference frame, such as the interior of a
vehicle or a floor that can help the player ground themselves in their
physical space.

Provide feedback

---

Methods

GetLargestCutoffDistance

Deprecated

Show details

---

GetPanSpeed

Deprecated

Show details

---

GetPartsObscuringTarget

Returns an array of [BaseParts](/docs/reference/engine/classes/BasePart) that are obscuring the
lines of sight between the camera's [CFrame](/docs/reference/engine/classes/Camera#CFrame) and the
cast points.

Camera:GetPartsObscuringTarget(

castPoints:[Array](/docs/luau/tables#arrays), ignoreList:Instances

):Instances

Parameters

|  |
| --- |
| castPoints:[Array](/docs/luau/tables#arrays)  An array of [Vector3](/docs/reference/engine/datatypes/Vector3) positions of cast points. |
| ignoreList:Instances  An array of [Instances](/docs/reference/engine/classes/Instance) that should be ignored, along with their descendants. |

Returns

Instances

An array of [BaseParts](/docs/reference/engine/classes/BasePart) that obscure the lines of sight
between the camera's [CFrame](/docs/reference/engine/classes/Camera#CFrame) and the
castPoints.

This method returns an array of [BaseParts](/docs/reference/engine/classes/BasePart) that are
obscuring the lines of sight between the camera's
[CFrame](/docs/reference/engine/classes/Camera#CFrame) and [Vector3](/docs/reference/engine/datatypes/Vector3) positions in the
castPoints array. Any [Instances](/docs/reference/engine/classes/Instance) included in the
ignoreList array will be ignored, along with their descendants.

The castPoints parameter is given as an array of [Vector3](/docs/reference/engine/datatypes/Vector3)
positions. Note that the array of [BaseParts](/docs/reference/engine/classes/BasePart) returned is
in an arbitrary order, and no additional raycast data is provided. If you
need data such as hit position, hit material, or surface normal, you
should opt for the [WorldRoot:Raycast()](/docs/reference/engine/classes/WorldRoot#Raycast) method.

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local castPoints = {



Vector3.new(0, 10, 0),



Vector3.new(0, 15, 0)



}



local ignoreList = {}



local partsObscuringTarget = camera:GetPartsObscuringTarget(castPoints, ignoreList)
```

If [Terrain](/docs/reference/engine/classes/Terrain) obscures a cast point, [BaseParts](/docs/reference/engine/classes/BasePart)
obscuring the cast point between the obscuring [Terrain](/docs/reference/engine/classes/Terrain) and the
cast point will not be returned.

Provide feedback

---

GetRenderCFrame

Returns the actual [CFrame](/docs/reference/engine/datatypes/CFrame)where the [Camera](/docs/reference/engine/classes/Camera) is being
rendered, accounting for any roll applied and the impact of VR devices.

Camera:GetRenderCFrame():[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

The [CFrame](/docs/reference/engine/datatypes/CFrame) the [Camera](/docs/reference/engine/classes/Camera) is being rendered at.

This method returns the actual [CFrame](/docs/reference/engine/datatypes/CFrame) of the [Camera](/docs/reference/engine/classes/Camera) as
it is rendered, including the impact of VR (VR head transformations are
not applied to the [CFrame](/docs/reference/engine/classes/Camera#CFrame) property, so it is best
practice to use [GetRenderCFrame()](/docs/reference/engine/classes/Camera#GetRenderCFrame) to
obtain the "true" [CFrame](/docs/reference/engine/datatypes/CFrame) of a player's view).

For example, when using VR, the [Camera](/docs/reference/engine/classes/Camera) is actually rendered at the
following [CFrame](/docs/reference/engine/datatypes/CFrame):

```
local UserInputService = game:GetService("UserInputService")



local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local headCFrame = UserInputService:GetUserCFrame(Enum.UserCFrame.Head)



headCFrame = headCFrame.Rotation + headCFrame.Position * camera.HeadScale



renderCFrame = camera.CFrame * headCFrame
```

The camera's render [CFrame](/docs/reference/engine/datatypes/CFrame) will only be changed to account for
the head when the [HeadLocked](/docs/reference/engine/classes/Camera#HeadLocked) property is true.

Provide feedback

---

GetRoll

Deprecated

Show details

---

GetTiltSpeed

Deprecated

Show details

---

Interpolate

Deprecated

Show details

---

PanUnits

Deprecated

Show details

---

ScreenPointToRay

Write Parallel

Creates a unit [Ray](/docs/reference/engine/datatypes/Ray) from a position on the screen (in pixels),
at a set depth from the [Camera](/docs/reference/engine/classes/Camera) orientated in the camera's
direction. Accounts for the GUI inset.

Camera:ScreenPointToRay(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), depth:[number](/docs/luau/numbers)

):[Ray](/docs/reference/engine/datatypes/Ray)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The position on the X axis, in pixels, of the screen point at which to originate the [Ray](/docs/reference/engine/datatypes/Ray). This position accounts for the GUI inset. |
| y:[number](/docs/luau/numbers)  The position on the Y axis, in pixels, of the screen point at which to originate the [Ray](/docs/reference/engine/datatypes/Ray). This position accounts for the GUI inset. |
| depth:[number](/docs/luau/numbers) Default Value: 0 The depth from the [Camera](/docs/reference/engine/classes/Camera), in studs, from which to offset the origin of the [Ray](/docs/reference/engine/datatypes/Ray). |

Returns

[Ray](/docs/reference/engine/datatypes/Ray)

A unit [Ray](/docs/reference/engine/datatypes/Ray), originating from the equivalent
[Vector3](/docs/reference/engine/datatypes/Vector3) world position of the given screen coordinates at
the given depth away from the [Camera](/docs/reference/engine/classes/Camera). This ray is orientated
in the direction of the [Camera](/docs/reference/engine/classes/Camera).

This method creates a unit [Ray](/docs/reference/engine/datatypes/Ray) from a 2D position on the screen
(defined in pixels), accounting for the GUI inset. The [Ray](/docs/reference/engine/datatypes/Ray)
originates from the [Vector3](/docs/reference/engine/datatypes/Vector3) equivalent of the 2D position in
the world at the given depth (in studs) away from the [Camera](/docs/reference/engine/classes/Camera).

As this method acknowledges the GUI inset, the offset applied to GUI
elements (such as from the top bar) is accounted for. This means the
screen position specified will start in the top left corner below the top
bar. For an otherwise identical method that does not account for the GUI
offset, use [ViewportPointToRay()](/docs/reference/engine/classes/Camera#ViewportPointToRay).

As the [Ray](/docs/reference/engine/datatypes/Ray) created is a unit ray, it is only one stud long. To
create a longer ray, you can do the following:

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local length = 500



local unitRay = camera:ScreenPointToRay(100, 100)



local extendedRay = Ray.new(unitRay.Origin, unitRay.Direction * length)
```

This method only works for the current [Workspace](/docs/reference/engine/classes/Workspace) camera. Other
cameras, such as those you create for a [ViewportFrame](/docs/reference/engine/classes/ViewportFrame), have an
initial viewport size of (1, 1) and are
only updated after you set them to [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). The
mismatch in viewport size causes the camera to return a ray with an
incorrect [Ray.Direction](/docs/reference/engine/datatypes/Ray#Direction).

Provide feedback

---

SetCameraPanMode

Deprecated

Show details

---

SetRoll

Deprecated

Show details

---

TiltUnits

Deprecated

Show details

---

ViewportPointToRay

Write Parallel

Creates a unit [Ray](/docs/reference/engine/datatypes/Ray) from a position on the viewport (in pixels),
at a given depth from the [Camera](/docs/reference/engine/classes/Camera), orientated in the camera's
direction. Does not account for the [CoreUISafeInsets](/docs/reference/engine/enums/ScreenInsets)
inset.

Camera:ViewportPointToRay(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), depth:[number](/docs/luau/numbers)

):[Ray](/docs/reference/engine/datatypes/Ray)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The position on the X axis, in pixels, of the viewport point at which to originate the [Ray](/docs/reference/engine/datatypes/Ray), in device safe area coordinates. |
| y:[number](/docs/luau/numbers)  The position on the Y axis, in pixels, of the viewport point at which to originate the [Ray](/docs/reference/engine/datatypes/Ray), in device safe area coordinates. |
| depth:[number](/docs/luau/numbers) Default Value: 0 The depth from the [Camera](/docs/reference/engine/classes/Camera), in studs, from which to offset the origin of the [Ray](/docs/reference/engine/datatypes/Ray). |

Returns

[Ray](/docs/reference/engine/datatypes/Ray)

A unit [Ray](/docs/reference/engine/datatypes/Ray), originating from the equivalent
[Vector3](/docs/reference/engine/datatypes/Vector3) world position of the given viewport coordinates at
the given depth away from the [Camera](/docs/reference/engine/classes/Camera). This ray is orientated
in the direction of the [Camera](/docs/reference/engine/classes/Camera).

This method creates a unit [Ray](/docs/reference/engine/datatypes/Ray) from a 2D position in device
safe viewport coordinates, defined in pixels. The ray originates from the
[Vector3](/docs/reference/engine/datatypes/Vector3) equivalent of the 2D position in the world at the given
depth (in studs) away from the [Camera](/docs/reference/engine/classes/Camera).

As illustrated below, (0, 0) corresponds to the top‑left point of the
Roblox top bar. This means that the input 2D position does not account
for the [CoreUISafeInsets](/docs/reference/engine/enums/ScreenInsets) inset, but it does account
for any [DeviceSafeInsets](/docs/reference/engine/enums/ScreenInsets).

![Diagram showing the origin of the device safe area viewport coordinate system.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/Camera/ViewportPointToRayOrigin.png)

Note that UI instances use a different coordinate system
([GuiObject.AbsolutePosition](/docs/reference/engine/classes/GuiObject#AbsolutePosition) uses the
[CoreUISafeInsets](/docs/reference/engine/enums/ScreenInsets) viewport coordinate system while this
method uses the [DeviceSafeInsets](/docs/reference/engine/enums/ScreenInsets) viewport coordinate
system). If you would like to specify position in core UI coordinates,
please use [ScreenPointToRay()](/docs/reference/engine/classes/Camera#ScreenPointToRay).

Also note that this method only works for the
[Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) camera. Other cameras, such as those you
create for a [ViewportFrame](/docs/reference/engine/classes/ViewportFrame), have an initial viewport size of
(1, 1) and are only updated after you set them to
[CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). The mismatch in viewport
size causes the camera to return a ray with an incorrect
[Ray.Direction](/docs/reference/engine/datatypes/Ray#Direction).

This method can be used in conjunction with the
[ViewportSize](/docs/reference/engine/classes/Camera#ViewportSize) property to create a ray from the
centre of the screen, for example:

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local viewportPoint = camera.ViewportSize / 2



local unitRay = camera:ViewportPointToRay(viewportPoint.X, viewportPoint.Y, 0)
```

As the [Ray](/docs/reference/engine/datatypes/Ray) created is a unit ray, it is only one stud long. To
create a longer ray, you can do the following:

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local length = 500



local unitRay = camera:ScreenPointToRay(100, 100)



local extendedRay = Ray.new(unitRay.Origin, unitRay.Direction * length)
```

Provide feedback

---

WorldToScreenPoint

Write Parallel

Returns the screen location and depth of a [Vector3](/docs/reference/engine/datatypes/Vector3) worldPoint
and whether this point is within the bounds of the screen. Accounts for
the GUI inset.

Camera:WorldToScreenPoint(worldPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| worldPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)  The [Vector3](/docs/reference/engine/datatypes/Vector3) world position. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing, in order:

* A [Vector3](/docs/reference/engine/datatypes/Vector3) whose X and Y components represent the
  offset of the worldPoint from the top left corner of the screen,
  in pixels. The [Vector3](/docs/reference/engine/datatypes/Vector3) Z component represents the
  depth of the worldPoint from the screen (in studs).
* A boolean indicating if the worldPoint is within the bounds of the
  screen.

This method returns the screen location and depth of a [Vector3](/docs/reference/engine/datatypes/Vector3)
worldPoint and whether this point is within the bounds of the screen.

This method takes in account the current GUI inset, such as the space
occupied by the top bar, meaning that the 2D position returned is in the
same term as GUI positions and can be used to place GUI elements. For an
otherwise identical method that ignores the GUI inset, see
[WorldToViewportPoint()](/docs/reference/engine/classes/Camera#WorldToViewportPoint).

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local worldPoint = Vector3.new(0, 10, 0)



local vector, onScreen = camera:WorldToScreenPoint(worldPoint)



local screenPoint = Vector2.new(vector.X, vector.Y)



local depth = vector.Z
```

Note this method does not perform any raycasting and the boolean
indicating whether worldPoint is within the bounds of the screen will be
true regardless of whether the point is obscured by
[BaseParts](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain).

Provide feedback

---

WorldToViewportPoint

Write Parallel

Returns the screen location and depth of a [Vector3](/docs/reference/engine/datatypes/Vector3) worldPoint
and whether this point is within the bounds of the screen. Does not
account for the GUI inset.

Camera:WorldToViewportPoint(worldPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| worldPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)  The [Vector3](/docs/reference/engine/datatypes/Vector3) world position. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing, in order:

* A [Vector3](/docs/reference/engine/datatypes/Vector3) whose X and Y components represent the
  offset of the worldPoint from the top left corner of the viewport,
  in pixels. The [Vector3](/docs/reference/engine/datatypes/Vector3) Z component represents the
  depth of the worldPoint from the screen (in studs).
* A boolean indicating if the worldPoint is within the bounds of the
  screen.

This method returns the screen location and depth of a [Vector3](/docs/reference/engine/datatypes/Vector3)
worldPoint and whether this point is within the bounds of the screen.

This method does not take in account the current GUI inset, such as the
space occupied by the top bar, meaning that the 2D position returned is
taken from the top left corner of the viewport. Unless you are using
[ScreenGui.IgnoreGuiInset](/docs/reference/engine/classes/ScreenGui#IgnoreGuiInset), this position is not appropriate for
placing GUI elements.

For an otherwise identical method that accounts for the GUI inset, see
[WorldToScreenPoint()](/docs/reference/engine/classes/Camera#WorldToScreenPoint).

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local worldPoint = Vector3.new(0, 10, 0)



local vector, onScreen = camera:WorldToViewportPoint(worldPoint)



local viewportPoint = Vector2.new(vector.X, vector.Y)



local depth = vector.Z
```

Note this method does not perform any raycasting and the boolean
indicating whether worldPoint is within the bounds of the screen will be
true regardless of whether the point is obscured by
[BaseParts](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain).

Provide feedback

---

ZoomToExtents

Adjusts the [CFrame](/docs/reference/engine/classes/Camera#CFrame) so that the specified bounding
box is fully visible within the camera's viewport.

Camera:ZoomToExtents(

boundingBoxCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame), boundingBoxSize:[Vector3](/docs/reference/engine/datatypes/Vector3)

):()

Parameters

|  |
| --- |
| boundingBoxCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)  The [CFrame](/docs/reference/engine/datatypes/CFrame) representing the center and orientation of the bounding box to fit into the viewport. |
| boundingBoxSize:[Vector3](/docs/reference/engine/datatypes/Vector3)  The [Vector3](/docs/reference/engine/datatypes/Vector3) size of the bounding box to fit into the viewport. |

Returns

()

This method adjusts the [CFrame](/docs/reference/engine/classes/Camera#CFrame) so that a specified
bounding box is fully visible within the camera's viewport, without
cropping any part of the box.

The bounding box is defined by its center and orientation
(boundingBoxCFrame) and its size (boundingBoxSize).

This can be used to focus the camera on a 3D object or model, such as when
framing content in a [ViewportFrame](/docs/reference/engine/classes/ViewportFrame), taking screenshots, or
smoothly transitioning the camera to highlight specific content.

The method automatically accounts for the camera's field of view and
viewport aspect ratio to ensure the entire bounding box fits.

```
local Workspace = game:GetService("Workspace")



local camera = Workspace.CurrentCamera



local model = Workspace:FindFirstChild("MyModel")



if model then



local modelCFrame = model:GetModelCFrame()



local extentsSize = model:GetExtentsSize()



camera:ZoomToExtents(modelCFrame, extentsSize)



end
```

Provide feedback

---

Events

InterpolationFinished

Deprecated

Show details

---