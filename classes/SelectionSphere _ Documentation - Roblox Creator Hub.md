# SelectionSphere | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SelectionSphere
Scraped: 2026-01-11T02:34:24.073697Z

## Inherits
- PVAdornment
- SelectionSphere
- Adornee
- GuiBase3d
- Instance
- Object
- Workspace
- MeshPart
- Highlight
- Color3
- BasePart.Transparency
- Transparency
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PVAdornment](/docs/reference/engine/classes/PVAdornment)
6. /
7. [SelectionSphere](/docs/reference/engine/classes/SelectionSphere)

English

Feedback

Engine Class

![SelectionSphere](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SelectionSphere-Dark.webp)SelectionSphere

Renders a 3D sphere around its [Adornee](/docs/reference/engine/classes/PVAdornment#Adornee).

---

Summary

Properties

|  |
| --- |
| [SurfaceColor](#SurfaceColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |
| [SurfaceColor3](#SurfaceColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [SurfaceTransparency](#SurfaceTransparency):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [PVAdornment](/docs/reference/engine/classes/PVAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

SelectionSphere renders a 3D sphere around its
[Adornee](/docs/reference/engine/classes/PVAdornment#Adornee) when it is a descendant of the
[Workspace](/docs/reference/engine/classes/Workspace) or anywhere where GUI objects are rendered. The sphere's
geometry consists of a ring/outline in addition to a surface.
SelectionSphere does not capture any form of input; it is solely a visual
effect.

For an outline/fill overlay effect which covers non‑primitive geometry such as
that of a [MeshPart](/docs/reference/engine/classes/MeshPart), see [Highlight](/docs/reference/engine/classes/Highlight).

---

API Reference

Properties

SurfaceColor

Deprecated

Show details

---

SurfaceColor3

Read Parallel

Determines the color of the sphere's surface.

SelectionSphere.SurfaceColor3:[Color3](/docs/reference/engine/datatypes/Color3)

SurfaceColor3 determines the color of the sphere's surface.

See also [Color3](/docs/reference/engine/classes/SelectionSphere#Color3), a property of the
superclass [GuiBase3d](/docs/reference/engine/classes/GuiBase3d) which controls the color of the outline
rather than the surface faces.

Provide feedback

---

SurfaceTransparency

Read Parallel

Determines the transparency of the sphere's surface.

SelectionSphere.SurfaceTransparency:[number](/docs/luau/numbers)

SurfaceTransparency determines the transparency of the sphere's surface,
similar to the way [BasePart.Transparency](/docs/reference/engine/classes/BasePart#Transparency) works. By default, this
property is 1 which causes the surfaces to be invisible.

See also [Transparency](/docs/reference/engine/classes/SelectionSphere#Transparency), a property of
the superclass [GuiBase3d](/docs/reference/engine/classes/GuiBase3d) which controls the transparency of the
outline rather than the surface.

Provide feedback

---