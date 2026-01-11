# BlockMesh | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BlockMesh
Scraped: 2026-01-11T02:39:51.371354Z

## Inherits
- BevelMesh
- BlockMesh
- BasePart
- SpecialMesh
- SpecialMesh.MeshType
- DataModelMesh
- Instance
- Object
- Part
- BasePart.Size
- DataModelMesh.Scale
- DataModelMesh.Offset
- BasePart.Position
- DataModelMesh.VertexColor
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BevelMesh](/docs/reference/engine/classes/BevelMesh)
6. /
7. [BlockMesh](/docs/reference/engine/classes/BlockMesh)

English

Feedback

Engine Class

![BlockMesh](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BlockMesh-Dark.webp)BlockMesh

The BlockMesh object applies a 'brick' mesh to the [BasePart](/docs/reference/engine/classes/BasePart) it is
parented to. It behaves identically to a [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) with
[SpecialMesh.MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) set to 'Brick'.

---

Summary

Inherited Members

3 inherited from [DataModelMesh](/docs/reference/engine/classes/DataModelMesh)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The BlockMesh object applies a 'brick' mesh to the [BasePart](/docs/reference/engine/classes/BasePart) it is
parented to. It behaves identically to a [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) with
[SpecialMesh.MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) set to 'brick'.

What does a BlockMesh do?
-------------------------

A BlockMesh gives the [BasePart](/docs/reference/engine/classes/BasePart) it was applied to a brick shaped mesh.
It is identical in appearance to a standard Roblox [Part](/docs/reference/engine/classes/Part).

The dimensions of the mesh will scale linearly in all directions with
[BasePart.Size](/docs/reference/engine/classes/BasePart#Size), this means a part containing a BlockMesh can be resized
the same way as any other part.

The additional functionality a BlockMesh brings however, is the ability to set
the [DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale) and [DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) properties.
These allow the position and dimensions of the mesh that is displayed to be
changed without changing the [BasePart.Position](/docs/reference/engine/classes/BasePart#Position) or
[BasePart.Size](/docs/reference/engine/classes/BasePart#Size) of the [BasePart](/docs/reference/engine/classes/BasePart) the mesh is parented to.

Note as the [BlockMesh](/docs/reference/engine/classes/BlockMesh) object does not include a texture the
[DataModelMesh.VertexColor](/docs/reference/engine/classes/DataModelMesh#VertexColor) property does not do anything.

Code Samples

BlockMesh Instantiation

A simple demonstration of how a BlockMesh can be created and how the
[DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale) and [DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) properties can be
used.

```
local part = Instance.new("Part")



part.Position = Vector3.new(0, 2, 0)



part.Size = Vector3.new(5, 2, 5)



part.Anchored = true



local mesh = Instance.new("BlockMesh")



mesh.Scale = Vector3.new(0.5, 0.5, 0.5)



mesh.Offset = Vector3.new(0, 2, 0)



mesh.Parent = part



local adornment = Instance.new("SelectionBox")



adornment.Adornee = part



adornment.Parent = part



part.Parent = workspace
```