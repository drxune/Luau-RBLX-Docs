# MeshPart | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MeshPart
Scraped: 2026-01-11T02:33:52.685825Z

## Tags
- Not Replicated

## Inherits
- TriangleMeshPart
- MeshPart
- BasePart
- PVInstance
- Instance
- Object
- SpecialMesh
- BlockMesh
- MeshId
- TextureID
- EditableMesh
- AssetService:CreateMeshPartAsync()
- CollisionFidelity
- MeshPart:ApplyMesh()
- MeshContent
- TextureContent
- EditableImage
- MeshPart.MeshId
- MeshPart.MeshContent
- MeshPart.TextureContent
- MeshPart.RenderFidelity
- MeshPart.CollisionFidelity
- MeshPart.FluidFidelity
- MeshPart.MeshSize
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart)
6. /
7. [MeshPart](/docs/reference/engine/classes/MeshPart)

English

Feedback

Engine Class

![MeshPart](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/MeshPart-Dark.webp)MeshPart

A form of [BasePart](/docs/reference/engine/classes/BasePart) that includes a physically simulated custom mesh.

---

Summary

Properties

|  |
| --- |
| [DoubleSided](#DoubleSided):[boolean](/docs/luau/booleans) |
| [HasJointOffset](#HasJointOffset):[boolean](/docs/luau/booleans)  Deprecated |
| [HasSkinnedMesh](#HasSkinnedMesh):[boolean](/docs/luau/booleans) |
| [JointOffset](#JointOffset):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [MeshContent](#MeshContent):[Content](/docs/reference/engine/datatypes/Content) |
| [MeshId](#MeshId):ContentId |
| [RenderFidelity](#RenderFidelity):[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) |
| [TextureContent](#TextureContent):[Content](/docs/reference/engine/datatypes/Content) |
| [TextureID](#TextureID):ContentId |

Methods

|  |
| --- |
| [ApplyMesh](#ApplyMesh)(meshPart: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

3 inherited from [TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart)

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[MeshPart](/docs/reference/engine/classes/MeshPart) is a form of [BasePart](/docs/reference/engine/classes/BasePart) that includes a physically
simulated custom mesh. Unlike with other mesh classes, such as
[SpecialMesh](/docs/reference/engine/classes/SpecialMesh) and [BlockMesh](/docs/reference/engine/classes/BlockMesh), they are not parented to a
[BasePart](/docs/reference/engine/classes/BasePart) but rather behave as a [BasePart](/docs/reference/engine/classes/BasePart) in their own right.

The mesh and texture of a [MeshPart](/docs/reference/engine/classes/MeshPart) are determined by the
[MeshId](/docs/reference/engine/classes/MeshPart#MeshId) and [TextureID](/docs/reference/engine/classes/MeshPart#TextureID)
properties. For more information, see [Meshes](/docs/parts/meshes).

---

API Reference

Properties

DoubleSided

Plugin Security

Read Parallel

Determines whether to render both faces of polygons in the mesh.

MeshPart.DoubleSided:[boolean](/docs/luau/booleans)

This property determines whether to render both faces of polygons in the
mesh. It is only changeable in Studio. This is useful for meshes that are
typically modeled as "cards" such as a leaf, hair, or cloth.

Provide feedback

---

HasJointOffset

Deprecated

Show details

---

HasSkinnedMesh

Hidden

Not Accessible Security

Read Parallel

MeshPart.HasSkinnedMesh:[boolean](/docs/luau/booleans)

Provide feedback

---

JointOffset

Deprecated

Show details

---

MeshContent

Not Accessible Security

Read Parallel

The mesh that is displayed on the [MeshPart](/docs/reference/engine/classes/MeshPart). Supports
[asset URIs](/docs/projects/assets#asset-uris) and
[EditableMesh](/docs/reference/engine/classes/EditableMesh) objects.

MeshPart.MeshContent:[Content](/docs/reference/engine/datatypes/Content)

The mesh that is displayed on the [MeshPart](/docs/reference/engine/classes/MeshPart). Supports
[asset URIs](/docs/projects/assets#asset-uris) and
[EditableMesh](/docs/reference/engine/classes/EditableMesh) objects.

Note that this property cannot be changed directly by scripts, as the
collision geometry of the mesh cannot be recomputed in real time. See
[AssetService:CreateMeshPartAsync()](/docs/reference/engine/classes/AssetService#CreateMeshPartAsync) as a method to create a new
[MeshPart](/docs/reference/engine/classes/MeshPart) from a given [Content](/docs/reference/engine/datatypes/Content) with a specified
[CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity).
[MeshPart:ApplyMesh()](/docs/reference/engine/classes/MeshPart#ApplyMesh) can be used to overwrite the
[MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent),
[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent), and collision geometry of
an existing [MeshPart](/docs/reference/engine/classes/MeshPart).

Provide feedback

---

MeshId

Not Accessible Security

Read Parallel

The [asset URIs](/docs/projects/assets#asset-uris) of the mesh
that is displayed on the [MeshPart](/docs/reference/engine/classes/MeshPart). Reads and writes to
[MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent).

MeshPart.MeshId:ContentId

The [asset URIs](/docs/projects/assets#asset-uris) of the mesh
that is displayed on the [MeshPart](/docs/reference/engine/classes/MeshPart). Reads and writes to
[MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent).

Note that this property cannot be changed directly by scripts, as the
collision geometry of the mesh cannot be recomputed in real time. See
[AssetService:CreateMeshPartAsync()](/docs/reference/engine/classes/AssetService#CreateMeshPartAsync) as a method to create a new
[MeshPart](/docs/reference/engine/classes/MeshPart) from a given [Content](/docs/reference/engine/datatypes/Content) with a specified
[CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity).
[MeshPart:ApplyMesh()](/docs/reference/engine/classes/MeshPart#ApplyMesh) can be used to overwrite the
[MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent),
[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent), and collision geometry of
an existing [MeshPart](/docs/reference/engine/classes/MeshPart).

Provide feedback

---

RenderFidelity

Not Replicated

Plugin Security

Read Parallel

The level of detail used to render the [MeshPart](/docs/reference/engine/classes/MeshPart).

MeshPart.RenderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)

This property determines the level of detail that the [MeshPart](/docs/reference/engine/classes/MeshPart)
will be shown in. It can be set to the possible values of the
[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) enum.

The default value is [Automatic](/docs/reference/engine/enums/RenderFidelity#Automatic), meaning
the mesh's detail is based on its distance from the camera as outlined in
the following table.

| Distance From Camera | Render Fidelity | Example |
| --- | --- | --- |
| Less than 250 studs | Highest |  |
| 250-500 studs | Medium |  |
| 500 or more studs | Lowest |  |

Provide feedback

---

TextureContent

Read Parallel

The texture applied to the [MeshPart](/docs/reference/engine/classes/MeshPart). Supports
[asset URIs](/docs/projects/assets#asset-uris) and
[EditableImage](/docs/reference/engine/classes/EditableImage) objects.

MeshPart.TextureContent:[Content](/docs/reference/engine/datatypes/Content)

The texture applied to the [MeshPart](/docs/reference/engine/classes/MeshPart). Supports
[asset URIs](/docs/projects/assets#asset-uris) and
[EditableImage](/docs/reference/engine/classes/EditableImage) objects.

When this property is set to [Content.none](/docs/reference/engine/datatypes/Content#none), no texture will be
applied to the mesh.

```
local Workspace = game:GetService("Workspace")



local meshPart = Workspace.MeshPart



meshPart.TextureContent = Content.none  -- No texture
```

Note that the [MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent) property cannot be
directly changed during runtime but the texture can.

##### Changing a Mesh Texture

Using the [TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) property, the
texture of a mesh can be changed without having to re-upload the mesh. To
do this, a new image can be uploaded to Roblox with the desired texture.
The original texture image file can be obtained by exporting the mesh
using the Export Selection option in Studio. The image file will be
saved alongside the exported .obj file.

The new texture can then be uploaded to Roblox as a decal and its
[asset URI](/docs/projects/assets#asset-uris) can be applied
to the mesh using the [TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) or
[TextureID](/docs/reference/engine/classes/MeshPart#TextureID) property.

[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) can also be set to
reference an [EditableImage](/docs/reference/engine/classes/EditableImage) that has not been published yet.

```
local AssetService = game:GetService("AssetService")



local Workspace = game:GetService("Workspace")



local meshPart = Workspace.MeshPart



local editableImage = AssetService:CreateEditableImageAsync(meshPart.TextureContent)



meshPart.TextureContent = Content.fromObject(editableImage)  -- Live updates
```

When [TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) references an
[EditableImage](/docs/reference/engine/classes/EditableImage), the texture will live update with any edits to the
[EditableImage](/docs/reference/engine/classes/EditableImage) object.

##### Making a Textured Mesh

A mesh can only be textured if the mesh has been UV mapped, referring to
the practice of projecting a texture map onto a mesh. This cannot be done
using Roblox Studio and must be done using an external 3D modeling
application such as [Blender](https://www.blender.org/).

Provide feedback

---

TextureID

Read Parallel

The texture applied to the [MeshPart](/docs/reference/engine/classes/MeshPart). Reads and writes to
[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent).

MeshPart.TextureID:ContentId

The texture applied to the [MeshPart](/docs/reference/engine/classes/MeshPart). Reads and writes to
[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent).

When this property is set to an empty string, no texture will be applied
to the mesh.

```
local Workspace = game:GetService("Workspace")



local meshPart = Workspace.MeshPart



meshPart.TextureID = ""  -- No texture
```

Note that the [MeshPart.MeshId](/docs/reference/engine/classes/MeshPart#MeshId) property cannot be changed during
runtime but the texture can. See
[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) for details.

Provide feedback

---

Methods

ApplyMesh

Overwrites the [MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent),
[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent), and collision geometry
properties of this [MeshPart](/docs/reference/engine/classes/MeshPart) from the given source meshPart.

MeshPart:ApplyMesh(meshPart:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| meshPart:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

Overwrites the [MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent),
[TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent), and collision geometry
properties of this [MeshPart](/docs/reference/engine/classes/MeshPart) from the given source meshPart.

Most of these properties are read-only and cannot be changed during
runtime on their own directly. To keep
[MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent) and physics data in sync, they
must be updated together.

Copies the following properties:

* [MeshPart.MeshContent](/docs/reference/engine/classes/MeshPart#MeshContent) (implicitly updates
  [MeshId](/docs/reference/engine/classes/MeshPart#MeshId))
* [MeshPart.TextureContent](/docs/reference/engine/classes/MeshPart#TextureContent) (implicitly updates
  [TextureID](/docs/reference/engine/classes/MeshPart#TextureID))
* [MeshPart.RenderFidelity](/docs/reference/engine/classes/MeshPart#RenderFidelity)
* [MeshPart.CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity) (with any internal collision
  geometry)
* [MeshPart.FluidFidelity](/docs/reference/engine/classes/MeshPart#FluidFidelity) (with any internal aero geometry)
* [MeshPart.MeshSize](/docs/reference/engine/classes/MeshPart#MeshSize)

Provide feedback

---