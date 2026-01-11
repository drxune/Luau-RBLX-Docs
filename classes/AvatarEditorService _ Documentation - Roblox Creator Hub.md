# AvatarEditorService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AvatarEditorService
Scraped: 2026-01-11T02:30:59.997616Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- AvatarEditorService
- HumanoidDescription
- InventoryPages
- OutfitPages
- CatalogPages
- Object
- AvatarEditorService.GetItemDetails
- AvatarEditorService.GetBatchItemDetails
- AvatarEditorService.GetRecommendedAssets
- AvatarEditorService.GetRecommendedBundles
- AvatarEditorService.SearchCatalog
- AvatarEditorService.PromptSetFavorite
- AvatarEditorService.GetFavorite
- Players.LocalPlayer
- Players:GetHumanoidDescriptionFromOutfitId()
- AvatarEditorService:PromptAllowInventoryReadAccess()
- AvatarEditorService:GetInventory()
- AvatarEditorService:GetOutfits()
- AvatarEditorService:GetFavorite()
- AvatarEditorService.PromptCreateOutfitCompleted
- AvatarEditorService.PromptDeleteOutfitCompleted
- AvatarEditorService.PromptRenameOutfitCompleted
- AvatarEditorService:PromptSaveAvatar()
- AvatarEditorService:PromptSetFavorite()
- AvatarEditorService:PromptUpdateOutfit()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AvatarEditorService](/docs/reference/engine/classes/AvatarEditorService)

English

Feedback

Engine Class

![AvatarEditorService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AvatarEditorService-Dark.webp)AvatarEditorService

A service to support developer Avatar Editors.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [CheckApplyDefaultClothingAsync](#CheckApplyDefaultClothingAsync)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |
| [CheckApplyDefaultClothing](#CheckApplyDefaultClothing)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  Deprecated |
| [ConformToAvatarRulesAsync](#ConformToAvatarRulesAsync)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |
| [ConformToAvatarRules](#ConformToAvatarRules)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  Deprecated |
| [GetAccessoryType](#GetAccessoryType)(avatarAssetType: [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)):[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType) |
| [GetAvatarRulesAsync](#GetAvatarRulesAsync)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetAvatarRules](#GetAvatarRules)():[Dictionary](/docs/luau/tables#dictionaries)  Deprecated |
| [GetBatchItemDetailsAsync](#GetBatchItemDetailsAsync)(itemIds: [Array](/docs/luau/tables#arrays),itemType: [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)):[Array](/docs/luau/tables#arrays) |
| [GetBatchItemDetails](#GetBatchItemDetails)(itemIds: [Array](/docs/luau/tables#arrays),itemType: [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetFavoriteAsync](#GetFavoriteAsync)(itemId: [number](/docs/luau/numbers),itemType: [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)):[boolean](/docs/luau/booleans) |
| [GetFavorite](#GetFavorite)(itemId: [number](/docs/luau/numbers),itemType: [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)):[boolean](/docs/luau/booleans)  Deprecated |
| [GetInventoryAsync](#GetInventoryAsync)(assetTypes: [Array](/docs/luau/tables#arrays)):[InventoryPages](/docs/reference/engine/classes/InventoryPages) |
| [GetInventory](#GetInventory)(assetTypes: [Array](/docs/luau/tables#arrays)):[InventoryPages](/docs/reference/engine/classes/InventoryPages)  Deprecated |
| [GetItemDetailsAsync](#GetItemDetailsAsync)(itemId: [number](/docs/luau/numbers),itemType: [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetItemDetails](#GetItemDetails)(itemId: [number](/docs/luau/numbers),itemType: [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)):[Dictionary](/docs/luau/tables#dictionaries)  Deprecated |
| [GetOutfitDetailsAsync](#GetOutfitDetailsAsync)(outfitId: [number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetOutfitDetails](#GetOutfitDetails)(outfitId: [number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries)  Deprecated |
| [GetOutfitsAsync](#GetOutfitsAsync)(outfitSource: [Enum.OutfitSource](/docs/reference/engine/enums/OutfitSource),outfitType: [Enum.OutfitType](/docs/reference/engine/enums/OutfitType)):[OutfitPages](/docs/reference/engine/classes/OutfitPages) |
| [GetOutfits](#GetOutfits)(outfitSource: [Enum.OutfitSource](/docs/reference/engine/enums/OutfitSource),outfitType: [Enum.OutfitType](/docs/reference/engine/enums/OutfitType)):[OutfitPages](/docs/reference/engine/classes/OutfitPages)  Deprecated |
| [GetRecommendedAssetsAsync](#GetRecommendedAssetsAsync)(assetType: [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType),contextAssetId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetRecommendedAssets](#GetRecommendedAssets)(assetType: [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType),contextAssetId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetRecommendedBundlesAsync](#GetRecommendedBundlesAsync)(bundleId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetRecommendedBundles](#GetRecommendedBundles)(bundleId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [PromptAllowInventoryReadAccess](#PromptAllowInventoryReadAccess)():() |
| [PromptCreateOutfit](#PromptCreateOutfit)(outfit: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),rigType: [Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)):() |
| [PromptDeleteOutfit](#PromptDeleteOutfit)(outfitId: [number](/docs/luau/numbers)):() |
| [PromptRenameOutfit](#PromptRenameOutfit)(outfitId: [number](/docs/luau/numbers)):() |
| [PromptSaveAvatar](#PromptSaveAvatar)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),rigType: [Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)):() |
| [PromptSetFavorite](#PromptSetFavorite)(itemId: [number](/docs/luau/numbers),itemType: [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType),shouldFavorite: [boolean](/docs/luau/booleans)):() |
| [PromptUpdateOutfit](#PromptUpdateOutfit)(outfitId: [number](/docs/luau/numbers),updatedOutfit: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),rigType: [Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)):() |
| [SearchCatalogAsync](#SearchCatalogAsync)(searchParameters: [CatalogSearchParams](/docs/reference/engine/datatypes/CatalogSearchParams)):[CatalogPages](/docs/reference/engine/classes/CatalogPages) |
| [SearchCatalog](#SearchCatalog)(searchParameters: [CatalogSearchParams](/docs/reference/engine/datatypes/CatalogSearchParams)):[CatalogPages](/docs/reference/engine/classes/CatalogPages)  Deprecated |

Events

|  |
| --- |
| [PromptAllowInventoryReadAccessCompleted](#PromptAllowInventoryReadAccessCompleted)(result: [Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptCreateOutfitCompleted](#PromptCreateOutfitCompleted)(result: [Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult),failureType: Variant):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptDeleteOutfitCompleted](#PromptDeleteOutfitCompleted)(result: [Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptRenameOutfitCompleted](#PromptRenameOutfitCompleted)(result: [Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptSaveAvatarCompleted](#PromptSaveAvatarCompleted)(result: [Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult),humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptSetFavoriteCompleted](#PromptSetFavoriteCompleted)(result: [Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptUpdateOutfitCompleted](#PromptUpdateOutfitCompleted)(result: [Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

AvatarEditorService is a service to support developer Avatar Editors. It
provides methods to modify the player's platform avatar, request information
about a user's inventory, and request information about the catalog.

For more information regarding the Avatar Editor, see
[Avatar Editor Service](/docs/players/avatar-editor).

#### Throttling

The following endpoints on AvatarEditorService have experience-level
throttling:

* [AvatarEditorService.GetItemDetails](/docs/reference/engine/classes/AvatarEditorService#GetItemDetails)
* [AvatarEditorService.GetBatchItemDetails](/docs/reference/engine/classes/AvatarEditorService#GetBatchItemDetails)
* [AvatarEditorService.GetRecommendedAssets](/docs/reference/engine/classes/AvatarEditorService#GetRecommendedAssets)
* [AvatarEditorService.GetRecommendedBundles](/docs/reference/engine/classes/AvatarEditorService#GetRecommendedBundles)
* [AvatarEditorService.SearchCatalog](/docs/reference/engine/classes/AvatarEditorService#SearchCatalog)
* [AvatarEditorService.PromptSetFavorite](/docs/reference/engine/classes/AvatarEditorService#PromptSetFavorite)
* [AvatarEditorService.GetFavorite](/docs/reference/engine/classes/AvatarEditorService#GetFavorite)

For each experience, this throttling allows you to send up to 100 requests per
second to these AvatarEditorService endpoints, regardless of the number of
servers or user count. Exceeding these limits returns a
429 Too Many Requests error.

---

API Reference

Methods

CheckApplyDefaultClothingAsync

Yields

Used to apply default clothing to the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) if
necessary.

AvatarEditorService:CheckApplyDefaultClothingAsync(humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Parameters

|  |
| --- |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  The HumanoidDescription to check if default clothing is required. |

Returns

[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Returns a HumanoidDescription if default clothing was necessary.
Otherwise returns nil.

Returns a new [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) with the Shirt and Pants
properties updated if necessary. Returns nil if default clothing was not
needed.

Default clothing is necessary if the HumanoidDescription does not
currently have Shirt and Pants equipped and the body colors are too
similar.

Provide feedback

---

CheckApplyDefaultClothing

Deprecated

Show details

---

ConformToAvatarRulesAsync

Yields

AvatarEditorService:ConformToAvatarRulesAsync(humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Parameters

|  |
| --- |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |

Returns

[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Provide feedback

---

ConformToAvatarRules

Deprecated

Show details

---

GetAccessoryType

AvatarEditorService:GetAccessoryType(avatarAssetType:[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)):[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType)

Parameters

|  |
| --- |
| avatarAssetType:[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType) |

Returns

[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType)

Provide feedback

---

GetAvatarRulesAsync

Yields

Returns the platform Avatar rules for things such as scaling, default
shirts and pants, number of wearable assets.

AvatarEditorService:GetAvatarRulesAsync():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary containing the platform Avatar rules for things like
scaling, default shirts and pants, number of wearable assets, ect. See
the example return in the main description above.

This function returns the platform Avatar rules for things like scaling,
default shirts and pants, number of wearable assets, ect.

The returned table includes the following fields:

```
{



"PlayerAvatarTypes": [



"R6"



],



"Scales": {},



"WearableAssetTypes": [



{



"MaxNumber": 0,



"Id": 0,



"Name": "string"



}



],



"BodyColorsPalette": [



{



"BrickColorId": 0,



"NexColor": "string",



"Name": "string"



}



],



"BasicBodyColorsPalette": [



{



"BrickColorId": 0,



"HexColor": "string",



"Name": "string"



}



],



"MinimumDeltaEBodyColorDifference": 0,



"ProportionsAndBodyTypeEnabledForUser": true,



"DefaultClothingAssetLists": {



"DefaultShirtAssetIds": [



0



],



"DefaultPantAssetIds": [



0



]



},



"BundlesEnabledForUser": true,



"EmotesEnabledForUser": true



}
```

Provide feedback

---

GetAvatarRules

Deprecated

Show details

---

GetBatchItemDetailsAsync

Yields

Gets the item details for a list of items at once.

AvatarEditorService:GetBatchItemDetailsAsync(

itemIds:[Array](/docs/luau/tables#arrays), itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| itemIds:[Array](/docs/luau/tables#arrays)  The list of item ids to get details of. |
| itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)  The type of the item ids provided. |

Returns

[Array](/docs/luau/tables#arrays)

Returns an array of item details with the following fields:

```
{



"AssetType" = "string",



"CreatorName" = "string",



"CreatorTargetId" = 0,



"CreatorType" = "string",



"Description" = "string",



"FavoriteCount" = 0,



"Genres" = [



"All"



],



"Id" = 0,



"ItemRestrictions" = [



"Limited"



],



"ItemStatus": [



"New"



],



"ItemType" = "string",



"LowestPrice" = 0,



"Name" = "string",



"Price" = 0,



"ProductId" = 0



}
```

.

Gets the item details for a list of items at once. More efficient than
AvatarEditorService:GetItemDetails if you need to get all the item details
of a list.

Provide feedback

---

GetBatchItemDetails

Deprecated

Show details

---

GetFavoriteAsync

Yields

Returns if the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) has favorited the given bundle
or asset.

AvatarEditorService:GetFavoriteAsync(

itemId:[number](/docs/luau/numbers), itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| itemId:[number](/docs/luau/numbers)  The ID of the specified asset or bundle. |
| itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)  The [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType) of the specified asset or bundle. |

Returns

[boolean](/docs/luau/booleans)

Whether the LocalPlayer has favorited the given bundle or asset.

This function returns if the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) has favorited the
given bundle or asset.

Provide feedback

---

GetFavorite

Deprecated

Show details

---

GetInventoryAsync

Yields

Returns an [InventoryPages](/docs/reference/engine/classes/InventoryPages) object with information about owned
items in the users inventory with the given AvatarAssetTypes.

AvatarEditorService:GetInventoryAsync(assetTypes:[Array](/docs/luau/tables#arrays)):[InventoryPages](/docs/reference/engine/classes/InventoryPages)

Parameters

|  |
| --- |
| assetTypes:[Array](/docs/luau/tables#arrays)  The [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType) that can will be checked for in the player's inventory. |

Returns

[InventoryPages](/docs/reference/engine/classes/InventoryPages)

Returns an [InventoryPages](/docs/reference/engine/classes/InventoryPages) object with information about owned
items in the users inventory with the given
[AvatarAssetTypes](/docs/reference/engine/enums/AvatarAssetType).

The returned table includes the following fields:

```
[



{



"AssetId": 0,



"AssetType" : "string",



"Created": "string",



"Name": "string",



}



]
```

Provide feedback

---

GetInventory

Deprecated

Show details

---

GetItemDetailsAsync

Yields

Returns the item details for the given item.

AvatarEditorService:GetItemDetailsAsync(

itemId:[number](/docs/luau/numbers), itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)

):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| itemId:[number](/docs/luau/numbers)  The ID of the item whose details are being retrieved. |
| itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)  An enum value indicating the type of item whose details are being retrieved. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A table containing the item info for the retrieved item. See above for
a sample table.

This function returns the item details for the given item. It accepts two
parameters - the first indicating the ID of the item being retrieved and
the second indicating its [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType).

Data returned in the format:

```
{



"IsForRent": true,



"ExpectedSellerId": 0,



"Owned": true,



"IsPurchasable": true,



"Id": 0,



"ItemType": "Asset",



"AssetType": "Image",



"BundleType": "BodyParts",



"Name": "string",



"Description": "string",



"ProductId": 0,



"Genres": [



"All"



],



"BundledItems": [



{



"Owned": true,



"Id": 0,



"Name": "string",



"Type": "string"



}



],



"ItemStatus": [



"New"



],



"ItemRestrictions": [



"ThirteenPlus"



],



"CreatorType": "User",



"CreatorTargetId": 0,



"CreatorName": "string",



"Price": 0,



"PremiumPricing": {



"PremiumDiscountPercentage": 0,



"PremiumPriceInRobux": 0



},



"LowestPrice": 0,



"PriceStatus": "string",



"UnitsAvailableForConsumption": 0,



"PurchaseCount": 0,



"FavoriteCount": 0



}
```

To query for limited or unlimited assets, use the following
itemRestrictions values:

| itemRestrictions | Limited or Unlimited |
| --- | --- |
| empty | Unlimited |
| Collectible | UGC Limited |
| Limited | Roblox Limited |
| LimitedUnique | Roblox Limited Unique |

Provide feedback

---

GetItemDetails

Deprecated

Show details

---

GetOutfitDetailsAsync

Yields

Returns the outfit details for the given outfit.

AvatarEditorService:GetOutfitDetailsAsync(outfitId:[number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| outfitId:[number](/docs/luau/numbers)  The ID of the outfit whose details are being retrieved. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A table containing the outfit info for the retrieved outfit. See above
for a sample table.

This function returns the outfit details for the given outfit. It accepts
one parameter: the ID of the outfit.

Data returns in the following format:

```
{



"Assets": [



{



"AssetType": {



"Id": 31,



"Name": "RightLeg"



}



"CurrentVersionId": 16447385805,



"Id": 11584239464,



"Name": "Anime Female - Right Leg"



}



],



"BodyColors": {



"HeadColor": Color3(204, 142, 105),



"LeftArmColor": Color3(204, 142, 105),



"LeftLegColor": Color3(204, 142, 105),



"RightArmColor": Color3(204, 142, 105),



"RightLegColor": Color3(204, 142, 105),



"TorsoColor": Color3(204, 142, 105)



},



"Id": 14703770624,



"IsEditable": true,



"Name": "Your Costume",



"OutfitType": "Avatar",



"PlayerAvatarType": "R15",



"Scale": {



"BodyType": 0,



"Depth": 1,



"Head": 1,



"Height": 1,



"Proportion": 0,



"Width": 1



},



}
```

Provide feedback

---

GetOutfitDetails

Deprecated

Show details

---

GetOutfitsAsync

Yields

Returns outfit data for the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer).

AvatarEditorService:GetOutfitsAsync(

outfitSource:[Enum.OutfitSource](/docs/reference/engine/enums/OutfitSource), outfitType:[Enum.OutfitType](/docs/reference/engine/enums/OutfitType)

):[OutfitPages](/docs/reference/engine/classes/OutfitPages)

Parameters

|  |
| --- |
| outfitSource:[Enum.OutfitSource](/docs/reference/engine/enums/OutfitSource) Default Value: "All" |
| outfitType:[Enum.OutfitType](/docs/reference/engine/enums/OutfitType) Default Value: "All" |

Returns

[OutfitPages](/docs/reference/engine/classes/OutfitPages)

This function returns outfit data for the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer).
This would be used with
[Players:GetHumanoidDescriptionFromOutfitId()](/docs/reference/engine/classes/Players#GetHumanoidDescriptionFromOutfitId) to update the players
character to the outfit. Access to this would also depend on
[AvatarEditorService:PromptAllowInventoryReadAccess()](/docs/reference/engine/classes/AvatarEditorService#PromptAllowInventoryReadAccess) being
accepted by the user.

The returned table includes the following fields:

```
[



{



"Id": 0,



"Name": "string",



"IsEditable": true



}



]
```

| Name | type | Description |
| --- | --- | --- |
| id | int |  |
| name | string |  |
| isEditable | boolean |  |

Provide feedback

---

GetOutfits

Deprecated

Show details

---

GetRecommendedAssetsAsync

Yields

Returns a list of recommended assets based on a given [Enum.AssetType](/docs/reference/engine/enums/AssetType) and
asset ID.

AvatarEditorService:GetRecommendedAssetsAsync(

assetType:[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType), contextAssetId:[number](/docs/luau/numbers)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| assetType:[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)  The type of asset recommendations to retrieve recommendations for. Only affects the response when item based recommendations don't exist for the given contextAssetId. |
| contextAssetId:[number](/docs/luau/numbers) Default Value: 0 The ID of an asset with a type matching the provided assetType used for context when retrieving recommendations. |

Returns

[Array](/docs/luau/tables#arrays)

A list of recommendations based on the given [Enum.AssetType](/docs/reference/engine/enums/AssetType).

Returns a list of recommended assets based on a given [Enum.AssetType](/docs/reference/engine/enums/AssetType) and
asset ID. Use this to gather a list of similar assets to the asset
provided. Take a look at the code sample below for more information on
possible usages for this function.

Data is in the format:

```
[



{



"Item": {



"AssetId": 0,



"Name": "string",



"Price": 0,



"PremiumPrice": 0,



},



"Creator": {



"CreatorId": 0,



"CreatorType": "string",



"Name": "string",



},



"Product": {



"Id": 0,



"PriceInRobux": 0,



"IsForSale": true,



"IsResellable": true,



"IsLimited": true,



"IsLimitedUnique": true,



"TotalPrivateSales": 0,



"OffsaleDeadline": "string",



"IsFree": true



}



}



]
```

Code Samples

Getting a Hat Recommendation

This will return a list of similar hats much like how similar assets are
displayed when viewing the catalog page on the website. The contextAssetId is
optional and if not provided it will return some popular items from that
category.

```
local AvatarEditorService = game:GetService("AvatarEditorService")



local assets = AvatarEditorService:GetRecommendedAssets(Enum.AvatarAssetType.Hat, 9255093)



for _, asset in ipairs(assets) do



print(asset.Item.Name)



end
```

Provide feedback

---

GetRecommendedAssets

Deprecated

Show details

---

GetRecommendedBundlesAsync

Yields

Returns a list of recommended bundles for a given bundle id.

AvatarEditorService:GetRecommendedBundlesAsync(bundleId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| bundleId:[number](/docs/luau/numbers)  A list of recommended bundles. |

Returns

[Array](/docs/luau/tables#arrays)

The bundle ID that the recommended bundles will be returned for.

This function returns a list of recommended bundles for a given bundle id.

Data is in the format:

```
[



{



"Id": 0,



"Name": "string",



"Description": "string",



"BundleType": "string",



"Items": [



{



"Owned": true,



"Id": 0,



"Name": "string",



"Type": "string"



}



],



"Creator": {



"Id": 0,



"Name": "string",



"Type": "string"



},



"Product": {



"Id": 0,



"Type": "string",



"IsPublicDomain": true,



"IsForSale": true,



"PriceInRobux": 0,



"PremiumPricing": {



"PremiumDiscountPercentage": 0,



"PremiumPriceInRobux": 0



}



}



}



]
```

Provide feedback

---

GetRecommendedBundles

Deprecated

Show details

---

PromptAllowInventoryReadAccess

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to allow the developer to read
what items the user has in their inventory and other avatar editor related
information.

AvatarEditorService:PromptAllowInventoryReadAccess():()

Returns

()

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to allow the developer to read
what items the user has in their inventory and other avatar editor related
information. The prompt needs to be confirmed by the user for the
developer to use [AvatarEditorService:GetInventory()](/docs/reference/engine/classes/AvatarEditorService#GetInventory),
[AvatarEditorService:GetOutfits()](/docs/reference/engine/classes/AvatarEditorService#GetOutfits) and
[AvatarEditorService:GetFavorite()](/docs/reference/engine/classes/AvatarEditorService#GetFavorite). Permission does not persist
between sessions.

Provide feedback

---

PromptCreateOutfit

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to save the given
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) as an outfit.

AvatarEditorService:PromptCreateOutfit(

outfit:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)

):()

Parameters

|  |
| --- |
| outfit:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  The Outfit that the player will be prompted to created. |
| rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)  The [Enum.RigType](/docs/reference/engine/enums/RigType) that the outfit will be created for if the player confirms the prompt. |

Returns

()

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to save the given
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) as an outfit. Does not yield. The result can
be retrieved by listening to the
[AvatarEditorService.PromptCreateOutfitCompleted](/docs/reference/engine/classes/AvatarEditorService#PromptCreateOutfitCompleted) event.

Provide feedback

---

PromptDeleteOutfit

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to delete the given outfit.

AvatarEditorService:PromptDeleteOutfit(outfitId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| outfitId:[number](/docs/luau/numbers)  The outfitId of the outfit to delete. |

Returns

()

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to delete the given outfit. Does
not yield. The result can be retrieved by listening to the
[AvatarEditorService.PromptDeleteOutfitCompleted](/docs/reference/engine/classes/AvatarEditorService#PromptDeleteOutfitCompleted) event.

Provide feedback

---

PromptRenameOutfit

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to rename the given outfit.

AvatarEditorService:PromptRenameOutfit(outfitId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| outfitId:[number](/docs/luau/numbers)  The outfitId of the outfit to rename. |

Returns

()

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to rename the given outfit. Does
not yield. The result can be retrieved by listening to the
[AvatarEditorService.PromptRenameOutfitCompleted](/docs/reference/engine/classes/AvatarEditorService#PromptRenameOutfitCompleted) event.

Provide feedback

---

PromptSaveAvatar

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to update their avatar based on
the given [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) and [Enum.RigType](/docs/reference/engine/enums/RigType) of R6 or R15.

AvatarEditorService:PromptSaveAvatar(

humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)

):()

Parameters

|  |
| --- |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  The given [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) being prompted to save. |
| rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)  The [Enum.RigType](/docs/reference/engine/enums/RigType) that the avatar will be saved for if the player confirms the prompt. |

Returns

()

This function prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to update their
avatar based on the given [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) and [Enum.RigType](/docs/reference/engine/enums/RigType)
(R6 or R15). Does not yield and can get the result by listening to the
PromptSaveAvatarCompleted event. This is similar to how other prompts such
as PromptPurchase work.

Provide feedback

---

PromptSetFavorite

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to favorite or unfavorite the
given asset or bundle.

AvatarEditorService:PromptSetFavorite(

itemId:[number](/docs/luau/numbers), itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType), shouldFavorite:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| itemId:[number](/docs/luau/numbers)  The ItemId of the item being prompted to favorite. |
| itemType:[Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType)  The type of item being prompted to favorite. |
| shouldFavorite:[boolean](/docs/luau/booleans) |

Returns

()

This function prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to favorite or
unfavorite the given asset or bundle.

Provide feedback

---

PromptUpdateOutfit

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to update the given outfit.

AvatarEditorService:PromptUpdateOutfit(

outfitId:[number](/docs/luau/numbers), updatedOutfit:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)

):()

Parameters

|  |
| --- |
| outfitId:[number](/docs/luau/numbers)  The outfitId of the outfit to update. |
| updatedOutfit:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  A HumanoidDescription that represents the new outfit data. |
| rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)  The HumanoidRigType to update the outfit to. |

Returns

()

Prompts the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) to update the given outfit with
the given HumanoidDescription.

Provide feedback

---

SearchCatalogAsync

Yields

Returns a [CatalogPages](/docs/reference/engine/classes/CatalogPages) object containing the result of the given
search.

AvatarEditorService:SearchCatalogAsync(searchParameters:[CatalogSearchParams](/docs/reference/engine/datatypes/CatalogSearchParams)):[CatalogPages](/docs/reference/engine/classes/CatalogPages)

Parameters

|  |
| --- |
| searchParameters:[CatalogSearchParams](/docs/reference/engine/datatypes/CatalogSearchParams)  An object containing the parameters used for the search. |

Returns

[CatalogPages](/docs/reference/engine/classes/CatalogPages)

This function returns a [CatalogPages](/docs/reference/engine/classes/CatalogPages) object containing the result
of the given search.

The returned data has the format:

```
[



{



"Id": 0,



"ItemType": "Asset",



"AssetType": "Image",



"BundleType": "BodyParts",



"Name": "string",



"Description": "string",



"ProductId": 0,



"Genres": [



"All"



],



"BundledItems": [



{



"Owned": true,



"Id": 0,



"Name": "string",



"Type": "string"



}



],



"ItemStatus": [



"New"



],



"ItemRestrictions": [



"ThirteenPlus"



],



"CreatorType": "User",



"CreatorTargetId": 0,



"CreatorName": "string",



"Price": 0,



"PremiumPricing": {



"PremiumDiscountPercentage": 0,



"PremiumPriceInRobux": 0



},



"LowestPrice": 0,



"PriceStatus": "string",



"UnitsAvailableForConsumption": 0,



"PurchaseCount": 0,



"FavoriteCount": 0



}



]
```

Provide feedback

---

SearchCatalog

Deprecated

Show details

---

Events

PromptAllowInventoryReadAccessCompleted

Fires when the
[AvatarEditorService:PromptAllowInventoryReadAccess()](/docs/reference/engine/classes/AvatarEditorService#PromptAllowInventoryReadAccess) prompt is
responded to by the user.

AvatarEditorService.PromptAllowInventoryReadAccessCompleted(result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)  The result of the prompt. |

This event fires when the
[AvatarEditorService:PromptAllowInventoryReadAccess()](/docs/reference/engine/classes/AvatarEditorService#PromptAllowInventoryReadAccess) prompt is
responded to by the user. It can only return the Success or
PermissionDenied [enum](/docs/reference/engine/enums/AvatarPromptResult) statuses as it does not
perform any web requests which could fail.

Provide feedback

---

PromptCreateOutfitCompleted

Fires when the PromptSaveOutfit operation is completed.

AvatarEditorService.PromptCreateOutfitCompleted(

result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult), failureType:Variant

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)  The result of the prompt. |
| failureType:Variant |

This event fires when the PromptSaveOutfit operation is completed. It
gives a status [enum](/docs/reference/engine/enums/AvatarPromptResult) indicating whether the
prompt succeeded, failed or permission was not granted by the user.

Provide feedback

---

PromptDeleteOutfitCompleted

Fires when the PromptDeleteOutfit operation is completed.

AvatarEditorService.PromptDeleteOutfitCompleted(result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)  The result of the prompt. |

Fires when the PromptDeleteOutfit operation is completed. It gives a
status [enum](/docs/reference/engine/enums/AvatarPromptResult) indicating whether the prompt
succeeded, failed or permission was not granted by the user.

Provide feedback

---

PromptRenameOutfitCompleted

Fires when the PromptRenameOutfit operation is completed.

AvatarEditorService.PromptRenameOutfitCompleted(result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)  The result of the prompt. |

Fires when the PromptRenameOutfit operation is completed. It gives a
status [enum](/docs/reference/engine/enums/AvatarPromptResult) indicating whether the prompt
succeeded, failed or permission was not granted by the user.

Provide feedback

---

PromptSaveAvatarCompleted

Fires when the [AvatarEditorService:PromptSaveAvatar()](/docs/reference/engine/classes/AvatarEditorService#PromptSaveAvatar) operation is
completed.

AvatarEditorService.PromptSaveAvatarCompleted(

result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult), humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)  The result of the prompt. |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |

This event fires when the [AvatarEditorService:PromptSaveAvatar()](/docs/reference/engine/classes/AvatarEditorService#PromptSaveAvatar)
operation is completed. It gives a status [enum](/docs/reference/engine/enums/AvatarPromptResult)
indicating whether the prompt succeeded, failed or permission was not
granted by the user.

Provide feedback

---

PromptSetFavoriteCompleted

Fires when the [AvatarEditorService:PromptSetFavorite()](/docs/reference/engine/classes/AvatarEditorService#PromptSetFavorite) operation
is completed.

AvatarEditorService.PromptSetFavoriteCompleted(result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)  The result of the prompt. |

Fires when the [AvatarEditorService:PromptSetFavorite()](/docs/reference/engine/classes/AvatarEditorService#PromptSetFavorite) operation
is completed. It gives a status [enum](/docs/reference/engine/enums/AvatarPromptResult) indicating
whether the prompt succeeded, failed or permission was not granted by the
user.

Provide feedback

---

PromptUpdateOutfitCompleted

Fires when the [AvatarEditorService:PromptUpdateOutfit()](/docs/reference/engine/classes/AvatarEditorService#PromptUpdateOutfit) operation
is completed.

AvatarEditorService.PromptUpdateOutfitCompleted(result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| result:[Enum.AvatarPromptResult](/docs/reference/engine/enums/AvatarPromptResult)  The result of the prompt. |

Fires when the [AvatarEditorService:PromptUpdateOutfit()](/docs/reference/engine/classes/AvatarEditorService#PromptUpdateOutfit) operation
is completed. It gives a status [enum](/docs/reference/engine/enums/AvatarPromptResult) indicating
whether the prompt succeeded, failed or permission was not granted by the
user.

Provide feedback

---