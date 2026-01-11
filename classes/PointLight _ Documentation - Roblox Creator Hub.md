# PointLight | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PointLight
Scraped: 2026-01-11T02:39:12.624967Z

## Inherits
- Light
- PointLight
- Instance
- Object
- PointLight.Range
- BasePart
- Attachment
- Workspace
- BasePart.Position
- Attachment.WorldPosition
- SurfaceLight
- SpotLight
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Light](/docs/reference/engine/classes/Light)
6. /
7. [PointLight](/docs/reference/engine/classes/PointLight)

English

Feedback

Engine Class

![PointLight](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/PointLight-Dark.webp)PointLight

A light source that emits illumination from a single point.

---

Summary

Properties

|  |
| --- |
| [Range](#Range):[number](/docs/luau/numbers) |

Inherited Members

4 inherited from [Light](/docs/reference/engine/classes/Light)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A PointLight is a light source that emits illumination from a single point.
Light is emitted spherically based on the [PointLight.Range](/docs/reference/engine/classes/PointLight#Range) of the
PointLight.

In order for a PointLight to provide illumination, it must be the direct child
of a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) (the part or attachment itself
must be a descendant of the [Workspace](/docs/reference/engine/classes/Workspace)).

If a PointLight is parented to a part, then the light will emanate from the
part's [BasePart.Position](/docs/reference/engine/classes/BasePart#Position). If a PointLight is parented to an
attachment, then the light will emanate from the attachment's
[Attachment.WorldPosition](/docs/reference/engine/classes/Attachment#WorldPosition).

For more light types, see the see also section.

See Also
--------

* [SurfaceLight](/docs/reference/engine/classes/SurfaceLight)
* [SpotLight](/docs/reference/engine/classes/SpotLight)

Code Samples

Creating a New Point Light

This example creates a new anchored BasePart named *Part* at the position
{0, 0, 0}.

It then creates a new point light with brightness of 1, Color3 color of
{255/255, 255/255, 255/255} (white) and range of 16 studs. The point
light's parent is set to the BasePart we created. To view the light, navigate
to the part at {0, 0, 0} or move the *Part* created to a location visible to
the player.

Please note that the properties of the created point light can easily be
changed by modifying the property values in the code sample below.
Additionally, if you have an existing point light, you can also create a
similar script that modifies that light instead of creating a new BasePart and
light.

```
local part = Instance.new("Part")



part.Anchored = true



part.Position = Vector3.new(0, 0, 0)



part.Parent = workspace



local light = Instance.new("PointLight")



light.Color = Color3.new(1, 1, 1)



light.Brightness = 1



light.Range = 16



light.Parent = part
```

---

API Reference

Properties

Range

Read Parallel

The size of the area that the PointLight will illuminate.

PointLight.Range:[number](/docs/luau/numbers)

The size of the area that the PointLight will illuminate.

Provide feedback

---