# WrapLayer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/WrapLayer
Scraped: 2026-01-11T02:36:03.458155Z

## Tags
- Not Replicated

## Inherits
- BaseWrap
- WrapLayer
- Instance
- Object
- WrapTarget.DebugMode
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BaseWrap](/docs/reference/engine/classes/BaseWrap)
6. /
7. [WrapLayer](/docs/reference/engine/classes/WrapLayer)

English

Feedback

Engine Class

![WrapLayer](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/WrapLayer-Dark.webp)WrapLayer

The WrapLayer object defines a 3D accessory's inner and outer surfaces and
other properties related to layering accessories. These surfaces, or the Inner
Cage and Outer Cage, are similar to collision boxes, and describe the surfaces
of which other 3D accessories can be placed without clipping or breaking.

---

Summary

Properties

|  |
| --- |
| [AutoSkin](#AutoSkin):[Enum.WrapLayerAutoSkin](/docs/reference/engine/enums/WrapLayerAutoSkin) |
| [BindOffset](#BindOffset):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [DebugMode](#DebugMode):[Enum.WrapLayerDebugMode](/docs/reference/engine/enums/WrapLayerDebugMode) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Order](#Order):[number](/docs/luau/numbers) |
| [Puffiness](#Puffiness):[number](/docs/luau/numbers) |
| [ReferenceMeshContent](#ReferenceMeshContent):[Content](/docs/reference/engine/datatypes/Content) |
| [ReferenceMeshId](#ReferenceMeshId):ContentId |
| [ReferenceOrigin](#ReferenceOrigin):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [ReferenceOriginWorld](#ReferenceOriginWorld):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [ShrinkFactor](#ShrinkFactor):[number](/docs/luau/numbers) |

Inherited Members

7 inherited from [BaseWrap](/docs/reference/engine/classes/BaseWrap)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The WrapLayer object defines a 3D accessory's inner and outer surfaces and
other properties related to layering accessories. These surfaces, or the Inner
Cage and Outer Cage, are similar to collision boxes, and describe the surfaces
of which other 3D accessories can be placed without clipping or breaking.

Internally, WrapLayer also uses the UV layout of the Inner and Outer cages to
match coordinates to another 3D object's cage. This powers the deformation of
objects around differently shaped avatars and underlying accessories.

---

API Reference

Properties

AutoSkin

Read Parallel

WrapLayer.AutoSkin:[Enum.WrapLayerAutoSkin](/docs/reference/engine/enums/WrapLayerAutoSkin)

Provide feedback

---

BindOffset

Plugin Security

Read Parallel

[CFrame](/docs/reference/engine/datatypes/CFrame) is used to adjust a binding point for clothing item
mesh. Could be used to move and rotate clothing items. This property is
intended for fine-tuning only and it is heavily optional.

WrapLayer.BindOffset:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property is intended for fine-tuning purposes and is highly optional.

[CFrame](/docs/reference/engine/datatypes/CFrame) to adjust a binding point for a clothing item mesh.
Allows for fine-tuning of clothing items (slight adjustment of
position/rotation to get a unique look) in contexts such as community-made
avatar editors.

Provide feedback

---

Color

Not Replicated

Not Scriptable

Read Parallel

Sets color used for the debug rendering. See [WrapTarget.DebugMode](/docs/reference/engine/classes/WrapTarget#DebugMode).

WrapLayer.Color:[Color3](/docs/reference/engine/datatypes/Color3)

Sets color used for the debug rendering. See [WrapTarget.DebugMode](/docs/reference/engine/classes/WrapTarget#DebugMode)

Provide feedback

---

DebugMode

Not Replicated

Not Scriptable

Read Parallel

Allows switching between different debugging visualization modes for cage
meshes.

WrapLayer.DebugMode:[Enum.WrapLayerDebugMode](/docs/reference/engine/enums/WrapLayerDebugMode)

Allows switching between different debugging visualization modes for cage
meshes.

Provide feedback

---

Enabled

Read Parallel

Allows for disabling of the [WrapLayer](/docs/reference/engine/classes/WrapLayer) object as if it does not
exist.

WrapLayer.Enabled:[boolean](/docs/luau/booleans)

Allows for disabling of the [WrapLayer](/docs/reference/engine/classes/WrapLayer) object as if it does not
exist.

Provide feedback

---

Order

Read Parallel

Controls the composition order for layered clothing.

WrapLayer.Order:[number](/docs/luau/numbers)

Controls the composition order for layered clothing. Clothing items with
higher order will appear on top of clothing items with lower order. If two
items have the same order, the deformer composition order is ambiguous and
depends on serialization order. Default value is 1.

Provide feedback

---

Puffiness

Read Parallel

Controls how much underlying clothing items inflate the current clothing
item.

WrapLayer.Puffiness:[number](/docs/luau/numbers)

Controls how much underlying clothing items inflate the current clothing
item.

Valid range is -1 to 1. A value of -1 compresses the clothing, body, and
all underlying layers such that the clothing itself takes the shape of the
body. A value of 0 makes the clothing item fit as if it was the only piece
of clothing being worn, compressing all underlying layers. A value of 1
(default) never compresses anything and infinitely inflates over
underlying clothing items.

Provide feedback

---

ReferenceMeshContent

Plugin Security

Read Parallel

WrapLayer.ReferenceMeshContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

ReferenceMeshId

Plugin Security

Read Parallel

AssetID for reference mesh used to define Inner Cage of a 3D object.

WrapLayer.ReferenceMeshId:ContentId

AssetID for reference mesh used to define Inner Cage of a 3D object

Reference mesh is used to define standard topology and UV coordinates for
index matching. It is expected that for all catalog avatars, this will
point to one of 15 standard reference meshes provided by Roblox. But for
some NPCs or a custom avatar system, this might point to other meshes.

Note: this property is set up automatically by the FBX importer

Provide feedback

---

ReferenceOrigin

Plugin Security

Read Parallel

Reference mesh offset relative to parent MeshPart (in the parent MeshPart
space)

Note: this property is set up automatically by the FBX importer.

WrapLayer.ReferenceOrigin:[CFrame](/docs/reference/engine/datatypes/CFrame)

Reference mesh offset relative to parent MeshPart (in the parent MeshPart
space)

Note: this property is set up automatically by the FBX importer

Provide feedback

---

ReferenceOriginWorld

Read Only

Not Replicated

Read Parallel

Reference mesh offset relative to parent MeshPart (in the world space)

Note: this property is set up automatically by the FBX importer.

WrapLayer.ReferenceOriginWorld:[CFrame](/docs/reference/engine/datatypes/CFrame)

Reference mesh offset relative to parent MeshPart (in the world space)

Note: this property is set up automatically by the FBX importer

Provide feedback

---

ShrinkFactor

Plugin Security

Read Parallel

Allows slight shrinking/expanding of the resulting render mesh, without
affecting any other layers.

WrapLayer.ShrinkFactor:[number](/docs/luau/numbers)

This property is intended for fine-tuning purposes and is highly optional.

Allows slight shrinking/expanding of the resulting render mesh, without
affecting any other layers. This is useful in rare cases when the clothing
mesh does not precisely fit the underlying clothing layers (the cage is
usually slightly overestimated atop the real shape to avoid layer
interpenetration). Even slight overestimation has the tendency to
accumulate, especially when there are a lot of layers. While this is
usually not critical, some items like backpacks may be problematic.

Valid range is -1 to 1. A value of -1 will maximally expand while a value
of 1 will maximally shrink. A value of 0 (default) has no effect.

Provide feedback

---