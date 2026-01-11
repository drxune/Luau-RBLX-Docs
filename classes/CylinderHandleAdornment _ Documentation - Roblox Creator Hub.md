# CylinderHandleAdornment | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CylinderHandleAdornment
Scraped: 2026-01-11T02:27:23.145131Z

## Inherits
- HandleAdornment
- CylinderHandleAdornment
- BasePart
- PVAdornment
- GuiBase3d
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [HandleAdornment](/docs/reference/engine/classes/HandleAdornment)
6. /
7. [CylinderHandleAdornment](/docs/reference/engine/classes/CylinderHandleAdornment)

English

Feedback

Engine Class

![CylinderHandleAdornment](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/CylinderHandleAdornment-Dark.webp)CylinderHandleAdornment

A cylinder that can be adorned to a [BasePart](/docs/reference/engine/classes/BasePart).

---

Summary

Properties

|  |
| --- |
| [Angle](#Angle):[number](/docs/luau/numbers) |
| [Height](#Height):[number](/docs/luau/numbers) |
| [InnerRadius](#InnerRadius):[number](/docs/luau/numbers) |
| [Radius](#Radius):[number](/docs/luau/numbers) |
| [Shading](#Shading):AdornShading |

Inherited Members

9 inherited from [HandleAdornment](/docs/reference/engine/classes/HandleAdornment)

1 inherited from [PVAdornment](/docs/reference/engine/classes/PVAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

For handles to be interactive, they must be parented to a player's PlayerGui
or the CoreGui.

The CylinderHandleAdornment is a cylinder that can be adorned to a
[BasePart](/docs/reference/engine/classes/BasePart). This adornment can listen to input events and is commonly
used to make dragger tools.

---

API Reference

Properties

Angle

Read Parallel

Angle of cylindrical sector (pie-slice).

CylinderHandleAdornment.Angle:[number](/docs/luau/numbers)

If Angle is <360, a cylindrical sector (aka a pie-slice) of that angle
is rendered instead of a full cylinder. The Angle property can be
combined with InnerRadius to render a sector of a hollow cylinder.

Provide feedback

---

Height

Read Parallel

The height of the cylinder adornment.

CylinderHandleAdornment.Height:[number](/docs/luau/numbers)

The height of the cylinder adornment.

Provide feedback

---

InnerRadius

Read Parallel

Inner radius of a hollow cylinder.

CylinderHandleAdornment.InnerRadius:[number](/docs/luau/numbers)

If InnerRadius is >0, a hollow cylinder with that inner radius is
rendered instead of a full cylinder. The InnerRadius property can be
combined with Angle to render a sector of a hollow cylinder.

Provide feedback

---

Radius

Read Parallel

The radius of the cylinder adornment.

CylinderHandleAdornment.Radius:[number](/docs/luau/numbers)

The radius of the cylinder adornment.

Provide feedback

---

Shading

Read Parallel

CylinderHandleAdornment.Shading:AdornShading

Provide feedback

---