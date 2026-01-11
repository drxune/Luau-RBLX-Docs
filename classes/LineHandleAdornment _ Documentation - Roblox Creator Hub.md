# LineHandleAdornment | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LineHandleAdornment
Scraped: 2026-01-11T02:34:21.373174Z

## Inherits
- HandleAdornment
- LineHandleAdornment
- BasePart
- PVAdornment
- GuiBase3d
- Instance
- Object
- HandleAdornment.CFrame
- HandleAdornment.SizeRelativeOffset
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [HandleAdornment](/docs/reference/engine/classes/HandleAdornment)
6. /
7. [LineHandleAdornment](/docs/reference/engine/classes/LineHandleAdornment)

English

Feedback

Engine Class

![LineHandleAdornment](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/LineHandleAdornment-Dark.webp)LineHandleAdornment

A line that can be adorned to a [BasePart](/docs/reference/engine/classes/BasePart).

---

Summary

Properties

|  |
| --- |
| [Length](#Length):[number](/docs/luau/numbers) |
| [Thickness](#Thickness):[number](/docs/luau/numbers) |

Inherited Members

9 inherited from [HandleAdornment](/docs/reference/engine/classes/HandleAdornment)

1 inherited from [PVAdornment](/docs/reference/engine/classes/PVAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

For handles to be interactive, they must be parented to a player's PlayerGui
or the CoreGui. The LineHandleAdornment is a line that can be adorned to a
[BasePart](/docs/reference/engine/classes/BasePart). This line starts at the center of the adornment's
[HandleAdornment.CFrame](/docs/reference/engine/classes/HandleAdornment#CFrame) (offset by the adornment's
[HandleAdornment.SizeRelativeOffset](/docs/reference/engine/classes/HandleAdornment#SizeRelativeOffset)) and will be oriented along its
CFrame. This adornment can listen to input events and is commonly used to make
dragger tools.

---

API Reference

Properties

Length

Read Parallel

The length of the line.

LineHandleAdornment.Length:[number](/docs/luau/numbers)

The length of the line.

Provide feedback

---

Thickness

Read Parallel

The thickness of the line in pixels.

LineHandleAdornment.Thickness:[number](/docs/luau/numbers)

The thickness of the line in pixels.

Provide feedback

---