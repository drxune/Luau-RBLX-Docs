# SelectionBox | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SelectionBox
Scraped: 2026-01-11T02:29:58.137253Z

## Inherits
- InstanceAdornment
- SelectionBox
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
5. [InstanceAdornment](/docs/reference/engine/classes/InstanceAdornment)
6. /
7. [SelectionBox](/docs/reference/engine/classes/SelectionBox)

English

Feedback

Engine Class

![SelectionBox](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SelectionBox-Dark.webp)SelectionBox

Renders a 3D box around its [Adornee](/docs/reference/engine/classes/PVAdornment#Adornee).

---

Summary

Properties

|  |
| --- |
| [LineThickness](#LineThickness):[number](/docs/luau/numbers) |
| [SurfaceColor](#SurfaceColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |
| [SurfaceColor3](#SurfaceColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [SurfaceTransparency](#SurfaceTransparency):[number](/docs/luau/numbers) |

Inherited Members

1 inherited from [InstanceAdornment](/docs/reference/engine/classes/InstanceAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

SelectionBox renders a 3D box around its [Adornee](/docs/reference/engine/classes/PVAdornment#Adornee)
when it is a descendant of the [Workspace](/docs/reference/engine/classes/Workspace) or anywhere where GUI objects
are rendered. The box's geometry consists of rectangular prisms forming an
outline/wireframe in addition to a surface for each of its faces.
SelectionBox does not capture any form of input; it is solely a visual
effect.

For an outline/fill overlay effect which covers non‑primitive geometry such as
that of a [MeshPart](/docs/reference/engine/classes/MeshPart), see [Highlight](/docs/reference/engine/classes/Highlight).

---

API Reference

Properties

LineThickness

Read Parallel

Determines the thickness of the boxes outlines, in studs.

SelectionBox.LineThickness:[number](/docs/luau/numbers)

LineThickness determines the thickness of the box's outlines, measured
in studs. If set to 0, the outline will not be visible at all.

Provide feedback

---

SurfaceColor

Deprecated

Show details

---

SurfaceColor3

Read Parallel

Determines the color of the box's surfaces.

SelectionBox.SurfaceColor3:[Color3](/docs/reference/engine/datatypes/Color3)

SurfaceColor3 determines the color of the box's surfaces.

See also [Color3](/docs/reference/engine/classes/SelectionBox#Color3), a property of the superclass
[GuiBase3d](/docs/reference/engine/classes/GuiBase3d) which controls the color of the outline rather than the
surface faces.

Provide feedback

---

SurfaceTransparency

Read Parallel

Determines the transparency of the box's surfaces.

SelectionBox.SurfaceTransparency:[number](/docs/luau/numbers)

SurfaceTransparency determines the transparency of the box's surfaces,
similar to the way [BasePart.Transparency](/docs/reference/engine/classes/BasePart#Transparency) works. By default, this
property is 1 which causes the surfaces to be invisible.

See also [Transparency](/docs/reference/engine/classes/SelectionBox#Transparency), a property of the
superclass [GuiBase3d](/docs/reference/engine/classes/GuiBase3d) which controls the transparency of the
outline rather than the surfaces.

Provide feedback

---