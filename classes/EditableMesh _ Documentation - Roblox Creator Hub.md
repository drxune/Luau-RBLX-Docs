# EditableMesh | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/EditableMesh
Scraped: 2026-01-11T02:40:53.065202Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- EditableMesh
- MeshPart
- AssetService:CreateEditableMeshAsync()
- FixedSize
- MeshParts
- AssetService:CreateEditableMesh()
- AssetService:CreateMeshPartAsync()
- MeshPart:ApplyMesh()
- GetVertices()
- GetFaces()
- DoubleSided
- GetFacsPoses()
- FaceControls
- RaycastLocal()
- GetVerticesWithColor()
- GetVerticesWithNormal()
- GetVerticesWithUV()
- GetFacesWithColor()
- GetFacesWithNormal()
- GetFacesWithUV()
- SetVertexBoneWeights()
- GetVertexBoneWeights(vertexId)[i]
- GetVertexBones(vertexId)[i]
- SetVertexBones()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [EditableMesh](/docs/reference/engine/classes/EditableMesh)

English

Feedback

Engine Class

![EditableMesh](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/EditableMesh-Dark.webp)EditableMesh

Instance which allows for the runtime creation and manipulation of meshes.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [FixedSize](#FixedSize):[boolean](/docs/luau/booleans) |
| [SkinningEnabled](#SkinningEnabled):[boolean](/docs/luau/booleans)  Deprecated |

Methods

|  |
| --- |
| [AddBone](#AddBone)(boneProperties: [Dictionary](/docs/luau/tables#dictionaries)):[number](/docs/luau/numbers) |
| [AddColor](#AddColor)(color: [Color3](/docs/reference/engine/datatypes/Color3),alpha: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [AddNormal](#AddNormal)(normal: [Vector3](/docs/reference/engine/datatypes/Vector3)?):[number](/docs/luau/numbers) |
| [AddTriangle](#AddTriangle)(vertexId0: [number](/docs/luau/numbers),vertexId1: [number](/docs/luau/numbers),vertexId2: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [AddUV](#AddUV)(uv: [Vector2](/docs/reference/engine/datatypes/Vector2)):[number](/docs/luau/numbers) |
| [AddVertex](#AddVertex)(p: [Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers) |
| [Destroy](#Destroy)():() |
| [FindClosestPointOnSurface](#FindClosestPointOnSurface)(point: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Tuple](/docs/luau/tuples) |
| [FindClosestVertex](#FindClosestVertex)(toThisPoint: [Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers) |
| [FindVerticesWithinSphere](#FindVerticesWithinSphere)(center: [Vector3](/docs/reference/engine/datatypes/Vector3),radius: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetAdjacentFaces](#GetAdjacentFaces)(faceId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetAdjacentVertices](#GetAdjacentVertices)(vertexId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetBoneByName](#GetBoneByName)(boneName: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [GetBoneCFrame](#GetBoneCFrame)(boneId: [number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [GetBoneIsVirtual](#GetBoneIsVirtual)(boneId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [GetBoneName](#GetBoneName)(boneId: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [GetBoneParent](#GetBoneParent)(boneId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [GetBones](#GetBones)():[Array](/docs/luau/tables#arrays) |
| [GetCenter](#GetCenter)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GetColor](#GetColor)(colorId: [number](/docs/luau/numbers)):[Color3](/docs/reference/engine/datatypes/Color3)? |
| [GetColorAlpha](#GetColorAlpha)(colorId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers)? |
| [GetColors](#GetColors)():[Array](/docs/luau/tables#arrays) |
| [GetFaceColors](#GetFaceColors)(faceId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFaceNormals](#GetFaceNormals)(faceId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFaces](#GetFaces)():[Array](/docs/luau/tables#arrays) |
| [GetFacesWithAttribute](#GetFacesWithAttribute)(id: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetFacesWithColor](#GetFacesWithColor)(colorId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFacesWithNormal](#GetFacesWithNormal)(normalId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFacesWithUV](#GetFacesWithUV)(uvId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFaceUVs](#GetFaceUVs)(faceId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFaceVertices](#GetFaceVertices)(faceId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFacsCorrectivePose](#GetFacsCorrectivePose)(actions: [Array](/docs/luau/tables#arrays)):[Tuple](/docs/luau/tuples) |
| [GetFacsCorrectivePoses](#GetFacsCorrectivePoses)():[Array](/docs/luau/tables#arrays) |
| [GetFacsPose](#GetFacsPose)(action: [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit)):[Tuple](/docs/luau/tuples) |
| [GetFacsPoses](#GetFacsPoses)():[Array](/docs/luau/tables#arrays) |
| [GetNormal](#GetNormal)(normalId: [number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3)? |
| [GetNormals](#GetNormals)():[Array](/docs/luau/tables#arrays) |
| [GetPosition](#GetPosition)(vertexId: [number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GetSize](#GetSize)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GetUV](#GetUV)(uvId: [number](/docs/luau/numbers)):[Vector2](/docs/reference/engine/datatypes/Vector2)? |
| [GetUVs](#GetUVs)():[Array](/docs/luau/tables#arrays) |
| [GetVertexBones](#GetVertexBones)(vertexId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVertexBoneWeights](#GetVertexBoneWeights)(vertexId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVertexColors](#GetVertexColors)(vertexId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVertexFaceColor](#GetVertexFaceColor)(vertexId: [number](/docs/luau/numbers),faceId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [GetVertexFaceNormal](#GetVertexFaceNormal)(vertexId: [number](/docs/luau/numbers),faceId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [GetVertexFaces](#GetVertexFaces)(vertexId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVertexFaceUV](#GetVertexFaceUV)(vertexId: [number](/docs/luau/numbers),faceId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [GetVertexNormals](#GetVertexNormals)(vertexId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVertexUVs](#GetVertexUVs)(vertexId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVertices](#GetVertices)():[Array](/docs/luau/tables#arrays) |
| [GetVerticesWithAttribute](#GetVerticesWithAttribute)(id: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetVerticesWithColor](#GetVerticesWithColor)(colorId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVerticesWithNormal](#GetVerticesWithNormal)(normalId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetVerticesWithUV](#GetVerticesWithUV)(uvId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [IdDebugString](#IdDebugString)(id: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [MergeVertices](#MergeVertices)(mergeTolerance: [number](/docs/luau/numbers)):Map |
| [RaycastLocal](#RaycastLocal)(origin: [Vector3](/docs/reference/engine/datatypes/Vector3),direction: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Tuple](/docs/luau/tuples) |
| [RemoveBone](#RemoveBone)(boneId: [number](/docs/luau/numbers)):() |
| [RemoveFace](#RemoveFace)(faceId: [number](/docs/luau/numbers)):() |
| [RemoveUnused](#RemoveUnused)():[Array](/docs/luau/tables#arrays) |
| [ResetNormal](#ResetNormal)(normalId: [number](/docs/luau/numbers)):() |
| [SetBoneCFrame](#SetBoneCFrame)(boneId: [number](/docs/luau/numbers),cframe: [CFrame](/docs/reference/engine/datatypes/CFrame)):() |
| [SetBoneIsVirtual](#SetBoneIsVirtual)(boneId: [number](/docs/luau/numbers),virtual: [boolean](/docs/luau/booleans)):() |
| [SetBoneName](#SetBoneName)(boneId: [number](/docs/luau/numbers),name: [string](/docs/luau/strings)):() |
| [SetBoneParent](#SetBoneParent)(boneId: [number](/docs/luau/numbers),parentBoneId: [number](/docs/luau/numbers)):() |
| [SetColor](#SetColor)(colorId: [number](/docs/luau/numbers),color: [Color3](/docs/reference/engine/datatypes/Color3)):() |
| [SetColorAlpha](#SetColorAlpha)(colorId: [number](/docs/luau/numbers),alpha: [number](/docs/luau/numbers)):() |
| [SetFaceColors](#SetFaceColors)(faceId: [number](/docs/luau/numbers),ids: [Array](/docs/luau/tables#arrays)):() |
| [SetFaceNormals](#SetFaceNormals)(faceId: [number](/docs/luau/numbers),ids: [Array](/docs/luau/tables#arrays)):() |
| [SetFaceUVs](#SetFaceUVs)(faceId: [number](/docs/luau/numbers),ids: [Array](/docs/luau/tables#arrays)):() |
| [SetFaceVertices](#SetFaceVertices)(faceId: [number](/docs/luau/numbers),ids: [Array](/docs/luau/tables#arrays)):() |
| [SetFacsBonePose](#SetFacsBonePose)(action: [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit),boneId: [number](/docs/luau/numbers),cframe: [CFrame](/docs/reference/engine/datatypes/CFrame)):() |
| [SetFacsCorrectivePose](#SetFacsCorrectivePose)(actions: [Array](/docs/luau/tables#arrays),boneIds: [Array](/docs/luau/tables#arrays),cframes: [Array](/docs/luau/tables#arrays)):() |
| [SetFacsPose](#SetFacsPose)(action: [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit),boneIds: [Array](/docs/luau/tables#arrays),cframes: [Array](/docs/luau/tables#arrays)):() |
| [SetNormal](#SetNormal)(normalId: [number](/docs/luau/numbers),normal: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [SetPosition](#SetPosition)(vertexId: [number](/docs/luau/numbers),p: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [SetUV](#SetUV)(uvId: [number](/docs/luau/numbers),uv: [Vector2](/docs/reference/engine/datatypes/Vector2)):() |
| [SetVertexBones](#SetVertexBones)(vertexId: [number](/docs/luau/numbers),boneIDs: [Array](/docs/luau/tables#arrays)):() |
| [SetVertexBoneWeights](#SetVertexBoneWeights)(vertexId: [number](/docs/luau/numbers),boneWeights: [Array](/docs/luau/tables#arrays)):() |
| [SetVertexFaceColor](#SetVertexFaceColor)(vertexId: [number](/docs/luau/numbers),faceId: [number](/docs/luau/numbers),colorId: [number](/docs/luau/numbers)):() |
| [SetVertexFaceNormal](#SetVertexFaceNormal)(vertexId: [number](/docs/luau/numbers),faceId: [number](/docs/luau/numbers),normalId: [number](/docs/luau/numbers)):() |
| [SetVertexFaceUV](#SetVertexFaceUV)(vertexId: [number](/docs/luau/numbers),faceId: [number](/docs/luau/numbers),uvId: [number](/docs/luau/numbers)):() |
| [Triangulate](#Triangulate)():() |

Inherited Members

6 inherited from [Object](/docs/reference/engine/classes/Object)

EditableMesh changes the applied visual mesh when linked to a
[MeshPart](/docs/reference/engine/classes/MeshPart), allowing for querying and modification of the mesh both in
Studio and in experience.

#### Enabling for Published Experiences

For security purposes, using EditableMesh fails by default for published
experiences. To enable usage of EditableMesh, you must be 13+ age verified
and ID verified. After you are verified, open Studio's
[Game Settings](/docs/studio/game-settings), select Security, and
enable the Allow Mesh & Image APIs toggle. Remember to
review the
[Terms of Use](https://en.help.roblox.com/hc/en-us/articles/115004647846-Roblox-Terms-of-Use#creators-restrictions-on-use)
before enabling the toggle.

#### Permissions

To prevent misuse, [AssetService:CreateEditableMeshAsync()](/docs/reference/engine/classes/AssetService#CreateEditableMeshAsync) will only
allow you to load and edit mesh assets:

* That are owned by the creator of the experience (if the experience is owned
  by an individual).
* That are owned by a group (if the experience is owned by the group).
* That are owned by the logged in Studio user (if the place file has not yet
  been saved or published to Roblox).

#### Memory Limits

Editable assets are currently expensive for memory usage. To minimize its
impact on client performance, EditableMesh has strict client-side memory
budgets, although the server, Studio, and plugins operate with unlimited
memory. Using [FixedSize](/docs/reference/engine/classes/EditableMesh#FixedSize) may help you stay
within the memory budget and, in some scenarios, linking one EditableMesh to
multiple [MeshParts](/docs/reference/engine/classes/MeshPart) (multi-referencing) can help with memory
optimization.

#### Creation and Display

An EditableMesh can be created from an existing [Content](/docs/reference/engine/datatypes/Content) of a
[MeshPart](/docs/reference/engine/classes/MeshPart) or a mesh ID using
[AssetService:CreateEditableMeshAsync()](/docs/reference/engine/classes/AssetService#CreateEditableMeshAsync), or a blank EditableMesh can
be created with [AssetService:CreateEditableMesh()](/docs/reference/engine/classes/AssetService#CreateEditableMesh). It can then be
displayed, modified, and its collision model updated. Not all of the steps are
necessary; for example, you might want to create an EditableMesh just to
raycast without ever displaying it.

```
local AssetService = game:GetService("AssetService")



-- Create empty EditableMesh



local editableMesh = AssetService:CreateEditableMesh()



-- Create EditableMesh from asset ID



local editableMeshFromAsset = nil



local success, errorMessage = pcall(function()



editableMeshFromAsset = AssetService:CreateEditableMeshAsync(Content.fromAssetId(ASSET_ID))



end)



-- Create EditableMesh from another EditableMesh



local editableMeshFromAnother = nil



local success, errorMessage = pcall(function()



editableMeshFromAnother = AssetService:CreateEditableMeshAsync(Content.fromObject(OTHER_EDITABLE_MESH))



end)



-- Create EditableMesh from MeshPart



local editableMeshFromMeshPart = nil



local success, errorMessage = pcall(function()



editableMeshFromMeshPart = AssetService:CreateEditableMeshAsync(MESH_PART.MeshContent)



end)
```

An EditableMesh is displayed when it's linked to a new [MeshPart](/docs/reference/engine/classes/MeshPart),
through [AssetService:CreateMeshPartAsync()](/docs/reference/engine/classes/AssetService#CreateMeshPartAsync). You can create more
[MeshPart](/docs/reference/engine/classes/MeshPart) instances that reference the same EditableMesh
[Content](/docs/reference/engine/datatypes/Content), or link to an existing [MeshPart](/docs/reference/engine/classes/MeshPart) through
[MeshPart:ApplyMesh()](/docs/reference/engine/classes/MeshPart#ApplyMesh).

```
local AssetService = game:GetService("AssetService")



local Workspace = game:GetService("Workspace")



-- Create EditableMesh from asset ID



local editableMeshFromAsset = nil



local success, errorMessage = pcall(function()



editableMeshFromAsset = AssetService:CreateEditableMeshAsync(Content.fromAssetId(ASSET_ID))



end)



-- Create new MeshPart linked to the EditableMesh



local newMeshPart = nil



local success, errorMessage = pcall(function()



newMeshPart = AssetService:CreateMeshPartAsync(Content.fromObject(editableMeshFromAsset))



end)



-- Alternatively, link the new MeshPart created above to an existing MeshPart



local existingMeshPart = Workspace:FindFirstChild("EXISTING_MESH_PART")



existingMeshPart:ApplyMesh(newMeshPart)
```

To recalculate collision and fluid geometry after editing, you can again call
[AssetService:CreateMeshPartAsync()](/docs/reference/engine/classes/AssetService#CreateMeshPartAsync) and [MeshPart:ApplyMesh()](/docs/reference/engine/classes/MeshPart#ApplyMesh) to
update an existing [MeshPart](/docs/reference/engine/classes/MeshPart). It's generally recommended to do this at
the end of a conceptual edit, not after individual calls to methods that
manipulate geometry. Visual changes to the mesh will always be immediately
reflected by the engine, without the need to call
[AssetService:CreateMeshPartAsync()](/docs/reference/engine/classes/AssetService#CreateMeshPartAsync).

#### Fixed-Size Meshes

When creating an EditableMesh from an existing mesh asset (via
[AssetService:CreateEditableMeshAsync()](/docs/reference/engine/classes/AssetService#CreateEditableMeshAsync)), the resulting editable mesh
is fixed-size by default. Fixed-size meshes are more efficient in terms of
memory but you cannot change the number of vertices, faces, or attributes.
Only the values of vertex attributes and positions can be edited.

```
local AssetService = game:GetService("AssetService")



-- Create EditableMesh without fixed-size default



local editableMeshFromAsset = nil



local success, errorMessage = pcall(function()



editableMeshFromAsset = AssetService:CreateEditableMeshAsync(Content.fromAssetId(ASSET_ID), {FixedSize = false})



end)
```

#### Stable Vertex/Face IDs

Many EditableMesh methods take vertex, normal, UV, color and
face IDs. These are represented as integers in Luau but they require some
special handling. The main difference is that IDs are stable and they remain
the same even if other parts of the mesh change. For example, if an
EditableMesh has five vertices {1, 2, 3, 4, 5} and you remove vertex 4,
the new vertices will be {1, 2, 3, 5}.

Note that the IDs are not guaranteed to be in order and there may be holes in
the numbering, so when iterating through vertices or faces, you should iterate
through the table returned by [GetVertices()](/docs/reference/engine/classes/EditableMesh#GetVertices)
or [GetFaces()](/docs/reference/engine/classes/EditableMesh#GetFaces).

#### Split Vertex Attributes

A vertex is a corner of a face, and topologically connects faces together.
Vertices can have several attributes: position, normal, UV coordinate, color,
and transparency.

Sometimes it's useful for all faces that touch a vertex to use the same
attribute values, but sometimes you'll want different faces to use different
attribute values on the same vertex. For example, on a smooth sphere, each
vertex will only have a single normal. In contrast, at the corner of a cube,
the vertex will have 3 different normals (one for each adjacent face). You can
also have seams in the UV coordinates or sharp changes in the vertex colors.

When creating faces, every vertex will by default have one of each attribute:
one normal, one UV coordinate, and one color/transparency. If you want to
create a seam, you should create new attributes and set them on the face. For
example, this code will create a sharp cube:

```
local AssetService = game:GetService("AssetService")



-- Given 4 vertex IDs, adds a new normal and 2 triangles, making a sharp quad



local function addSharpQuad(editableMesh, vid0, vid1, vid2, vid3)



local nid = editableMesh:AddNormal()  -- This creates a normal ID which is automatically computed



local fid1 = editableMesh:AddTriangle(vid0, vid1, vid2)



editableMesh:SetFaceNormals(fid1, {nid, nid, nid})



local fid2 = editableMesh:AddTriangle(vid0, vid2, vid3)



editableMesh:SetFaceNormals(fid2, {nid, nid, nid})



end



-- Makes a cube with creased edges between the 6 sides



local function makeSharpCube()



local editableMesh = AssetService:CreateEditableMesh()



local v1 = editableMesh:AddVertex(Vector3.new(0, 0, 0))



local v2 = editableMesh:AddVertex(Vector3.new(1, 0, 0))



local v3 = editableMesh:AddVertex(Vector3.new(0, 1, 0))



local v4 = editableMesh:AddVertex(Vector3.new(1, 1, 0))



local v5 = editableMesh:AddVertex(Vector3.new(0, 0, 1))



local v6 = editableMesh:AddVertex(Vector3.new(1, 0, 1))



local v7 = editableMesh:AddVertex(Vector3.new(0, 1, 1))



local v8 = editableMesh:AddVertex(Vector3.new(1, 1, 1))



addSharpQuad(editableMesh, v5, v6, v8, v7)  -- Front



addSharpQuad(editableMesh, v1, v3, v4, v2)  -- Back



addSharpQuad(editableMesh, v1, v5, v7, v3)  -- Left



addSharpQuad(editableMesh, v2, v4, v8, v6)  -- Right



addSharpQuad(editableMesh, v1, v2, v6, v5)  -- Bottom



addSharpQuad(editableMesh, v3, v7, v8, v4)  -- Top



editableMesh:RemoveUnused()



return editableMesh



end
```

#### Winding

Mesh faces have a front side and a back side. When drawing meshes, only the
front of the faces are drawn by default, although you can change this by
setting the mesh' [DoubleSided](/docs/reference/engine/classes/MeshPart#DoubleSided) property to true.

The order of the vertices around the face determines whether you are looking
at the front or the back. The front of the face is visible when the vertices
go counterclockwise around it.

![Order of the vertices around the face](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/EditableMesh/Winding.png)

#### FACS Poses

Animatable heads use the Facial Action Coding System (FACS). See the
[FACS poses reference](/docs/art/characters/facial-animation/facs-poses-reference)
for helpful information when using
[GetFacsPoses()](/docs/reference/engine/classes/EditableMesh#GetFacsPoses) and similar methods.

Each FACS pose is specified by an [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit) value. For the FACS
pose, virtual bones can each have a [CFrame](/docs/reference/engine/datatypes/CFrame) that transforms the
bones' initial [CFrame](/docs/reference/engine/datatypes/CFrame) in the bind pose of the mesh into the
[CFrame](/docs/reference/engine/datatypes/CFrame) for that FACS action unit's pose. All bone
[CFrames](/docs/reference/engine/datatypes/CFrame) are in the mesh's local space.

These FACS poses are blended together during animation. Sometimes, the
blending of the base poses produces poor results. In those cases, you can
override the blending of specific combinations of base poses with a
[corrective pose](/docs/art/characters/facial-animation/create-basic-heads#combination-poses)
that is more pleasing. A corrective pose is specified by 2 or 3
[Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit) values. Like a base FACS pose, for a corrective pose,
virtual bones can each have a [CFrame](/docs/reference/engine/datatypes/CFrame) that transforms the bones'
initial [CFrame](/docs/reference/engine/datatypes/CFrame) in the bind pose of the mesh into the
[CFrame](/docs/reference/engine/datatypes/CFrame) for that FACS corrective.

Please note that corrective poses that operate on both left and right action
units are not currently expressible. For example, using LeftCheekPuff and
RightEyeClosed together in a corrective pose is not currently possible.

#### Limitations

EditableMesh currently has a limit of 60,000 vertices and 20,000 triangles.
Attempting to add too many vertices or triangles will cause an error.

---

API Reference

Properties

FixedSize

Read Only

Not Replicated

Roblox Security

Read Parallel

Returns true if a mesh is fixed-size.

EditableMesh.FixedSize:[boolean](/docs/luau/booleans)

Fixed-sized meshes allow changing the values of vertex attributes but do
not allow vertices and triangles to be added or deleted.

Provide feedback

---

SkinningEnabled

Deprecated

Show details

---

Methods

AddBone

Adds a new bone and returns a stable bone ID.

EditableMesh:AddBone(boneProperties:[Dictionary](/docs/luau/tables#dictionaries)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| boneProperties:[Dictionary](/docs/luau/tables#dictionaries)  Options table containing bone parameters:   * Name — A string that specifies the bone name. Note that all bone   names in a mesh must be unique. * ParentId — Optional bone ID of the new bone's parent. * CFrame — Initial [CFrame](/docs/reference/engine/datatypes/CFrame) of the bone in the bind pose of   the mesh, in the mesh's local space. * Virtual — Boolean that specifies whether this bone is virtual.   Virtual bones can only be bound to a [FaceControls](/docs/reference/engine/classes/FaceControls) instance. |

Returns

[number](/docs/luau/numbers)

Stable bone ID of the new bone.

Adds a new bone and returns a stable bone ID.

Provide feedback

---

AddColor

Adds a new color to the geometry and returns a stable color ID.

EditableMesh:AddColor(

color:[Color3](/docs/reference/engine/datatypes/Color3), alpha:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| color:[Color3](/docs/reference/engine/datatypes/Color3)  The new color. |
| alpha:[number](/docs/luau/numbers)  The color alpha (transparency). |

Returns

[number](/docs/luau/numbers)

Stable color ID of the new color.

Adds a new color to the geometry and returns a stable color ID.

Provide feedback

---

AddNormal

Adds a new normal to the geometry and returns a stable normal ID.

EditableMesh:AddNormal(normal:[Vector3](/docs/reference/engine/datatypes/Vector3)?):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| normal:[Vector3](/docs/reference/engine/datatypes/Vector3)?  The normal vector. If the normal value isn't specified, the normal will be automatically calculated. |

Returns

[number](/docs/luau/numbers)

Stable normal ID of the new normal.

Adds a new normal to the geometry and returns a stable normal ID. If the
normal value isn't specified, the normal will be automatically calculated.

Provide feedback

---

AddTriangle

Adds a new triangle to the mesh and returns a stable face ID.

EditableMesh:AddTriangle(

vertexId0:[number](/docs/luau/numbers), vertexId1:[number](/docs/luau/numbers), vertexId2:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| vertexId0:[number](/docs/luau/numbers)  ID of the first vertex of the triangle. |
| vertexId1:[number](/docs/luau/numbers)  ID of the second vertex of the triangle. |
| vertexId2:[number](/docs/luau/numbers)  ID of the third vertex of the triangle. |

Returns

[number](/docs/luau/numbers)

Stable face ID of the new face.

Adds a new triangle to the mesh and returns a stable face ID.

Provide feedback

---

AddUV

Adds a new UV to the geometry and returns a stable UV ID.

EditableMesh:AddUV(uv:[Vector2](/docs/reference/engine/datatypes/Vector2)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| uv:[Vector2](/docs/reference/engine/datatypes/Vector2)  The new UV coordinate. |

Returns

[number](/docs/luau/numbers)

Stable UV ID of the new UV.

Adds a new UV to the geometry and returns a stable UV ID.

Provide feedback

---

AddVertex

Adds a new vertex to the geometry and returns a stable vertex ID.

EditableMesh:AddVertex(p:[Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| p:[Vector3](/docs/reference/engine/datatypes/Vector3)  Position in the mesh's local object space. |

Returns

[number](/docs/luau/numbers)

Stable vertex ID of the new vertex.

Adds a new vertex to the geometry and returns a stable vertex ID.

Provide feedback

---

Destroy

Destroys the mesh.

EditableMesh:Destroy():()

Returns

()

Destroys the contents of the mesh, immediately reclaiming used memory.

Provide feedback

---

FindClosestPointOnSurface

Finds the closest point on the mesh's surface.

EditableMesh:FindClosestPointOnSurface(point:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| point:[Vector3](/docs/reference/engine/datatypes/Vector3)  Point position in the mesh's local object space. |

Returns

[Tuple](/docs/luau/tuples)

Tuple of the face ID, point on the mesh in local object space, and the
barycentric coordinate of the position within the face.

Finds the closest point on the mesh's surface. Returns the face ID, point
on the mesh in local object space, and the barycentric coordinate of the
position within the face. See
[RaycastLocal()](/docs/reference/engine/classes/EditableMesh#RaycastLocal) for more information on
barycentric coordinates.

Provide feedback

---

FindClosestVertex

Finds the closest vertex to a specific point in space.

EditableMesh:FindClosestVertex(toThisPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| toThisPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)  Point position in the mesh's local object space. |

Returns

[number](/docs/luau/numbers)

Closest stable vertex ID to the specified point in space.

Finds the closest vertex to a specific point in space and returns a stable
vertex ID.

Provide feedback

---

FindVerticesWithinSphere

Finds all vertices within a specific sphere.

EditableMesh:FindVerticesWithinSphere(

center:[Vector3](/docs/reference/engine/datatypes/Vector3), radius:[number](/docs/luau/numbers)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| center:[Vector3](/docs/reference/engine/datatypes/Vector3)  Center of the sphere in the mesh's local object space. |
| radius:[number](/docs/luau/numbers)  Radius of the sphere. |

Returns

[Array](/docs/luau/tables#arrays)

List of stable vertex IDs within the requested sphere.

Finds all vertices within a specific sphere and returns a list of stable
vertex IDs.

Provide feedback

---

GetAdjacentFaces

Returns a list of faces adjacent to a given face.

EditableMesh:GetAdjacentFaces(faceId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers) |

Returns

[Array](/docs/luau/tables#arrays)

List of face IDs adjacent to the given face.

Given a stable face ID, returns a list of adjacent faces.

![Adjacent faces indicated around requested face](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/EditableMesh/GetAdjacentTriangles.png)

Provide feedback

---

GetAdjacentVertices

Returns a list of vertices adjacent to a given vertex.

EditableMesh:GetAdjacentVertices(vertexId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Vertex ID around which to get adjacent vertices. |

Returns

[Array](/docs/luau/tables#arrays)

List of IDs of adjacent vertices around the given vertex ID.

Given a stable vertex ID, returns a list of adjacent vertices.

![Adjacent vertices indicated around requested vertex](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/EditableMesh/GetAdjacentVertices.png)

Provide feedback

---

GetBoneByName

Finds the bone ID of the bone with the given name.

EditableMesh:GetBoneByName(boneName:[string](/docs/luau/strings)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| boneName:[string](/docs/luau/strings)  Bone name to search for. |

Returns

[number](/docs/luau/numbers)

Bone ID of the bone with the given name.

Finds the bone ID of the bone with the given name. Errors if no bone with
that name exists.

Provide feedback

---

GetBoneCFrame

Returns the initial [CFrame](/docs/reference/engine/datatypes/CFrame) of the bone in the bind pose of the
mesh.

EditableMesh:GetBoneCFrame(boneId:[number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to get the [CFrame](/docs/reference/engine/datatypes/CFrame). |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Initial [CFrame](/docs/reference/engine/datatypes/CFrame) of the bone in the bind pose of the mesh, in
the mesh's local space.

Returns the initial [CFrame](/docs/reference/engine/datatypes/CFrame) of the bone in the bind pose of the
mesh, in the mesh's local space.

Provide feedback

---

GetBoneIsVirtual

Returns true if the bone is virtual.

EditableMesh:GetBoneIsVirtual(boneId:[number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to get whether the bone is virtual. |

Returns

[boolean](/docs/luau/booleans)

Whether the bone with the given bone ID is virtual. Virtual bones can
only be bound to a [FaceControls](/docs/reference/engine/classes/FaceControls) instance.

Returns true if the bone is virtual. Virtual bones can only be bound to
a [FaceControls](/docs/reference/engine/classes/FaceControls) instance.

Provide feedback

---

GetBoneName

Returns the bone name.

EditableMesh:GetBoneName(boneId:[number](/docs/luau/numbers)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to get the name. |

Returns

[string](/docs/luau/strings)

Name of the bone with the given bone ID.

Returns the bone name.

Provide feedback

---

GetBoneParent

Returns the parent bone ID, if any.

EditableMesh:GetBoneParent(boneId:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to get the parent. |

Returns

[number](/docs/luau/numbers)

Bone ID for the parent of the bone with the given bone ID. If there is
no parent, returns 0.

Returns the parent bone ID, if any.

Provide feedback

---

GetBones

Returns all bones of the mesh.

EditableMesh:GetBones():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

List of stable bone IDs.

Returns all bones of the mesh as a list of stable bone IDs.

Provide feedback

---

GetCenter

EditableMesh:GetCenter():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Center of the bounding box of the EditableMesh.

Provide feedback

---

GetColor

Returns the color for the given color ID.

EditableMesh:GetColor(colorId:[number](/docs/luau/numbers)):[Color3](/docs/reference/engine/datatypes/Color3)?

Parameters

|  |
| --- |
| colorId:[number](/docs/luau/numbers)  Color ID for which to get the color. |

Returns

[Color3](/docs/reference/engine/datatypes/Color3)?

Color for the requested stable color ID.

Returns the color for the given color ID.

Provide feedback

---

GetColorAlpha

Returns the color alpha (transparency) at the given color ID.

EditableMesh:GetColorAlpha(colorId:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)?

Parameters

|  |
| --- |
| colorId:[number](/docs/luau/numbers)  Color ID for which to get the alpha. |

Returns

[number](/docs/luau/numbers)?

Color alpha at the request stable color ID.

Returns the color alpha (transparency) at the given stable color ID.

Provide feedback

---

GetColors

Returns all colors of the mesh.

EditableMesh:GetColors():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

List of stable color IDs.

Returns all colors of the mesh as a list of stable color IDs.

Provide feedback

---

GetFaceColors

Returns the face's color IDs for the vertices on the face.

EditableMesh:GetFaceColors(faceId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers)  Face ID for which to get the color IDs. |

Returns

[Array](/docs/luau/tables#arrays)

List of color IDs used for the vertices on the given face.

Returns the face's color IDs for the vertices on the face.

Provide feedback

---

GetFaceNormals

Returns the face's normal IDs for the vertices on the face.

EditableMesh:GetFaceNormals(faceId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers)  Face ID for which to get the normal IDs. |

Returns

[Array](/docs/luau/tables#arrays)

List of normal IDs used for the vertices on the given face.

Returns the face's normal IDs for the vertices on the face.

Provide feedback

---

GetFaces

Returns all faces of the mesh.

EditableMesh:GetFaces():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

List of stable face IDs.

Returns all faces of the mesh as a list of stable face IDs.

Provide feedback

---

GetFacesWithAttribute

Deprecated

Show details

---

GetFacesWithColor

Returns an array of face IDs that use the given color ID.

EditableMesh:GetFacesWithColor(colorId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| colorId:[number](/docs/luau/numbers)  Color ID to find faces for. |

Returns

[Array](/docs/luau/tables#arrays)

List of face IDs that use the provided color ID.

Returns an array of face IDs that use the given color ID. Use together
with [GetVerticesWithColor()](/docs/reference/engine/classes/EditableMesh#GetVerticesWithColor) to
obtain all face/vertex pairs.

Provide feedback

---

GetFacesWithNormal

Returns an array of face IDs that use the given normal ID.

EditableMesh:GetFacesWithNormal(normalId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| normalId:[number](/docs/luau/numbers)  Normal ID to find faces for. |

Returns

[Array](/docs/luau/tables#arrays)

List of face IDs that use the provided normal ID.

Returns an array of face IDs that use the given normal ID. Use together
with [GetVerticesWithNormal()](/docs/reference/engine/classes/EditableMesh#GetVerticesWithNormal)
to obtain all face/vertex pairs.

Provide feedback

---

GetFacesWithUV

Returns an array of face IDs that use the given UV ID.

EditableMesh:GetFacesWithUV(uvId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| uvId:[number](/docs/luau/numbers)  UV ID to find faces for. |

Returns

[Array](/docs/luau/tables#arrays)

List of face IDs that use the provided UV ID.

Returns an array of face IDs that use the given UV ID. Use together with
[GetVerticesWithUV()](/docs/reference/engine/classes/EditableMesh#GetVerticesWithUV) to obtain all
face/vertex pairs.

Provide feedback

---

GetFaceUVs

Returns the face's UV IDs for the vertices on the face.

EditableMesh:GetFaceUVs(faceId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers)  Face ID for which to get the UV IDs. |

Returns

[Array](/docs/luau/tables#arrays)

List of UV IDs used for the vertices on the given face.

Returns the face's UV IDs for the vertices on the face.

Provide feedback

---

GetFaceVertices

Returns the face's vertex IDs.

EditableMesh:GetFaceVertices(faceId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers) |

Returns

[Array](/docs/luau/tables#arrays)

List of vertex IDs around the given face.

Returns the face's vertex IDs.

Provide feedback

---

GetFacsCorrectivePose

Returns bone IDs and bone [CFrames](/docs/reference/engine/datatypes/CFrame) for all bones in a
specific FACS corrective pose.

EditableMesh:GetFacsCorrectivePose(actions:[Array](/docs/luau/tables#arrays)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| actions:[Array](/docs/luau/tables#arrays)  Array or 2 or 3 [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit) values that specify a corrective pose. |

Returns

[Tuple](/docs/luau/tuples)

Array of bone IDs and corresponding array of bone
[CFrames](/docs/reference/engine/datatypes/CFrame).

Returns bone IDs and bone [CFrames](/docs/reference/engine/datatypes/CFrame) for all bones in a
specific FACS corrective pose. Each bone [CFrame](/docs/reference/engine/datatypes/CFrame) transforms the
bone from the initial bone [CFrame](/docs/reference/engine/datatypes/CFrame) in the bind pose of the mesh
to the combined bone [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. All
[CFrames](/docs/reference/engine/datatypes/CFrame) are in the mesh's local space.

Provide feedback

---

GetFacsCorrectivePoses

Returns all FACS corrective poses that are in use.

EditableMesh:GetFacsCorrectivePoses():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Array of corrective poses. Each corrective pose is specified by a
small array of 2 or 3 [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit) values.

Returns all FACS corrective poses that are in use. Each corrective pose is
specified by 2 or 3 [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit) values.

Provide feedback

---

GetFacsPose

Returns bone IDs and bone [CFrames](/docs/reference/engine/datatypes/CFrame) for all bones in a
specific FACS action unit.

EditableMesh:GetFacsPose(action:[Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| action:[Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit)  FACS action unit for which to get the pose. |

Returns

[Tuple](/docs/luau/tuples)

Array of bone IDs and corresponding array of bone [CFrame](/docs/reference/engine/datatypes/CFrame).

Returns bone IDs and bone [CFrames](/docs/reference/engine/datatypes/CFrame) for all bones in a
specific FACS action unit. Each bone [CFrame](/docs/reference/engine/datatypes/CFrame) transforms the bone
from the initial bone [CFrame](/docs/reference/engine/datatypes/CFrame) in the bind pose of the mesh to
the combined bone [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. All
[CFrames](/docs/reference/engine/datatypes/CFrame) are in the mesh's local space.

Provide feedback

---

GetFacsPoses

Returns all FACS action units that have poses defined.

EditableMesh:GetFacsPoses():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Array of [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit), one for each FACS action unit that has
a pose defined.

Returns all FACS action units that have poses defined.

Provide feedback

---

GetNormal

Returns the normal vector for the given normal ID.

EditableMesh:GetNormal(normalId:[number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3)?

Parameters

|  |
| --- |
| normalId:[number](/docs/luau/numbers)  Normal ID for which to get the normal vector. |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)?

Normal vector at the requested normal ID.

Returns the normal vector for the given normal ID.

Provide feedback

---

GetNormals

Returns all normals of the mesh.

EditableMesh:GetNormals():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

List of stable normal IDs.

Returns all normals of the mesh as a list of stable normal IDs.

Provide feedback

---

GetPosition

Gets the position of a vertex.

EditableMesh:GetPosition(vertexId:[number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID for which to get the position. |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Position of a vertex in the mesh's local object space.

Gets the position of a vertex in the mesh's local object space.

Provide feedback

---

GetSize

EditableMesh:GetSize():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Size of the EditableMesh.

Provide feedback

---

GetUV

Returns UV coordinates at the given UV ID.

EditableMesh:GetUV(uvId:[number](/docs/luau/numbers)):[Vector2](/docs/reference/engine/datatypes/Vector2)?

Parameters

|  |
| --- |
| uvId:[number](/docs/luau/numbers)  UV ID for which to get the UV coordinate. |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)?

UV coordinates at the requested UV ID.

Returns UV coordinates at the given UV ID.

Provide feedback

---

GetUVs

Returns all UVs of the mesh.

EditableMesh:GetUVs():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

List of stable UV IDs.

Returns all UVs of the mesh as a list of stable UV IDs.

Provide feedback

---

GetVertexBones

Returns all bone IDs that are associated with the vertex for skinning.

EditableMesh:GetVertexBones(vertexId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Vertex ID for which to get the associated bones. |

Returns

[Array](/docs/luau/tables#arrays)

Bone IDs associated with the vertex for skinning.

Returns all bone IDs that are associated with the vertex for skinning.

Provide feedback

---

GetVertexBoneWeights

Returns skinning blend weights for each bone that is associated with the
vertex.

EditableMesh:GetVertexBoneWeights(vertexId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Vertex ID for which to get the associated bone weights. |

Returns

[Array](/docs/luau/tables#arrays)

Skinning blend weights for each bone that is associated with the
vertex.

Returns skinning blend weights for each bone that is associated with the
vertex.

Provide feedback

---

GetVertexColors

Returns the color IDs of the faces attached to the given vertex.

EditableMesh:GetVertexColors(vertexId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID to find color IDs. |

Returns

[Array](/docs/luau/tables#arrays)

Array of color IDs of faces attached to the given vertex.

Returns the color IDs of the faces attached to the given vertex.

Provide feedback

---

GetVertexFaceColor

Returns the color ID of a vertex/face pair.

EditableMesh:GetVertexFaceColor(

vertexId:[number](/docs/luau/numbers), faceId:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID. |
| faceId:[number](/docs/luau/numbers)  Stable face ID. |

Returns

[number](/docs/luau/numbers)

Stable color ID of the vertex/face pair.

Returns the color ID of a vertex/face pair.

Provide feedback

---

GetVertexFaceNormal

Returns the normal ID of a vertex/face pair.

EditableMesh:GetVertexFaceNormal(

vertexId:[number](/docs/luau/numbers), faceId:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID. |
| faceId:[number](/docs/luau/numbers)  Stable face ID. |

Returns

[number](/docs/luau/numbers)

Stable normal ID of the vertex/face pair.

Returns the normal ID of a vertex/face pair.

Provide feedback

---

GetVertexFaces

Returns the face IDs of the faces attached to the given vertex.

EditableMesh:GetVertexFaces(vertexId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID to find faces for. |

Returns

[Array](/docs/luau/tables#arrays)

Array of face IDs attached to the given vertex.

Returns the face IDs of the faces attached to the given vertex.

Provide feedback

---

GetVertexFaceUV

Returns the UV ID of a vertex/face pair.

EditableMesh:GetVertexFaceUV(

vertexId:[number](/docs/luau/numbers), faceId:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID. |
| faceId:[number](/docs/luau/numbers)  Stable face ID. |

Returns

[number](/docs/luau/numbers)

Stable UV ID of the vertex/face pair.

Returns the UV ID of a vertex/face pair.

Provide feedback

---

GetVertexNormals

Returns the normal IDs of the faces attached to the given vertex.

EditableMesh:GetVertexNormals(vertexId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID to find normal IDs. |

Returns

[Array](/docs/luau/tables#arrays)

Array of normal IDs of faces attached to the given vertex.

Returns the normal IDs of the faces attached to the given vertex.

Provide feedback

---

GetVertexUVs

Returns the UV IDs of the faces attached to the given vertex.

EditableMesh:GetVertexUVs(vertexId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID to find UV IDs. |

Returns

[Array](/docs/luau/tables#arrays)

Array of UV IDs of faces attached to the given vertex.

Returns the UV IDs of the faces attached to the given vertex.

Provide feedback

---

GetVertices

Returns all vertices as a list of stable vertex IDs.

EditableMesh:GetVertices():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

List of stable vertex IDs.

Returns all vertices as a list of stable vertex IDs.

Provide feedback

---

GetVerticesWithAttribute

Deprecated

Show details

---

GetVerticesWithColor

Returns an array of vertex IDs that use the given color ID.

EditableMesh:GetVerticesWithColor(colorId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| colorId:[number](/docs/luau/numbers)  Color ID to find faces for. |

Returns

[Array](/docs/luau/tables#arrays)

List of face IDs that use the provided color ID.

Returns an array of vertex IDs that use the given color ID. Use together
with [GetFacesWithColor()](/docs/reference/engine/classes/EditableMesh#GetFacesWithColor) to
obtain all face/vertex pairs.

Provide feedback

---

GetVerticesWithNormal

Returns an array of vertex IDs that use the given normal ID.

EditableMesh:GetVerticesWithNormal(normalId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| normalId:[number](/docs/luau/numbers)  Normal ID to find vertices for. |

Returns

[Array](/docs/luau/tables#arrays)

List of vertex IDs that use the provided normal ID.

Returns an array of vertex IDs that use the given normal ID. Use together
with [GetFacesWithNormal()](/docs/reference/engine/classes/EditableMesh#GetFacesWithNormal) to
obtain all face/vertex pairs.

Provide feedback

---

GetVerticesWithUV

Returns an array of vertex IDs that use the given UV ID.

EditableMesh:GetVerticesWithUV(uvId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| uvId:[number](/docs/luau/numbers)  UV ID to find vertices for. |

Returns

[Array](/docs/luau/tables#arrays)

List of vertex IDs that use the provided UV ID.

Returns an array of vertex IDs that use the given UV ID. Use together with
[GetFacesWithUV()](/docs/reference/engine/classes/EditableMesh#GetFacesWithUV) to obtain all
face/vertex pairs.

Provide feedback

---

IdDebugString

Returns a string describing a stable ID, useful for debugging purposes.

EditableMesh:IdDebugString(id:[number](/docs/luau/numbers)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| id:[number](/docs/luau/numbers)  ID for which to return a debugging information string. |

Returns

[string](/docs/luau/strings)

String that describes the ID in human-readable format.

Returns a string describing a stable ID, useful for debugging purposes,
like f17 or v12, containing the type, ID number, and version.

Provide feedback

---

MergeVertices

Merges vertices that touch together.

EditableMesh:MergeVertices(mergeTolerance:[number](/docs/luau/numbers)):Map

Parameters

|  |
| --- |
| mergeTolerance:[number](/docs/luau/numbers)  The distance at which the vertices are considered to touch each other. |

Returns

Map

A mapping of old vertex ID to new vertex ID for vertices that have
been merged.

Merges vertices that touch together, to use a single vertex ID but keep
the other original attribute IDs.

Provide feedback

---

RaycastLocal

EditableMesh:RaycastLocal(

origin:[Vector3](/docs/reference/engine/datatypes/Vector3), direction:[Vector3](/docs/reference/engine/datatypes/Vector3)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| origin:[Vector3](/docs/reference/engine/datatypes/Vector3)  Origin of the ray in the mesh's local object space. |
| direction:[Vector3](/docs/reference/engine/datatypes/Vector3)  Direction of the ray. |

Returns

[Tuple](/docs/luau/tuples)

Tuple of the point of intersection, face ID, and barycentric
coordinates.

Casts a ray and returns a point of intersection, face ID, and barycentric
coordinates. The inputs and outputs of this method are in the mesh's local
object space.

A barycentric coordinate is a way of specifying a point within a face
as a weighted combination of the 3 vertices of the face. This is useful as
a general way of blending vertex attributes. See this method's code sample
as an illustration.

Code Samples

EditableMesh:RaycastLocal()

This code finds the position and UV coordinates of the closest point on an [EditableMesh](/docs/reference/engine/classes/EditableMesh) to the input point.

```
local AssetService = game:GetService("AssetService")



local Workspace = game:GetService("Workspace")



-- Initialize EditableMesh in space



local editableMesh = nil



local success, errorMsg = pcall(function()



editableMesh = AssetService:CreateEditableMeshAsync(Content.fromUri("rbxassetid://ASSET_ID"))



end)



local meshPart = nil



if success and editableMesh then



meshPart = AssetService:CreateMeshPartAsync(



Content.fromObject(editableMesh),



{ CollisionFidelity = Enum.CollisionFidelity.Hull }



)



meshPart.Parent = Workspace



else



warn(errorMsg)



end



-- Function that will cast a ray from the given point, returning the world point of the hit and the UV coordinate



local function castRayFromCamera(meshPart: MeshPart, editableMesh: EditableMesh, viewportPoint: Vector3)



if not meshPart then



return



end



-- Calculate how much the object is being scaled in each dimension



local renderScale = meshPart.Size / meshPart.MeshSize



-- Create ray from camera along the direction of a clicked point



local ray = Workspace.CurrentCamera:ViewportPointToRay(viewportPoint.X, viewportPoint.Y)



-- Convert to object space to use with RaycastLocal()



local relativeOrigin = meshPart.CFrame:PointToObjectSpace(ray.Origin) / renderScale



local relativeTarget = meshPart.CFrame:PointToObjectSpace(ray.Origin + ray.Direction * 100) / renderScale



local relativeDirection = relativeTarget - relativeOrigin



local faceId, point, barycentricCoordinate, vertId1, vertId2, vertId3 =



editableMesh:RaycastLocal(relativeOrigin, relativeDirection)



if not faceId then



-- Didn't hit any faces



return



end



-- Compute the hit point in world space



local worldHitPoint = meshPart.CFrame:PointToWorldSpace(point * renderScale)



-- Get the UVs on the face



local uvId1 = editableMesh:GetVertexFaceUV(vertId1, faceId)



local uvId2 = editableMesh:GetVertexFaceUV(vertId2, faceId)



local uvId3 = editableMesh:GetVertexFaceUV(vertId3, faceId)



local uv1 = editableMesh:GetUV(uvId1)



local uv2 = editableMesh:GetUV(uvId2)



local uv3 = editableMesh:GetUV(uvId3)



-- Interpolate UVs within the face based on the barycentric coordinate



local u = (barycentricCoordinate.x * uv1.x) + (barycentricCoordinate.y * uv2.x) + (barycentricCoordinate.z * uv3.x)



local v = (barycentricCoordinate.x * uv1.y) + (barycentricCoordinate.y * uv2.y) + (barycentricCoordinate.z * uv3.y)



return worldHitPoint, Vector2.new(u, v)



end
```

Provide feedback

---

RemoveBone

Removes a bone using its stable bone ID.

EditableMesh:RemoveBone(boneId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers) |

Returns

()

Removes a bone using its stable bone ID.

Provide feedback

---

RemoveFace

Removes a face using its stable face ID.

EditableMesh:RemoveFace(faceId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers) |

Returns

()

Removes a face using its stable face ID.

Provide feedback

---

RemoveUnused

Removes all unused vertices, normals, UVs, and colors, and returns the
removed IDs.

EditableMesh:RemoveUnused():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

All of the removed stable IDs.

Removes all vertices, normals, UVs, and colors which are not used in any
face, and returns the removed IDs.

Provide feedback

---

ResetNormal

Reset this normal ID to be automatically calculated.

EditableMesh:ResetNormal(normalId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| normalId:[number](/docs/luau/numbers)  Stable normal ID to reset. |

Returns

()

Reset this normal ID to be automatically calculated based on the shape of
the mesh, instead of manually set.

Provide feedback

---

SetBoneCFrame

Set the initial [CFrame](/docs/reference/engine/datatypes/CFrame) for a bone in the mesh's bind pose.

EditableMesh:SetBoneCFrame(

boneId:[number](/docs/luau/numbers), cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)

):()

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to set the initial [CFrame](/docs/reference/engine/datatypes/CFrame). |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  Initial [CFrame](/docs/reference/engine/datatypes/CFrame) for the bone in the mesh's bind pose, in the mesh's local space. |

Returns

()

Set the initial [CFrame](/docs/reference/engine/datatypes/CFrame) for a bone in the mesh's bind pose, in
the mesh's local space.

Provide feedback

---

SetBoneIsVirtual

Set whether a bone is virtual.

EditableMesh:SetBoneIsVirtual(

boneId:[number](/docs/luau/numbers), virtual:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to set whether the bone is virtual. |
| virtual:[boolean](/docs/luau/booleans)  Whether the bone should be virtual. |

Returns

()

Set whether a bone is virtual. Virtual bones can only be bound to a
[FaceControls](/docs/reference/engine/classes/FaceControls) instance.

Provide feedback

---

SetBoneName

Sets the name for a bone.

EditableMesh:SetBoneName(

boneId:[number](/docs/luau/numbers), name:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to set the name. |
| name:[string](/docs/luau/strings)  Bone name to set. |

Returns

()

Sets the name for a bone. Bone names can be 100 characters long and must
be unique in the mesh.

Provide feedback

---

SetBoneParent

Set a parent for a bone.

EditableMesh:SetBoneParent(

boneId:[number](/docs/luau/numbers), parentBoneId:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| boneId:[number](/docs/luau/numbers)  Bone ID for which to set the parent. |
| parentBoneId:[number](/docs/luau/numbers)  Parent bone ID. |

Returns

()

Set a parent for a bone.

Provide feedback

---

SetColor

Sets the color for a color ID.

EditableMesh:SetColor(

colorId:[number](/docs/luau/numbers), color:[Color3](/docs/reference/engine/datatypes/Color3)

):()

Parameters

|  |
| --- |
| colorId:[number](/docs/luau/numbers)  Stable color ID for which to set the color. |
| color:[Color3](/docs/reference/engine/datatypes/Color3)  Color to set. |

Returns

()

Sets the color for a color ID.

Provide feedback

---

SetColorAlpha

Sets the color alpha (transparency) for a color ID.

EditableMesh:SetColorAlpha(

colorId:[number](/docs/luau/numbers), alpha:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| colorId:[number](/docs/luau/numbers)  Stable color ID for which to set the color alpha. |
| alpha:[number](/docs/luau/numbers)  Alpha to set. |

Returns

()

Sets the color alpha (transparency) for a color ID.

Provide feedback

---

SetFaceColors

Sets the face's vertex colors to new color IDs.

EditableMesh:SetFaceColors(

faceId:[number](/docs/luau/numbers), ids:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers)  Face ID for which to update the vertex colors. |
| ids:[Array](/docs/luau/tables#arrays)  List of new stable color IDs to use for the given face's vertices. |

Returns

()

Sets the face's vertex colors to new color IDs.

Provide feedback

---

SetFaceNormals

Sets the face's vertex normals to new normal IDs.

EditableMesh:SetFaceNormals(

faceId:[number](/docs/luau/numbers), ids:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers)  Face ID for which to update the vertex normals. |
| ids:[Array](/docs/luau/tables#arrays)  List of new stable normal IDs to use for the given face's vertices. |

Returns

()

Sets the face's vertex normals to new normal IDs.

Provide feedback

---

SetFaceUVs

Sets the face's vertex UVs to new UV IDs.

EditableMesh:SetFaceUVs(

faceId:[number](/docs/luau/numbers), ids:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers)  Face ID for which to update the vertex UVs. |
| ids:[Array](/docs/luau/tables#arrays)  List of new stable UV IDs to use for the given face's vertices. |

Returns

()

Sets the face's vertex UVs to new UV IDs.

Provide feedback

---

SetFaceVertices

Sets the face's vertices to new vertex IDs.

EditableMesh:SetFaceVertices(

faceId:[number](/docs/luau/numbers), ids:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| faceId:[number](/docs/luau/numbers)  Face ID for which to update the vertices. |
| ids:[Array](/docs/luau/tables#arrays)  List of new stable vertex IDs to use for the given face. |

Returns

()

Sets the face's vertices to new vertex IDs.

Provide feedback

---

SetFacsBonePose

Set [CFrame](/docs/reference/engine/datatypes/CFrame) for an individual bone in a specific FACS action
unit.

EditableMesh:SetFacsBonePose(

action:[Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit), boneId:[number](/docs/luau/numbers), cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)

):()

Parameters

|  |
| --- |
| action:[Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit)  FACS action unit for which to set the pose. |
| boneId:[number](/docs/luau/numbers)  Bone to set a [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  [CFrame](/docs/reference/engine/datatypes/CFrame) which transforms the bone from the initial bone [CFrame](/docs/reference/engine/datatypes/CFrame) in the bind pose of the mesh to the combined bone [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. All [CFrames](/docs/reference/engine/datatypes/CFrame) are in the mesh's local space. |

Returns

()

Set [CFrame](/docs/reference/engine/datatypes/CFrame) for an individual bone in a specific FACS action
unit.

Provide feedback

---

SetFacsCorrectivePose

Set pose for all bones in a specific FACS corrective pose.

EditableMesh:SetFacsCorrectivePose(

actions:[Array](/docs/luau/tables#arrays), boneIds:[Array](/docs/luau/tables#arrays), cframes:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| actions:[Array](/docs/luau/tables#arrays)  Array or 2 or 3 [Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit) values to apply as a corrective pose. |
| boneIds:[Array](/docs/luau/tables#arrays)  Bones to set a [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. |
| cframes:[Array](/docs/luau/tables#arrays)  [CFrame](/docs/reference/engine/datatypes/CFrame) transforms for the bones in this corrective pose.  Each bone [CFrame](/docs/reference/engine/datatypes/CFrame) transforms the bone from the initial bone [CFrame](/docs/reference/engine/datatypes/CFrame) in the bind pose of the mesh to the combined bone [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. All [CFrames](/docs/reference/engine/datatypes/CFrame) are in the mesh's local space. |

Returns

()

Set pose for all bones in a specific FACS corrective pose.

Provide feedback

---

SetFacsPose

Set pose for all bones in a specific FACS action unit.

EditableMesh:SetFacsPose(

action:[Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit), boneIds:[Array](/docs/luau/tables#arrays), cframes:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| action:[Enum.FacsActionUnit](/docs/reference/engine/enums/FacsActionUnit)  FACS action unit to set the pose for. |
| boneIds:[Array](/docs/luau/tables#arrays)  Bones for which to set a [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. |
| cframes:[Array](/docs/luau/tables#arrays)  [CFrame](/docs/reference/engine/datatypes/CFrame) transforms for the bones in this pose.  Each bone [CFrame](/docs/reference/engine/datatypes/CFrame) transforms the bone from the initial bone [CFrame](/docs/reference/engine/datatypes/CFrame) in the bind pose of the mesh to the combined bone [CFrame](/docs/reference/engine/datatypes/CFrame) for this pose. All [CFrames](/docs/reference/engine/datatypes/CFrame) are in the mesh's local space. |

Returns

()

Set pose for all bones in a specific FACS action unit.

Provide feedback

---

SetNormal

Set the normal for a normal ID.

EditableMesh:SetNormal(

normalId:[number](/docs/luau/numbers), normal:[Vector3](/docs/reference/engine/datatypes/Vector3)

):()

Parameters

|  |
| --- |
| normalId:[number](/docs/luau/numbers)  Stable normal ID for which to set the normal vector. |
| normal:[Vector3](/docs/reference/engine/datatypes/Vector3)  Normal vector to set. |

Returns

()

Set the normal for a normal ID. This will change the normal value for
every face vertex which is using the normal ID.

Provide feedback

---

SetPosition

Sets a vertex position in the mesh's local object space.

EditableMesh:SetPosition(

vertexId:[number](/docs/luau/numbers), p:[Vector3](/docs/reference/engine/datatypes/Vector3)

):()

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID of the vertex to position. |
| p:[Vector3](/docs/reference/engine/datatypes/Vector3)  Position in the mesh's local object space. |

Returns

()

Sets a vertex position in the mesh's local object space.

Provide feedback

---

SetUV

Sets UV coordinates for a UV ID.

EditableMesh:SetUV(

uvId:[number](/docs/luau/numbers), uv:[Vector2](/docs/reference/engine/datatypes/Vector2)

):()

Parameters

|  |
| --- |
| uvId:[number](/docs/luau/numbers)  UV ID for which to set the UV coordinates. |
| uv:[Vector2](/docs/reference/engine/datatypes/Vector2)  UV coordinates. |

Returns

()

Sets UV coordinates for a UV ID.

Provide feedback

---

SetVertexBones

Assign a list of bones with the vertex for skinning.

EditableMesh:SetVertexBones(

vertexId:[number](/docs/luau/numbers), boneIDs:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Vertex ID to set vertex skinning bones. |
| boneIDs:[Array](/docs/luau/tables#arrays)  Bone IDs to use with this vertex for skinning. |

Returns

()

Assign a list of bones with the vertex for skinning.

Corresponds with the skinning blend weights used in
[SetVertexBoneWeights()](/docs/reference/engine/classes/EditableMesh#SetVertexBoneWeights). In
other words,
[GetVertexBoneWeights(vertexId)[i]](/docs/reference/engine/classes/EditableMesh#GetVertexBoneWeights)
is the weight on this vertex for
[GetVertexBones(vertexId)[i]](/docs/reference/engine/classes/EditableMesh#GetVertexBones).

This method should be called before calling
[SetVertexBoneWeights()](/docs/reference/engine/classes/EditableMesh#SetVertexBoneWeights).

Provide feedback

---

SetVertexBoneWeights

Sets skinning blend weights for each bone associated with the vertex.

EditableMesh:SetVertexBoneWeights(

vertexId:[number](/docs/luau/numbers), boneWeights:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Vertex ID on which to set skinning blend weights. |
| boneWeights:[Array](/docs/luau/tables#arrays)  Skinning blend weights to set on the vertex. |

Returns

()

Sets skinning blend weights for each bone associated with the vertex.

Corresponds with the bone IDs used in
[SetVertexBones()](/docs/reference/engine/classes/EditableMesh#SetVertexBones). In other words,
[GetVertexBoneWeights(vertexId)[i]](/docs/reference/engine/classes/EditableMesh#GetVertexBoneWeights)
is the weight on this vertex for
[GetVertexBones(vertexId)[i]](/docs/reference/engine/classes/EditableMesh#GetVertexBones).

This method should be called after calling
[SetVertexBones()](/docs/reference/engine/classes/EditableMesh#SetVertexBones).

Provide feedback

---

SetVertexFaceColor

Sets the color ID of a vertex/face pair.

EditableMesh:SetVertexFaceColor(

vertexId:[number](/docs/luau/numbers), faceId:[number](/docs/luau/numbers), colorId:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID. |
| faceId:[number](/docs/luau/numbers)  Stable face ID. |
| colorId:[number](/docs/luau/numbers)  Stable color ID to set for the vertex/face pair. |

Returns

()

Sets the color ID of a vertex/face pair.

Provide feedback

---

SetVertexFaceNormal

Sets the normal ID of a vertex/face pair.

EditableMesh:SetVertexFaceNormal(

vertexId:[number](/docs/luau/numbers), faceId:[number](/docs/luau/numbers), normalId:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID. |
| faceId:[number](/docs/luau/numbers)  Stable face ID. |
| normalId:[number](/docs/luau/numbers)  Stable normal ID to set for the vertex/face pair. |

Returns

()

Sets the normal ID of a vertex/face pair.

Provide feedback

---

SetVertexFaceUV

Sets the UV ID of a vertex/face pair.

EditableMesh:SetVertexFaceUV(

vertexId:[number](/docs/luau/numbers), faceId:[number](/docs/luau/numbers), uvId:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| vertexId:[number](/docs/luau/numbers)  Stable vertex ID. |
| faceId:[number](/docs/luau/numbers)  Stable face ID. |
| uvId:[number](/docs/luau/numbers)  Stable UV ID to set for the vertex/face pair. |

Returns

()

Sets the UV ID of a vertex/face pair.

Provide feedback

---

Triangulate

Splits all faces on the mesh to be triangles.

EditableMesh:Triangulate():()

Returns

()

Splits all faces on the mesh to be triangles. Currently this does nothing
since only triangles can be created, but if your code relies on triangles,
it's recommended that you call this method after calling
[AssetService:CreateEditableMeshAsync()](/docs/reference/engine/classes/AssetService#CreateEditableMeshAsync).

Provide feedback

---