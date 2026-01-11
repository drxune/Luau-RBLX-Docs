# MaterialService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MaterialService
Scraped: 2026-01-11T02:32:05.087213Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- MaterialService
- MaterialVariant
- MaterialVariant.Name
- MaterialVariant.BaseMaterial
- MaterialService:GetBaseMaterialOverride()
- MaterialService:SetBaseMaterialOverride()
- MaterialService.Use2022Materials
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MaterialService](/docs/reference/engine/classes/MaterialService)

English

Feedback

Engine Class

MaterialService

The game service responsible for managing materials.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [AsphaltName](#AsphaltName):[string](/docs/luau/strings) |
| [BasaltName](#BasaltName):[string](/docs/luau/strings) |
| [BrickName](#BrickName):[string](/docs/luau/strings) |
| [CardboardName](#CardboardName):[string](/docs/luau/strings) |
| [CarpetName](#CarpetName):[string](/docs/luau/strings) |
| [CeramicTilesName](#CeramicTilesName):[string](/docs/luau/strings) |
| [ClayRoofTilesName](#ClayRoofTilesName):[string](/docs/luau/strings) |
| [CobblestoneName](#CobblestoneName):[string](/docs/luau/strings) |
| [ConcreteName](#ConcreteName):[string](/docs/luau/strings) |
| [CorrodedMetalName](#CorrodedMetalName):[string](/docs/luau/strings) |
| [CrackedLavaName](#CrackedLavaName):[string](/docs/luau/strings) |
| [DiamondPlateName](#DiamondPlateName):[string](/docs/luau/strings) |
| [FabricName](#FabricName):[string](/docs/luau/strings) |
| [FoilName](#FoilName):[string](/docs/luau/strings) |
| [GlacierName](#GlacierName):[string](/docs/luau/strings) |
| [GraniteName](#GraniteName):[string](/docs/luau/strings) |
| [GrassName](#GrassName):[string](/docs/luau/strings) |
| [GroundName](#GroundName):[string](/docs/luau/strings) |
| [IceName](#IceName):[string](/docs/luau/strings) |
| [LeafyGrassName](#LeafyGrassName):[string](/docs/luau/strings) |
| [LeatherName](#LeatherName):[string](/docs/luau/strings) |
| [LimestoneName](#LimestoneName):[string](/docs/luau/strings) |
| [MarbleName](#MarbleName):[string](/docs/luau/strings) |
| [MetalName](#MetalName):[string](/docs/luau/strings) |
| [MudName](#MudName):[string](/docs/luau/strings) |
| [PavementName](#PavementName):[string](/docs/luau/strings) |
| [PebbleName](#PebbleName):[string](/docs/luau/strings) |
| [PlasterName](#PlasterName):[string](/docs/luau/strings) |
| [PlasticName](#PlasticName):[string](/docs/luau/strings) |
| [RockName](#RockName):[string](/docs/luau/strings) |
| [RoofShinglesName](#RoofShinglesName):[string](/docs/luau/strings) |
| [RubberName](#RubberName):[string](/docs/luau/strings) |
| [SaltName](#SaltName):[string](/docs/luau/strings) |
| [SandName](#SandName):[string](/docs/luau/strings) |
| [SandstoneName](#SandstoneName):[string](/docs/luau/strings) |
| [SlateName](#SlateName):[string](/docs/luau/strings) |
| [SmoothPlasticName](#SmoothPlasticName):[string](/docs/luau/strings) |
| [SnowName](#SnowName):[string](/docs/luau/strings) |
| [Use2022Materials](#Use2022Materials):[boolean](/docs/luau/booleans) |
| [WoodName](#WoodName):[string](/docs/luau/strings) |
| [WoodPlanksName](#WoodPlanksName):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetBaseMaterialOverride](#GetBaseMaterialOverride)(material: [Enum.Material](/docs/reference/engine/enums/Material)):[string](/docs/luau/strings) |
| [GetMaterialVariant](#GetMaterialVariant)(material: [Enum.Material](/docs/reference/engine/enums/Material),name: [string](/docs/luau/strings)):[MaterialVariant](/docs/reference/engine/classes/MaterialVariant) |
| [SetBaseMaterialOverride](#SetBaseMaterialOverride)(material: [Enum.Material](/docs/reference/engine/enums/Material),name: [string](/docs/luau/strings)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

MaterialService is the game service responsible for managing materials. It is
the container for global [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) instances.
[MaterialVariant](/docs/reference/engine/classes/MaterialVariant) can be child or descendant of MaterialService. For
each base Material type, MaterialService internally keeps a set of
MaterialVariant references. [MaterialVariant.Name](/docs/reference/engine/classes/MaterialVariant#Name) is the key to access
it. The [MaterialVariant.Name](/docs/reference/engine/classes/MaterialVariant#Name) and [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
are combined to work as an identifier. If more than one MaterialVariant object
has the same name and BaseMaterial under MaterialService, only one of them can
be used.

MaterialService has some (Material)Name properties. Assigning a
MaterialVariant Name replaces the built-in material with the specified
MaterialVariant. If the MaterialService can't find a matching MaterialVariant,
it falls back to built-in material. Note BaseMaterial should also match, for
example, a MaterialVariant with BaseMaterial Grass can only be assigned to
MaterialService.GrassName, not AsphaltName or any other names. These
properties are not scriptable but can read and write using
[MaterialService:GetBaseMaterialOverride()](/docs/reference/engine/classes/MaterialService#GetBaseMaterialOverride) and
[MaterialService:SetBaseMaterialOverride()](/docs/reference/engine/classes/MaterialService#SetBaseMaterialOverride) function.

MaterialService has a [MaterialService.Use2022Materials](/docs/reference/engine/classes/MaterialService#Use2022Materials) property that
switches between legacy materials and new materials introduced in year 2022.
Because legacy and user-generated (new) terrain materials use different
encoding, using legacy terrain materials and MaterialVariant at the same time
has a performance penalty. If your game is using pre-2022 terrain materials,
avoid overriding any built-in materials. Migrate to 2022 materials if
possible.

---

API Reference

Properties

AsphaltName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Asphalt.

MaterialService.AsphaltName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Asphalt. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Asphalt.

Provide feedback

---

BasaltName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Basalt.

MaterialService.BasaltName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Basalt. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Basalt.

Provide feedback

---

BrickName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Brick.

MaterialService.BrickName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Brick. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Brick.

Provide feedback

---

CardboardName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.CardboardName:[string](/docs/luau/strings)

Provide feedback

---

CarpetName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.CarpetName:[string](/docs/luau/strings)

Provide feedback

---

CeramicTilesName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.CeramicTilesName:[string](/docs/luau/strings)

Provide feedback

---

ClayRoofTilesName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.ClayRoofTilesName:[string](/docs/luau/strings)

Provide feedback

---

CobblestoneName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Cobblestone.

MaterialService.CobblestoneName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Cobblestone. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Cobblestone.

Provide feedback

---

ConcreteName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Concrete.

MaterialService.ConcreteName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Concrete. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Concrete.

Provide feedback

---

CorrodedMetalName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in CorrodedMetal.

MaterialService.CorrodedMetalName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in CorrodedMetal.
The Specified MaterialVariant must have
[MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial) set to CorrodedMetal.

Provide feedback

---

CrackedLavaName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in CrackedLava.

MaterialService.CrackedLavaName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in CrackedLava. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to CrackedLava.

Provide feedback

---

DiamondPlateName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in DiamondPlate.

MaterialService.DiamondPlateName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in DiamondPlate.
The Specified MaterialVariant must have
[MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial) set to DiamondPlate.

Provide feedback

---

FabricName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Fabric.

MaterialService.FabricName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Fabric. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Fabric.

Provide feedback

---

FoilName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Foil.

MaterialService.FoilName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Foil. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Foil.

Provide feedback

---

GlacierName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Glacier.

MaterialService.GlacierName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Glacier. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Glacier.

Provide feedback

---

GraniteName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Granite.

MaterialService.GraniteName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Granite. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Granite.

Provide feedback

---

GrassName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Grass.

MaterialService.GrassName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Grass. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Grass.

Provide feedback

---

GroundName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Ground.

MaterialService.GroundName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Ground. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Ground.

Provide feedback

---

IceName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Ice.

MaterialService.IceName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Ice. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Ice.

Provide feedback

---

LeafyGrassName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in LeafyGrass.

MaterialService.LeafyGrassName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in LeafyGrass. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to LeafyGrass.

Provide feedback

---

LeatherName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.LeatherName:[string](/docs/luau/strings)

Provide feedback

---

LimestoneName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Limestone.

MaterialService.LimestoneName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Limestone. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Limestone.

Provide feedback

---

MarbleName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Marble.

MaterialService.MarbleName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Marble. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Marble.

Provide feedback

---

MetalName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Metal.

MaterialService.MetalName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Metal. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Metal.

Provide feedback

---

MudName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Mud.

MaterialService.MudName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Mud. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Mud.

Provide feedback

---

PavementName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Pavement.

MaterialService.PavementName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Pavement. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Pavement.

Provide feedback

---

PebbleName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Pebble.

MaterialService.PebbleName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Pebble. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Pebble.

Provide feedback

---

PlasterName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.PlasterName:[string](/docs/luau/strings)

Provide feedback

---

PlasticName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Plastic.

MaterialService.PlasticName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Plastic. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Plastic.

Provide feedback

---

RockName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Rock.

MaterialService.RockName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Rock. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Rock.

Provide feedback

---

RoofShinglesName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.RoofShinglesName:[string](/docs/luau/strings)

Provide feedback

---

RubberName

Not Scriptable

Roblox Security

Read Parallel

MaterialService.RubberName:[string](/docs/luau/strings)

Provide feedback

---

SaltName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Salt.

MaterialService.SaltName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Salt. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Salt.

Provide feedback

---

SandName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Sand.

MaterialService.SandName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Sand. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Sand.

Provide feedback

---

SandstoneName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Sandstone.

MaterialService.SandstoneName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Sandstone. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Sandstone.

Provide feedback

---

SlateName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Slate.

MaterialService.SlateName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Slate. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Slate.

Provide feedback

---

SmoothPlasticName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in SmoothPlastic.

MaterialService.SmoothPlasticName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in SmoothPlastic.
The Specified MaterialVariant must have
[MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial) set to SmoothPlastic.

Provide feedback

---

SnowName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Snow.

MaterialService.SnowName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Snow. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Snow.

Provide feedback

---

Use2022Materials

Not Replicated

Roblox Script Security

Read Parallel

Switch built-in material pack.

MaterialService.Use2022Materials:[boolean](/docs/luau/booleans)

When it's false, built-in materials use the material pack before 2022.
When it's true, built-in materials use the material pack released in 2022.

Provide feedback

---

WoodName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Wood.

MaterialService.WoodName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in Wood. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to Wood.

Provide feedback

---

WoodPlanksName

Not Scriptable

Roblox Security

Read Parallel

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in WoodPlanks.

MaterialService.WoodPlanksName:[string](/docs/luau/strings)

Specify [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name to override built-in WoodPlanks. The
Specified MaterialVariant must have [MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial)
set to WoodPlanks.

Provide feedback

---

Methods

GetBaseMaterialOverride

Get the override [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name of specified Material type.

MaterialService:GetBaseMaterialOverride(material:[Enum.Material](/docs/reference/engine/enums/Material)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| material:[Enum.Material](/docs/reference/engine/enums/Material)  Material type to be fetched. |

Returns

[string](/docs/luau/strings)

MaterialVariant name currently set as override.

Get the override [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name of specified Material type.

Provide feedback

---

GetMaterialVariant

Get the effective MaterialVariant reference given a name and Material.

MaterialService:GetMaterialVariant(

material:[Enum.Material](/docs/reference/engine/enums/Material), name:[string](/docs/luau/strings)

):[MaterialVariant](/docs/reference/engine/classes/MaterialVariant)

Parameters

|  |
| --- |
| material:[Enum.Material](/docs/reference/engine/enums/Material)  BaseMaterial of MaterialVariant. |
| name:[string](/docs/luau/strings)  Name of MaterialVariant. |

Returns

[MaterialVariant](/docs/reference/engine/classes/MaterialVariant)

A MaterialVariant instance that matches parameters.

Get the effective MaterialVariant reference given a MaterialVariant name
and BaseMaterial. This MaterialVariant must be a descendant of
MaterialService. Returns nil if no matching instance exists.

Provide feedback

---

SetBaseMaterialOverride

Set a [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name that overrides a built-in material.

MaterialService:SetBaseMaterialOverride(

material:[Enum.Material](/docs/reference/engine/enums/Material), name:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| material:[Enum.Material](/docs/reference/engine/enums/Material)  The Material type to be changed. |
| name:[string](/docs/luau/strings)  Name of the MaterialVariant object. |

Returns

()

Set a [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) name that overrides a built-in material.

Provide feedback

---