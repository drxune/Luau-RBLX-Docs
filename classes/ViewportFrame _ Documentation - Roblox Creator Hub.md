# ViewportFrame | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ViewportFrame
Scraped: 2026-01-11T02:37:29.995161Z

## Tags
- Not Replicated

## Inherits
- GuiObject
- ViewportFrame
- Camera
- GuiBase2d
- Instance
- Object
- ScreenGui
- GuiObjects
- Lighting.EnvironmentSpecularScale
- Lighting.EnvironmentDiffuseScale
- SurfaceAppearance.MetalnessMap
- Sky
- ViewportFrame.CurrentCamera
- Camera.CFrame
- Camera.FieldOfView
- ImageTransparency
- ImageColor3
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiObject](/docs/reference/engine/classes/GuiObject)
6. /
7. [ViewportFrame](/docs/reference/engine/classes/ViewportFrame)

English

Feedback

Engine Class

![ViewportFrame](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ViewportFrame-Dark.webp)ViewportFrame

[GuiObject](/docs/reference/engine/classes/GuiObject) that renders 3D objects inside its bounds.

---

Summary

Properties

|  |
| --- |
| [Ambient](#Ambient):[Color3](/docs/reference/engine/datatypes/Color3) |
| [CurrentCamera](#CurrentCamera):[Camera](/docs/reference/engine/classes/Camera) |
| [ImageColor3](#ImageColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ImageTransparency](#ImageTransparency):[number](/docs/luau/numbers) |
| [LightColor](#LightColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [LightDirection](#LightDirection):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

ViewportFrame is a [GuiObject](/docs/reference/engine/classes/GuiObject) that renders 3D objects inside its
bounds, offering a way to display 3D objects in a 2D space like a
[ScreenGui](/docs/reference/engine/classes/ScreenGui). This object has the following caveats:

* No shadows or
  [post-processing](/docs/environment/post-processing-effects) effects
  are rendered.
* [Enum.Material.Neon](/docs/reference/engine/enums/Material#Neon) and [Enum.Material.Glass](/docs/reference/engine/enums/Material#Glass) materials render at the
  lowest quality.
* Nested [GuiObjects](/docs/reference/engine/classes/GuiObject) aren't supported.
* By default, lighting inside a ViewportFrame acts as if
  [Lighting.EnvironmentSpecularScale](/docs/reference/engine/classes/Lighting#EnvironmentSpecularScale) and
  [Lighting.EnvironmentDiffuseScale](/docs/reference/engine/classes/Lighting#EnvironmentDiffuseScale) are both set to 0, so properties
  that rely on these fields, such as [SurfaceAppearance.MetalnessMap](/docs/reference/engine/classes/SurfaceAppearance#MetalnessMap),
  may look different.
* This object can use a [Sky](/docs/reference/engine/classes/Sky) child as a cubemap for reflections, in
  which case only the [Sky](/docs/reference/engine/classes/Sky) object's six Skybox[…] properties are
  used. Assuming these properties are valid, lighting inside the
  ViewportFrame acts similarly to if
  [Lighting.EnvironmentSpecularScale](/docs/reference/engine/classes/Lighting#EnvironmentSpecularScale) and
  [Lighting.EnvironmentDiffuseScale](/docs/reference/engine/classes/Lighting#EnvironmentDiffuseScale) are both set to 1. For details,
  see [here](/docs/ui/viewport-frames).

Code Samples

ViewportFrame - Create GUI

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local playerGui = player:WaitForChild("PlayerGui")



local screenGui = Instance.new("ScreenGui")



screenGui.Parent = playerGui



local viewportFrame = Instance.new("ViewportFrame")



viewportFrame.Size = UDim2.new(0.3, 0, 0.4, 0)



viewportFrame.Position = UDim2.new(0, 15, 0, 15)



viewportFrame.BackgroundColor3 = Color3.new(0, 0, 0)



viewportFrame.BorderColor3 = Color3.new(0.6, 0.5, 0.4)



viewportFrame.BorderSizePixel = 2



viewportFrame.BackgroundTransparency = 0.25



viewportFrame.Parent = screenGui



local part = Instance.new("Part")



part.Material = Enum.Material.Concrete



part.Color = Color3.new(0.25, 0.75, 1)



part.Position = Vector3.new(0, 0, 0)



part.Parent = viewportFrame



local viewportCamera = Instance.new("Camera")



viewportFrame.CurrentCamera = viewportCamera



viewportCamera.Parent = viewportFrame



viewportCamera.CFrame = CFrame.new(Vector3.new(0, 2, 12), part.Position)
```

ViewportFrame - Control Camera

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local playerGui = player:WaitForChild("PlayerGui")



local screenGui = Instance.new("ScreenGui")



screenGui.Parent = playerGui



local TweenService = game:GetService("TweenService")



local viewportFrame = Instance.new("ViewportFrame")



viewportFrame.Size = UDim2.new(0.3, 0, 0.4, 0)



viewportFrame.Position = UDim2.new(0, 15, 0, 15)



viewportFrame.BackgroundColor3 = Color3.new(0, 0, 0)



viewportFrame.BorderColor3 = Color3.new(0.6, 0.5, 0.4)



viewportFrame.BorderSizePixel = 2



viewportFrame.BackgroundTransparency = 0.25



viewportFrame.Parent = screenGui



local part = Instance.new("Part")



part.Material = Enum.Material.Concrete



part.Color = Color3.new(0.25, 0.75, 1)



part.Position = Vector3.new(0, 0, 0)



part.Parent = viewportFrame



local viewportCamera = Instance.new("Camera")



viewportFrame.CurrentCamera = viewportCamera



viewportCamera.Parent = viewportFrame



viewportCamera.CFrame = CFrame.new(Vector3.new(0, 2, 12), part.Position)



task.wait(2)



local cameraGoal = {



CFrame = CFrame.new(Vector3.new(0, 6, 4), part.Position),



}



local tweenInfo = TweenInfo.new(2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)



local tween = TweenService:Create(viewportCamera, tweenInfo, cameraGoal)



tween:Play()
```

---

API Reference

Properties

Ambient

Read Parallel

The lighting hue applied to the area within the ViewportFrame.

ViewportFrame.Ambient:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines the lighting hue applied to the area within the
ViewportFrame. Defaults to
[Color3.fromRGB(200, 200, 200)](/docs/reference/engine/datatypes/Color3)
(ghost grey).

Provide feedback

---

CurrentCamera

Not Replicated

Read Parallel

[Camera](/docs/reference/engine/classes/Camera) that is used to render children objects.

ViewportFrame.CurrentCamera:[Camera](/docs/reference/engine/classes/Camera)

[Camera](/docs/reference/engine/classes/Camera) instance that is used to render children objects. Defaults
to nil.

The [Camera](/docs/reference/engine/classes/Camera) object does not replicate so the
[ViewportFrame.CurrentCamera](/docs/reference/engine/classes/ViewportFrame#CurrentCamera) won't replicate either. When you set
this property, [Camera.CFrame](/docs/reference/engine/classes/Camera#CFrame) and [Camera.FieldOfView](/docs/reference/engine/classes/Camera#FieldOfView) will
be saved and replicate with the ViewportFrame internally so the client
can render the frame without a [Camera](/docs/reference/engine/classes/Camera) object.

Provide feedback

---

ImageColor3

Read Parallel

Determines how the rendered viewport image will be colorized.

ViewportFrame.ImageColor3:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines how the rendered viewport image will be
colorized, allowing you to change the color without directly modifying the
rendered object. The default colorization value is [Color3.new(1, 1, 1)](/docs/reference/engine/datatypes/Color3) (white) at which
no color modification occurs.

See also [ImageTransparency](/docs/reference/engine/classes/ViewportFrame#ImageTransparency) which
determines the transparency of the rendered image.

Provide feedback

---

ImageTransparency

Read Parallel

Determines the transparency of the rendered viewport image.

ViewportFrame.ImageTransparency:[number](/docs/luau/numbers)

This property determines the transparency of the rendered viewport image,
allowing you to change the transparency without directly modifying the
rendered object. A value of 0 (default) is completely opaque and a value
of 1 is completely transparent (invisible).

See also [ImageColor3](/docs/reference/engine/classes/ViewportFrame#ImageColor3) which determines
how the rendered image will be colorized.

Provide feedback

---

LightColor

Read Parallel

The color of the emitted light.

ViewportFrame.LightColor:[Color3](/docs/reference/engine/datatypes/Color3)

The color of the emitted light. Defaults to
[Color3.fromRGB(140, 140, 140)](/docs/reference/engine/datatypes/Color3)
(silver).

Provide feedback

---

LightDirection

Read Parallel

A [Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the light source.

ViewportFrame.LightDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)

A [Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the light source from
position (0, 0, 0). Defaults to
[Vector3.new(-1, -1, -1)](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---