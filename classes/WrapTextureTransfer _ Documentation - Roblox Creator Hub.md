# WrapTextureTransfer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WrapTextureTransfer
Scraped: 2026-01-11T02:38:25.380769Z

## Inherits
- Instance
- WrapTextureTransfer
- Decal
- MeshPart
- WrapTarget
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [WrapTextureTransfer](/docs/reference/engine/classes/WrapTextureTransfer)

English

Feedback

Engine Class

WrapTextureTransfer

[WrapTextureTransfer](/docs/reference/engine/classes/WrapTextureTransfer) allows a parent [Decal](/docs/reference/engine/classes/Decal) to be wrapped around
its parent [MeshPart](/docs/reference/engine/classes/MeshPart) based on the cage of its [WrapTarget](/docs/reference/engine/classes/WrapTarget).

Not Browsable

---

Summary

Properties

|  |
| --- |
| [ReferenceCageMeshContent](#ReferenceCageMeshContent):[Content](/docs/reference/engine/datatypes/Content) |
| [UVMaxBound](#UVMaxBound):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [UVMinBound](#UVMinBound):[Vector2](/docs/reference/engine/datatypes/Vector2) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

WrapTextureTransfer provides an alternative projection mode for [Decal](/docs/reference/engine/classes/Decal)
where this [Decal](/docs/reference/engine/classes/Decal) is fit to the parent [MeshPart](/docs/reference/engine/classes/MeshPart) based on it's
CageMesh provided in [WrapTarget](/docs/reference/engine/classes/WrapTarget).

This is useful as it allows fitting of Decals to a wide variety of differently
shaped MeshParts that share a similar WrapTarget CageMesh topology. By
authoring textures that are in the WrapTarget UV space, these textures can be
reused across many different MeshParts with different texture layouts.

* DataModel Structure
  + [MeshPart](/docs/reference/engine/classes/MeshPart)
    - [WrapTarget](/docs/reference/engine/classes/WrapTarget)
    - [Decal](/docs/reference/engine/classes/Decal)
      * [WrapTextureTransfer](/docs/reference/engine/classes/WrapTextureTransfer)

A way to visualize how this works is to imagine the Decals textures on the
WrapTarget CageMesh, which is wrapped around the MeshPart. These textures are
then projected from the CageMesh onto the MeshPart surface. Geometry that is
internal to the MeshPart, or that is not covered by the CageMesh, will not
receive any projected decal textures. Segmented regions of the target
[MeshPart](/docs/reference/engine/classes/MeshPart) are used to improve projection quality near holes or
boundaries in the CageMesh.

---

API Reference

Properties

ReferenceCageMeshContent

Read Parallel

An optional reference mesh used for pruning and validating the target
cage.

WrapTextureTransfer.ReferenceCageMeshContent:[Content](/docs/reference/engine/datatypes/Content)

The reference cage mesh is the cage mesh that the texture was authored
for. This target cage mesh defined in [WrapTarget](/docs/reference/engine/classes/WrapTarget) is pruned against
this ReferenceCageMeshContent. If the target cage mesh contains vertices
or faces that are not present in the reference cage mesh, these vertices
and faces are removed from the target cage mesh before performing the
texture transfer. If there are no shared UVs between
ReferenceCageMeshContent and cage mesh defined in [WrapTarget](/docs/reference/engine/classes/WrapTarget),
the texture transfer fails.

When not defined, the cage in [WrapTarget](/docs/reference/engine/classes/WrapTarget) in ancestor
[MeshPart](/docs/reference/engine/classes/MeshPart) is used for transfer without any pruning or validation.

Provide feedback

---

UVMaxBound

Read Parallel

Determines the maximum bound of the UV space to include in the transfer.

WrapTextureTransfer.UVMaxBound:[Vector2](/docs/reference/engine/datatypes/Vector2)

Determines the maximum bound of the UV space to include in the transfer.
Areas of the cage mesh with UV values greater than the maximum bound
aren't included when applying the texture.

The Decal textures apply to the parent [MeshPart](/docs/reference/engine/classes/MeshPart) with the textures
scaling linearly between UVMinBound and UVMaxBound.

When set to default -inf, the maximum UV value is used from WrapTarget's
cage.

Provide feedback

---

UVMinBound

Read Parallel

Determines the minimum bound of the UV space to include in the transfer.

WrapTextureTransfer.UVMinBound:[Vector2](/docs/reference/engine/datatypes/Vector2)

Determines the minimum bound of the UV space to include in the transfer.
Areas of the cage mesh with UV values smaller than the minimum bound
aren't included when applying the texture.

The Decal textures apply to the parent [MeshPart](/docs/reference/engine/classes/MeshPart) with the textures
scaling linearly between UVMinBound and UVMaxBound.

When set to default inf, uses the minimum UV value from WrapTarget's cage.

Provide feedback

---