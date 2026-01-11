# RenderSettings | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RenderSettings
Scraped: 2026-01-11T02:36:02.272877Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- RenderSettings
- RenderSettings.EnableFRM
- MeshParts
- MeshPart.RenderFidelity
- MeshPart
- PartOperation
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [RenderSettings](/docs/reference/engine/classes/RenderSettings)

English

Feedback

Engine Class

RenderSettings

Not Creatable

Service

Not Replicated

Not Browsable

---

Summary

Properties

|  |
| --- |
| [AutoFRMLevel](#AutoFRMLevel):[number](/docs/luau/numbers) |
| [EagerBulkExecution](#EagerBulkExecution):[boolean](/docs/luau/booleans) |
| [EditQualityLevel](#EditQualityLevel):[Enum.QualityLevel](/docs/reference/engine/enums/QualityLevel) |
| [Enable VR Mode](#Enable-VR-Mode):[boolean](/docs/luau/booleans) |
| [EnableFRM](#EnableFRM):[boolean](/docs/luau/booleans) |
| [ExportMergeByMaterial](#ExportMergeByMaterial):[boolean](/docs/luau/booleans) |
| [FrameRateManager](#FrameRateManager):[Enum.FramerateManagerMode](/docs/reference/engine/enums/FramerateManagerMode) |
| [GraphicsMode](#GraphicsMode):[Enum.GraphicsMode](/docs/reference/engine/enums/GraphicsMode) |
| [MeshCacheSize](#MeshCacheSize):[number](/docs/luau/numbers) |
| [MeshPartDetailLevel](#MeshPartDetailLevel):[Enum.MeshPartDetailLevel](/docs/reference/engine/enums/MeshPartDetailLevel) |
| [QualityLevel](#QualityLevel):[Enum.QualityLevel](/docs/reference/engine/enums/QualityLevel) |
| [ReloadAssets](#ReloadAssets):[boolean](/docs/luau/booleans) |
| [RenderCSGTrianglesDebug](#RenderCSGTrianglesDebug):[boolean](/docs/luau/booleans) |
| [ShowBoundingBoxes](#ShowBoundingBoxes):[boolean](/docs/luau/booleans) |
| [ViewMode](#ViewMode):[Enum.ViewMode](/docs/reference/engine/enums/ViewMode) |

Methods

|  |
| --- |
| [GetMaxQualityLevel](#GetMaxQualityLevel)():[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The RenderSettings is a singleton class, which lets developers debug
components of Roblox's graphics engine.

It can be found under the Rendering tab in Roblox Studio's settings menu.

---

API Reference

Properties

AutoFRMLevel

Read Parallel

Sets the starting quality level of the framerate manager, when
[RenderSettings.EnableFRM](/docs/reference/engine/classes/RenderSettings#EnableFRM) is set to true.

RenderSettings.AutoFRMLevel:[number](/docs/luau/numbers)

Sets the starting quality level of the framerate manager, when
[RenderSettings.EnableFRM](/docs/reference/engine/classes/RenderSettings#EnableFRM) is set to true.

Provide feedback

---

EagerBulkExecution

Read Parallel

When set to true, all scene updates will be given an unlimited budget,
regardless of how computationally expensive it may be.

RenderSettings.EagerBulkExecution:[boolean](/docs/luau/booleans)

When set to true, all scene updates will be given an unlimited budget,
regardless of how computationally expensive it may be. This ensures each
frame will look as it should, at the cost of a more unstable frame rate.

This is used when rendering game thumbnails.

Provide feedback

---

EditQualityLevel

Read Parallel

Sets the graphics quality level in Roblox Studio, when
[RenderSettings.EnableFRM](/docs/reference/engine/classes/RenderSettings#EnableFRM) is set to false.

RenderSettings.EditQualityLevel:[Enum.QualityLevel](/docs/reference/engine/enums/QualityLevel)

Sets the graphics quality level in Roblox Studio, when
[RenderSettings.EnableFRM](/docs/reference/engine/classes/RenderSettings#EnableFRM) is set to false.

Provide feedback

---

Enable VR Mode

Read Parallel

RenderSettings.Enable VR Mode:[boolean](/docs/luau/booleans)

Provide feedback

---

EnableFRM

Hidden

Not Replicated

Read Parallel

Toggles the enabled state of the framerate manager.

RenderSettings.EnableFRM:[boolean](/docs/luau/booleans)

Toggles the enabled state of the framerate manager.

Provide feedback

---

ExportMergeByMaterial

Read Parallel

Sets whether materials should be generated per part, or per unique
appearance in Roblox's obj exporter.

RenderSettings.ExportMergeByMaterial:[boolean](/docs/luau/booleans)

Sets whether materials should be generated per part, or per unique
appearance in Roblox's obj exporter.

Provide feedback

---

FrameRateManager

Read Parallel

Specifies the behavior of the framerate manager.

RenderSettings.FrameRateManager:[Enum.FramerateManagerMode](/docs/reference/engine/enums/FramerateManagerMode)

Specifies the behavior of the framerate manager.

Provide feedback

---

GraphicsMode

Read Parallel

The graphics API that Roblox will use on startup.

RenderSettings.GraphicsMode:[Enum.GraphicsMode](/docs/reference/engine/enums/GraphicsMode)

The graphics API that Roblox will use on startup.

Provide feedback

---

MeshCacheSize

Read Parallel

The size in bytes of the mesh cache. Defaults to 32 MB.

RenderSettings.MeshCacheSize:[number](/docs/luau/numbers)

The size in bytes of the mesh cache. Defaults to 32 MB (32 \* 2^20 bytes).

Provide feedback

---

MeshPartDetailLevel

Read Parallel

Studio only. Used to visually verify the quality of
[MeshParts](/docs/reference/engine/classes/MeshPart) at lower level of detail at close range.

RenderSettings.MeshPartDetailLevel:[Enum.MeshPartDetailLevel](/docs/reference/engine/enums/MeshPartDetailLevel)

Determines the mode for the selection of detail levels for mesh parts. For
a good balance between performance and fidelity, this should be set to
[Enum.MeshPartDetailLevel.DistanceBased](/docs/reference/engine/enums/MeshPartDetailLevel#DistanceBased) (default), which is what the
client uses.

Note that the [MeshPart.RenderFidelity](/docs/reference/engine/classes/MeshPart#RenderFidelity) needs to be set to
[Enum.RenderFidelity.Automatic](/docs/reference/engine/enums/RenderFidelity#Automatic) for this to work. If you set it to
[Enum.RenderFidelity.Precise](/docs/reference/engine/enums/RenderFidelity#Precise), you will always see the higher resolution
version and the [Enum.MeshPartDetailLevel](/docs/reference/engine/enums/MeshPartDetailLevel) value will be ignored for that
[MeshPart](/docs/reference/engine/classes/MeshPart).

Provide feedback

---

QualityLevel

Read Parallel

If [RenderSettings.EnableFRM](/docs/reference/engine/classes/RenderSettings#EnableFRM) is set to true, this property controls
the quality level in Roblox Studio.

RenderSettings.QualityLevel:[Enum.QualityLevel](/docs/reference/engine/enums/QualityLevel)

If [RenderSettings.EnableFRM](/docs/reference/engine/classes/RenderSettings#EnableFRM) is set to true, this property controls
the quality level in Roblox Studio.

Provide feedback

---

ReloadAssets

Read Parallel

When set to true, Roblox Studio will automatically reload changes that are
made to files in Roblox's content folder.

RenderSettings.ReloadAssets:[boolean](/docs/luau/booleans)

When set to true, Roblox Studio will automatically reload changes that are
made to files in Roblox's content folder.

Provide feedback

---

RenderCSGTrianglesDebug

Read Parallel

When set to true, a wireframe of polygons will be shown on all
[PartOperation](/docs/reference/engine/classes/PartOperation) objects.

RenderSettings.RenderCSGTrianglesDebug:[boolean](/docs/luau/booleans)

When set to true, a wireframe of polygons will be shown on all
[PartOperation](/docs/reference/engine/classes/PartOperation) objects.

Provide feedback

---

ShowBoundingBoxes

Read Parallel

If set to true, renders bounding boxes around each individual rendered
entity in the scene.

RenderSettings.ShowBoundingBoxes:[boolean](/docs/luau/booleans)

If set to true, renders bounding boxes around each individual rendered
entity in the scene.

Provide feedback

---

ViewMode

Read Parallel

RenderSettings.ViewMode:[Enum.ViewMode](/docs/reference/engine/enums/ViewMode)

Provide feedback

---

Methods

GetMaxQualityLevel

Returns the maximum quality level.

RenderSettings:GetMaxQualityLevel():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the maximum quality level.

Provide feedback

---