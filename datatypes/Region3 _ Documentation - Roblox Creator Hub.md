# Region3 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Region3
Scraped: 2026-01-11T02:41:51.910474Z

## Inherits
- Terrain
- WorldRoot:FindPartsInRegion3()
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Region3](/docs/reference/engine/datatypes/Region3)

English

Feedback

Engine Data Type

Region3

Describes a rectangular volume in 3D space.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(min: [Vector3](/docs/reference/engine/datatypes/Vector3),max: [Vector3](/docs/reference/engine/datatypes/Vector3)) |

Properties

|  |
| --- |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Size](#Size):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [ExpandToGrid](#ExpandToGrid)(resolution: [number](/docs/luau/numbers)):[Region3](/docs/reference/engine/datatypes/Region3) |

The [Region3](/docs/reference/engine/datatypes/Region3) data type describes a volume in 3D space similar to an
axis-aligned rectangular prism. It is commonly used with [Terrain](/docs/reference/engine/classes/Terrain)
functions and functions that detect parts within a volume, such as
[WorldRoot:FindPartsInRegion3()](/docs/reference/engine/classes/WorldRoot#FindPartsInRegion3).

The prism's center is accessible using the [Region3.CFrame](/docs/reference/engine/datatypes/Region3#CFrame) property
and the prism's size is accessible through the [Region3.Size](/docs/reference/engine/datatypes/Region3#Size)
property. Note that the components of this property may be negative.

The [Region3:ExpandToGrid()](/docs/reference/engine/datatypes/Region3#ExpandToGrid) method returns a new [Region3](/docs/reference/engine/datatypes/Region3)
whose bounds comply with a provided resolution value. The resulting volume may
be equal to or greater than the original volume, but never smaller.

See also:

* [Region3int16](/docs/reference/engine/datatypes/Region3int16)

---

API Reference

Constructors

new

Returns a new [Region3](/docs/reference/engine/datatypes/Region3) using the provided vectors as boundaries.

Region3.new(

min:[Vector3](/docs/reference/engine/datatypes/Vector3), max:[Vector3](/docs/reference/engine/datatypes/Vector3) )

Parameters

|  |
| --- |
| min:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| max:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns a new [Region3](/docs/reference/engine/datatypes/Region3) given the [Vector3](/docs/reference/engine/datatypes/Vector3) bounds of the
rectangular prism volume.

Note that the order of the provided bounds matters: by switching them, the
polarity of the size components will switch. It is possible to create a
[Region3](/docs/reference/engine/datatypes/Region3) with a negative volume.

Provide feedback

---

Properties

CFrame

The center location and rotation of the [Region3](/docs/reference/engine/datatypes/Region3).

Region3.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

The center location and rotation of the [Region3](/docs/reference/engine/datatypes/Region3).

Provide feedback

---

Size

The 3D size of the [Region3](/docs/reference/engine/datatypes/Region3).

Region3.Size:[Vector3](/docs/reference/engine/datatypes/Vector3)

The 3D size of the [Region3](/docs/reference/engine/datatypes/Region3).

Provide feedback

---

Methods

ExpandToGrid

Expands the [Region3](/docs/reference/engine/datatypes/Region3) to fit a grid based on the provided
resolution.

Region3:ExpandToGrid(resolution:[number](/docs/luau/numbers)):[Region3](/docs/reference/engine/datatypes/Region3)

Parameters

|  |
| --- |
| resolution:[number](/docs/luau/numbers) |

Returns

[Region3](/docs/reference/engine/datatypes/Region3)

Expands the [Region3](/docs/reference/engine/datatypes/Region3) based on the provided resolution and
returns the expanded [Region3](/docs/reference/engine/datatypes/Region3) aligned to the [Terrain](/docs/reference/engine/classes/Terrain)
voxel grid.

Provide feedback

---