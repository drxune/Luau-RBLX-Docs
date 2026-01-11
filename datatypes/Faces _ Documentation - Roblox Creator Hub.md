# Faces | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Faces
Scraped: 2026-01-11T02:41:43.319195Z

## Inherits
- BasePart
- Handles
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Faces](/docs/reference/engine/datatypes/Faces)

English

Feedback

Engine Data Type

Faces

A data type containing six booleans, each representing a face of a
[BasePart](/docs/reference/engine/classes/BasePart).

---

Summary

Constructors

|  |
| --- |
| [new](#new)(normalIds...: [Tuple](/docs/luau/tuples)) |

Properties

|  |
| --- |
| [Top](#Top):[boolean](/docs/luau/booleans) |
| [Bottom](#Bottom):[boolean](/docs/luau/booleans) |
| [Left](#Left):[boolean](/docs/luau/booleans) |
| [Right](#Right):[boolean](/docs/luau/booleans) |
| [Back](#Back):[boolean](/docs/luau/booleans) |
| [Front](#Front):[boolean](/docs/luau/booleans) |

The [Faces](/docs/reference/engine/datatypes/Faces) data type contains six booleans representing whether a
feature is enabled for each face ([Enum.NormalId](/docs/reference/engine/enums/NormalId)) of a Part. In other words,
this contains a boolean for each axes (X/Y/Z) in both directions
(positive/negative). The [Handles](/docs/reference/engine/classes/Handles) object uses this data type to enable
whether a direction has a visible handle on a Part's face.

```
local handles = Instance.new("Handles")



handles.Faces = Faces.new(Enum.NormalId.Front, Enum.NormalId.Left)
```

Like most data types on Roblox, the Faces data type is immutable: you cannot
assign to its properties once created.

---

API Reference

Constructors

new

Returns a Faces with the corresponding face of each passed [Enum.NormalId](/docs/reference/engine/enums/NormalId) as true.

Faces.new(normalIds...:[Tuple](/docs/luau/tuples))

Parameters

|  |
| --- |
| normalIds...:[Tuple](/docs/luau/tuples) |

Creates a new Faces given some number of [Enum.NormalId](/docs/reference/engine/enums/NormalId) as arguments. Each NormalId provided indicates the property of the same name in the new Faces will be true.

* The [table.unpack()](/docs/reference/engine/libraries/table#unpack) function can be used to unpack a table of NormalId to be included.
* Passing values that are not a [Enum.NormalId](/docs/reference/engine/enums/NormalId) will do nothing; they are ignored silently.

Provide feedback

---

Properties

Top

Whether the top face is included.

Faces.Top:[boolean](/docs/luau/booleans)

Whether the top face is included.

Provide feedback

---

Bottom

Whether the bottom face is included.

Faces.Bottom:[boolean](/docs/luau/booleans)

Whether the bottom face is included.

Provide feedback

---

Left

Whether the left face is included.

Faces.Left:[boolean](/docs/luau/booleans)

Whether the left face is included.

Provide feedback

---

Right

Whether the right face is included.

Faces.Right:[boolean](/docs/luau/booleans)

Whether the right face is included.

Provide feedback

---

Back

Whether the back face is included.

Faces.Back:[boolean](/docs/luau/booleans)

Whether the back face is included.

Provide feedback

---

Front

Whether the front face is included.

Faces.Front:[boolean](/docs/luau/booleans)

Whether the front face is included.

Provide feedback

---