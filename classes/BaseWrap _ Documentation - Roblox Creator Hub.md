# BaseWrap | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BaseWrap
Scraped: 2026-01-11T02:29:18.239504Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- BaseWrap
- WrapDeformer
- WrapLayer
- WrapTarget
- MeshPart
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [BaseWrap](/docs/reference/engine/classes/BaseWrap)

English

Feedback

Engine Class

BaseWrap

Not Creatable

---

Summary

Properties

|  |
| --- |
| [CageMeshContent](#CageMeshContent):[Content](/docs/reference/engine/datatypes/Content) |
| [CageMeshId](#CageMeshId):ContentId |
| [CageOrigin](#CageOrigin):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [CageOriginWorld](#CageOriginWorld):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [HSRAssetId](#HSRAssetId):ContentId |
| [ImportOrigin](#ImportOrigin):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [ImportOriginWorld](#ImportOriginWorld):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[WrapDeformer](/docs/reference/engine/classes/WrapDeformer), [WrapLayer](/docs/reference/engine/classes/WrapLayer), [WrapTarget](/docs/reference/engine/classes/WrapTarget)

The base class for [WrapTarget](/docs/reference/engine/classes/WrapTarget) and [WrapLayer](/docs/reference/engine/classes/WrapLayer) objects. Note that
[MeshPart](/docs/reference/engine/classes/MeshPart) is the only valid parent type for [BaseWrap](/docs/reference/engine/classes/BaseWrap) and that
it behaves more like a component of [MeshPart](/docs/reference/engine/classes/MeshPart) than an independent
object.

---

API Reference

Properties

CageMeshContent

Plugin Security

Read Parallel

BaseWrap.CageMeshContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

CageMeshId

Plugin Security

Read Parallel

Asset ID for cage mesh.

BaseWrap.CageMeshId:ContentId

This property is set up automatically by the 3D Importer.

Asset ID for cage mesh.

Provide feedback

---

CageOrigin

Plugin Security

Read Parallel

Cage mesh offset relative to parent [MeshPart](/docs/reference/engine/classes/MeshPart).

BaseWrap.CageOrigin:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property is set up automatically by the 3D Importer.

Cage mesh offset relative to parent [MeshPart](/docs/reference/engine/classes/MeshPart).

Provide feedback

---

CageOriginWorld

Read Only

Not Replicated

Read Parallel

Cage mesh offset in world space.

BaseWrap.CageOriginWorld:[CFrame](/docs/reference/engine/datatypes/CFrame)

Cage mesh offset in world space.

Provide feedback

---

HSRAssetId

Roblox Script Security

Roblox Security

Read Parallel

BaseWrap.HSRAssetId:ContentId

Provide feedback

---

ImportOrigin

Plugin Security

Read Parallel

Describes where a global zero was while authoring the cage mesh in an
asset creation tool.

BaseWrap.ImportOrigin:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property is set up automatically by the 3D Importer.

Describes where a global zero was while authoring the cage mesh in an
asset creation tool such as Blender or Maya. This property is not used by
the deformer but it is useful for tools/aligning scripts, for example
aligning two parts by matching their pivots as follows:

```
local function alignWraps()



local selectionService = game:GetService("Selection")



local selectedObjects = selectionService:Get()



local alignObjects = {}



for _, obj in selectedObjects do



if obj:IsA("BaseWrap") then



--print("Wrap: " .. obj.Name)



table.insert(alignObjects, obj)



else



print("Ignore: " .. obj.Name)



end



end



if #alignObjects < 2 then



warn("You need to select at least two wraps")



return



end



local anchorWrap = alignObjects[1]



local worldA_from_Wrap = anchorWrap.ImportOriginWorld



print("Anchor: " .. anchorWrap.Name)



for i = 2, #alignObjects do



local wrapToAlign = alignObjects[i]



print("Align: " .. wrapToAlign.Name)



local wrap_from_WorldB = wrapToAlign.ImportOriginWorld:Inverse()



local worldA_from_WorldB = worldA_from_Wrap * wrap_from_WorldB



local worldB = wrapToAlign.Parent.CFrame



-- Note: adjust CFrame of the parent part



wrapToAlign.Parent.CFrame = (worldB_from_WorldB * worldB)



end



end
```

Provide feedback

---

ImportOriginWorld

Read Only

Not Replicated

Read Parallel

Describes where the origin (in world space) was while authoring the cage
mesh in an asset creation tool.

BaseWrap.ImportOriginWorld:[CFrame](/docs/reference/engine/datatypes/CFrame)

Describes where the origin (in world space) was while authoring the cage
mesh in an asset creation tool such as Blender or Maya.

Provide feedback

---