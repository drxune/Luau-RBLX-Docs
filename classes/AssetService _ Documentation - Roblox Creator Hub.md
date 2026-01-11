# AssetService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AssetService
Scraped: 2026-01-11T02:41:26.820645Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- AssetService
- Decal
- EditableImage
- EditableMesh
- MeshPart
- SurfaceAppearance
- Player
- AudioSearchParams
- AudioPages
- AssetService:LoadAssetAsync()
- Size
- FixedSize
- CollisionFidelity
- RenderFidelity
- FluidFidelity
- MeshPart.MeshId
- PlaceId
- TeleportService
- DataStores
- AssetService:CreateEditableImageAsync(Content.fromUri(uri))
- StandardPages
- Model
- InsertService:LoadAsset()
- InsertService:LoadAssetVersion()
- Sandboxed
- AssetService:CreatePlaceAsync()
- AssetService:SearchAudio()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AssetService](/docs/reference/engine/classes/AssetService)

English

Feedback

Engine Class

AssetService

A non-replicated service that handles asset-related queries to the Roblox web
API.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [AllowInsertFreeAssets](#AllowInsertFreeAssets):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [ComposeDecalAsync](#ComposeDecalAsync)(layers: [Array](/docs/luau/tables#arrays)):[Decal](/docs/reference/engine/classes/Decal) |
| [CreateAssetAsync](#CreateAssetAsync)(object: [Object](/docs/reference/engine/classes/Object),assetType: [Enum.AssetType](/docs/reference/engine/enums/AssetType),requestParameters: [Dictionary](/docs/luau/tables#dictionaries)):[Tuple](/docs/luau/tuples) |
| [CreateAssetVersionAsync](#CreateAssetVersionAsync)(object: [Object](/docs/reference/engine/classes/Object),assetType: [Enum.AssetType](/docs/reference/engine/enums/AssetType),assetId: [number](/docs/luau/numbers),requestParameters: [Dictionary](/docs/luau/tables#dictionaries)):[Tuple](/docs/luau/tuples) |
| [CreateEditableImage](#CreateEditableImage)(editableImageOptions: [Dictionary](/docs/luau/tables#dictionaries)?):[EditableImage](/docs/reference/engine/classes/EditableImage) |
| [CreateEditableImageAsync](#CreateEditableImageAsync)(content: [Content](/docs/reference/engine/datatypes/Content),editableImageOptions: [Dictionary](/docs/luau/tables#dictionaries)?):[EditableImage](/docs/reference/engine/classes/EditableImage) |
| [CreateEditableMesh](#CreateEditableMesh)(editableMeshOptions: [Dictionary](/docs/luau/tables#dictionaries)?):[EditableMesh](/docs/reference/engine/classes/EditableMesh) |
| [CreateEditableMeshAsync](#CreateEditableMeshAsync)(content: [Content](/docs/reference/engine/datatypes/Content),editableMeshOptions: [Dictionary](/docs/luau/tables#dictionaries)?):[EditableMesh](/docs/reference/engine/classes/EditableMesh) |
| [CreateMeshPartAsync](#CreateMeshPartAsync)(meshContent: [Content](/docs/reference/engine/datatypes/Content),options: [Dictionary](/docs/luau/tables#dictionaries)):[MeshPart](/docs/reference/engine/classes/MeshPart) |
| [CreatePlaceAsync](#CreatePlaceAsync)(placeName: [string](/docs/luau/strings),templatePlaceID: [number](/docs/luau/numbers),description: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [CreatePlaceInPlayerInventoryAsync](#CreatePlaceInPlayerInventoryAsync)(player: [Instance](/docs/reference/engine/datatypes/Instance),placeName: [string](/docs/luau/strings),templatePlaceID: [number](/docs/luau/numbers),description: [string](/docs/luau/strings)):[number](/docs/luau/numbers)  Deprecated |
| [CreateSurfaceAppearanceAsync](#CreateSurfaceAppearanceAsync)(content: [Dictionary](/docs/luau/tables#dictionaries)):[SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) |
| [GetAssetIdsForPackageAsync](#GetAssetIdsForPackageAsync)(packageAssetId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetAssetIdsForPackage](#GetAssetIdsForPackage)(packageAssetId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetAudioMetadataAsync](#GetAudioMetadataAsync)(idList: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |
| [GetBundleDetailsAsync](#GetBundleDetailsAsync)(bundleId: [number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetCreatorAssetID](#GetCreatorAssetID)(creationID: [number](/docs/luau/numbers)):[number](/docs/luau/numbers)  Deprecated |
| [GetGamePlacesAsync](#GetGamePlacesAsync)():[Instance](/docs/reference/engine/datatypes/Instance) |
| [LoadAssetAsync](#LoadAssetAsync)(assetId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [PromptCreateAssetAsync](#PromptCreateAssetAsync)(player: [Player](/docs/reference/engine/classes/Player),instance: [Instance](/docs/reference/engine/datatypes/Instance),assetType: [Enum.AssetType](/docs/reference/engine/enums/AssetType)):[Tuple](/docs/luau/tuples) |
| [PromptImportAnimationClipFromVideoAsync](#PromptImportAnimationClipFromVideoAsync)(player: [Player](/docs/reference/engine/classes/Player),progressCallback: [function](/docs/luau/functions)):[Tuple](/docs/luau/tuples) |
| [SavePlaceAsync](#SavePlaceAsync)(requestParameters: [Dictionary](/docs/luau/tables#dictionaries)?):() |
| [SearchAudioAsync](#SearchAudioAsync)(searchParameters: [AudioSearchParams](/docs/reference/engine/classes/AudioSearchParams)):[AudioPages](/docs/reference/engine/classes/AudioPages) |
| [SearchAudio](#SearchAudio)(searchParameters: [AudioSearchParams](/docs/reference/engine/classes/AudioSearchParams)):[AudioPages](/docs/reference/engine/classes/AudioPages)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

AssetService is a non-replicated service that handles asset-related
queries to the Roblox web API.

---

API Reference

Properties

AllowInsertFreeAssets

Roblox Script Security

Read Parallel

Controls whether [AssetService:LoadAssetAsync()](/docs/reference/engine/classes/AssetService#LoadAssetAsync) can load assets
that are not owned by the experience creator.

AssetService.AllowInsertFreeAssets:[boolean](/docs/luau/booleans)

This property can only be modified in Studio by changing Allow Loading
Third Party Assets in Home > Game Settings > Security.

When false (default), [AssetService:LoadAssetAsync()](/docs/reference/engine/classes/AssetService#LoadAssetAsync) can only
load assets that meet one of the following:

* The asset must be created or owned by the game creator.
* The asset must be shared by the asset owner.
* The asset must be owned by Roblox.

When true, [AssetService:LoadAssetAsync()](/docs/reference/engine/classes/AssetService#LoadAssetAsync) can additionally load
any public free asset on the Creator Store.

Provide feedback

---

Methods

ComposeDecalAsync

Yields

Creates a Decal instance that uses composite PBR textures created by
layering the provided textures in the order they are provided in the
layers array. Textures layer based on the alpha value of the ColorMap.

AssetService:ComposeDecalAsync(layers:[Array](/docs/luau/tables#arrays)):[Decal](/docs/reference/engine/classes/Decal)

Parameters

|  |
| --- |
| layers:[Array](/docs/luau/tables#arrays)  An array of Dictionary tables that maps PBR names to ContentID. |

Returns

[Decal](/docs/reference/engine/classes/Decal)

A new [Decal](/docs/reference/engine/classes/Decal) containing the composed texture set.

Creates a new [Decal](/docs/reference/engine/classes/Decal) that contains a composed texture derived from
one or more layered texture sets. Each set can include color, roughness,
metalness, and normal maps. Each layer is composited in the order they
are provided, with the ColorMap alpha channel used to determine blending.

* There is a limit of 8 layers.
* Layering order is bottom-to-top: the first layer in the list provides
  the bottom-most textures.
* Each dictionary table should contain the following key-value pairs:
  + ColorMap: A [Content](/docs/reference/engine/datatypes/Content) referencing a color (albedo)
    texture by assetId.
  + RoughnessMap: A [Content](/docs/reference/engine/datatypes/Content) referencing a roughness texture
    by assetId.
  + MetalnessMap: A [Content](/docs/reference/engine/datatypes/Content) referencing a metalness texture
    by assetId.
  + NormalMap: A [Content](/docs/reference/engine/datatypes/Content) referencing a normal texture by
    assetId.
* ColorMap is mandatory in every layer. The ColorMap's alpha channel is
  used to control blending of the entire layer.
* NormalMap, MetalnessMap, RoughnessMap are optional. If omitted,
  this layer doesn't perform any blending for those maps.

Code Samples

```
-- Get AssetService



local AssetService = game:GetService("AssetService")



-- Create two decal instances



local DecalA = Instance.new("Decal")



local DecalB = Instance.new("Decal")



-- Build composite info table



local compositeInfo = {



{



ColorMap = DecalA.ColorMapContent,



RoughnessMap = DecalA.RoughnessMapContent,



MetalnessMap = DecalA.MetalnessMapContent,



NormalMap = DecalA.NormalMapContent,



},



{



ColorMap = Content.fromAssetId(123456),



RoughnessMap = DecalB.RoughnessMapContent,



MetalnessMap = DecalB.MetalnessMapContent,



NormalMap = DecalB.NormalMapContent,



}



}



-- Compose a new decal using AssetService



local compositeDecal = AssetService:ComposeDecalAsync(compositeInfo)
```

Provide feedback

---

CreateAssetAsync

Yields

Uploads a new asset to Roblox from the given object.

AssetService:CreateAssetAsync(

object:[Object](/docs/reference/engine/classes/Object), assetType:[Enum.AssetType](/docs/reference/engine/enums/AssetType), requestParameters:[Dictionary](/docs/luau/tables#dictionaries)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| object:[Object](/docs/reference/engine/classes/Object)  The object to be created as an asset. |
| assetType:[Enum.AssetType](/docs/reference/engine/enums/AssetType)  Currently supported types are:   * [Enum.AssetType.Model](/docs/reference/engine/enums/AssetType#Model) – with object as any valid [Instance](/docs/reference/engine/classes/Instance)   root. * [Enum.AssetType.Plugin](/docs/reference/engine/enums/AssetType#Plugin) – with object as any valid   [Instance](/docs/reference/engine/classes/Instance) root. * [Enum.AssetType.Mesh](/docs/reference/engine/enums/AssetType#Mesh) – with object as any valid   [EditableMesh](/docs/reference/engine/classes/EditableMesh) root. * [Enum.AssetType.Image](/docs/reference/engine/enums/AssetType#Image) – with object as any valid   [EditableImage](/docs/reference/engine/classes/EditableImage) root. |
| requestParameters:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Options table containing asset metadata:   * Name – Name of the asset as a string. Defaults to [object.Name]. * Description – Description of the asset as a string. Defaults to   "Created with AssetService:CreateAssetAsync". * CreatorId – ID of the asset creator as a number. Defaults to the   logged in Roblox Studio user for Plugin context. Required for Open   Cloud Luau Execution context. * CreatorType – [Enum.AssetCreatorType](/docs/reference/engine/enums/AssetCreatorType) indicating the type of asset   creator. Defaults to [Enum.AssetCreatorType.User](/docs/reference/engine/enums/AssetCreatorType#User) in Plugin context.   Required for Open Cloud Luau Execution context. * IsPackage – Boolean value, only applicable to the   [Enum.AssetType.Model](/docs/reference/engine/enums/AssetType#Model) type. Defaults to true. |

Returns

[Tuple](/docs/luau/tuples)

The [Enum.CreateAssetResult](/docs/reference/engine/enums/CreateAssetResult) and asset ID pair if successful.

Uploads a new asset to Roblox from the given object.

Currently, this method can only be used in locally loaded plugins and
uploads assets without prompting first.

Code Samples

AssetService:CreateAssetAsync

The following code creates a Mesh asset from an EditableMesh.

```
local AssetService = game:GetService("AssetService")



local editableMesh = AssetService:CreateEditableMesh()



-- add vertices, faces, and uvs to the mesh



local requestParameters = {



CreatorId = 123,



CreatorType = Enum.AssetCreatorType.User,



Name = "My asset",



Description = "a good asset",



}



local ok, result, idOrUploadErr = pcall(function()



return AssetService:CreateAssetAsync(editableMesh, Enum.AssetType.Mesh, requestParameters)



end)



if not ok then



warn(`error calling CreateAssetAsync: {result}`)



elseif result == Enum.CreateAssetResult.Success then



print(`success, new asset ID: {idOrUploadErr}`)



else



warn(`upload error in CreateAssetAsync: {result}, {idOrUploadErr}`)



end
```

Provide feedback

---

CreateAssetVersionAsync

Yields

Uploads a new version for an existing asset from the given object.

AssetService:CreateAssetVersionAsync(

object:[Object](/docs/reference/engine/classes/Object), assetType:[Enum.AssetType](/docs/reference/engine/enums/AssetType), assetId:[number](/docs/luau/numbers), requestParameters:[Dictionary](/docs/luau/tables#dictionaries)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| object:[Object](/docs/reference/engine/classes/Object)  The object to be created as an asset. |
| assetType:[Enum.AssetType](/docs/reference/engine/enums/AssetType)  Currently supported types are:   * [Enum.AssetType.Model](/docs/reference/engine/enums/AssetType#Model) – with object as any valid [Instance](/docs/reference/engine/classes/Instance)   root. * [Enum.AssetType.Plugin](/docs/reference/engine/enums/AssetType#Plugin) – with object as any valid   [Instance](/docs/reference/engine/classes/Instance) root. * [Enum.AssetType.Mesh](/docs/reference/engine/enums/AssetType#Mesh) – with object as any valid   [EditableMesh](/docs/reference/engine/classes/EditableMesh) root. * [Enum.AssetType.Image](/docs/reference/engine/enums/AssetType#Image) – with object as any valid   [EditableImage](/docs/reference/engine/classes/EditableImage) root. |
| assetId:[number](/docs/luau/numbers)  The ID of the asset for the new version. |
| requestParameters:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Options table containing asset metadata:   * Name – A string. Name of the asset. Default: object.Name. * Description – A string. Description of the asset. Default:   "Created with AssetService:CreateAssetAsync". * CreatorId – A number. ID of the asset creator. Default: The   logged in Roblox Studio user for Plugin context. Required for Open   Cloud Luau Execution context. * CreatorType – A [Enum.AssetCreatorType](/docs/reference/engine/enums/AssetCreatorType). Type of asset creator.   Default: [Enum.AssetCreatorType.User](/docs/reference/engine/enums/AssetCreatorType#User) in Plugin context. Required   for Open Cloud Luau Execution context. * IsPackage – A bool. Only applicable to the   [Enum.AssetType.Model](/docs/reference/engine/enums/AssetType#Model) type. Default: true. |

Returns

[Tuple](/docs/luau/tuples)

The [Enum.CreateAssetResult](/docs/reference/engine/enums/CreateAssetResult) and asset version number pair if
successful.

Uploads a new version for an existing asset from the given object.

Currently, this method can only be used in locally loaded plugins and
uploads assets without prompting first.

Code Samples

AssetService:CreateAssetVersionAsync

The following code creates a new Model asset version.

```
local AssetService = game:GetService("AssetService")



local assetIdToUpdate = 321



local model = Instance.new("Model")



local requestParameters = {



CreatorId = 123,



CreatorType = Enum.AssetCreatorType.User,



}



local ok, result, versionOrUploadErr = pcall(function()



return AssetService:CreateAssetVersionAsync(model, Enum.AssetType.Model, assetIdToUpdate, requestParameters)



end)



if not ok then



warn(`error calling CreateAssetVersionAsync: {result}`)



elseif result == Enum.CreateAssetResult.Success then



print(`success, new asset version: {versionOrUploadErr}`)



else



warn(`upload error in CreateAssetVersionAsync: {result}, {versionOrUploadErr}`)



end
```

Provide feedback

---

CreateEditableImage

Creates a new [EditableImage](/docs/reference/engine/classes/EditableImage).

AssetService:CreateEditableImage(editableImageOptions:[Dictionary](/docs/luau/tables#dictionaries)?):[EditableImage](/docs/reference/engine/classes/EditableImage)

Parameters

|  |
| --- |
| editableImageOptions:[Dictionary](/docs/luau/tables#dictionaries)?  Options table containing controls for the method:   * Size – A [Vector2](/docs/reference/engine/datatypes/Vector2) that specifies the image's desired   width and height. |

Returns

[EditableImage](/docs/reference/engine/classes/EditableImage)

Creates a new [EditableImage](/docs/reference/engine/classes/EditableImage). By default, the resolution is set at
512×512, but you can specify a different size using the method's
option table.

If the device‑specific editable memory budget is exhausted, creation fails
and this method returns nil.

Provide feedback

---

CreateEditableImageAsync

Yields

Creates a new [EditableImage](/docs/reference/engine/classes/EditableImage) object populated with the given image.

AssetService:CreateEditableImageAsync(

content:[Content](/docs/reference/engine/datatypes/Content), editableImageOptions:[Dictionary](/docs/luau/tables#dictionaries)?

):[EditableImage](/docs/reference/engine/classes/EditableImage)

Parameters

|  |
| --- |
| content:[Content](/docs/reference/engine/datatypes/Content)  Reference to asset content stored externally or as an object within the place, wrapping a single value of one of the supported [Enum.ContentSourceType](/docs/reference/engine/enums/ContentSourceType) values. |
| editableImageOptions:[Dictionary](/docs/luau/tables#dictionaries)?  Table containing options for the created [EditableImage](/docs/reference/engine/classes/EditableImage). Currently no options are available since resizing via [Size](/docs/reference/engine/classes/EditableImage#Size) is not supported. |

Returns

[EditableImage](/docs/reference/engine/classes/EditableImage)

A new [EditableImage](/docs/reference/engine/classes/EditableImage) containing the provided image.

Creates a new [EditableImage](/docs/reference/engine/classes/EditableImage) object populated with the given
texture. Non-asset texture IDs such as rbxthumb:// are supported. If
using an image asset, it must be associated with and/or owned by a creator
of the experience, or it must have been created inside the experience. If
the device-specific editable memory budget is exhausted, creation will
fail and this method will return nil.

See the [EditableImage](/docs/reference/engine/classes/EditableImage) documentation for special considerations
when using this API.

Provide feedback

---

CreateEditableMesh

Creates a new, empty [EditableMesh](/docs/reference/engine/classes/EditableMesh).

AssetService:CreateEditableMesh(editableMeshOptions:[Dictionary](/docs/luau/tables#dictionaries)?):[EditableMesh](/docs/reference/engine/classes/EditableMesh)

Parameters

|  |
| --- |
| editableMeshOptions:[Dictionary](/docs/luau/tables#dictionaries)?  Table containing options for the created [EditableMesh](/docs/reference/engine/classes/EditableMesh). Currently no options are available since [FixedSize](/docs/reference/engine/classes/EditableMesh#FixedSize) will always be false for empty editable meshes. |

Returns

[EditableMesh](/docs/reference/engine/classes/EditableMesh)

Creates a new, empty [EditableMesh](/docs/reference/engine/classes/EditableMesh). Vertices, triangles, and their
attributes can be added dynamically to it. If the device‑specific editable
memory budget is exhausted, creation will fail and this method will return
nil.

Provide feedback

---

CreateEditableMeshAsync

Yields

Returns a new [EditableMesh](/docs/reference/engine/classes/EditableMesh) object created from an existing mesh
content ID.

AssetService:CreateEditableMeshAsync(

content:[Content](/docs/reference/engine/datatypes/Content), editableMeshOptions:[Dictionary](/docs/luau/tables#dictionaries)?

):[EditableMesh](/docs/reference/engine/classes/EditableMesh)

Parameters

|  |
| --- |
| content:[Content](/docs/reference/engine/datatypes/Content)  Reference to asset content stored externally or as an object within the place, wrapping a single value of one of the supported [Enum.ContentSourceType](/docs/reference/engine/enums/ContentSourceType) values. |
| editableMeshOptions:[Dictionary](/docs/luau/tables#dictionaries)?  Options table containing controls for the method:   * FixedSize – A bool. Default value is true, and the returned   [EditableMesh](/docs/reference/engine/classes/EditableMesh) will not allow you to add or remove vertices,   only modify their values. Set to false if the ability to change   the mesh topology is required, at the expense of using more memory. |

Returns

[EditableMesh](/docs/reference/engine/classes/EditableMesh)

The new [EditableMesh](/docs/reference/engine/classes/EditableMesh) instance.

Returns a new [EditableMesh](/docs/reference/engine/classes/EditableMesh) object created from an existing
[EditableMesh](/docs/reference/engine/classes/EditableMesh) or mesh [Content](/docs/reference/engine/datatypes/Content) ID. By default, an
[EditableMesh](/docs/reference/engine/classes/EditableMesh) created from this method will be fixed size such that
mesh data can only be modified, not added nor removed. A fixed size
[EditableMesh](/docs/reference/engine/classes/EditableMesh) consumes less memory and should be preferred when
possible.

If the device-specific editable memory budget is exhausted, creation will
fail and this method will return nil.

See the Enabling EditableMesh for Published Experiences and
Permissions sections of [EditableMesh](/docs/reference/engine/classes/EditableMesh) for special
considerations when using this API.

Provide feedback

---

CreateMeshPartAsync

Yields

Creates a new [MeshPart](/docs/reference/engine/classes/MeshPart) with a specified mesh ID and an optional
table of fidelity values.

AssetService:CreateMeshPartAsync(

meshContent:[Content](/docs/reference/engine/datatypes/Content), options:[Dictionary](/docs/luau/tables#dictionaries)

):[MeshPart](/docs/reference/engine/classes/MeshPart)

Parameters

|  |
| --- |
| meshContent:[Content](/docs/reference/engine/datatypes/Content)  Reference to asset content stored externally or as an object within the place, wrapping a single value of one of the supported [Enum.ContentSourceType](/docs/reference/engine/enums/ContentSourceType) values. |
| options:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Options table containing one or more controls for the method:   * CollisionFidelity – The value of   [CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity) in the   resulting part. Defaults to [Enum.CollisionFidelity.Default](/docs/reference/engine/enums/CollisionFidelity#Default) if the   option is absent or the options table is nil. * RenderFidelity – The value of   [RenderFidelity](/docs/reference/engine/classes/MeshPart#RenderFidelity) in the resulting   part. Defaults to [Enum.RenderFidelity.Automatic](/docs/reference/engine/enums/RenderFidelity#Automatic) if the option is   absent or the options table is nil. * FluidFidelity – The value of   [FluidFidelity](/docs/reference/engine/classes/MeshPart#FluidFidelity) in the resulting part.   Defaults to [Enum.FluidFidelity.Automatic](/docs/reference/engine/enums/FluidFidelity#Automatic) if the option is absent   or the options table is nil. |

Returns

[MeshPart](/docs/reference/engine/classes/MeshPart)

This method creates a [MeshPart](/docs/reference/engine/classes/MeshPart) with a specified
[CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity),
[RenderFidelity](/docs/reference/engine/classes/MeshPart#RenderFidelity), and
[FluidFidelity](/docs/reference/engine/classes/MeshPart#FluidFidelity). Because
[MeshPart.MeshId](/docs/reference/engine/classes/MeshPart#MeshId) is read only, this method is for creating a mesh
with any mesh ID through scripts, without having to clone an existing
[MeshPart](/docs/reference/engine/classes/MeshPart). It throws errors if creation fails.

Provide feedback

---

CreatePlaceAsync

Yields

Clones a place through the given templatePlaceID.

AssetService:CreatePlaceAsync(

placeName:[string](/docs/luau/strings), templatePlaceID:[number](/docs/luau/numbers), description:[string](/docs/luau/strings)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| placeName:[string](/docs/luau/strings)  Name of the new place. |
| templatePlaceID:[number](/docs/luau/numbers)  [PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the place to clone. |
| description:[string](/docs/luau/strings)  Description of the new place. |

Returns

[number](/docs/luau/numbers)

[PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the new place.

Clones a place through the given templatePlaceID and returns the
[PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the new place, which you can use with
[TeleportService](/docs/reference/engine/classes/TeleportService). The clone place displays within the inventory of
the place's creator with the given name and description.

Note that the template place must have template copying enabled through
place settings. You cannot use this method to clone places that you don't
own.

Frequent use of this API is not recommended, particularly if the created
places contain scripts, as updating the code in a large volume of places
quickly becomes infeasible. For user-generated worlds, consider
serializing user creations and saving them in [DataStores](/docs/reference/engine/classes/DataStore)
instead.

Provide feedback

---

CreatePlaceInPlayerInventoryAsync

Deprecated

Show details

---

CreateSurfaceAppearanceAsync

Yields

Creates a new [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) object using the provided content
maps.

AssetService:CreateSurfaceAppearanceAsync(content:[Dictionary](/docs/luau/tables#dictionaries)):[SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance)

Parameters

|  |
| --- |
| content:[Dictionary](/docs/luau/tables#dictionaries)  Dictionary containing the following key-value pairs:   * ColorMap — A [Content](/docs/reference/engine/datatypes/Content) object that contains the color   map. Default is nil. * MetalnessMap — A [Content](/docs/reference/engine/datatypes/Content) object that contains the   metalness map. If more than one channel is present, only the red   channel is used. Default is nil. * NormalMap — A [Content](/docs/reference/engine/datatypes/Content) object that contains the normal   map. Default is nil. * RoughnessMap — A [Content](/docs/reference/engine/datatypes/Content) object that contains the   roughness map. If more than one channel is present, only the red   channel is used. Default is nil. * EmissiveMask — A [Content](/docs/reference/engine/datatypes/Content) object that contains the   emissive mask. If more than one channel is present, only the red   channel is used. Default is nil. |

Returns

[SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance)

A new [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) instance with the given maps from the
content parameter.

Creates a new [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) object using the provided content
maps.

Currently, content only supports [EditableImage](/docs/reference/engine/classes/EditableImage) and only content
maps can be specified, but functionality will expand to include asset IDs
as input. If you need to achieve this today, you can create an
[EditableImage](/docs/reference/engine/classes/EditableImage) from an asset ID using the following:

[AssetService:CreateEditableImageAsync(Content.fromUri(uri))](/docs/reference/engine/classes/AssetService#CreateEditableImageAsync)

Default values will be used for all other [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance)
properties.

Code Samples

AssetService:CreateSurfaceAppearanceAsync

The following code creates a [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) instance with the given
[EditableImage](/docs/reference/engine/classes/EditableImage) content and assigns it to a [MeshPart](/docs/reference/engine/classes/MeshPart).

```
local AssetService = game:GetService("AssetService")



local Workspace = game:GetService("Workspace")



-- Red color



local colorEditableImage = AssetService:CreateEditableImage({ Size = Vector2.new(4, 4) })



colorEditableImage:DrawRectangle(Vector2.zero, colorEditableImage.Size, Color3.fromRGB(255, 0, 0), 0, Enum.ImageCombineType.Overwrite)



-- Metalness (only look at the red channel)



local metalnessEditableImage = AssetService:CreateEditableImage({ Size = Vector2.new(1, 1) })



metalnessEditableImage:DrawRectangle(Vector2.zero, metalnessEditableImage.Size, Color3.new(1, 0, 0), 0, Enum.ImageCombineType.Overwrite)



-- Roughness (only look at the red channel)



local roughnessEditableImage = AssetService:CreateEditableImage({ Size = Vector2.new(1, 1) })



roughnessEditableImage:DrawRectangle(Vector2.zero, roughnessEditableImage.Size, Color3.new(0.2, 0, 0), 0, Enum.ImageCombineType.Overwrite)



local surfaceAppearance = AssetService:CreateSurfaceAppearanceAsync({



ColorMap = Content.fromObject(colorEditableImage),



MetalnessMap = Content.fromObject(metalnessEditableImage),



RoughnessMap = Content.fromObject(roughnessEditableImage)



})



local meshPart = Instance.new("MeshPart")



meshPart.Parent = Workspace



-- Apply surface appearance to mesh part



surfaceAppearance.Parent = meshPart
```

Provide feedback

---

GetAssetIdsForPackageAsync

Yields

Returns an array of asset IDs that are contained in a specified package.

AssetService:GetAssetIdsForPackageAsync(packageAssetId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| packageAssetId:[number](/docs/luau/numbers) |

Returns

[Array](/docs/luau/tables#arrays)

Asset IDs that are contained in a specified package.

Returns an array of asset IDs that are contained in a specified package.

Provide feedback

---

GetAssetIdsForPackage

Deprecated

Show details

---

GetAudioMetadataAsync

Yields

Provides relevant metadata about a specific audio source.

AssetService:GetAudioMetadataAsync(idList:[Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| idList:[Array](/docs/luau/tables#arrays)  Array of asset or content IDs for which to retrieve metadata. Max batch size is 30. |

Returns

[Array](/docs/luau/tables#arrays)

Array of dictionary tables in the same order as the request, where
each dictionary contains the following metadata for its asset/content:

* AssetId (string)
* Title (string)
* Artist (string)
* Duration (number) in seconds
* AudioType ([Enum.AudioSubType](/docs/reference/engine/enums/AudioSubType))

Note that if an error occurs on fetching metadata for any of the
requested assets, for example the asset ID doesn't exist, its
dictionary table is still included in the returned array but it only
contains the AssetId field for reference purposes. Additionally, if
the AudioType cannot be determined for a given asset (perhaps
because it's private audio), the resulting dictionary will not contain
an AudioType entry.

Provides relevant metadata about a specific audio source (artist, title,
duration, type, etc.).

Code Samples

```
local AssetService = game:GetService("AssetService")



local SoundService = game:GetService("SoundService")



local trackIDs = {



SoundService.Sound1.SoundId,



SoundService.Sound2.SoundId,



SoundService.Sound3.SoundId,



SoundService.Sound4.SoundId,



}



local success, result = pcall(function()



return AssetService:GetAudioMetadataAsync(trackIDs)



end)



if success then



for i = 1, #trackIDs do



local contentId = "rbxassetid://" .. result[i].AssetId



if trackIDs[i] == contentId then



print(result[i].Title, "by", result[i].Artist)



else



warn("No metadata fetched for requested asset #" .. tostring(i))



end



end



end
```

Provide feedback

---

GetBundleDetailsAsync

Yields

Returns details of the contents of specified bundle.

AssetService:GetBundleDetailsAsync(bundleId:[number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| bundleId:[number](/docs/luau/numbers)  The ID of the specified bundle. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Dictionary with the following key-value pairs containing details about
the specified bundle:

* Id — Bundle ID (same as passed bundleId argument)
* Name — Bundle name
* Description — Bundle description
* BundleType — String representing the [Enum.BundleType](/docs/reference/engine/enums/BundleType), for
  example "BodyParts" or "DynamicHead"
* Items — Array of items in the bundle, each with details
  represented through the following keys:

  + Id — Item ID
  + Name — Item name
  + Type — Item type such as "Asset" .

This function returns details of the contents of the specified bundle.

If the bundle ID does not exist, it throws HTTP 400 (Bad Request). If
bundleId is not convertible to an integer, it throws
Unable to cast string to int64.

Code Samples

Getting Bundle Details

```
local AssetService = game:GetService("AssetService")



local BUNDLE_ID = 14



local success, result = pcall(function()



return AssetService:GetBundleDetailsAsync(BUNDLE_ID)



end)



if success then



print(result)



--[[



{



["BundleType"] = "BodyParts",



["Description"] = "The year is 5003, Battlebot 5000 must face his mightiest foe, or face becoming obsolete.",



["Id"] = 14,



["Items"] = {



[1] = {...},



[2] = {



["Id"] = 1678225030,



["Name"] = "SinisterBot 5001 Left Arm",



["Type"] = "Asset"



},



[3] = {...},



[4] = {...},



[5] = {...},



[6] = {...},



[7] = {...}



},



["Name"] = "SinisterBot 5001"



}



--]]



end
```

Provide feedback

---

GetCreatorAssetID

Deprecated

Show details

---

GetGamePlacesAsync

Yields

Returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object which contains the name and
[PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of places within the current experience.

AssetService:GetGamePlacesAsync():[Instance](/docs/reference/engine/datatypes/Instance)

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object which contains the name and
[PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of places within the current experience.

Code Samples

AssetService:GetGamePlacesAsync

The following code prints the name and [PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of
each place in the experience.

```
local AssetService = game:GetService("AssetService")



local placePages = AssetService:GetGamePlacesAsync()



while true do



for _, place in placePages:GetCurrentPage() do



print("Name:", place.Name)



print("PlaceId:", place.PlaceId)



end



if placePages.IsFinished then



break



end



placePages:AdvanceToNextPageAsync()



end
```

Provide feedback

---

LoadAssetAsync

Yields

Loads a [Model](/docs/reference/engine/classes/Model) instance given its asset ID. This is the modern
replacement for [InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) and supports loading
third-party assets.

AssetService:LoadAssetAsync(assetId:[number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| assetId:[number](/docs/luau/numbers)  The asset ID number of the asset being loaded. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

A [Model](/docs/reference/engine/classes/Model) instance containing the loaded asset.

Loads the latest version of an asset from the given assetId and returns
it wrapped in a [Model](/docs/reference/engine/classes/Model). This method is the modern replacement for
[InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) and
[InsertService:LoadAssetVersion()](/docs/reference/engine/classes/InsertService#LoadAssetVersion) methods.

Calls to this function may fail if the asset does not exist, or if the
server providing the model is having problems. It is recommended to wrap
calls to this function in pcall() to handle potential errors.

```
local AssetService = game:GetService("AssetService")



local assetId = 257489726



local success, model = pcall(AssetService.LoadAssetAsync, AssetService, assetId)



if success and model then



print("Model loaded successfully")



model.Parent = workspace



else



warn("Model failed to load:", model) -- 'model' will contain the error message



end
```

#### Script Sandbox Security

For enhanced security, the returned [Model](/docs/reference/engine/classes/Model) is sandboxed by default
([Sandboxed](/docs/reference/engine/classes/Model#Sandboxed) is true) and has no script
[Capabilities](/docs/reference/engine/enums/SecurityCapability). This prevents untrusted scripts
descending from the returned Model from running. To enable scripts in a
model you trust, you can manually grant a safe set of
[Capabilities](/docs/reference/engine/enums/SecurityCapability) on the Model after loading.

#### Third-Party Asset Loading

Unlike [InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset), this method can load public
assets created by third parties (assets not owned by the experience
creator). To enable this functionality, you must first enable the Allow
Loading Third Party Assets setting in Home > Game Settings >
Security.

If this setting is disabled (which it is by default), LoadAssetAsync
will only load assets that are owned by the experience creator, behaving
identically to the old [InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) security check.

Provide feedback

---

PromptCreateAssetAsync

Yields

Allows in-experience asset creation for users by prompting a publish
dialog.

AssetService:PromptCreateAssetAsync(

player:[Player](/docs/reference/engine/classes/Player), instance:[Instance](/docs/reference/engine/datatypes/Instance), assetType:[Enum.AssetType](/docs/reference/engine/enums/AssetType)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The user who submits an asset creation. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The asset to be created. Currently can't contain scripts or nest non-public assets. |
| assetType:[Enum.AssetType](/docs/reference/engine/enums/AssetType)  The asset type. Currently can only be [Enum.AssetType.Model](/docs/reference/engine/enums/AssetType#Model). |

Returns

[Tuple](/docs/luau/tuples)

The [Enum.PromptCreateAssetResult](/docs/reference/engine/enums/PromptCreateAssetResult) and asset ID pair if successful.

Allows in-experience asset creation for users by prompting a publish
dialog. When called, it presents a dialog to the user, allowing them to
enter a name, description, and preview the asset. Upon submitting, it
saves the asset to the user's inventory. Can only be invoked on the server
side.

Provide feedback

---

PromptImportAnimationClipFromVideoAsync

Yields

AssetService:PromptImportAnimationClipFromVideoAsync(

player:[Player](/docs/reference/engine/classes/Player), progressCallback:[function](/docs/luau/functions)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |
| progressCallback:[function](/docs/luau/functions) |

Returns

[Tuple](/docs/luau/tuples)

Provide feedback

---

SavePlaceAsync

Yields

Saves the state of the current place.

AssetService:SavePlaceAsync(requestParameters:[Dictionary](/docs/luau/tables#dictionaries)?):()

Parameters

|  |
| --- |
| requestParameters:[Dictionary](/docs/luau/tables#dictionaries)?  Optional dictionary that includes SaveWithoutPublish, a boolean indicating whether to save with publish or without publish, and PlaceId, the destination place ID to save over. An example usage would be: AssetService:SavePlaceAsync({PlaceId = 1, SaveWithoutPublish = true}). If PlaceId is not provided, the default behavior will save over the current original place which is calling SavePlaceAsync. If SaveWithoutPublish is not provided, the default behavior is SaveWithoutPublish=false. |

Returns

()

Saves the current state of the place. Keep in mind the following
guidelines and restrictions:

* This method only works for places that are created with
  [AssetService:CreatePlaceAsync()](/docs/reference/engine/classes/AssetService#CreatePlaceAsync) or that have the API enabled
  through the place's settings.
* This method overwrites the previous state of the place. To revert a
  save, publish an older version of the place.
* There are cases when saves can occur simultaneously in Studio and in
  multiple experience servers. The order of the saves happen in the order
  they are called.
* An active Team Create session in Studio blocks all saves from occurring.

Provide feedback

---

SearchAudioAsync

Yields

Finds audio assets matching a variety of search criteria.

AssetService:SearchAudioAsync(searchParameters:[AudioSearchParams](/docs/reference/engine/classes/AudioSearchParams)):[AudioPages](/docs/reference/engine/classes/AudioPages)

Parameters

|  |
| --- |
| searchParameters:[AudioSearchParams](/docs/reference/engine/classes/AudioSearchParams) |

Returns

[AudioPages](/docs/reference/engine/classes/AudioPages)

Returns a [AudioPages](/docs/reference/engine/classes/AudioPages) object containing the result of the given
search. Will not return fields with empty values.

Note that this method has a low HTTP request limit and can throw an error,
so it should always be wrapped in pcall() for error handling. Possible
error messages include:

| Error Message | Reason |
| --- | --- |
| HTTP 429 (Too Many Requests) | [AssetService:SearchAudio()](/docs/reference/engine/classes/AssetService#SearchAudio) has been called too many times. |
| Unexpected type for data, expected array got null | The keyword argument was filtered. |

Code Samples

Getting Music Search Titles

This code gets the music assets returned by the keyword "happy" and prints out their titles.

```
local AssetService = game:GetService("AssetService")



local audioSearchParams = Instance.new("AudioSearchParams")



audioSearchParams.SearchKeyword = "happy"



local success, result = pcall(function()



return AssetService:SearchAudio(audioSearchParams)



end)



if success then



local currentPage = result:GetCurrentPage()



for _, audio in currentPage do



print(audio.Title)



end



else



warn("AssetService error: " .. result)



end



--[[ Returned data format



{



"AudioType": string,



"Artist": string,



"Title": string,



"Tags": {



"string"



},



"Id": number,



"IsEndorsed": boolean,



"Description": string,



"Duration": number,



"CreateTime": string,



"UpdateTime": string,



"Creator": {



"Id": number,



"Name": string,



"Type": number,



"IsVerifiedCreator": boolean



}



}



--]]
```

Provide feedback

---

SearchAudio

Deprecated

Show details

---