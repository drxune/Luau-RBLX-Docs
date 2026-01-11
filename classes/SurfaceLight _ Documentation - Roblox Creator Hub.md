# SurfaceLight | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SurfaceLight
Scraped: 2026-01-11T02:41:11.935377Z

## Inherits
- Light
- SurfaceLight
- Instance
- Object
- Light.Color
- Light.Brightness
- SurfaceLight.Face
- SurfaceLight.Range
- BasePart
- Attachment
- SpotLight
- PointLight
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Light](/docs/reference/engine/classes/Light)
6. /
7. [SurfaceLight](/docs/reference/engine/classes/SurfaceLight)

English

Feedback

Engine Class

![SurfaceLight](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SurfaceLight-Dark.webp)SurfaceLight

A light source that emits illumination of a specified color and brightness
from a face for a specified range.

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

A SurfaceLight is a light source that emits illumination of a specified
[Light.Color](/docs/reference/engine/classes/Light#Color) and [Light.Brightness](/docs/reference/engine/classes/Light#Brightness) from a
[SurfaceLight.Face](/docs/reference/engine/classes/SurfaceLight#Face) for a specified [SurfaceLight.Range](/docs/reference/engine/classes/SurfaceLight#Range).

In order for a SurfaceLight to provide illumination, it must be the direct
child of a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) (the part or attachment
itself must be a descendant of the Workspace). If a SurfaceLight is parented
to a part, then the light will emanate from the part's selected face(s). If
parented to an attachment SurfaceLight is equivalent to a [SpotLight](/docs/reference/engine/classes/SpotLight).

For more light types, please see the see also section.

See Also
--------

* [PointLight](/docs/reference/engine/classes/PointLight)
* [SpotLight](/docs/reference/engine/classes/SpotLight)

Code Samples

Creating a New Surface Light

This example creates a new anchored BasePart named *Part* at the position
{0, 0, 0}.

It then creates a new surface light with brightness of 1, Color3 color
of {255/255, 255/255, 255/255} (white) and range of 16 studs. The surface
light's parent is set to the BasePart we created. To view the light, navigate
to the part at {0, 0, 0} or move the *Part* created to a location visible to
the player.

Please note that the properties of the created surface light can easily be
changed by modifying the property values in the code sample below.
Additionally, if you have an existing surface light, you can also create a
similar script that modifies that surface light instead of creating a new
BasePart and light.

```
local part = Instance.new("Part")



part.Anchored = true



part.Position = Vector3.new(0, 0, 0)



part.Parent = workspace



local light = Instance.new("SurfaceLight")



light.Color = Color3.fromRGB(255, 255, 255)



light.Brightness = 1



light.Range = 16



light.Parent = part
```

---

API Reference

Properties

Angle

Read Parallel

The angle of which the light is shone from the SurfaceLight.

SurfaceLight.Angle:[number](/docs/luau/numbers)

The angle of which the light is shone from the SurfaceLight.

Provide feedback

---

Face

Read Parallel

Sets the side of the parent that the SurfaceLight comes from.

SurfaceLight.Face:[Enum.NormalId](/docs/reference/engine/enums/NormalId)

Sets the side of the parent that the SurfaceLight comes from.

Provide feedback

---

Range

Read Parallel

The distance from the SurfaceLight's face that will illuminate.

SurfaceLight.Range:[number](/docs/luau/numbers)

The distance from the SurfaceLight's face that will illuminate.

Provide feedback

---