# WrapDeformer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WrapDeformer
Scraped: 2026-01-11T02:38:55.742454Z

## Inherits
- BaseWrap
- WrapDeformer
- MeshPart
- EditableMesh
- Instance
- Object
- WrapTarget
- MeshParts
- WrapLayer
- FixedSize
- DataModel
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BaseWrap](/docs/reference/engine/classes/BaseWrap)
6. /
7. [WrapDeformer](/docs/reference/engine/classes/WrapDeformer)

English

Feedback

Engine Class

![WrapDeformer](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/WrapDeformer-Dark.webp)WrapDeformer

Allows for the real-time deformation of a [MeshPart](/docs/reference/engine/classes/MeshPart).

---

Summary

Methods

|  |
| --- |
| [CreateEditableMeshAsync](#CreateEditableMeshAsync)():[EditableMesh](/docs/reference/engine/classes/EditableMesh) |
| [GetDeformedCFrameAsync](#GetDeformedCFrameAsync)(originalCFrame: [CFrame](/docs/reference/engine/datatypes/CFrame)):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [SetCageMeshContent](#SetCageMeshContent)(content: [Content](/docs/reference/engine/datatypes/Content),cageOrigin: [CFrame](/docs/reference/engine/datatypes/CFrame)?):() |

Inherited Members

7 inherited from [BaseWrap](/docs/reference/engine/classes/BaseWrap)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [WrapDeformer](/docs/reference/engine/classes/WrapDeformer) object provides a low-resolution cage mesh that pairs
with a [WrapTarget](/docs/reference/engine/classes/WrapTarget) sibling to deform a parent [MeshPart](/docs/reference/engine/classes/MeshPart). The
[MeshPart](/docs/reference/engine/classes/MeshPart) geometry is deformed according to the displacement between
pairs of [WrapTarget](/docs/reference/engine/classes/WrapTarget) cage mesh vertices and [WrapDeformer](/docs/reference/engine/classes/WrapDeformer) cage
mesh vertices. Cage mesh vertices are paired based on UV equivalence.

[WrapDeformer](/docs/reference/engine/classes/WrapDeformer) may be used with avatars or on distinct
[MeshParts](/docs/reference/engine/classes/MeshPart), as long as [WrapTarget](/docs/reference/engine/classes/WrapTarget) children are present
for the parent [MeshParts](/docs/reference/engine/classes/MeshPart). [WrapDeformer](/docs/reference/engine/classes/WrapDeformer) is similar to
[WrapLayer](/docs/reference/engine/classes/WrapLayer) but doesn't require layered clothing and can directly deform
[MeshParts](/docs/reference/engine/classes/MeshPart) for publishing.

---

API Reference

Methods

CreateEditableMeshAsync

Yields

Returns an [EditableMesh](/docs/reference/engine/classes/EditableMesh) (currently unskinned) equivalent to the
deformed parent mesh.

WrapDeformer:CreateEditableMeshAsync():[EditableMesh](/docs/reference/engine/classes/EditableMesh)

Returns

[EditableMesh](/docs/reference/engine/classes/EditableMesh)

Constructs and returns an [EditableMesh](/docs/reference/engine/classes/EditableMesh) corresponding to the
deformed parent mesh geometry. This method respects all updates made to
the deformation inputs prior to the request. It also sets the returned
result's [FixedSize](/docs/reference/engine/classes/EditableMesh#FixedSize) to true.

Provide feedback

---

GetDeformedCFrameAsync

Yields

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) deformed comparably to the [MeshPart](/docs/reference/engine/classes/MeshPart).

WrapDeformer:GetDeformedCFrameAsync(originalCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| originalCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame) |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) deformed by the same deformation field used
for the geometry of the parent [MeshPart](/docs/reference/engine/classes/MeshPart). This method is useful for
the placement of accessories.

The input and output [CFrame](/docs/reference/engine/datatypes/CFrame) are both in the space of the parent
[MeshPart](/docs/reference/engine/classes/MeshPart); only position (not rotation) will be deformed. This
method respects all updates made to the deformation inputs prior to the
request.

Provide feedback

---

SetCageMeshContent

Sets the cage mesh used to deform against a sibling [WrapTarget](/docs/reference/engine/classes/WrapTarget)
cage mesh.

WrapDeformer:SetCageMeshContent(

content:[Content](/docs/reference/engine/datatypes/Content), cageOrigin:[CFrame](/docs/reference/engine/datatypes/CFrame)?

):()

Parameters

|  |
| --- |
| content:[Content](/docs/reference/engine/datatypes/Content) |
| cageOrigin:[CFrame](/docs/reference/engine/datatypes/CFrame)? |

Returns

()

Sets the cage mesh used to deform the parent [MeshPart](/docs/reference/engine/classes/MeshPart) in
conjunction with a sibling [WrapTarget](/docs/reference/engine/classes/WrapTarget) cage mesh. The content
parameter should represent a Roblox mesh asset ID or an
[EditableMesh](/docs/reference/engine/classes/EditableMesh) reference in your [DataModel](/docs/reference/engine/classes/DataModel).

Provide feedback

---