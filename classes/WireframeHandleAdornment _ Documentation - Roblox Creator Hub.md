# WireframeHandleAdornment | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WireframeHandleAdornment
Scraped: 2026-01-11T02:35:05.591471Z

## Inherits
- HandleAdornment
- WireframeHandleAdornment
- BasePart
- Terrain
- Workspace
- PVAdornment
- GuiBase3d
- Instance
- Object
- PlayerGui
- CoreGui
- AddLines()
- AddPath()
- Thickness
- Color3
- Transparency
- Adornee
- AddLine()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [HandleAdornment](/docs/reference/engine/classes/HandleAdornment)
6. /
7. [WireframeHandleAdornment](/docs/reference/engine/classes/WireframeHandleAdornment)

English

Feedback

Engine Class

![WireframeHandleAdornment](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/WireframeHandleAdornment-Dark.webp)WireframeHandleAdornment

Renders a wireframe adornment consisting of one or more lines onto a
[BasePart](/docs/reference/engine/classes/BasePart) (including [Terrain](/docs/reference/engine/classes/Terrain)) or into the [Workspace](/docs/reference/engine/classes/Workspace).

---

Summary

Properties

|  |
| --- |
| [Scale](#Scale):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Thickness](#Thickness):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [AddLine](#AddLine)(from: [Vector3](/docs/reference/engine/datatypes/Vector3),to: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [AddLines](#AddLines)(points: [Array](/docs/luau/tables#arrays)):() |
| [AddPath](#AddPath)(points: [Array](/docs/luau/tables#arrays),loop: [boolean](/docs/luau/booleans)):() |
| [AddText](#AddText)(point: [Vector3](/docs/reference/engine/datatypes/Vector3),text: [string](/docs/luau/strings),size: [number](/docs/luau/numbers)):() |
| [Clear](#Clear)():() |

Inherited Members

9 inherited from [HandleAdornment](/docs/reference/engine/classes/HandleAdornment)

1 inherited from [PVAdornment](/docs/reference/engine/classes/PVAdornment)

4 inherited from [GuiBase3d](/docs/reference/engine/classes/GuiBase3d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

WireframeHandleAdornment renders a wireframe adornment consisting of one or
more lines onto a [BasePart](/docs/reference/engine/classes/BasePart) (including [Terrain](/docs/reference/engine/classes/Terrain)) or into the
[Workspace](/docs/reference/engine/classes/Workspace). If parented to a player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) or the
[CoreGui](/docs/reference/engine/classes/CoreGui), this adornment can listen to input events for purposes such
as making dragger tools.

Note that a WireframeHandleAdornment instance begins empty and you must
add lines or paths to it through methods like
[AddLines()](/docs/reference/engine/classes/WireframeHandleAdornment#AddLines) or
[AddPath()](/docs/reference/engine/classes/WireframeHandleAdornment#AddPath).

The rendered wireframe can be customized visually through its
[Thickness](/docs/reference/engine/classes/WireframeHandleAdornment#Thickness),
[Color3](/docs/reference/engine/classes/WireframeHandleAdornment#Color3), and
[Transparency](/docs/reference/engine/classes/WireframeHandleAdornment#Transparency) properties,
although these properties only affect subsequent draws and do not update lines
already drawn into the adornment.

Code Samples

Basic Path Wireframe

```
local wireframe = script.Parent



-- Declare four points in a square arrangement



local pathArray = {



Vector3.new(-10, 10, 0),



Vector3.new(10, 10, 0),



Vector3.new(10, -10, 0),



Vector3.new(-10, -10, 0)



}



-- Apply path to adornment and close it (connect starting and ending points)



wireframe:AddPath(pathArray, true)
```

Multicolor Wireframe

```
local wireframe = script.Parent



wireframe.Color3 = Color3.fromRGB(255, 0, 0) -- Sets next line to red



wireframe:AddLine(Vector3.new(-10, 0, 0), Vector3.new(10, 0, 0))



wireframe.Color3 = Color3.fromRGB(0, 255, 0) -- Sets next line to green



wireframe:AddLine(Vector3.new(0, -10, 0), Vector3.new(0, 10, 0))



wireframe.Color3 = Color3.fromRGB(0, 0, 255) -- Sets next line to blue



wireframe:AddLine(Vector3.new(0, 0, -10), Vector3.new(0, 0, 10))
```

---

API Reference

Properties

Scale

Read Parallel

The XYZ scale of the wireframe adornment.

WireframeHandleAdornment.Scale:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property specifies the XYZ scale of the wireframe adornment as a
[Vector3](/docs/reference/engine/datatypes/Vector3). For example, a scale of
[Vector3.new(1, 2, 1)](/docs/reference/engine/datatypes/Vector3#new) will scale the adornment twice its normal
size on the Y axis while keeping the X and Z axes unchanged.

Provide feedback

---

Thickness

Read Parallel

Thickness of the wireframe adornment's lines in pixels.

WireframeHandleAdornment.Thickness:[number](/docs/luau/numbers)

This property determines the thickness of the wireframe adornment's lines
in pixels. Note that this visual thickness does not change relative to the
adornment's distance from the viewer's camera.

Provide feedback

---

Methods

AddLine

Adds a line to the wireframe adornment from a starting point to an ending
point relative to the center of the
[Adornee](/docs/reference/engine/classes/WireframeHandleAdornment#Adornee).

WireframeHandleAdornment:AddLine(

from:[Vector3](/docs/reference/engine/datatypes/Vector3), to:[Vector3](/docs/reference/engine/datatypes/Vector3)

):()

Parameters

|  |
| --- |
| from:[Vector3](/docs/reference/engine/datatypes/Vector3)  Starting point of the line. |
| to:[Vector3](/docs/reference/engine/datatypes/Vector3)  Ending point of the line. |

Returns

()

This method adds a line to the wireframe adornment from a starting point
to an ending point, both defined as a [Vector3](/docs/reference/engine/datatypes/Vector3) relative to the
center of the [Adornee](/docs/reference/engine/classes/WireframeHandleAdornment#Adornee).

Note that you can make a multicolor wireframe by changing the adornment's
[Color3](/docs/reference/engine/classes/WireframeHandleAdornment#Color3) property before new lines
are drawn via [AddLine()](/docs/reference/engine/classes/WireframeHandleAdornment#AddLine), as
demonstrated in the following code sample.

Code Samples

Multicolor Wireframe

```
local wireframe = script.Parent



wireframe.Color3 = Color3.fromRGB(255, 0, 0) -- Sets next line to red



wireframe:AddLine(Vector3.new(-10, 0, 0), Vector3.new(10, 0, 0))



wireframe.Color3 = Color3.fromRGB(0, 255, 0) -- Sets next line to green



wireframe:AddLine(Vector3.new(0, -10, 0), Vector3.new(0, 10, 0))



wireframe.Color3 = Color3.fromRGB(0, 0, 255) -- Sets next line to blue



wireframe:AddLine(Vector3.new(0, 0, -10), Vector3.new(0, 0, 10))
```

Provide feedback

---

AddLines

Adds one or more lines to the wireframe adornment using an array.

WireframeHandleAdornment:AddLines(points:[Array](/docs/luau/tables#arrays)):()

Parameters

|  |
| --- |
| points:[Array](/docs/luau/tables#arrays)  Array of [Vector3](/docs/reference/engine/datatypes/Vector3) points in which each pair acts as a starting point and ending point for a line. |

Returns

()

This method adds one or more lines of the current
[Color3](/docs/reference/engine/classes/WireframeHandleAdornment#Color3) color to the wireframe
adornment using an array. Each pair of [Vector3](/docs/reference/engine/datatypes/Vector3) points in the
array acts as a starting point and ending point for a line, relative to
the center of the [Adornee](/docs/reference/engine/classes/WireframeHandleAdornment#Adornee).

Note that lines are rendered independently and their ending points are not
connected to the starting point of any other line. To connect multiple
line segments in a sequence from point to point, see
[AddPath()](/docs/reference/engine/classes/WireframeHandleAdornment#AddPath).

Code Samples

Wireframe Lines From Array

```
local wireframe = script.Parent



local linesArray = {



Vector3.new(-10, 0, 0), -- Starting point of first line



Vector3.new(10, 0, 0), -- Ending point of first line



Vector3.new(0, -10, 0), -- Starting point of second line



Vector3.new(0, 10, 0), -- Ending point of second line



Vector3.new(0, 0, -10), -- Starting point of third line



Vector3.new(0, 0, 10) -- Ending point of third line



}



-- Apply path to adornment



wireframe:AddLines(linesArray)
```

Provide feedback

---

AddPath

Adds multiple line segments to the wireframe adornment in a sequence from
point to point.

WireframeHandleAdornment:AddPath(

points:[Array](/docs/luau/tables#arrays), loop:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| points:[Array](/docs/luau/tables#arrays)  Array of [Vector3](/docs/reference/engine/datatypes/Vector3) points to connect in sequence with line segments. |
| loop:[boolean](/docs/luau/booleans)  Whether the path is closed by connecting its ending point to its starting point with an additional line. |

Returns

()

This method adds multiple line segments of the current
[Color3](/docs/reference/engine/classes/WireframeHandleAdornment#Color3) color to the wireframe
adornment in a sequence from point to point. The path can be closed
(ending point connected to starting point) by setting the loop parameter
to true.

Code Samples

Basic Path Wireframe

```
local wireframe = script.Parent



-- Declare four points in a square arrangement



local pathArray = {



Vector3.new(-10, 10, 0),



Vector3.new(10, 10, 0),



Vector3.new(10, -10, 0),



Vector3.new(-10, -10, 0)



}



-- Apply path to adornment and close it (connect starting and ending points)



wireframe:AddPath(pathArray, true)
```

Provide feedback

---

AddText

Adds a text label to the wireframe adornment.

WireframeHandleAdornment:AddText(

point:[Vector3](/docs/reference/engine/datatypes/Vector3), text:[string](/docs/luau/strings), size:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| point:[Vector3](/docs/reference/engine/datatypes/Vector3)  Position of the text in the adornment. |
| text:[string](/docs/luau/strings)  String to display. |
| size:[number](/docs/luau/numbers) Default Value: 12 Size of the text. |

Returns

()

Adds a text label to the wireframe adornment at a [Vector3](/docs/reference/engine/datatypes/Vector3) point
relative to the center of the
[Adornee](/docs/reference/engine/classes/WireframeHandleAdornment#Adornee). You can adjust the size
of the text through the size parameter, and the label renders in the
current [Color3](/docs/reference/engine/classes/WireframeHandleAdornment#Color3) color.

Provide feedback

---

Clear

Instantly clears all lines and text in the wireframe adornment.

WireframeHandleAdornment:Clear():()

Returns

()

Instantly clears all lines and text in the wireframe adornment.

Provide feedback

---