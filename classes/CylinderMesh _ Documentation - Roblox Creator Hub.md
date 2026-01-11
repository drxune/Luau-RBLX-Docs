# CylinderMesh | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CylinderMesh
Scraped: 2026-01-11T02:34:49.695446Z

## Inherits
- BevelMesh
- CylinderMesh
- BasePart
- CylinderMeshes
- DataModelMesh
- Instance
- Object
- SpecialMesh.MeshType
- SpecialMesh
- Part.Shape
- BasePart.Size
- DataModelMesh.VertexColor
- DataModelMesh.Scale
- DataModelMesh.Offset
- BasePart.Position
- Part
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BevelMesh](/docs/reference/engine/classes/BevelMesh)
6. /
7. [CylinderMesh](/docs/reference/engine/classes/CylinderMesh)

English

Feedback

Engine Class

CylinderMesh

Deprecated

The CylinderMesh object applies a 'cylinder' mesh to the [BasePart](/docs/reference/engine/classes/BasePart) it
is parented to.

This class is deprecated, and [CylinderMeshes](/docs/reference/engine/classes/CylinderMesh) are no
longer supported. Do not use it for new work.

---

Summary

Inherited Members

3 inherited from [DataModelMesh](/docs/reference/engine/classes/DataModelMesh)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The CylinderMesh object applies a 'cylinder' mesh to the [BasePart](/docs/reference/engine/classes/BasePart) it
is parented to.

What does a CylinderMesh do?
----------------------------

A CylinderMesh gives the [BasePart](/docs/reference/engine/classes/BasePart) it was applied to a cylinder shaped
mesh.

The mesh applied gives the same appearance as that due to the
[SpecialMesh.MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) of a [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) being set to 'Cylinder'
or [Part.Shape](/docs/reference/engine/classes/Part#Shape) being set to 'Cylinder'. However, unlike those two
cases, it is orientated so that the height of the cylinder is along the
[BasePart](/docs/reference/engine/classes/BasePart) Y axis.

The dimensions of the mesh scale relative to the [BasePart.Size](/docs/reference/engine/classes/BasePart#Size) of the
[BasePart](/docs/reference/engine/classes/BasePart). This scale is uniformly along the [BasePart](/docs/reference/engine/classes/BasePart) Y axis
and maintaining a 1:1 ratio for the part's X and Z axis, using the lowest
value. This means the [BasePart](/docs/reference/engine/classes/BasePart) can be resized normally, but the cross
section of the cylinder will always remain a circle and cannot be stretched or
compressed.

Note as the CylinderMesh object does not include a texture the
[DataModelMesh.VertexColor](/docs/reference/engine/classes/DataModelMesh#VertexColor) property does not do anything.

Why use a CylinderMesh?
-----------------------

The advantage of using a mesh over setting the [Part.Shape](/docs/reference/engine/classes/Part#Shape) property of
a part to 'Cylinder' is that the [DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale) and
[DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) properties are exposed. These allow the position
and dimensions of the mesh that is displayed to be changed without changing
the [BasePart.Position](/docs/reference/engine/classes/BasePart#Position) or [BasePart.Size](/docs/reference/engine/classes/BasePart#Size) of the [Part](/docs/reference/engine/classes/Part) the
mesh is parented to.

The key difference between a CylinderMesh or a [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) with
[SpecialMesh.MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) set to 'Cylinder' is the orientation of the
cylinder mesh. With a CylinderMesh, the height of the cylinder is aligned with
the height (Y axis) of the part. With a [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) (or [Part](/docs/reference/engine/classes/Part)
with [Part.Shape](/docs/reference/engine/classes/Part#Shape) set to 'Cylinder'), the height of the cylinder is
aligned with the X axis.

Code Samples

CylinderMesh Instantiation

This code sample includes a demonstration of how a CylinderMesh can be used,
and how it scales so as to maintain a constant ratio of length to width.

```
local part = Instance.new("Part")



part.Position = Vector3.new(0, 2, 0)



part.Size = Vector3.new(10, 2, 5)



part.Anchored = true



local mesh = Instance.new("CylinderMesh")



mesh.Parent = part



mesh.Scale = Vector3.new(1, 1, 1)



mesh.Offset = Vector3.new(0, 0, 0)



local adornment = Instance.new("SelectionBox")



adornment.Adornee = part



adornment.Parent = part



part.Parent = workspace
```