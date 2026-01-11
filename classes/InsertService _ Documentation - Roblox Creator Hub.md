# InsertService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/InsertService
Scraped: 2026-01-11T02:32:25.161405Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- InsertService
- MeshPart
- LoadAsset
- LoadAsset()
- HttpService:GetSecret()
- AssetService
- MeshPart.CollisionFidelity
- MeshPart.RenderFidelity
- CollisionFidelity
- RenderFidelity
- MeshPart.MeshId
- Decals
- Models
- InsertService:GetFreeModels()
- InsertService:GetFreeDecals()
- InsertService:LoadAssetVersion()
- Model
- AssetService:LoadAssetAsync()
- AssetService.AllowInsertFreeAssets
- AssetService:GetBundleDetailsAsync()
- DataModel:GetObjects()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [InsertService](/docs/reference/engine/classes/InsertService)

English

Feedback

Engine Class

InsertService

Used to insert assets from the Roblox website.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [AllowClientInsertModels](#AllowClientInsertModels):[boolean](/docs/luau/booleans) |
| [AllowInsertFreeModels](#AllowInsertFreeModels):[boolean](/docs/luau/booleans)  Deprecated |

Methods

|  |
| --- |
| [ApproveAssetId](#ApproveAssetId)(assetId: [number](/docs/luau/numbers)):()  Deprecated |
| [ApproveAssetVersionId](#ApproveAssetVersionId)(assetVersionId: [number](/docs/luau/numbers)):()  Deprecated |
| [CreateMeshPartAsync](#CreateMeshPartAsync)(meshId: ContentId,collisionFidelity: [Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity),renderFidelity: [Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)):[MeshPart](/docs/reference/engine/classes/MeshPart) |
| [GetBaseCategories](#GetBaseCategories)():[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetBaseSets](#GetBaseSets)():[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetCollection](#GetCollection)(categoryId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetFreeDecalsAsync](#GetFreeDecalsAsync)(searchText: [string](/docs/luau/strings),pageNum: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFreeDecals](#GetFreeDecals)(searchText: [string](/docs/luau/strings),pageNum: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetFreeModelsAsync](#GetFreeModelsAsync)(searchText: [string](/docs/luau/strings),pageNum: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFreeModels](#GetFreeModels)(searchText: [string](/docs/luau/strings),pageNum: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetLatestAssetVersionAsync](#GetLatestAssetVersionAsync)(assetId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [GetUserCategories](#GetUserCategories)(userId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetUserSets](#GetUserSets)(userId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [Insert](#Insert)(instance: [Instance](/docs/reference/engine/datatypes/Instance)):()  Deprecated |
| [LoadAsset](#LoadAsset)(assetId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [loadAsset](#loadAsset)(assetId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [LoadAssetVersion](#LoadAssetVersion)(assetVersionId: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

InsertService is used to insert assets from the Roblox website, typically the
[LoadAsset](/docs/reference/engine/classes/InsertService#LoadAsset) function.

To load an asset, it must be accessible by the creator of the experience
loading it, which can be either a user or group. Should an experience be
uploaded by a different creator, the asset data would not be accessible. See
the [LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) method for more details on
this security check. Note that you should not use this service for loading
API keys or other secrets. Use [HttpService:GetSecret()](/docs/reference/engine/classes/HttpService#GetSecret) instead.

#### See Also

* [AssetService](/docs/reference/engine/classes/AssetService), which can provide information about assets you might
  want to load using InsertService

---

API Reference

Properties

AllowClientInsertModels

Not Scriptable

Read Parallel

InsertService.AllowClientInsertModels:[boolean](/docs/luau/booleans)

Provide feedback

---

AllowInsertFreeModels

Deprecated

Show details

---

Methods

ApproveAssetId

Deprecated

Show details

---

ApproveAssetVersionId

Deprecated

Show details

---

CreateMeshPartAsync

Yields

Creates a new [MeshPart](/docs/reference/engine/classes/MeshPart) with specified fidelity values.

InsertService:CreateMeshPartAsync(

meshId:ContentId, collisionFidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity), renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)

):[MeshPart](/docs/reference/engine/classes/MeshPart)

Parameters

|  |
| --- |
| meshId:ContentId  Mesh asset ID. |
| collisionFidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity)  Set [MeshPart.CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity). |
| renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)  Set [MeshPart.RenderFidelity](/docs/reference/engine/classes/MeshPart#RenderFidelity). |

Returns

[MeshPart](/docs/reference/engine/classes/MeshPart)

New [MeshPart](/docs/reference/engine/classes/MeshPart) instance.

Creates a new [MeshPart](/docs/reference/engine/classes/MeshPart) with specified
[CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity) and
[RenderFidelity](/docs/reference/engine/classes/MeshPart#RenderFidelity). Because
[MeshPart.MeshId](/docs/reference/engine/classes/MeshPart#MeshId) is read only, this is the way to create a
[MeshPart](/docs/reference/engine/classes/MeshPart) through scripts without having to clone an existing one.
It throws errors if creation fails.

Provide feedback

---

GetBaseCategories

Deprecated

Show details

---

GetBaseSets

Deprecated

Show details

---

GetCollection

Deprecated

Show details

---

GetFreeDecalsAsync

Yields

Retrieves a list of free Decals from the Catalog.

InsertService:GetFreeDecalsAsync(

searchText:[string](/docs/luau/strings), pageNum:[number](/docs/luau/numbers)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| searchText:[string](/docs/luau/strings)  String used to search for free decals in the Catalog. |
| pageNum:[number](/docs/luau/numbers)  The page number in the Catalog to return. |

Returns

[Array](/docs/luau/tables#arrays)

A single table (of returned free decals) wrapped in a table.

The GetFreeDecals function retrieves a list of free [Decals](/docs/reference/engine/classes/Decal)
from the Catalog. The return type for this method is very odd, as it
returns a single table wrapped in a table.

The best way to explain it is to show a visual of the array returned:

```
[1] = {



CurrentStartIndex = 1, -- This can vary depending on the page you input.



TotalCount = 21, -- Always 21.



Results = {



-- All parameters here are pseudo. They can vary depending on the asset.



[1] = {



Name = "Asset Name",



AssetId = 0000000,



AssetVersionId = 0000000,



CreatorName = "Roblox",



},



-- [2], [3], and so on... up to [21]



},



}
```

An example for iterating over this list has been provided at the bottom of
this page.

Additionally, if you want to insert [Models](/docs/reference/engine/classes/Model) instead, you can
use the [InsertService:GetFreeModels()](/docs/reference/engine/classes/InsertService#GetFreeModels) function.

*Note:* The page argument starts at 0. So Page 1 = 0, Page 2 = 1, etc.

Code Samples

InsertService:GetFreeDecals

```
local InsertService = game:GetService("InsertService")



local page = unpack(InsertService:GetFreeDecals("Cats", 0)) -- Search for "Cats" on Page 1.



for i = 1, page.TotalCount do



local item = page.Results[i]



print("Item #" .. i)



for key, value in pairs(item) do



print(" " .. key .. ": " .. value)



end



end
```

Provide feedback

---

GetFreeDecals

Deprecated

Show details

---

GetFreeModelsAsync

Yields

Retrieves a list of Free Models from the Catalog.

InsertService:GetFreeModelsAsync(

searchText:[string](/docs/luau/strings), pageNum:[number](/docs/luau/numbers)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| searchText:[string](/docs/luau/strings)  String used to search for free decals in the Catalog. |
| pageNum:[number](/docs/luau/numbers)  The page number in the Catalog to return. |

Returns

[Array](/docs/luau/tables#arrays)

A single table (of returned free models) wrapped in a table.

The GetFreeModels function retrieves a list of Free [Models](/docs/reference/engine/classes/Model)
from the Catalog. The return type for this method is very odd, as it
returns a single table wrapped in a table.

The best way to explain it is to show a visual of the array returned:

```
[1] = {



CurrentStartIndex = 1, -- This can vary depending on the page you input.



TotalCount = 21, -- Always 21.



Results = {



-- All parameters here are pseudo. They can vary depending on the asset.



[1] = {



Name = "Asset Name",



AssetId = 0000000,



AssetVersionId = 0000000,



CreatorName = "Roblox",



}



-- [2], [3], and so on... up to [21]



}



}
```

An example for iterating over this list has been provided at the bottom of
this page.

Additionally, if you would like to insert free [Decals](/docs/reference/engine/classes/Decal), you
can use the [InsertService:GetFreeDecals()](/docs/reference/engine/classes/InsertService#GetFreeDecals) function.

Code Samples

InsertService:GetFreeModels

```
local InsertService = game:GetService("InsertService")



local page = unpack(InsertService:GetFreeModels("Cats", 0)) -- Search for "Cats" on Page 1.



for i = 1, page.TotalCount do



local item = page.Results[i]



print("Item #" .. i)



for key, value in pairs(item) do



print(" " .. key .. ": " .. value)



end



end
```

Provide feedback

---

GetFreeModels

Deprecated

Show details

---

GetLatestAssetVersionAsync

Yields

Returns the latest AssetVersionId of an asset for assets created by the
place creator. Can be used in combination with
[InsertService:LoadAssetVersion()](/docs/reference/engine/classes/InsertService#LoadAssetVersion) to load the latest version of a
model, even if it gets updated while the game is running.

InsertService:GetLatestAssetVersionAsync(assetId:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| assetId:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the latest AssetVersionId of an asset for assets created by the
place creator. Can be used in combination with
[InsertService:LoadAssetVersion()](/docs/reference/engine/classes/InsertService#LoadAssetVersion) to load the latest version of a
model, even if it gets updated while the game is running.

Provide feedback

---

GetUserCategories

Deprecated

Show details

---

GetUserSets

Deprecated

Show details

---

Insert

Deprecated

Show details

---

LoadAsset

Yields

Returns a [Model](/docs/reference/engine/classes/Model) containing the asset.

InsertService:LoadAsset(assetId:[number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| assetId:[number](/docs/luau/numbers)  The asset ID of the asset being loaded. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

An instance of the loaded asset.

The LoadAsset function fetches an asset given its ID and returns a
[Model](/docs/reference/engine/classes/Model) containing the asset. For example, to load this public
[Doge](https://www.roblox.com/library/257489726/Doge) [Model](/docs/reference/engine/classes/Model), which
has the asset ID *257489726*, you can use:

```
local InsertService = game:GetService("InsertService")



local Workspace = game:GetService("Workspace")



local assetId = 257489726



local model = InsertService:LoadAsset(assetId)



model.Parent = Workspace
```

Calls to this function may fail if a server providing a model is having
problems. As such, it's generally a good idea to wrap calls to this
function in pcall to catch these kinds of errors.

```
local InsertService = game:GetService("InsertService")



local Workspace = game:GetService("Workspace")



local assetId = 257489726



local success, model = pcall(InsertService.LoadAsset, InsertService, assetId)



if success and model then



print("Model loaded successfully")



model.Parent = Workspace



else



print("Model failed to load!")



end
```

#### Security Check

An asset loaded by this function must meet one of the following:

* The asset must be created or owned by the game creator.
* The asset must be shared by the asset owner.
* The asset must be owned by Roblox.

Additionally, benign asset types such as t-shirts, shirts, pants and
avatar accessories are loadable from any game as they are OpenUse.

To load assets which do not meet the above criteria, such as free Models
published on the Store, you must use [AssetService:LoadAssetAsync()](/docs/reference/engine/classes/AssetService#LoadAssetAsync)
and enable [AssetService.AllowInsertFreeAssets](/docs/reference/engine/classes/AssetService#AllowInsertFreeAssets).

See also:

* [AssetService:GetBundleDetailsAsync()](/docs/reference/engine/classes/AssetService#GetBundleDetailsAsync), to find out which assets
  are associated with a bundle.
* For plugins, see [DataModel:GetObjects()](/docs/reference/engine/classes/DataModel#GetObjects)

Code Samples

InsertService:LoadAsset

```
local InsertService = game:GetService("InsertService")



local ASSET_ID = 82353



local asset = InsertService:LoadAsset(ASSET_ID)



asset.Parent = workspace
```

Provide feedback

---

loadAsset

Deprecated

Show details

---

LoadAssetVersion

Yields

Returns a model inserted into [InsertService](/docs/reference/engine/classes/InsertService) containing the asset
with the given assetVersionId.

InsertService:LoadAssetVersion(assetVersionId:[number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| assetVersionId:[number](/docs/luau/numbers) |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Returns a model inserted into [InsertService](/docs/reference/engine/classes/InsertService) containing the asset
with the given assetVersionId.

Code Samples

InsertService:LoadAssetVersion

```
local InsertService = game:GetService("InsertService")



local ASSET_VERSION_ID = 296050499



local asset = InsertService:LoadAssetVersion(ASSET_VERSION_ID)



asset.Parent = game.Workspace
```

Provide feedback

---