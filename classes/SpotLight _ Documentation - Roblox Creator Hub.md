# SpotLight | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SpotLight
Scraped: 2026-01-11T02:32:23.901209Z

## Inherits
- Light
- SpotLight
- Instance
- Object
- Color
- Brightness
- Range
- Angle
- BasePart
- Attachment
- Face
- Attachments
- SurfaceLight
- PointLight
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Light](/docs/reference/engine/classes/Light)
6. /
7. [SpotLight](/docs/reference/engine/classes/SpotLight)

English

Feedback

Engine Class

![SpotLight](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SpotLight-Dark.webp)SpotLight

A light source that emits light directionally in the shape of a cone with a
spherical base.

---

Summary

Properties

|  |
| --- |
| [Angle](#Angle):[number](/docs/luau/numbers) |
| [Face](#Face):[Enum.NormalId](/docs/reference/engine/enums/NormalId) |
| [Range](#Range):[number](/docs/luau/numbers) |

Inherited Members

4 inherited from [Light](/docs/reference/engine/classes/Light)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A Spotlight emits light of a specified [Color](/docs/reference/engine/classes/Light#Color) and
[Brightness](/docs/reference/engine/classes/Light#Brightness) in the shape of a cone with a spherical
base. This object is ideal for directional light sources like flashlights
and headlights.

[Range](/docs/reference/engine/classes/SpotLight#Range) controls the distance of illumination and
[Angle](/docs/reference/engine/classes/SpotLight#Angle) defines the angle of light emission from the
cone's apex as illustrated below.

A spotlight must be a direct child of a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment)
and will exhibit the following behavior:

* When the spotlight is parented to a [BasePart](/docs/reference/engine/classes/BasePart), the
  [Face](/docs/reference/engine/classes/SpotLight#Face) property determines the face of the part from
  which light emanates.
* Although [Attachments](/docs/reference/engine/classes/Attachment) don't have faces, the
  [Face](/docs/reference/engine/classes/SpotLight#Face) property determines the axis of the attachment
  from which light emanates; -Z is front, +X is right, +Y is top,
  etc.

See also [SurfaceLight](/docs/reference/engine/classes/SurfaceLight) and [PointLight](/docs/reference/engine/classes/PointLight).

---

API Reference

Properties

Angle

Read Parallel

The angle of which the light is shone from the SpotLight.

SpotLight.Angle:[number](/docs/luau/numbers)

The angle of which the light is shone from the SpotLight.

Provide feedback

---

Face

Read Parallel

Sets the side of the parent that the SpotLight comes from.

SpotLight.Face:[Enum.NormalId](/docs/reference/engine/enums/NormalId)

Sets the side of the parent that the SpotLight comes from.

Provide feedback

---

Range

Read Parallel

The size of the area that the SpotLight will illuminate.

SpotLight.Range:[number](/docs/luau/numbers)

The size of the area that the SpotLight will illuminate.

Provide feedback

---