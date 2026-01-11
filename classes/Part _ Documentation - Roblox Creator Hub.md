# Part | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Part
Scraped: 2026-01-11T02:40:14.930216Z

## Tags
- Not Replicated

## Inherits
- FormFactorPart
- Part
- BasePart
- PVInstance
- Instance
- Object
- FlagStand
- Platform
- Seat
- SkateboardPlatform
- SpawnLocation
- Part.Shape
- MeshPart
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [FormFactorPart](/docs/reference/engine/classes/FormFactorPart)
6. /
7. [Part](/docs/reference/engine/classes/Part)

English

Feedback

Engine Class

![Part](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Part-Dark.webp)Part

A common type of [BasePart](/docs/reference/engine/classes/BasePart) that comes in different primitive shapes.

---

Summary

Properties

|  |
| --- |
| [Shape](#Shape):[Enum.PartType](/docs/reference/engine/enums/PartType) |

Inherited Members

2 inherited from [FormFactorPart](/docs/reference/engine/classes/FormFactorPart)

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[FlagStand](/docs/reference/engine/classes/FlagStand), [Platform](/docs/reference/engine/classes/Platform), [Seat](/docs/reference/engine/classes/Seat), [SkateboardPlatform](/docs/reference/engine/classes/SkateboardPlatform), [SpawnLocation](/docs/reference/engine/classes/SpawnLocation)

The Part object is a type of [BasePart](/docs/reference/engine/classes/BasePart). It comes in five different
primitive shapes: Ball, Block, Cylinder, Wedge, and CornerWedge.

Code Samples

Create a Part in a Script

The script below spawns a new Part instance and sets several of the part's
properties.

Most notably, the script sets the [Part.Shape](/docs/reference/engine/classes/Part#Shape) property to
[Enum.PartType.Ball](/docs/reference/engine/enums/PartType#Ball). It also names the part *JurassicPart*, anchors it, makes
it a child of *Workspace*, and sets its color to white.

```
local part = Instance.new("Part")



part.Name = "JurassicPart"



part.Anchored = true



part.Shape = Enum.PartType.Ball



part.Color = Color3.new(1, 1, 1)



part.Parent = workspace -- Put the part into the Workspace
```

---

API Reference

Properties

Shape

Not Replicated

Read Parallel

Sets the overall shape of the object.

Part.Shape:[Enum.PartType](/docs/reference/engine/enums/PartType)

The Shape property sets the overall shape of the object to one of a
predetermined list of built-in shapes.

The [Enum.PartType](/docs/reference/engine/enums/PartType) enum controls the shape value, and has five possible
shapes:

| Shape/Value | Description |
| --- | --- |
| Ball | A spherical shape. |
| Block | A block shape. |
| Cylinder | A cylinder shape. |
| Wedge | A wedge shape with a slope on one side. |
| CornerWedge | A wedge shape with slopes on two sides. |

[MeshPart](/docs/reference/engine/classes/MeshPart) and [solid modeling](/docs/parts/solid-modeling)
can be used to obtain completely custom part shapes.

Collisions between balls, blocks, and wedges, and corner wedges are exact,
whereas collisions between terrain, cylinders, TriangleMeshes, and other
geometry types are approximations. This means that the ball shape can be
useful to create stable colliders for car wheels.

Code Samples

Create a Part in a Script

The script below spawns a new Part instance and sets several of the part's
properties.

Most notably, the script sets the [Part.Shape](/docs/reference/engine/classes/Part#Shape) property to
[Enum.PartType.Ball](/docs/reference/engine/enums/PartType#Ball). It also names the part *JurassicPart*, anchors it, makes
it a child of *Workspace*, and sets its color to white.

```
local part = Instance.new("Part")



part.Name = "JurassicPart"



part.Anchored = true



part.Shape = Enum.PartType.Ball



part.Color = Color3.new(1, 1, 1)



part.Parent = workspace -- Put the part into the Workspace
```

Provide feedback

---