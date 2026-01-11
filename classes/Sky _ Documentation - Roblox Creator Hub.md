# Sky | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Sky
Scraped: 2026-01-11T02:41:29.210518Z

## Inherits
- Object
- Instance
- Sky
- Lighting
- SkyboxOrientation
- CelestialBodiesShown
- StarCount
- ViewportFrames
- TweenService
- RunService
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Sky](/docs/reference/engine/classes/Sky)

English

Feedback

Engine Class

![Sky](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Sky-Dark.webp)Sky

Changes the default appearance of the experience's sky.

---

Summary

Properties

|  |
| --- |
| [CelestialBodiesShown](#CelestialBodiesShown):[boolean](/docs/luau/booleans) |
| [MoonAngularSize](#MoonAngularSize):[number](/docs/luau/numbers) |
| [MoonTextureContent](#MoonTextureContent):[Content](/docs/reference/engine/datatypes/Content) |
| [MoonTextureId](#MoonTextureId):ContentId |
| [SkyboxBackContent](#SkyboxBackContent):[Content](/docs/reference/engine/datatypes/Content) |
| [SkyboxBk](#SkyboxBk):ContentId |
| [SkyboxDn](#SkyboxDn):ContentId |
| [SkyboxDownContent](#SkyboxDownContent):[Content](/docs/reference/engine/datatypes/Content) |
| [SkyboxFrontContent](#SkyboxFrontContent):[Content](/docs/reference/engine/datatypes/Content) |
| [SkyboxFt](#SkyboxFt):ContentId |
| [SkyboxLeftContent](#SkyboxLeftContent):[Content](/docs/reference/engine/datatypes/Content) |
| [SkyboxLf](#SkyboxLf):ContentId |
| [SkyboxOrientation](#SkyboxOrientation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [SkyboxRightContent](#SkyboxRightContent):[Content](/docs/reference/engine/datatypes/Content) |
| [SkyboxRt](#SkyboxRt):ContentId |
| [SkyboxUp](#SkyboxUp):ContentId |
| [SkyboxUpContent](#SkyboxUpContent):[Content](/docs/reference/engine/datatypes/Content) |
| [StarCount](#StarCount):[number](/docs/luau/numbers) |
| [SunAngularSize](#SunAngularSize):[number](/docs/luau/numbers) |
| [SunTextureContent](#SunTextureContent):[Content](/docs/reference/engine/datatypes/Content) |
| [SunTextureId](#SunTextureId):ContentId |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Sky object, when placed inside [Lighting](/docs/reference/engine/classes/Lighting), changes the default
appearance of the experience's sky. This object's
[skybox](/docs/environment/skybox) is composed of six sides, like a
cube. Rotation of the skybox can be changed through
[SkyboxOrientation](/docs/reference/engine/classes/Sky#SkyboxOrientation).

The skybox sun, moon, and other celestial objects remain visible unless you
turn off the [CelestialBodiesShown](/docs/reference/engine/classes/Sky#CelestialBodiesShown) property.
By adjusting the [StarCount](/docs/reference/engine/classes/Sky#StarCount) property, you can change how
many stars appear in the sky at night.

This object can also be used as a cubemap for reflections in
[ViewportFrames](/docs/reference/engine/classes/ViewportFrame), in which case only the [Sky](/docs/reference/engine/classes/Sky)
object's six‑side Skybox[…] properties are used. For details, see
[viewport frames](/docs/ui/viewport-frames).

---

API Reference

Properties

CelestialBodiesShown

Read Parallel

Sets whether the sun, moon, and stars will show.

Sky.CelestialBodiesShown:[boolean](/docs/luau/booleans)

Sets whether the sun, moon, and stars will show.

Provide feedback

---

MoonAngularSize

Read Parallel

The perceived angular size of the moon while using this skybox, in
degrees.

Sky.MoonAngularSize:[number](/docs/luau/numbers)

The perceived angular size of the moon while using this skybox, in
degrees.

Provide feedback

---

MoonTextureContent

Read Parallel

Sky.MoonTextureContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

MoonTextureId

Read Parallel

The texture of the moon while using this skybox.

Sky.MoonTextureId:ContentId

The texture of the moon while using this skybox.

Provide feedback

---

SkyboxBackContent

Read Parallel

Sky.SkyboxBackContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

SkyboxBk

Read Parallel

The URL link to a picture for the back surface of the sky.

Sky.SkyboxBk:ContentId

The URL link to a picture for the back surface of the sky.

Provide feedback

---

SkyboxDn

Read Parallel

Asset ID for the bottom surface of the skybox.

Sky.SkyboxDn:ContentId

Asset ID for the bottom surface of the skybox.

Provide feedback

---

SkyboxDownContent

Read Parallel

Sky.SkyboxDownContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

SkyboxFrontContent

Read Parallel

Sky.SkyboxFrontContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

SkyboxFt

Read Parallel

Asset ID for the front surface of the skybox.

Sky.SkyboxFt:ContentId

Asset ID for the front surface of the skybox.

Provide feedback

---

SkyboxLeftContent

Read Parallel

Sky.SkyboxLeftContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

SkyboxLf

Read Parallel

Asset ID for the left surface of the skybox.

Sky.SkyboxLf:ContentId

Asset ID for the left surface of the skybox.

Provide feedback

---

SkyboxOrientation

Read Parallel

Angle of the skybox, in degrees, with rotation order of Y, X,
Z.

Sky.SkyboxOrientation:[Vector3](/docs/reference/engine/datatypes/Vector3)

Changes the orientation of the skybox surfaces. This property takes a
[Vector3](/docs/reference/engine/datatypes/Vector3) of degree values in the typical XYZ order, but
applies rotation first around the Y axis. After applying the Y
axis rotation, the orientation is applied to the X and Z axes to
allow for predictable control over complex movements. Your camera and
object orientation can affect how this rotation appears to be applied.

An easy way to script an orientation animation is to spin around the Y
axis (keeping the horizon level), then tilt this axis by setting X and
Z to a fixed value:

```
local Lighting = game:GetService("Lighting")



local RunService = game:GetService("RunService")



local sky = Lighting:FindFirstChild("Sky")



local ROTATION_SPEED = 5  -- In degrees per second



RunService.Heartbeat:Connect(function(deltaTime)



sky.SkyboxOrientation = Vector3.new(



30,



(sky.SkyboxOrientation.Y + ROTATION_SPEED * deltaTime) % 360,



0



)



end)
```

See [here](/docs/environment/skybox#orientation) for further info
and limitations.

Code Samples

Skybox Orientation with Tween

This script uses [TweenService](/docs/reference/engine/classes/TweenService) to create an oscillating tween on the X axis and [RunService](/docs/reference/engine/classes/RunService) to apply the tween's motion plus rotation around the Y axis.

```
local Lighting = game:GetService("Lighting")



local RunService = game:GetService("RunService")



local TweenService = game:GetService("TweenService")



local sky = Lighting:FindFirstChild("Sky")



local ROTATION_SPEED = 4 -- In degrees per second



local MAX_TILT = 2 -- In degrees



local TILT_SPEED = 4



local currentTilt = Instance.new("NumberValue")



currentTilt.Value = -MAX_TILT



local tweenGoal = { Value = MAX_TILT }



local tweenInfo = TweenInfo.new(TILT_SPEED, Enum.EasingStyle.Cubic, Enum.EasingDirection.InOut, -1, true)



local tween = TweenService:Create(currentTilt, tweenInfo, tweenGoal)



tween:Play()



RunService.Heartbeat:Connect(function(deltaTime)



sky.SkyboxOrientation =



Vector3.new(currentTilt.Value, (sky.SkyboxOrientation.Y + ROTATION_SPEED * deltaTime) % 360, 0)



end)
```

Provide feedback

---

SkyboxRightContent

Read Parallel

Sky.SkyboxRightContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

SkyboxRt

Read Parallel

Asset ID for the right surface of the skybox.

Sky.SkyboxRt:ContentId

Asset ID for the right surface of the skybox.

Provide feedback

---

SkyboxUp

Read Parallel

Asset ID for the top surface of the skybox.

Sky.SkyboxUp:ContentId

Asset ID for the top surface of the skybox.

Provide feedback

---

SkyboxUpContent

Read Parallel

Sky.SkyboxUpContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

StarCount

Read Parallel

How many stars are shown in the skybox.

Sky.StarCount:[number](/docs/luau/numbers)

How many stars are shown in the skybox. Only works if
[CelestialBodiesShown](/docs/reference/engine/classes/Sky#CelestialBodiesShown) is true.

Provide feedback

---

SunAngularSize

Read Parallel

The perceived angular size of the sun while using this skybox, in degrees.

Sky.SunAngularSize:[number](/docs/luau/numbers)

The perceived angular size of the sun while using this skybox, in degrees.

Provide feedback

---

SunTextureContent

Read Parallel

Sky.SunTextureContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

SunTextureId

Read Parallel

The texture of the sun while using this skybox.

Sky.SunTextureId:ContentId

The texture of the sun while using this skybox.

Provide feedback

---