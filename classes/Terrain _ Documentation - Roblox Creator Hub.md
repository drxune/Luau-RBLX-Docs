# Terrain | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Terrain
Scraped: 2026-01-11T02:44:06.202820Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- BasePart
- Terrain
- TerrainRegion
- TerrainIterateOperation
- TerrainModifyOperation
- TerrainReadOperation
- TerrainWriteOperation
- PVInstance
- Instance
- Object
- Decoration
- Terrain:GetMaterialColor()
- Terrain:SetMaterialColor()
- Terrain:FillBall()
- WedgePart
- Terrain:FillRegion()
- Terrain:CopyRegion()
- Terrain:PasteRegion()
- Terrain:ReplaceMaterial()
- ReadVoxelChannels()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BasePart](/docs/reference/engine/classes/BasePart)
6. /
7. [Terrain](/docs/reference/engine/classes/Terrain)

English

Feedback

Engine Class

![Terrain](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Terrain-Dark.webp)Terrain

Terrain lets you to create dynamically morphable environments.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Decoration](#Decoration):[boolean](/docs/luau/booleans) |
| [GrassLength](#GrassLength):[number](/docs/luau/numbers) |
| [IsSmooth](#IsSmooth):[boolean](/docs/luau/booleans)  Deprecated |
| [MaterialColors](#MaterialColors):BinaryString |
| [MaxExtents](#MaxExtents):[Region3int16](/docs/reference/engine/datatypes/Region3int16) |
| [WaterColor](#WaterColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [WaterReflectance](#WaterReflectance):[number](/docs/luau/numbers) |
| [WaterTransparency](#WaterTransparency):[number](/docs/luau/numbers) |
| [WaterWaveSize](#WaterWaveSize):[number](/docs/luau/numbers) |
| [WaterWaveSpeed](#WaterWaveSpeed):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [AutowedgeCell](#AutowedgeCell)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [AutowedgeCells](#AutowedgeCells)(region: [Region3int16](/docs/reference/engine/datatypes/Region3int16)):()  Deprecated |
| [CellCenterToWorld](#CellCenterToWorld)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [CellCornerToWorld](#CellCornerToWorld)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Clear](#Clear)():() |
| [ClearVoxelsAsync\_beta](#ClearVoxelsAsync_beta)(region: [Region3](/docs/reference/engine/datatypes/Region3),channelIds: [Array](/docs/luau/tables#arrays)):() |
| [ConvertToSmooth](#ConvertToSmooth)():()  Deprecated |
| [CopyRegion](#CopyRegion)(region: [Region3int16](/docs/reference/engine/datatypes/Region3int16)):[TerrainRegion](/docs/reference/engine/classes/TerrainRegion) |
| [CountCells](#CountCells)():[number](/docs/luau/numbers) |
| [FillBall](#FillBall)(center: [Vector3](/docs/reference/engine/datatypes/Vector3),radius: [number](/docs/luau/numbers),material: [Enum.Material](/docs/reference/engine/enums/Material)):() |
| [FillBlock](#FillBlock)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),size: [Vector3](/docs/reference/engine/datatypes/Vector3),material: [Enum.Material](/docs/reference/engine/enums/Material)):() |
| [FillCylinder](#FillCylinder)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),height: [number](/docs/luau/numbers),radius: [number](/docs/luau/numbers),material: [Enum.Material](/docs/reference/engine/enums/Material)):() |
| [FillRegion](#FillRegion)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),material: [Enum.Material](/docs/reference/engine/enums/Material)):() |
| [FillWedge](#FillWedge)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame),size: [Vector3](/docs/reference/engine/datatypes/Vector3),material: [Enum.Material](/docs/reference/engine/enums/Material)):() |
| [GetCell](#GetCell)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples)  Deprecated |
| [GetMaterialColor](#GetMaterialColor)(material: [Enum.Material](/docs/reference/engine/enums/Material)):[Color3](/docs/reference/engine/datatypes/Color3) |
| [GetWaterCell](#GetWaterCell)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples)  Deprecated |
| [IterateVoxelsAsync\_beta](#IterateVoxelsAsync_beta)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),channelIds: [Array](/docs/luau/tables#arrays)):[TerrainIterateOperation](/docs/reference/engine/classes/TerrainIterateOperation) |
| [ModifyVoxelsAsync\_beta](#ModifyVoxelsAsync_beta)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),channelIds: [Array](/docs/luau/tables#arrays)):[TerrainModifyOperation](/docs/reference/engine/classes/TerrainModifyOperation) |
| [PasteRegion](#PasteRegion)(region: [TerrainRegion](/docs/reference/engine/classes/TerrainRegion),corner: [Vector3int16](/docs/reference/engine/datatypes/Vector3int16),pasteEmptyCells: [boolean](/docs/luau/booleans)):() |
| [ReadVoxelChannels](#ReadVoxelChannels)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),channelIds: [Array](/docs/luau/tables#arrays)):[Dictionary](/docs/luau/tables#dictionaries) |
| [ReadVoxels](#ReadVoxels)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |
| [ReadVoxelsAsync\_beta](#ReadVoxelsAsync_beta)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),channelIds: [Array](/docs/luau/tables#arrays)):[TerrainReadOperation](/docs/reference/engine/classes/TerrainReadOperation) |
| [ReplaceMaterial](#ReplaceMaterial)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),sourceMaterial: [Enum.Material](/docs/reference/engine/enums/Material),targetMaterial: [Enum.Material](/docs/reference/engine/enums/Material)):() |
| [SetCell](#SetCell)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers),material: [Enum.CellMaterial](/docs/reference/engine/enums/CellMaterial),block: [Enum.CellBlock](/docs/reference/engine/enums/CellBlock),orientation: [Enum.CellOrientation](/docs/reference/engine/enums/CellOrientation)):()  Deprecated |
| [SetCells](#SetCells)(region: [Region3int16](/docs/reference/engine/datatypes/Region3int16),material: [Enum.CellMaterial](/docs/reference/engine/enums/CellMaterial),block: [Enum.CellBlock](/docs/reference/engine/enums/CellBlock),orientation: [Enum.CellOrientation](/docs/reference/engine/enums/CellOrientation)):()  Deprecated |
| [SetMaterialColor](#SetMaterialColor)(material: [Enum.Material](/docs/reference/engine/enums/Material),value: [Color3](/docs/reference/engine/datatypes/Color3)):() |
| [SetWaterCell](#SetWaterCell)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers),force: [Enum.WaterForce](/docs/reference/engine/enums/WaterForce),direction: [Enum.WaterDirection](/docs/reference/engine/enums/WaterDirection)):()  Deprecated |
| [WorldToCell](#WorldToCell)(position: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [WorldToCellPreferEmpty](#WorldToCellPreferEmpty)(position: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [WorldToCellPreferSolid](#WorldToCellPreferSolid)(position: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [WriteVoxelChannels](#WriteVoxelChannels)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),channels: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [WriteVoxels](#WriteVoxels)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),materials: [Array](/docs/luau/tables#arrays),occupancy: [Array](/docs/luau/tables#arrays)):() |
| [WriteVoxelsAsync\_beta](#WriteVoxelsAsync_beta)(region: [Region3](/docs/reference/engine/datatypes/Region3),resolution: [number](/docs/luau/numbers),channelIds: [Array](/docs/luau/tables#arrays)):[TerrainWriteOperation](/docs/reference/engine/classes/TerrainWriteOperation) |

Inherited Members

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Terrain lets you create dynamically morphable environments with little to no
lag. It is currently based on a 4×4×4 grid of cells, where each
cell has a number between 0 and 1 representing how much the geometry should
occupy the cell, and the material of the cell. The occupancy determines how
the cell will morph together with surrounding cells, and the result is the
illusion of having no grid constraint.

For more information, see [Terrain](/docs/parts/terrain).

---

API Reference

Properties

Decoration

Not Scriptable

Read Parallel

Enables or disables terrain decoration.

Terrain.Decoration:[boolean](/docs/luau/booleans)

Currently enables or disables animated grass on the Grass terrain
material, although future modifications of this property may control
additional decorative features.

Provide feedback

---

GrassLength

Not Scriptable

Read Parallel

Specifies the length of animated grass.

Terrain.GrassLength:[number](/docs/luau/numbers)

Specifies the length of animated grass on the Grass terrain material,
assuming [Decoration](/docs/reference/engine/classes/Terrain#Decoration) is enabled. Valid values
are between 0.1 and 1.

Provide feedback

---

IsSmooth

Deprecated

Show details

---

MaterialColors

Not Scriptable

Read Parallel

MaterialColors represents the editor for the Material Color feature, and
cannot be edited by scripts.

To get the color of a material, use: [Terrain:GetMaterialColor()](/docs/reference/engine/classes/Terrain#GetMaterialColor) To
set the color of a material, use: [Terrain:SetMaterialColor()](/docs/reference/engine/classes/Terrain#SetMaterialColor)

Terrain.MaterialColors:BinaryString

MaterialColors represents the editor for the Material Color feature, and
cannot be edited by scripts.

To get the color of a material, use: [Terrain:GetMaterialColor()](/docs/reference/engine/classes/Terrain#GetMaterialColor)

To set the color of a material, use: [Terrain:SetMaterialColor()](/docs/reference/engine/classes/Terrain#SetMaterialColor)

Provide feedback

---

MaxExtents

Read Only

Not Replicated

Read Parallel

Displays the boundaries of the largest possible editable region.

Terrain.MaxExtents:[Region3int16](/docs/reference/engine/datatypes/Region3int16)

Displays the boundaries of the largest possible editable region.

Provide feedback

---

WaterColor

Read Parallel

The tint of the Terrain water.

Terrain.WaterColor:[Color3](/docs/reference/engine/datatypes/Color3)

The tint of the Terrain water.

Provide feedback

---

WaterReflectance

Read Parallel

Controls how opaque the Terrain's water reflections are.

Terrain.WaterReflectance:[number](/docs/luau/numbers)

Controls how opaque the Terrain's water reflections are.

Provide feedback

---

WaterTransparency

Read Parallel

The transparency of the Terrain water.

Terrain.WaterTransparency:[number](/docs/luau/numbers)

The transparency of the Terrain water.

Provide feedback

---

WaterWaveSize

Read Parallel

Sets the maximum height of the Terrain water waves in studs.

Terrain.WaterWaveSize:[number](/docs/luau/numbers)

Sets the maximum height of the Terrain water waves in studs. This is
currently constrained to between 0 and 1.

Provide feedback

---

WaterWaveSpeed

Read Parallel

Sets how many times the Terrain water waves will move up and down per
minute.

Terrain.WaterWaveSpeed:[number](/docs/luau/numbers)

Sets how many times the Terrain water waves will move up and down per
minute. This is currently constrained to between 0 and 100.

Provide feedback

---

Methods

AutowedgeCell

Deprecated

Show details

---

AutowedgeCells

Deprecated

Show details

---

CellCenterToWorld

Returns the world position of the center of the terrain cell (x, y, z).

Terrain:CellCenterToWorld(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers)

):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |
| z:[number](/docs/luau/numbers) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the world position of the center of the terrain cell (x, y, z).

Provide feedback

---

CellCornerToWorld

Returns the position of the lower-left-forward corner of the grid cell (x,
y, z).

Terrain:CellCornerToWorld(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers)

):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |
| z:[number](/docs/luau/numbers) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the position of the lower-left-forward corner of the grid cell (x,
y, z).

Provide feedback

---

Clear

Clears the terrain.

Terrain:Clear():()

Returns

()

Clears the terrain.

Provide feedback

---

ClearVoxelsAsync\_beta

Terrain:ClearVoxelsAsync\_beta(

region:[Region3](/docs/reference/engine/datatypes/Region3), channelIds:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3) |
| channelIds:[Array](/docs/luau/tables#arrays) |

Returns

()

Provide feedback

---

ConvertToSmooth

Deprecated

Show details

---

CopyRegion

Stores a chunk of terrain into a [TerrainRegion](/docs/reference/engine/classes/TerrainRegion) object so it can be
loaded back later. Note: [TerrainRegion](/docs/reference/engine/classes/TerrainRegion) data does not replicate
between server and client.

Terrain:CopyRegion(region:[Region3int16](/docs/reference/engine/datatypes/Region3int16)):[TerrainRegion](/docs/reference/engine/classes/TerrainRegion)

Parameters

|  |
| --- |
| region:[Region3int16](/docs/reference/engine/datatypes/Region3int16) |

Returns

[TerrainRegion](/docs/reference/engine/classes/TerrainRegion)

Stores a chunk of terrain into a [TerrainRegion](/docs/reference/engine/classes/TerrainRegion) object so it can be
loaded back later. Note: [TerrainRegion](/docs/reference/engine/classes/TerrainRegion) data does not replicate
between server and client.

Code Samples

Terrain:CopyRegion

The following code will copy the whole Terrain and clear it. After 5 seconds
it will paste the terrain back.

```
local terrainRegion = workspace.Terrain:CopyRegion(workspace.Terrain.MaxExtents)



workspace.Terrain:Clear()



task.wait(5)



workspace.Terrain:PasteRegion(terrainRegion, workspace.Terrain.MaxExtents.Min, true)
```

Provide feedback

---

CountCells

Returns the number of non-empty cells in the Terrain.

Terrain:CountCells():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the number of non-empty cells in the Terrain.

Provide feedback

---

FillBall

Fills a ball of smooth terrain in a given space.

Terrain:FillBall(

center:[Vector3](/docs/reference/engine/datatypes/Vector3), radius:[number](/docs/luau/numbers), material:[Enum.Material](/docs/reference/engine/enums/Material)

):()

Parameters

|  |
| --- |
| center:[Vector3](/docs/reference/engine/datatypes/Vector3)  The position of the center of the terrain ball. |
| radius:[number](/docs/luau/numbers)  The radius in studs of the terrain ball. |
| material:[Enum.Material](/docs/reference/engine/enums/Material)  The [Enum.Material](/docs/reference/engine/enums/Material) of the terrain ball. |

Returns

()

Fills a ball of smooth terrain in a given space.

Code Samples

Filling a Ball of Terrain

[Terrain:FillBall()](/docs/reference/engine/classes/Terrain#FillBall) creates a ball of terrain given a center position, ball radius, and terrain materials.

```
local Workspace = game:GetService("Workspace")



-- Creates a ball of grass at (0,0,-10) with a radius of 10 studs



Workspace.Terrain:FillBall(Vector3.new(0, 0, -10), 10, Enum.Material.Grass)
```

Provide feedback

---

FillBlock

Fills a block of smooth terrain with a given location, rotation, size, and
material.

Terrain:FillBlock(

cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), size:[Vector3](/docs/reference/engine/datatypes/Vector3), material:[Enum.Material](/docs/reference/engine/enums/Material)

):()

Parameters

|  |
| --- |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  The position and orientation of the terrain block. |
| size:[Vector3](/docs/reference/engine/datatypes/Vector3)  The size in studs of the square block - both the height and width. |
| material:[Enum.Material](/docs/reference/engine/enums/Material)  The [Enum.Material](/docs/reference/engine/enums/Material) of the terrain block. |

Returns

()

Fills a block of smooth terrain with a given location, rotation, size, and
material.

Provide feedback

---

FillCylinder

Fills a cylinder of smooth terrain in a given space.

Terrain:FillCylinder(

cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), height:[number](/docs/luau/numbers), radius:[number](/docs/luau/numbers), material:[Enum.Material](/docs/reference/engine/enums/Material)

):()

Parameters

|  |
| --- |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  The position and orientation of the terrain cylinder. |
| height:[number](/docs/luau/numbers)  The height in studs of the terrain cylinder. |
| radius:[number](/docs/luau/numbers)  The radius in studs of the terrain cylinder. |
| material:[Enum.Material](/docs/reference/engine/enums/Material)  The [Enum.Material](/docs/reference/engine/enums/Material) of the terrain cylinder. |

Returns

()

Fills a cylinder of smooth terrain in a given space. The space is defined
using a CFrame, height, and radius.

```
local Workspace = game:GetService("Workspace")



Workspace.Terrain:FillCylinder(CFrame.new(0, 50, 0), 5, 30, Enum.Material.Asphalt)
```

Provide feedback

---

FillRegion

Fills a [Region3](/docs/reference/engine/datatypes/Region3) space with smooth terrain.

Terrain:FillRegion(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), material:[Enum.Material](/docs/reference/engine/enums/Material)

):()

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3) |
| resolution:[number](/docs/luau/numbers) |
| material:[Enum.Material](/docs/reference/engine/enums/Material) |

Returns

()

Fills a [Region3](/docs/reference/engine/datatypes/Region3) space with smooth terrain.

Provide feedback

---

FillWedge

Fills a wedge-shaped volume of Terrain with the given [Enum.Material](/docs/reference/engine/enums/Material) and
the area's CFrame and Size.

Terrain:FillWedge(

cframe:[CFrame](/docs/reference/engine/datatypes/CFrame), size:[Vector3](/docs/reference/engine/datatypes/Vector3), material:[Enum.Material](/docs/reference/engine/enums/Material)

):()

Parameters

|  |
| --- |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  The position and orientation of the wedge to fill. |
| size:[Vector3](/docs/reference/engine/datatypes/Vector3)  The size of the wedge to fill. |
| material:[Enum.Material](/docs/reference/engine/enums/Material)  The material with which the wedge will be filled. |

Returns

()

FillWedge() fills a wedge-shaped volume of [Terrain](/docs/reference/engine/classes/Terrain) with the
given [Enum.Material](/docs/reference/engine/enums/Material) and the area's [CFrame](/docs/reference/engine/datatypes/CFrame) and size. The
orientation of the wedge is the same as an equivalent [WedgePart](/docs/reference/engine/classes/WedgePart).

Provide feedback

---

GetCell

Deprecated

Show details

---

GetMaterialColor

Write Parallel

Returns current terrain material color for specified terrain material.

Terrain:GetMaterialColor(material:[Enum.Material](/docs/reference/engine/enums/Material)):[Color3](/docs/reference/engine/datatypes/Color3)

Parameters

|  |
| --- |
| material:[Enum.Material](/docs/reference/engine/enums/Material) |

Returns

[Color3](/docs/reference/engine/datatypes/Color3)

Returns the current terrain material color for the specified terrain
material.

Provide feedback

---

GetWaterCell

Deprecated

Show details

---

IterateVoxelsAsync\_beta

Terrain:IterateVoxelsAsync\_beta(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), channelIds:[Array](/docs/luau/tables#arrays)

):[TerrainIterateOperation](/docs/reference/engine/classes/TerrainIterateOperation)

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3) |
| resolution:[number](/docs/luau/numbers) |
| channelIds:[Array](/docs/luau/tables#arrays) |

Returns

[TerrainIterateOperation](/docs/reference/engine/classes/TerrainIterateOperation)

Provide feedback

---

ModifyVoxelsAsync\_beta

Terrain:ModifyVoxelsAsync\_beta(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), channelIds:[Array](/docs/luau/tables#arrays)

):[TerrainModifyOperation](/docs/reference/engine/classes/TerrainModifyOperation)

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3) |
| resolution:[number](/docs/luau/numbers) |
| channelIds:[Array](/docs/luau/tables#arrays) |

Returns

[TerrainModifyOperation](/docs/reference/engine/classes/TerrainModifyOperation)

Provide feedback

---

PasteRegion

Applies a chunk of terrain to the Terrain object. Note:
[TerrainRegion](/docs/reference/engine/classes/TerrainRegion) data does not replicate between server and client.

Terrain:PasteRegion(

region:[TerrainRegion](/docs/reference/engine/classes/TerrainRegion), corner:[Vector3int16](/docs/reference/engine/datatypes/Vector3int16), pasteEmptyCells:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| region:[TerrainRegion](/docs/reference/engine/classes/TerrainRegion) |
| corner:[Vector3int16](/docs/reference/engine/datatypes/Vector3int16) |
| pasteEmptyCells:[boolean](/docs/luau/booleans) |

Returns

()

Applies a chunk of terrain to the Terrain object. Note:
[TerrainRegion](/docs/reference/engine/classes/TerrainRegion) data does not replicate between server and client.

Code Samples

Create, Copy and Paste Terrain

Creates some terrain, copies it, then pastes it using the following API:

* [Terrain:FillRegion()](/docs/reference/engine/classes/Terrain#FillRegion)
* [Terrain:CopyRegion()](/docs/reference/engine/classes/Terrain#CopyRegion)
* [Terrain:PasteRegion()](/docs/reference/engine/classes/Terrain#PasteRegion)

```
--[[



Note: The use of int16 variants for these API is the result of legacy code.



The underlying voxel grid system uses Vector3int32 (Vector3).



]]



local Workspace = game:GetService("Workspace")



local Terrain = Workspace.Terrain



-- Create a simple terrain region (a 10x10x10 block of grass)



local initialRegion = Region3.new(Vector3.zero, Vector3.one * 10)



Terrain:FillRegion(initialRegion, 4, Enum.Material.Grass)



-- Copy the region using Terrain:CopyRegion



local copyRegion = Region3int16.new(Vector3int16.new(0, 0, 0), Vector3int16.new(10, 10, 10))



local copiedRegion = Terrain:CopyRegion(copyRegion)



-- Define where to paste the region (in this example, offsetting by 5 studs on the X-axis)



local newRegionCorner = Vector3int16.new(5, 0, 0)



-- Paste the region using Terrain:PasteRegion



Terrain:PasteRegion(copiedRegion, newRegionCorner, true)
```

Provide feedback

---

ReadVoxelChannels

Write Parallel

Returns a region of terrain voxel data in table format based on the
channel names.

Terrain:ReadVoxelChannels(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), channelIds:[Array](/docs/luau/tables#arrays)

):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3)  Target region to read from. Must be aligned to the voxel grid. Will throw an error if region is too large; limit is currently 4194304 voxels³. |
| resolution:[number](/docs/luau/numbers)  Voxel resolution. Must be 4. |
| channelIds:[Array](/docs/luau/tables#arrays)  Array of channel IDs (strings) that need to be accessed from the voxel data. Each channel ID represents a type of data that's stored in voxel. Current supported IDs are {"SolidMaterial", "SolidOccupancy", "LiquidOccupancy"}. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Returns voxel data as a dictionary based on the channelIds input.
Keys represent each channel ID with their respective value as an array
of 3D data.

* SolidMaterial — The [Enum.Material](/docs/reference/engine/enums/Material) material of the voxel. Note
  that [Water](/docs/reference/engine/enums/Material) is not supported anymore; instead, a
  voxel that contains water will have a value of LiquidOccupancy.
* SolidOccupancy — The occupancy of the voxel's material as
  specified in the SolidMaterial channel. This is a value between 0
  (empty) and 1 (full).
* LiquidOccupancy — Specifies the occupancy of the
  [Water](/docs/reference/engine/enums/Material) material in a voxel as a value between 0 (no
  water) and 1 (full of water). If the SolidOccupancy is 1 and the
  SolidMaterial is not [Air](/docs/reference/engine/enums/Material), this will be 0.

The dictionary also contains a Size key with a value representing
the 3D array size of each channel data.

Returns a region of terrain voxel data in table format based on the
channel names.

Code Samples

Terrain:ReadVoxelChannels()

```
local REGION_START = Vector3.new(-20, -20, -20)



local REGION_END = Vector3.new(20, 20, 20)



local function printRegion(terrain, region)



local channelOutput = terrain:ReadVoxelChannels(region, 4, { "SolidOccupancy", "SolidMaterial", "LiquidOccupancy" })



local size = channelOutput.Size



for x = 1, size.X do



for y = 1, size.Y do



for z = 1, size.Z do



print(



("(%2i, %2i, %2i): %.2f %s %.2f"):format(



x,



y,



z,



channelOutput.SolidOccupancy[x][y][z],



channelOutput.SolidMaterial[x][y][z].Name,



channelOutput.LiquidOccupancy[x][y][z]



)



)



end



end



end



end



local region = Region3.new(REGION_START, REGION_END)



printRegion(workspace.Terrain, region)
```

Provide feedback

---

ReadVoxels

Write Parallel

Returns a certain region of smooth terrain in table format.

Terrain:ReadVoxels(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3)  Target region to read from. Must be aligned to the voxel grid. Will throw an error if region is too large. The limit is currently 4194304 voxels^3. |
| resolution:[number](/docs/luau/numbers)  Voxel resolution. Must be 4. |

Returns

[Tuple](/docs/luau/tuples)

Returns raw voxel data as two 3D arrays.

* materials - 3D array of [Enum.Material](/docs/reference/engine/enums/Material) from the target area. Also
  contains a Size field, equal to the dimensions of the nested arrays.
* occupancies - 3D array of occupancy values from the target area.
  Also contains a Size field, equal to the dimensions of the nested
  arrays.

Returns a certain region of smooth terrain in table format.

Code Samples

Terrain:ReadVoxels() Code Example

```
local REGION_START = Vector3.new(-20, -20, -20)



local REGION_END = Vector3.new(20, 20, 20)



local function printRegion(terrain, region)



local materials, occupancies = terrain:ReadVoxels(region, 4)



local size = materials.Size -- Same as occupancies.Size



for x = 1, size.X, 1 do



for y = 1, size.Y, 1 do



for z = 1, size.Z, 1 do



print(("(%2i, %2i, %2i): %.2f %s"):format(x, y, z, occupancies[x][y][z], materials[x][y][z].Name))



end



end



end



end



local region = Region3.new(REGION_START, REGION_END)



printRegion(workspace.Terrain, region)
```

Provide feedback

---

ReadVoxelsAsync\_beta

Terrain:ReadVoxelsAsync\_beta(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), channelIds:[Array](/docs/luau/tables#arrays)

):[TerrainReadOperation](/docs/reference/engine/classes/TerrainReadOperation)

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3) |
| resolution:[number](/docs/luau/numbers) |
| channelIds:[Array](/docs/luau/tables#arrays) |

Returns

[TerrainReadOperation](/docs/reference/engine/classes/TerrainReadOperation)

Provide feedback

---

ReplaceMaterial

Replaces the terrain of a material within a region with another material.

Terrain:ReplaceMaterial(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), sourceMaterial:[Enum.Material](/docs/reference/engine/enums/Material), targetMaterial:[Enum.Material](/docs/reference/engine/enums/Material)

):()

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3)  The region in which the replacement operation will occur. |
| resolution:[number](/docs/luau/numbers)  The resolution at which the replacement operation will take place; at the moment this must be exactly 4. |
| sourceMaterial:[Enum.Material](/docs/reference/engine/enums/Material)  The old material that shall be replaced. |
| targetMaterial:[Enum.Material](/docs/reference/engine/enums/Material)  The new material. |

Returns

()

ReplaceMaterial replaces terrain of a certain [Enum.Material](/docs/reference/engine/enums/Material) within a
[Region3](/docs/reference/engine/datatypes/Region3) with another material. Essentially, it is a
find-and-replace operation on [Terrain](/docs/reference/engine/classes/Terrain) materials.

#### Constraints

When calling this method, the resolution parameter must be exactly 4.
Additionally, the Region3 must be aligned to the terrain materials grid,
i.e. the components of the Region3's minimum and maximum points must be
divisible by 4. Use [Region3:ExpandToGrid()](/docs/reference/engine/datatypes/Region3#ExpandToGrid) to make a region
compatible with this function.

Code Samples

Terrain:ReplaceMaterial

This code sample demonstrates the usage of [Terrain:ReplaceMaterial()](/docs/reference/engine/classes/Terrain#ReplaceMaterial)
by replacing grass near the game origin with asphalt. It does this by
constructing a [Region3](/docs/reference/engine/datatypes/Region3) using two [Vector3](/docs/reference/engine/datatypes/Vector3)s.

```
local Workspace = game:GetService("Workspace")



local terrain = Workspace.Terrain



local region = Region3.new(Vector3.new(-20, -20, -20), Vector3.new(20, 20, 20))



local resolution = 4



local materialToReplace = Enum.Material.Grass



local replacementMaterial = Enum.Material.Asphalt



terrain:ReplaceMaterial(region, resolution, materialToReplace, replacementMaterial)
```

Provide feedback

---

SetCell

Deprecated

Show details

---

SetCells

Deprecated

Show details

---

SetMaterialColor

Sets current terrain material color for specified terrain material.

Terrain:SetMaterialColor(

material:[Enum.Material](/docs/reference/engine/enums/Material), value:[Color3](/docs/reference/engine/datatypes/Color3)

):()

Parameters

|  |
| --- |
| material:[Enum.Material](/docs/reference/engine/enums/Material) |
| value:[Color3](/docs/reference/engine/datatypes/Color3) |

Returns

()

Sets current terrain material color for specified terrain material.
Terrain material will shift its base color toward specified color.

Provide feedback

---

SetWaterCell

Deprecated

Show details

---

WorldToCell

Returns the grid cell location that contains the point position.

Terrain:WorldToCell(position:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the grid cell location that contains the point position.

Provide feedback

---

WorldToCellPreferEmpty

Returns the grid cell location that contains the point position,
preferring empty grid cells when position is on a grid edge.

Terrain:WorldToCellPreferEmpty(position:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the grid cell location that contains the point position,
preferring empty grid cells when position is on a grid edge.

Provide feedback

---

WorldToCellPreferSolid

Returns the grid cell location that contains the point position,
preferring non-empty grid cells when position is on a grid edge.

Terrain:WorldToCellPreferSolid(position:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the grid cell location that contains the point position,
preferring non-empty grid cells when position is on a grid edge.

Provide feedback

---

WriteVoxelChannels

Sets a region of terrain using a dictionary of voxel channel data.

Terrain:WriteVoxelChannels(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), channels:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3)  Target region to write to. Must be aligned to the voxel grid. Will throw an error if region is too large; limit is currently 4194304 voxels³. |
| resolution:[number](/docs/luau/numbers)  Voxel resolution. Must be 4. |
| channels:[Dictionary](/docs/luau/tables#dictionaries)  Dictionary of voxel data similar to the return value of [ReadVoxelChannels()](/docs/reference/engine/classes/Terrain#ReadVoxelChannels). Keys represent each channel ID with their respective value as an array of 3D data. The dictionary can support single or multiple channel inputs.   * SolidMaterial — The [Enum.Material](/docs/reference/engine/enums/Material) material of the voxel. Note   that [Water](/docs/reference/engine/enums/Material) is not supported anymore; instead, a   voxel that contains only water should be entered as   SolidMaterial = Enum.Material.Air, LiquidOccupancy = x, where x   is a number between 0 (exclusive) and 1 (inclusive). * SolidOccupancy — The occupancy of the voxel's material as   specified in the SolidMaterial channel. This should be a value   between 0 (empty) and 1 (full). * LiquidOccupancy — Specifies the occupancy of the   [Water](/docs/reference/engine/enums/Material) material in a voxel as a value between 0 (no   water) and 1 (full of water). If the SolidOccupancy is 1 and the   SolidMaterial is not [Air](/docs/reference/engine/enums/Material), this will be 0. |

Returns

()

Sets a region of terrain using a dictionary of voxel channel data.

Code Samples

Terrain:WriteVoxelChannels()

```
local region = Region3.new(Vector3.new(0, 0, 0), Vector3.new(64, 32, 64))



local RESOLUTION = 4



local OCC_EPSILON = 1 / 256



local function generateRandomTerrainInRegion(regionInput)



local region = regionInput:ExpandToGrid(4)



local size = region.Size / 4



local solidMaterials = {}



local solidOccupancies = {}



local waterOcc = {}



for x = 1, size.X do



table.insert(solidMaterials, {})



table.insert(solidOccupancies, {})



table.insert(waterOcc, {})



for y = 1, size.Y do



table.insert(solidMaterials[x], {})



table.insert(solidOccupancies[x], {})



table.insert(waterOcc[x], {})



for z = 1, size.Z do



local mat = if math.random() < 0.5 then Enum.Material.Air else Enum.Material.Sand



local occ = 0



local water = math.random()



if mat == Enum.Material.Sand then



occ = math.random() / 2 + 0.5



if occ > 1 - OCC_EPSILON then



water = 0 -- Solids cannot contain water



end



else



occ = 0



end



table.insert(solidMaterials[x][y], mat)



table.insert(solidOccupancies[x][y], occ)



table.insert(waterOcc[x][y], water)



end



end



end



return { SolidMaterial = solidMaterials, SolidOccupancy = solidOccupancies, LiquidOccupancy = waterOcc }



end



local regionContent = generateRandomTerrainInRegion(region)



workspace.Terrain:WriteVoxelChannels(region, 4, regionContent)
```

Provide feedback

---

WriteVoxels

Sets a certain region of smooth terrain using table format.

Terrain:WriteVoxels(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), materials:[Array](/docs/luau/tables#arrays), occupancy:[Array](/docs/luau/tables#arrays)

):()

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3)  Target region to write to. Must be aligned to the voxel grid. Will throw an error if region is too large. |
| resolution:[number](/docs/luau/numbers)  Voxel resolution. Must be 4. |
| materials:[Array](/docs/luau/tables#arrays)  3D array of Enum.Material. Dimensions must exactly match the size of the target region in voxels. |
| occupancy:[Array](/docs/luau/tables#arrays)  3D array of voxel occupancies (number between 0 and 1). Dimensions must exactly match the size of the target region in voxels. |

Returns

()

Sets a certain region of smooth terrain using table format.

Code Samples

Example

Example

```
local Workspace = game:GetService("Workspace")



local terrain = Workspace.Terrain



local resolution = 4



local region = Region3.new(Vector3.new(0, 0, 0), Vector3.new(16, 28, 20)):ExpandToGrid(resolution)



local materials = {



{



{



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



},



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Mud, Enum.Material.Mud, Enum.Material.Mud, Enum.Material.Mud, Enum.Material.Mud },



{ Enum.Material.Air, Enum.Material.Air, Enum.Material.Air, Enum.Material.Air, Enum.Material.Air },



},



{



{



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



},



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Mud, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Mud },



{ Enum.Material.Air, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Air },



},



{



{



Enum.Material.CrackedLava,



Enum.Material.Sand,



Enum.Material.Sand,



Enum.Material.Sand,



Enum.Material.CrackedLava,



},



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Mud, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Mud },



{ Enum.Material.Air, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Snow, Enum.Material.Air },



},



{



{



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



Enum.Material.CrackedLava,



},



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock, Enum.Material.Rock },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand, Enum.Material.Sand },



{ Enum.Material.Mud, Enum.Material.Mud, Enum.Material.Mud, Enum.Material.Mud, Enum.Material.Mud },



{ Enum.Material.Air, Enum.Material.Air, Enum.Material.Air, Enum.Material.Air, Enum.Material.Air },



},



}



local occupancies = {



{



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 0.5, 0.5, 0.5, 0.5, 0.5 },



{ 0, 0, 0, 0, 0 },



},



{



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 0.5, 1, 1, 1, 0.5 },



{ 0, 1, 1, 1, 0 },



},



{



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 0.5, 1, 1, 1, 0.5 },



{ 0, 1, 1, 1, 0 },



},



{



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 1, 1, 1, 1, 1 },



{ 0.5, 0.5, 0.5, 0.5, 0.5 },



{ 0, 0, 0, 0, 0 },



},



}



terrain:WriteVoxels(region, resolution, materials, occupancies)
```

Maximum Region Size

Many terrain methods throw an error if their given region size is too large.
The limit is currently 4194304 voxels^3 for ReadVoxels() and WriteVoxels(),
and 67108864 voxels^3 for other methods. For methods that take a cframe + size
combination (e.g. FillBlock, FillCylinder etc.), then the region volume is
calculated from the AABB of the target area.

```
local REGION_START = Vector3.new(-20, -20, -20)



local REGION_END = Vector3.new(20, 20, 20)



local CFRAME = CFrame.new(0, 20, 0)



local SIZE = 50



local function getRegionVolumeVoxels(region)



local resolution = 4



local size = region.Size



return (size.x / resolution) * (size.y / resolution) * (size.z / resolution)



end



local function isRegionTooLargeForReadWriteVoxels(region)



return getRegionVolumeVoxels(region) > 4194304



end



local function isRegionTooLarge(region)



return getRegionVolumeVoxels(region) > 67108864



end



-- Helper function to get an axis-aligned Region3 from the given cframe and size



local function getAABBRegion(cframe, size)



local inv = cframe:Inverse()



local x = size * inv.RightVector



local y = size * inv.UpVector



local z = size * inv.LookVector



local w = math.abs(x.X) + math.abs(x.Y) + math.abs(x.Z)



local h = math.abs(y.X) + math.abs(y.Y) + math.abs(y.Z)



local d = math.abs(z.X) + math.abs(z.Y) + math.abs(z.Z)



local pos = cframe.Position



local halfSize = Vector3.new(w, h, d) / 2



return Region3.new(pos - halfSize, pos + halfSize):ExpandToGrid(4)



end



-- Specific functions for checking individual methods



local function isRegionTooLargeForFillBall(cframe, radius)



local diameter = radius * 2



return isRegionTooLarge(getAABBRegion(cframe, Vector3.new(diameter, diameter, diameter)))



end



local function isRegionTooLargeForFillBlock(cframe, size)



return isRegionTooLarge(getAABBRegion(cframe, size))



end



local function isRegionTooLargeForFillCylinder(cframe, height, radius)



local diameter = radius * 2



return isRegionTooLarge(getAABBRegion(cframe, Vector3.new(diameter, height, diameter)))



end



local function isRegionTooLargeForFillRegion(region)



return isRegionTooLarge(region)



end



local function isRegionTooLargeForFillWedge(cframe, size)



return isRegionTooLarge(getAABBRegion(cframe, size))



end



local function isRegionTooLargeForReplaceMaterial(region)



return isRegionTooLarge(region)



end



local region = Region3.new(REGION_START, REGION_END)



print(isRegionTooLargeForReadWriteVoxels(region))



print(isRegionTooLargeForFillBall(CFRAME, SIZE))



print(isRegionTooLargeForFillBlock(CFRAME, SIZE))



print(isRegionTooLargeForFillCylinder(CFRAME, SIZE, SIZE))



print(isRegionTooLargeForFillRegion(region))



print(isRegionTooLargeForFillWedge(CFRAME, SIZE))



print(isRegionTooLargeForReplaceMaterial(region))
```

Provide feedback

---

WriteVoxelsAsync\_beta

Terrain:WriteVoxelsAsync\_beta(

region:[Region3](/docs/reference/engine/datatypes/Region3), resolution:[number](/docs/luau/numbers), channelIds:[Array](/docs/luau/tables#arrays)

):[TerrainWriteOperation](/docs/reference/engine/classes/TerrainWriteOperation)

Parameters

|  |
| --- |
| region:[Region3](/docs/reference/engine/datatypes/Region3) |
| resolution:[number](/docs/luau/numbers) |
| channelIds:[Array](/docs/luau/tables#arrays) |

Returns

[TerrainWriteOperation](/docs/reference/engine/classes/TerrainWriteOperation)

Provide feedback

---