# MarketplaceService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MarketplaceService
Scraped: 2026-01-11T02:43:16.304486Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- MarketplaceService
- Player
- Object
- PromptProductPurchase
- PromptPurchase
- ProcessReceipt
- GetProductInfo
- GetDeveloperProductsAsync
- UserOwnsGamePassAsync()
- PlayerOwnsAsset
- PlayerOwnsBundle
- DataStoreService
- Pages
- Script
- RunContext
- GetUserSubscriptionStatusAsync
- GetUserSubscriptionPaymentHistoryAsync
- Players.UserSubscriptionStatusChanged
- RemoteEvent.OnServerEvent
- MarketplaceService.PromptPremiumPurchaseFinished
- Players.PlayerMembershipChanged
- PromptProductPurchase()
- MarketplaceService:PromptPurchase()
- RemoteEvent:FireServer()
- UserId
- PromptGamePassPurchase
- MarketplaceService.PlayerOwnsAsset
- MarketplaceService.PlayerOwnsBundle
- PromptProductPurchaseFinished
- PromptPurchaseFinished
- PromptPremiumPurchase
- PlayerMembershipChanged
- PromptGamePassPurchaseFinished
- PromptSubscriptionPurchase
- UserSubscriptionStatusChanged
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [MarketplaceService](/docs/reference/engine/classes/MarketplaceService)

English

Feedback

Engine Class

MarketplaceService

The service responsible for in-experience transactions.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [GetDeveloperProductsAsync](#GetDeveloperProductsAsync)():[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetProductInfoAsync](#GetProductInfoAsync)(assetId: [number](/docs/luau/numbers),infoType: [Enum.InfoType](/docs/reference/engine/enums/InfoType)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetProductInfo](#GetProductInfo)(assetId: [number](/docs/luau/numbers),infoType: [Enum.InfoType](/docs/reference/engine/enums/InfoType)):[Dictionary](/docs/luau/tables#dictionaries)  Deprecated |
| [GetSubscriptionProductInfoAsync](#GetSubscriptionProductInfoAsync)(subscriptionId: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetUsersPriceLevelsAsync](#GetUsersPriceLevelsAsync)(userIds: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |
| [GetUserSubscriptionDetailsAsync](#GetUserSubscriptionDetailsAsync)(user: [Player](/docs/reference/engine/classes/Player),subscriptionId: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetUserSubscriptionPaymentHistoryAsync](#GetUserSubscriptionPaymentHistoryAsync)(user: [Player](/docs/reference/engine/classes/Player),subscriptionId: [string](/docs/luau/strings)):[Array](/docs/luau/tables#arrays) |
| [GetUserSubscriptionStatusAsync](#GetUserSubscriptionStatusAsync)(user: [Player](/docs/reference/engine/classes/Player),subscriptionId: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries) |
| [PlayerOwnsAssetAsync](#PlayerOwnsAssetAsync)(player: [Instance](/docs/reference/engine/datatypes/Instance),assetId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [PlayerOwnsAsset](#PlayerOwnsAsset)(player: [Instance](/docs/reference/engine/datatypes/Instance),assetId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [PlayerOwnsBundleAsync](#PlayerOwnsBundleAsync)(player: [Player](/docs/reference/engine/classes/Player),bundleId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [PlayerOwnsBundle](#PlayerOwnsBundle)(player: [Player](/docs/reference/engine/classes/Player),bundleId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [PromptBulkPurchase](#PromptBulkPurchase)(player: [Player](/docs/reference/engine/classes/Player),lineItems: [Array](/docs/luau/tables#arrays),options: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [PromptBundlePurchase](#PromptBundlePurchase)(player: [Instance](/docs/reference/engine/datatypes/Instance),bundleId: [number](/docs/luau/numbers)):() |
| [PromptCancelSubscription](#PromptCancelSubscription)(user: [Player](/docs/reference/engine/classes/Player),subscriptionId: [string](/docs/luau/strings)):() |
| [PromptGamePassPurchase](#PromptGamePassPurchase)(player: [Instance](/docs/reference/engine/datatypes/Instance),gamePassId: [number](/docs/luau/numbers)):() |
| [PromptPremiumPurchase](#PromptPremiumPurchase)(player: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [PromptProductPurchase](#PromptProductPurchase)(player: [Instance](/docs/reference/engine/datatypes/Instance),productId: [number](/docs/luau/numbers),equipIfPurchased: [boolean](/docs/luau/booleans),currencyType: [Enum.CurrencyType](/docs/reference/engine/enums/CurrencyType)):() |
| [PromptPurchase](#PromptPurchase)(player: [Instance](/docs/reference/engine/datatypes/Instance),assetId: [number](/docs/luau/numbers),equipIfPurchased: [boolean](/docs/luau/booleans),currencyType: [Enum.CurrencyType](/docs/reference/engine/enums/CurrencyType)):() |
| [PromptSubscriptionPurchase](#PromptSubscriptionPurchase)(user: [Player](/docs/reference/engine/classes/Player),subscriptionId: [string](/docs/luau/strings)):() |
| [RankProductsAsync](#RankProductsAsync)(productIdentifiers: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |
| [RecommendTopProductsAsync](#RecommendTopProductsAsync)(infoTypes: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |
| [UserOwnsGamePassAsync](#UserOwnsGamePassAsync)(userId: [number](/docs/luau/numbers),gamePassId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |

Events

|  |
| --- |
| [PromptBulkPurchaseFinished](#PromptBulkPurchaseFinished)(player: [Instance](/docs/reference/engine/datatypes/Instance),status: [Enum.MarketplaceBulkPurchasePromptStatus](/docs/reference/engine/enums/MarketplaceBulkPurchasePromptStatus),results: [Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptBundlePurchaseFinished](#PromptBundlePurchaseFinished)(player: [Instance](/docs/reference/engine/datatypes/Instance),bundleId: [number](/docs/luau/numbers),wasPurchased: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptGamePassPurchaseFinished](#PromptGamePassPurchaseFinished)(player: [Instance](/docs/reference/engine/datatypes/Instance),gamePassId: [number](/docs/luau/numbers),wasPurchased: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptPremiumPurchaseFinished](#PromptPremiumPurchaseFinished)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptProductPurchaseFinished](#PromptProductPurchaseFinished)(userId: [number](/docs/luau/numbers),productId: [number](/docs/luau/numbers),isPurchased: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptPurchaseFinished](#PromptPurchaseFinished)(player: [Instance](/docs/reference/engine/datatypes/Instance),assetId: [number](/docs/luau/numbers),isPurchased: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PromptSubscriptionPurchaseFinished](#PromptSubscriptionPurchaseFinished)(user: [Player](/docs/reference/engine/classes/Player),subscriptionId: [string](/docs/luau/strings),didTryPurchasing: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Callbacks

|  |
| --- |
| [ProcessReceipt](#ProcessReceipt)(receiptInfo: [Dictionary](/docs/luau/tables#dictionaries)):[Enum.ProductPurchaseDecision](/docs/reference/engine/enums/ProductPurchaseDecision) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[MarketplaceService](/docs/reference/engine/classes/MarketplaceService) is responsible for in-experience transactions. The
most notable methods are
[PromptProductPurchase](/docs/reference/engine/classes/MarketplaceService#PromptProductPurchase) and
[PromptPurchase](/docs/reference/engine/classes/MarketplaceService#PromptPurchase), as well as the
callback [ProcessReceipt](/docs/reference/engine/classes/MarketplaceService#ProcessReceipt) which must
be defined so that developer product transactions do not fail.

[MarketplaceService](/docs/reference/engine/classes/MarketplaceService) also has methods that fetch information about
[developer products](/docs/production/monetization/developer-products)
([GetProductInfo](/docs/reference/engine/classes/MarketplaceService#GetProductInfo) and
[GetDeveloperProductsAsync](/docs/reference/engine/classes/MarketplaceService#GetDeveloperProductsAsync)),
[passes](/docs/production/monetization/game-passes)
([UserOwnsGamePassAsync()](/docs/reference/engine/classes/MarketplaceService#UserOwnsGamePassAsync)),
and other assets
([PlayerOwnsAsset](/docs/reference/engine/classes/MarketplaceService#PlayerOwnsAsset),
[PlayerOwnsBundle](/docs/reference/engine/classes/MarketplaceService#PlayerOwnsBundle)).

Understanding [MarketplaceService](/docs/reference/engine/classes/MarketplaceService) is the first step towards learning to
[monetize](/docs/production/monetization) an experience on Roblox,
as well as learning to use [DataStoreService](/docs/reference/engine/classes/DataStoreService), which is responsible for
saving and loading all data related to purchases.

---

API Reference

Methods

GetDeveloperProductsAsync

Yields

Returns a [Pages](/docs/reference/engine/classes/Pages) object which contains information for all of the
current experience's developer products.

MarketplaceService:GetDeveloperProductsAsync():[Instance](/docs/reference/engine/datatypes/Instance)

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Returns a [Pages](/docs/reference/engine/classes/Pages) object which contains information for all of the
current experience's
[developer products](/docs/production/monetization/developer-products).

Code Samples

MarketplaceService:GetDeveloperProductsAsync

The below example would print the name, price, ID, description and icon
AssetId for all of the developer products which belong to the current game.

```
local MarketplaceService = game:GetService("MarketplaceService")



local developerProducts = MarketplaceService:GetDeveloperProductsAsync():GetCurrentPage()



for _, developerProduct in pairs(developerProducts) do



for field, value in pairs(developerProduct) do



print(field .. ": " .. value)



end



print(" ")



end
```

Provide feedback

---

GetProductInfoAsync

Yields

Returns the product information of an asset using its asset ID.

MarketplaceService:GetProductInfoAsync(

assetId:[number](/docs/luau/numbers), infoType:[Enum.InfoType](/docs/reference/engine/enums/InfoType)

):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| assetId:[number](/docs/luau/numbers)  The asset ID of the specified product. |
| infoType:[Enum.InfoType](/docs/reference/engine/enums/InfoType) Default Value: "Asset" An [Enum.InfoType](/docs/reference/engine/enums/InfoType) enum value specifying the type of information being retrieved. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary containing information about the queried item, described
in the previous tables.

This method provides information about an asset,
[developer product](/docs/production/monetization/developer-products),
or [pass](/docs/production/monetization/game-passes) based on the
asset ID and the [Enum.InfoType](/docs/reference/engine/enums/InfoType). If an item with the given ID does not
exist, this method throws an error.

Information about the queried item is provided in a dictionary with the
following keys. Note that not all information is provided or necessarily
relevant for the kind of product you're querying.

| Key | Type | Description |
| --- | --- | --- |
| Name | string | The name shown on the asset's page. |
| Description | string | The description shown on the asset's page; can be nil if blank. |
| PriceInRobux | number | The cost of purchasing the asset using Robux. |
| ProductId | number | The product ID if [Enum.InfoType](/docs/reference/engine/enums/InfoType) is Product. |
| ProductType | string | A string describing what the product is. Not to be confused with [Enum.MarketplaceProductType](/docs/reference/engine/enums/MarketplaceProductType). |
| Created | string | Timestamp of when the asset was created, for example 2022-01-02T10:30:45Z. Formatted using ISO 8601. |
| Updated | string | Timestamp of when the asset was last updated by its creator, for example 2022-02-12T11:22:15Z. Formatted using ISO 8601. |
| ContentRatingTypeId | number | Indicates whether the item is marked as 13+ in catalog. |
| MinimumMembershipLevel | number | The minimum subscription level necessary to purchase the item. |
| IsPublicDomain | boolean | Describes whether the asset can be taken for free. |
| TargetId | number | The ID of the product or asset. |

##### Creator Information

| Key | Type | Description |
| --- | --- | --- |
| Creator | table | Dictionary table of information describing the creator of the asset, containing the following fields: |
|  | | CreatorType: Either User or Group. |
|  | | CreatorTargetId: The ID of the creator user or group. |
|  | | HasVerifiedBadge: Boolean of whether the creator has a verified badge. |
|  | | Name: The name/username of the creator. |
|  | | Id: Use CreatorTargetId instead. |

##### Asset Information

| Key | Type | Description |
| --- | --- | --- |
| AssetId | number | The asset ID if [Enum.InfoType](/docs/reference/engine/enums/InfoType) is Asset. |
| AssetTypeId | number | The type of asset. See [Enum.AssetType](/docs/reference/engine/enums/AssetType) for the asset type ID numbers. |
| IconImageAssetId | number | The asset ID of the product's icon, or 0 if there isn't one. |
| IsForSale | boolean | Describes whether the asset is purchasable. |
| IsLimited | boolean | Describes whether the asset is a Roblox Limited that is no longer (if ever) sold. |
| IsLimitedUnique | boolean | Describes whether the asset is a unique Roblox Limited ("Limited U") item that only has a fixed number sold. |
| IsNew | boolean | Describes whether the asset is marked as "new" in the catalog. |
| Remaining | number | The remaining number of times a limited unique item may be sold. |
| Sales | number | The number of times the asset has been sold. |

##### Collectibles Information

| Key | Type | Description |
| --- | --- | --- |
| CollectibleItemId | string | The unique item ID of the collectible. |
| CollectibleProductId | string | The unique product ID of the collectible. |
| CollectiblesItemDetails | table | Dictionary table of information describing the collectible, containing the following fields: |
|  | | CollectibleLowestAvailableResaleItemInstanceId: The unique item instance ID of the lowest available resale for the collectible. |
|  | | CollectibleLowestAvailableResaleProductId: The unique product ID of the lowest available resale for the collectible. |
|  | | CollectibleLowestResalePrice: The lowest resale price for the collectible in Robux. |
|  | | IsForSale: Boolean of whether the collectible is available for sale (not resale). |
|  | | IsLimited: Boolean of whether or not the collectible is limited. |
|  | | TotalQuantity: The total quantity of the collectible available for purchase (not resale). |

##### Sale Location Settings

| Key | Type | Description |
| --- | --- | --- |
| CanBeSoldInThisGame | boolean | Describes whether the asset is purchasable in the current experience. |
| SaleLocation | table | Dictionary table of information describing where the item can be sold, containing the following fields: |
|  | | SaleLocationType: The type of sale location setting. See [Enum.ProductLocationRestriction](/docs/reference/engine/enums/ProductLocationRestriction) for the sale location setting ID numbers. |
|  | | UniverseIds: Array table of universes in which the item can be sold (not currently implemented). |

Code Samples

Getting Product Info

The below example will print the name and description of the asset with an ID
of 125378389. In this case it will print: *"Mr. Fancy Top Hat :: So fancy that
even his top hat's top hat has a top hat."*

```
local MarketplaceService = game:GetService("MarketplaceService")



local ASSET_ID = 125378389



local asset = MarketplaceService:GetProductInfo(ASSET_ID)



print(asset.Name .. " :: " .. asset.Description)
```

Provide feedback

---

GetProductInfo

Deprecated

Show details

---

GetSubscriptionProductInfoAsync

Yields

Returns the product information of a subscription for the given
subscriptionId.

MarketplaceService:GetSubscriptionProductInfoAsync(subscriptionId:[string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| subscriptionId:[string](/docs/luau/strings)  The ID of the subscription to check. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Note: Because it returns a localized price, you can only call this
method from a [Script](/docs/reference/engine/classes/Script) with [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client).

Returns the product information of a subscription for the given
subscriptionId.

| Key | Type | Description |
| --- | --- | --- |
| Name | string | The name of the subscription product. |
| Description | string | The description of the subscription product. |
| IconImageAssetId | number | The asset ID of the subscription product icon. |
| SubscriptionPeriod | [Enum.SubscriptionPeriod](/docs/reference/engine/enums/SubscriptionPeriod) | The duration of the subscription (for example, Month, Year, etc.). |
| DisplayPrice | string | Localized price with the appropriate currency symbol for display (for example, $4.99). For users in unsupported countries, DisplayPrice returns a string without specific price information. |
| DisplaySubscriptionPeriod | string | Localized subscription period text for display (for example, /month). Can be used together with DisplayPrice. |
| SubscriptionProviderName | string | Name of the subscription benefit provider (for example, the name of the associated experience). |
| IsForSale | boolean | True if the subscription product is available for sale. |
| PriceTier | number | A number that can be used to compare the price of different subscription products. This is not the actual price of the subscription (for example, 499). |

Provide feedback

---

GetUsersPriceLevelsAsync

Yields

Returns the regionalized price level of a user, representing the
recommended price for an item in their regional market.

MarketplaceService:GetUsersPriceLevelsAsync(userIds:[Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| userIds:[Array](/docs/luau/tables#arrays)  An array of user IDs. |

Returns

[Array](/docs/luau/tables#arrays)

Returns an array of PriceLevelInfo objects with a dictionary where
the keys are user IDs (strings) and their values are the corresponding
price levels (integers between 1 and 1000).

Returns the regionalized price level of a user, representing the
recommended price for an item in their regional market. For example, a
price level of 100 means that the suggested price for that user (based on
their region and purchasing power) is 100 Robux.

See
[Protect your trades and gifts](/docs/production/monetization/regional-pricing#protect-your-trades-and-gifts)
for more information.

Code Samples

Get price levels for a list of users

The following example uses GetUsersPriceLevelsAsync to map each price level to a user ID and retrieve price levels for a list of users.

```
-- Get the MarketplaceService



local MarketplaceService = game:GetService("MarketplaceService")



-- Define a function to retrieve price levels for a list of users



local function getPriceLevels(userIds)



local success, result = pcall(function()



return MarketplaceService:GetUsersPriceLevelsAsync(userIds)



end)



if success then



-- Map each PriceLevelInfo to a UserId -> PriceLevel lookup table



local lookup = {}



for _, info in ipairs(result) do



lookup[info.UserId] = info.PriceLevel



end



return lookup



else



warn("Error getting price levels:", result)



return nil



end



end



-- Example using placeholder IDs



local user1Id = 123456789



local user2Id = 987654321



-- Call the function and store the result



local priceLevels = getPriceLevels({user1Id, user2Id})



-- If successful, print each user's level



if priceLevels then



print("Price level for User 1:", priceLevels[user1Id])



print("Price level for User 2:", priceLevels[user2Id])



else



print("Failed to retrieve price levels.")



end
```

Provide feedback

---

GetUserSubscriptionDetailsAsync

Yields

Returns a table that contains the details of the user's subscription for a
given subscriptionId.

MarketplaceService:GetUserSubscriptionDetailsAsync(

user:[Player](/docs/reference/engine/classes/Player), subscriptionId:[string](/docs/luau/strings)

):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) object whose subscription details you want to check. |
| subscriptionId:[string](/docs/luau/strings)  The ID of the subscription to check. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Returns a dictionary table containing the details of the user's
subscription for the given subscriptionId. The table contains the
following keys:

| Key | Type | Description |
| --- | --- | --- |
| SubscriptionState | [Enum.SubscriptionState](/docs/reference/engine/enums/SubscriptionState) | Current state of this particular subscription. |
| NextRenewTime | [DateTime](/docs/reference/engine/datatypes/DateTime) | Renewal time for this current subscription. May be in the past if the subscription is in [SubscribedRenewalPaymentPending](/docs/reference/engine/enums/SubscriptionState#SubscribedRenewalPaymentPending) state. This field is will be nil if the subscription will not renew, is [Expired](/docs/reference/engine/enums/SubscriptionState#Expired), or the user never subscribed. |
| ExpireTime | [DateTime](/docs/reference/engine/datatypes/DateTime) | When this subscription expires. This field will be nil if the subscription is not cancelled or the user never subscribed. |
| ExpirationDetails | [table](/docs/reference/engine/libraries/table) | Table containing the details of the subscription expiration. This field will be nil if the subscription is not in the [Expired](/docs/reference/engine/enums/SubscriptionState#Expired) state. If populated, the table contains a ExpirationReason key of type [Enum.SubscriptionExpirationReason](/docs/reference/engine/enums/SubscriptionExpirationReason) describing why the subscription is expired. |

Note that this method can only be called from a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) of
[Server](/docs/reference/engine/enums/RunContext#Server). If you only need to determine the
IsSubscribed status of a user, it's recommended to use
[GetUserSubscriptionStatusAsync](/docs/reference/engine/classes/MarketplaceService#GetUserSubscriptionStatusAsync)
as it is faster and more efficient for that particular purpose.

Provide feedback

---

GetUserSubscriptionPaymentHistoryAsync

Yields

Returns an [Array](/docs/reference/engine/libraries/table) that contains up to one year of the
user's subscription payment history for the given subscriptionId.

MarketplaceService:GetUserSubscriptionPaymentHistoryAsync(

user:[Player](/docs/reference/engine/classes/Player), subscriptionId:[string](/docs/luau/strings)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player) |
| subscriptionId:[string](/docs/luau/strings) |

Returns

[Array](/docs/luau/tables#arrays)

Note: You can only call this method from a [Script](/docs/reference/engine/classes/Script) with
[Enum.RunContext.Server](/docs/reference/engine/enums/RunContext#Server).

Returns an [Array](/docs/reference/engine/libraries/table) that contains up to one year of the
user's subscription payment history for the given subscriptionId, sorted
from the most recent status to the least recent.

Each entry in the payment history [Array](/docs/reference/engine/libraries/table) contains the
following keys:

| Key | Type | Description |
| --- | --- | --- |
| CycleStartTime | [DateTime](/docs/reference/engine/datatypes/DateTime) | [DateTime](/docs/reference/engine/datatypes/DateTime) at the start of this particular subscription period. |
| CycleEndTime | [DateTime](/docs/reference/engine/datatypes/DateTime) | [DateTime](/docs/reference/engine/datatypes/DateTime) at the end of this particular subscription period. |
| PaymentStatus | [Enum.SubscriptionPaymentStatus](/docs/reference/engine/enums/SubscriptionPaymentStatus) | [Enum.SubscriptionPaymentStatus.Paid](/docs/reference/engine/enums/SubscriptionPaymentStatus#Paid) if the user paid for this particular subscription period. [Enum.SubscriptionPaymentStatus.Refunded](/docs/reference/engine/enums/SubscriptionPaymentStatus#Refunded) if the user refunded this particular subscription period. |

#### Payment History Length

Only creators affiliated with the subscription product can access up to
one year worth of the user's subscription payment history.
Non-associated creators can only get the user's current subscription
payment status or an empty [Array](/docs/reference/engine/libraries/table) if the user has no active
subscription.

#### Grace Period

Subscription renewal payments can have some processing time. Payment
history doesn't return a table for this period. However, in order to
preserve a user's subscription experience during the processing period,
[GetUserSubscriptionStatusAsync](/docs/reference/engine/classes/MarketplaceService#GetUserSubscriptionStatusAsync)
returns IsSubscribed: true for the given user. Don't grant durable items
or currency type subscription benefits to the user until after payment has
been confirmed for the current cycle.

For example, on August 31, 2023, User A's Subscription B is up for
renewal. On September 1, 2023, the payment has yet to be processed. If you
call
[GetUserSubscriptionPaymentHistoryAsync](/docs/reference/engine/classes/MarketplaceService#GetUserSubscriptionPaymentHistoryAsync)
on September 1, 2023 on User A for Subscription B, the first entry of the
return value is:

| Key | Value |
| --- | --- |
| CycleStartTime | ... |
| CycleEndTime | August 31, 2023 |
| PaymentStatus | [Enum.SubscriptionPaymentStatus.Paid](/docs/reference/engine/enums/SubscriptionPaymentStatus#Paid) |

Note that since the user is within the grace period, the cycle they have
yet to pay for (September 1, 2023) does not appear in the return value at
all. This field only populates after the payment has been received and
processed.

At the same time,
[GetUserSubscriptionStatusAsync](/docs/reference/engine/classes/MarketplaceService#GetUserSubscriptionStatusAsync)
returns the following result until the renewal payment process fails or
the user cancels:

| Key | Return |
| --- | --- |
| IsSubscribed | True |
| IsRenewing | True |

Code Samples

MarketplaceService:GetUserSubscriptionPaymentHistoryAsync

This code sample demonstrates how to check the last 12 months of a user's
payment history for a given subscription ID. Rather than the raw values, it
prints formatted values for easier readability. Roblox Studio includes several
subscription IDs for testing purposes:

* EXP-0 represents an active and renewing subscription.
* EXP-1 represents a returning subscription.
* EXP-2 represents a refunded subscription. Depending on your subscription
  benefits, refunds can require special handling, so testing for this case is
  particularly useful.
* EXP-3 represents an active subscription that is pending successful payment
  for the current cycle. Continued failure to pay results in automatic
  cancellation of the subscription.

```
local MarketplaceService = game:GetService("MarketplaceService")



local Players = game:GetService("Players")



local SUBSCRIPTION_ID = "EXP-0"



local function checkSubscriptionHistory(player: Player)



local subscriptionHistory = {}



local success, err = pcall(function()



subscriptionHistory = MarketplaceService:GetUserSubscriptionPaymentHistoryAsync(player, SUBSCRIPTION_ID)



end)



if not success then



warn(`Error while checking subscription history: {err}`)



return



end



if next(subscriptionHistory) then



-- User has some subscription history within the past 12 months.



-- Print the details of each payment entry from the subscription history.



print(`Player {player.Name} has subscribed to {SUBSCRIPTION_ID} before:`)



for entryNum, paymentEntry in subscriptionHistory do



local paymentStatus = tostring(paymentEntry.PaymentStatus)



local cycleStartTime = paymentEntry.CycleStartTime:FormatLocalTime("LLL", "en-us")



local cycleEndTime = paymentEntry.CycleEndTime:FormatLocalTime("LLL", "en-us")



print(`{entryNum}: {paymentStatus} ({cycleStartTime} - {cycleEndTime})`)



end



else



print(`Player {player.Name} has never subscribed to {SUBSCRIPTION_ID} before.`)



end



end



-- Call checkSubscriptionHistory for any players already in the game



for _, player in ipairs(Players:GetPlayers()) do



checkSubscriptionHistory(player)



end



-- Call checkSubscriptionHistory for all future players



Players.PlayerAdded:Connect(checkSubscriptionHistory)
```

Provide feedback

---

GetUserSubscriptionStatusAsync

Yields

Returns a [table](/docs/reference/engine/libraries/table) that contains the subscription status of the
user for the given subscriptionId.

MarketplaceService:GetUserSubscriptionStatusAsync(

user:[Player](/docs/reference/engine/classes/Player), subscriptionId:[string](/docs/luau/strings)

):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) object whose subscription status you want to check. |
| subscriptionId:[string](/docs/luau/strings)  The ID of the subscription to check for. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Returns a [table](/docs/reference/engine/libraries/table) that contains the subscription status of the
user for the given subscriptionId. The table contains the following
keys:

| Key | Type | Description |
| --- | --- | --- |
| IsSubscribed | boolean | True if the user's subscription is active. |
| IsRenewing | boolean | True if the user is set to renew this subscription after the current subscription period ends. |

Note that IsSubscribed will be true only when a user has purchased the
subscription and the payment has been successfully processed. If the
payment for a user's initial subscription purchase is still processing or
has failed, IsSubscribed returns false. To understand when a user's
subscription status has changed, see the
[Players.UserSubscriptionStatusChanged](/docs/reference/engine/classes/Players#UserSubscriptionStatusChanged) event.

Code Samples

Check User Subscription Status

This code sample demonstrates how to check the subscription status of a user for a certain subscription.
As a user enters the game, their account is checked
for the status of that subscription and a message is printed.

Notice how the call to GetUserSubscriptionStatusAsync is wrapped in pcall - this prevents
the code from throwing an error in case the user's subscription status can't be
checked for some reason. Should such an error occur, the success variable
would be false.

```
local MarketplaceService = game:GetService("MarketplaceService")



local Players = game:GetService("Players")



local subscriptionID = "EXP-00000"



local function checkSubStatus(player)



local subStatus = {}



local success, message = pcall(function()



-- returns IsRenewing and IsSubscribed



subStatus = MarketplaceService:GetUserSubscriptionStatusAsync(player, subscriptionID)



end)



if not success then



warn("Error while checking if player has subscription: " .. tostring(message))



return



end



if subStatus["IsSubscribed"] then



print(player.Name .. " is subscribed with " .. subscriptionID)



-- Give player permissions associated with the subscription



end



end



Players.PlayerAdded:Connect(checkSubStatus)
```

Provide feedback

---

PlayerOwnsAssetAsync

Yields

Returns whether the given user has the given asset.

MarketplaceService:PlayerOwnsAssetAsync(

player:[Instance](/docs/reference/engine/datatypes/Instance), assetId:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) whose inventory is tested for ownership of the given asset. |
| assetId:[number](/docs/luau/numbers)  The asset ID for which the given player's inventory is tested. |

Returns

[boolean](/docs/luau/booleans)

Indicates whether the given player's inventory contains the given
asset.

Returns whether the inventory of a specific user contains an asset, based
on the asset ID. This method throws an error if the query fails, so you
should wrap calls to this method in pcall().

* This method should not be used for
  [passes](/docs/production/monetization/game-passes) since they use
  a separate ID system. Legacy passes that still depend on an asset ID
  should use
  [UserOwnsGamePassAsync()](/docs/reference/engine/classes/MarketplaceService#UserOwnsGamePassAsync)
  instead of this method.
* This method cannot be used to check for
  [developer products](/docs/production/monetization/developer-products)
  since they can be purchased multiple times but not owned themselves.
  Instead, use a [data store](/docs/../../../cloud-services/data-stores) to save
  when a user buys a developer product.

Code Samples

Check for Item Ownership

This code sample demonstrates how to check if a player owns a certain item.
Here, we're checking for the item
[Midnight Shades](https://www.roblox.com/catalog/30331986/Midnight-Shades), a
hat that costs R$ 250. As a player enters the game, their account is checked
for the ownership of that item and a message is printed.

Notice how the call to PlayerOwnsAsset is wrapped in pcall - this prevents
the code from throwing an error in case the player's inventory can't be
checked for some reason. Should such an error occur, the success variable
would be false.

```
local Players = game:GetService("Players")



local MarketplaceService = game:GetService("MarketplaceService")



-- The item we're checking for: https://www.roblox.com/catalog/30331986/Midnight-Shades



local ASSET_ID = 30331986



local ASSET_NAME = "Midnight Shades"



local function onPlayerAdded(player)



local success, doesPlayerOwnAsset = pcall(MarketplaceService.PlayerOwnsAsset, MarketplaceService, player, ASSET_ID)



if not success then



local errorMessage = doesPlayerOwnAsset



warn(`Error checking if {player.Name} owns {ASSET_NAME}: {errorMessage}`)



return



end



if doesPlayerOwnAsset then



print(`{player.Name} owns {ASSET_NAME}`)



else



print(`{player.Name} doesn't own {ASSET_NAME}`)



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

PlayerOwnsAsset

Deprecated

Show details

---

PlayerOwnsBundleAsync

Yields

Returns whether the given player owns the given bundle.

MarketplaceService:PlayerOwnsBundleAsync(

player:[Player](/docs/reference/engine/classes/Player), bundleId:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) whose inventory is tested for ownership of the given bundle. |
| bundleId:[number](/docs/luau/numbers)  The bundle ID for which the given player's inventory is tested. |

Returns

[boolean](/docs/luau/booleans)

Indicates whether the given player's inventory contains the given
bundle.

Returns whether the inventory of a specific user contains a bundle, based
on the bundle ID. This method throws an error if the query fails, so you
should wrap calls to this method in pcall().

Code Samples

Check for Bundle Ownership

This code sample demonstrates how to check if a player owns a certain bundle.
Here, we're checking for the bundle
[Junkbot](https://www.roblox.com/bundles/589/Junkbot). As a player enters the
game, their account is checked for the ownership of that item and a message is
printed.

Notice that a pcall() wraps the call to
MarketplaceService:PlayerOwnsBundle() to prevent the code from throwing an
error in case the player's inventory can't be checked. If such an error
occurs, the success variable is false.

```
local Players = game:GetService("Players")



local MarketplaceService = game:GetService("MarketplaceService")



-- The bundle we're checking for: https://www.roblox.com/bundles/589/Junkbot



local BUNDLE_ID = 589



local BUNDLE_NAME = "Junkbot"



Players.PlayerAdded:Connect(function(player)



local success, doesPlayerOwnBundle = pcall(function()



return MarketplaceService:PlayerOwnsBundle(player, BUNDLE_ID)



end)



if success == false then



print("PlayerOwnsBundle call failed: ", doesPlayerOwnBundle)



return



end



if doesPlayerOwnBundle then



print(player.Name .. " owns " .. BUNDLE_NAME)



else



print(player.Name .. " doesn't own " .. BUNDLE_NAME)



end



end)
```

Provide feedback

---

PlayerOwnsBundle

Deprecated

Show details

---

PromptBulkPurchase

Prompts a user to purchase multiple avatar items with the given assetId
or bundleId.

MarketplaceService:PromptBulkPurchase(

player:[Player](/docs/reference/engine/classes/Player), lineItems:[Array](/docs/luau/tables#arrays), options:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The user to prompt to purchase items. |
| lineItems:[Array](/docs/luau/tables#arrays)  An array of avatar items to be included in the bulk purchase.  Each line item contains the following structure:  ```  {  Type: MarketplaceProductType,  Id: string  } ```  Each line item contains the following pairs:   * Type: The corresponding [Enum.MarketplaceProductType](/docs/reference/engine/enums/MarketplaceProductType) (Enum). * Id: The ID of the asset or bundle. |
| options:[Dictionary](/docs/luau/tables#dictionaries)  Not available at this time. |

Returns

()

Prompts a user to purchase multiple avatar items with the given assetId
or bundleId. Does not work with non-avatar items.

PromptBulkPurchase only allows prompting from server scripts.

For limited items, original copies are prompted until they run out,
regardless of the price. Once original copies are out, resale copies are
prompted.

A maximum of 20 items can be added to a single bulk purchase prompt.

Code Samples

Prompt Bulk Purchase Client

The following sample prompts players to buy "Beautiful Hair for Beautiful People" and "Blue Collar Cat" when they join the experience.

Place this LocalScript somewhere on the client such as within Players -> StarterPlayerScripts so that it will be able to fire a remote event signal from a client to the server.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local promptBulkPurchaseEvent = ReplicatedStorage:WaitForChild("PromptBulkPurchaseEvent")



local part = Instance.new("Part")



part.Parent = workspace



local clickDetector = Instance.new("ClickDetector")



clickDetector.Parent = part



clickDetector.MouseClick:Connect(function()



promptBulkPurchaseEvent:FireServer({



{ Type = Enum.MarketplaceProductType.AvatarAsset, Id = "16630147" },



{ Type = Enum.MarketplaceProductType.AvatarBundle, Id = "182" },



})



end)
```

Prompt Bulk Purchase Server

The following code is listening for a [RemoteEvent.OnServerEvent](/docs/reference/engine/classes/RemoteEvent#OnServerEvent) to fire to the Server from a Client. Place this script somewhere on the server such as within ServerStorage.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local MarketplaceService = game:GetService("MarketplaceService")



local promptBulkPurchaseEvent = Instance.new("RemoteEvent")



promptBulkPurchaseEvent.Name = "PromptBulkPurchaseEvent"



promptBulkPurchaseEvent.Parent = ReplicatedStorage



--Listen for the RemoteEvent to fire from a Client and then trigger the bulk purchase prompt



promptBulkPurchaseEvent.OnServerEvent:Connect(function(player, items)



MarketplaceService:PromptBulkPurchase(player, items, {})



end)
```

Provide feedback

---

PromptBundlePurchase

Prompts a user to purchase a bundle with the given bundleId.

MarketplaceService:PromptBundlePurchase(

player:[Instance](/docs/reference/engine/datatypes/Instance), bundleId:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance) |
| bundleId:[number](/docs/luau/numbers) |

Returns

()

Prompts a user to purchase a bundle with the given bundleId.

Provide feedback

---

PromptCancelSubscription

Prompts a user to cancel a subscription for the given subscriptionId.

MarketplaceService:PromptCancelSubscription(

user:[Player](/docs/reference/engine/classes/Player), subscriptionId:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player) |
| subscriptionId:[string](/docs/luau/strings) |

Returns

()

Prompts a user to cancel a subscription for the given subscriptionId.
Once the user successfully cancels the subscription, the
[Players.UserSubscriptionStatusChanged](/docs/reference/engine/classes/Players#UserSubscriptionStatusChanged) event fires.

Provide feedback

---

PromptGamePassPurchase

Prompts a user to purchase a pass with the given gamePassId.

MarketplaceService:PromptGamePassPurchase(

player:[Instance](/docs/reference/engine/datatypes/Instance), gamePassId:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance) |
| gamePassId:[number](/docs/luau/numbers) |

Returns

()

Prompts a user to purchase a
[pass](/docs/production/monetization/game-passes) with the given
gamePassId.

Provide feedback

---

PromptPremiumPurchase

Prompts a user to purchase Roblox Premium.

MarketplaceService:PromptPremiumPurchase(player:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The user being prompted to purchase Premium. |

Returns

()

Prompts a user to purchase
[Roblox Premium](https://www.roblox.com/premium/membership). To learn more
about Premium and about incorporating Premium incentives into your
experience, see
[Engagement-based payouts](/docs/production/monetization/engagement-based-payouts).

##### See also

* [MarketplaceService.PromptPremiumPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptPremiumPurchaseFinished) which fires
  when the Premium purchase UI closes.
* [Players.PlayerMembershipChanged](/docs/reference/engine/classes/Players#PlayerMembershipChanged) which fires when the server
  recognizes that a user's membership has changed.

Code Samples

Prompt Premium Purchase

The following code prompts users to purchase Premium when their character touches the part that its containing [Script](/docs/reference/engine/classes/Script) is attached to, such as a teleporter that allows access to an exclusive area.

```
local MarketplaceService = game:GetService("MarketplaceService")



local Players = game:GetService("Players")



local teleporter = script.Parent



local showModal = true



local TELEPORT_POSITION = Vector3.new(1200, 200, 60)



-- Teleport character to exclusive area



local function teleportPlayer(player)



-- Request streaming around target location



player:RequestStreamAroundAsync(TELEPORT_POSITION)



-- Teleport character



local character = player.Character



if character and character.Parent then



local currentPivot = character:GetPivot()



character:PivotTo(currentPivot * CFrame.new(TELEPORT_POSITION))



end



end



-- Detect character parts touching teleporter



teleporter.Touched:Connect(function(otherPart)



local player = Players:GetPlayerFromCharacter(otherPart.Parent)



if not player then



return



end



if not player:GetAttribute("CharacterPartsTouching") then



player:SetAttribute("CharacterPartsTouching", 0)



end



player:SetAttribute("CharacterPartsTouching", player:GetAttribute("CharacterPartsTouching") + 1)



if player.MembershipType == Enum.MembershipType.Premium then



-- User has Premium; teleport character to exclusive area within experience



teleportPlayer(player)



else



-- Show purchase modal, using debounce to show once every few seconds at most



if not showModal then



return



end



showModal = false



task.delay(5, function()



showModal = true



end)



MarketplaceService:PromptPremiumPurchase(player)



end



end)



-- Detect character parts exiting teleporter



teleporter.TouchEnded:Connect(function(otherPart)



local player = Players:GetPlayerFromCharacter(otherPart.Parent)



if player and player:GetAttribute("CharacterPartsTouching") then



player:SetAttribute("CharacterPartsTouching", player:GetAttribute("CharacterPartsTouching") - 1)



end



end)



-- Handle membership changed event



Players.PlayerMembershipChanged:Connect(function(player)



warn("User membership changed; new membership is " .. tostring(player.MembershipType))



-- Teleport character if membership type is Premium and character is on teleporter



if player.MembershipType == Enum.MembershipType.Premium and player:GetAttribute("CharacterPartsTouching") > 0 then



teleportPlayer(player)



end



end)
```

Provide feedback

---

PromptProductPurchase

Prompts a user to purchase a developer product with the given productId.

MarketplaceService:PromptProductPurchase(

player:[Instance](/docs/reference/engine/datatypes/Instance), productId:[number](/docs/luau/numbers), equipIfPurchased:[boolean](/docs/luau/booleans), currencyType:[Enum.CurrencyType](/docs/reference/engine/enums/CurrencyType)

):()

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance) |
| productId:[number](/docs/luau/numbers) |
| equipIfPurchased:[boolean](/docs/luau/booleans) Default Value: true |
| currencyType:[Enum.CurrencyType](/docs/reference/engine/enums/CurrencyType) Default Value: "Default" |

Returns

()

Prompts a user to purchase a
[developer product](/docs/production/monetization/developer-products)
with the given productId.

Code Samples

MarketplaceService:PromptProductPurchase

The following example illustrates how to prompt purchase of a [developer
product](/docs/production/monetization/developer-products) with the
[PromptProductPurchase()](/docs/reference/engine/classes/MarketplaceService#PromptProductPurchase)
method. Depending on the needs of your experience, you can call the
promptPurchase() function in situations such as when the player presses a
[button](/docs/ui/buttons) or when their
character talks to a vendor NPC.

```
local MarketplaceService = game:GetService("MarketplaceService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local productId = 0000000 -- Change this to your developer product ID



-- Function to prompt purchase of the developer product



local function promptPurchase()



MarketplaceService:PromptProductPurchase(player, productId)



end



promptPurchase()
```

Provide feedback

---

PromptPurchase

Prompts a user to purchase an item with the given assetId. Does not work
for USD Creator Store purchases.

MarketplaceService:PromptPurchase(

player:[Instance](/docs/reference/engine/datatypes/Instance), assetId:[number](/docs/luau/numbers), equipIfPurchased:[boolean](/docs/luau/booleans), currencyType:[Enum.CurrencyType](/docs/reference/engine/enums/CurrencyType)

):()

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance) |
| assetId:[number](/docs/luau/numbers) |
| equipIfPurchased:[boolean](/docs/luau/booleans) Default Value: true |
| currencyType:[Enum.CurrencyType](/docs/reference/engine/enums/CurrencyType) Default Value: "Default" Ignored. |

Returns

()

Prompts a user to purchase an item with the given assetId.

* This does not work for
  [USD Creator Store](/docs/production/sell-on-creator-store)
  purchases.
* If the item has the
  [Sale Location](/docs/marketplace/publish-to-marketplace#sale-location)
  set as Experience By Place ID (API Only), you must call
  [MarketplaceService:PromptPurchase()](/docs/reference/engine/classes/MarketplaceService#PromptPurchase) from a server script.
* If prompting a purchase of a
  [limited](/docs/marketplace/marketplace-fees-and-commissions#limiteds)
  item:
  + (Recommended) Server requests prompt original copies until they run
    out, regardless of the price. Once original copies run out, resale
    copies are prompted.
  + Client requests prompt from the lowest resale price even if original
    copies are available.

Code Samples

LocalScript (Client)

The below example would prompt all new players to buy Beautiful Hair for
Beautiful People when they click on a part.

Place this LocalScript somewhere on the Client such as within Players ->
StarterPlayerScripts so that it will be able to fire a
[RemoteEvent:FireServer()](/docs/reference/engine/classes/RemoteEvent#FireServer) signal from a Client to the Server.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local promptPurchaseEvent = ReplicatedStorage:WaitForChild("PromptPurchaseEvent")



local part = Instance.new("Part")



part.Parent = workspace



local clickDetector = Instance.new("ClickDetector")



clickDetector.Parent = part



clickDetector.MouseClick:Connect(function()



promptPurchaseEvent:FireServer(16630147)



end)
```

Script (Server)

Since the below code is listening for a [RemoteEvent.OnServerEvent](/docs/reference/engine/classes/RemoteEvent#OnServerEvent) to
fire to the Server from a Client. Place this script somewhere on the Server
such as within ServerStorage.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local MarketplaceService = game:GetService("MarketplaceService")



local promptPurchaseEvent = Instance.new("RemoteEvent")



promptPurchaseEvent.Name = "PromptPurchaseEvent"



promptPurchaseEvent.Parent = ReplicatedStorage



-- Listen for the RemoteEvent to fire from a Client and then trigger the purchase prompt



promptPurchaseEvent.OnServerEvent:Connect(function(player, id)



MarketplaceService:PromptPurchase(player, id)



end)
```

Provide feedback

---

PromptSubscriptionPurchase

Prompts a user to purchase a subscription for the given subscriptionId.

MarketplaceService:PromptSubscriptionPurchase(

user:[Player](/docs/reference/engine/classes/Player), subscriptionId:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) object to be prompted to subscribe. |
| subscriptionId:[string](/docs/luau/strings)  The ID of the subscription to subscribe to. |

Returns

()

Prompts a user to purchase a subscription for the given subscriptionId.

Provide feedback

---

RankProductsAsync

Yields

Takes a list of product IDs and returns a personalized ordered list of
those products.

MarketplaceService:RankProductsAsync(productIdentifiers:[Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| productIdentifiers:[Array](/docs/luau/tables#arrays)  An array of objects identifying the products you want to rank. This array can include up to 50 items.  Each ProductIdentifier has:   * [Enum.InfoType](/docs/reference/engine/enums/InfoType): Enum.InfoType   + Must be either [Enum.InfoType.GamePass](/docs/reference/engine/enums/InfoType#GamePass) or     [Enum.InfoType.Product](/docs/reference/engine/enums/InfoType#Product). * Id: number   + The ID of the game pass or developer product.   ```  local ProductIdentifier = {  InfoType = Enum.InfoType.GamePass,  Id = 123456  } ``` |

Returns

[Array](/docs/luau/tables#arrays)

The array of ranked items in a personalized order for the current
user.

Each array has:

* ProductIdentifier: The corresponding ID from the input array.
* ProductInfo: The standard product info dictionary returned by
  [GetProductInfo](/docs/reference/engine/classes/MarketplaceService#GetProductInfo).

Takes a list of product IDs and returns a personalized ordered list of
those products.

This API has a client-side throttling limit of 10 requests per minute. If
you exceed this limit, wait 60 seconds and make the request again.

Code Samples

Get a list of ranked products based on the provided product IDs

This sample takes a list of product IDs and returns a ranked list of those products.

```
-- Get the MarketplaceService



local MarketplaceService = game:GetService("MarketplaceService")



-- Create the array of products you want to rank



local productIdentifiers = {



{InfoType = Enum.InfoType.GamePass, Id = 123},



{InfoType = Enum.InfoType.Product, Id = 456},



{InfoType = Enum.InfoType.Product, Id = 789}



}



-- Call in a protected call to handle errors gracefully



local success, rankedProducts = pcall(function()



return MarketplaceService:RankProductsAsync(productIdentifiers)



end)



if not success then



error("Failed to rank products")



end



-- Load the returned items into the store.



for i, rankedItem in ipairs(rankedProducts) do



local productIdentifier = rankedItem.ProductIdentifier



local productInfo = rankedItem.ProductInfo



-- ...



-- Logic to add products into store



end
```

Provide feedback

---

RecommendTopProductsAsync

Yields

* Takes an array of [Enum.InfoType](/docs/reference/engine/enums/InfoType) and returns up to 50 items
  representing the products a user is most likely to engage with and
  purchase.

MarketplaceService:RecommendTopProductsAsync(infoTypes:[Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| infoTypes:[Array](/docs/luau/tables#arrays)  An array of [Enum.InfoType](/docs/reference/engine/enums/InfoType) values specifying the types of product to retrieve recommendations for.  Supported InfoTypes: [Enum.InfoType.GamePass](/docs/reference/engine/enums/InfoType#GamePass), [Enum.InfoType.Product](/docs/reference/engine/enums/InfoType#Product).  ```  local infoTypes = {  Enum.InfoType.GamePass,  Enum.InfoType.Product  } ``` |

Returns

[Array](/docs/luau/tables#arrays)

A ranked list of up to 50 items the user is most likely to engage
with, based on the provided InfoTypes. If no recommendations can be
determined, the method returns an empty list.

Takes an array of [Enum.InfoType](/docs/reference/engine/enums/InfoType) and returns up to 50 items representing
the products a user is most likely to engage with and purchase. If no
recommendations can be determined, the method returns an empty list.

This API has a client-side throttling limit of 5 requests per minute. If
you exceed this limit, wait 60 seconds and make the request again.

Code Samples

Get a ranked list of the top products for in your in-experience store

This sample returns a ranked list of the top products for a user in your in-experience store.

```
-- Get the MarketplaceService



local MarketplaceService = game:GetService("MarketplaceService")



-- Create an array of product types to include. In this case both game passes and developer products



local productTypes = {Enum.InfoType.GamePass, Enum.InfoType.Product}



-- Call in a protected call to handle errors gracefully



local success, topRankedItems = pcall(function()



return MarketplaceService:RecommendTopProductsAsync(productTypes)



end)



if not success then



error("Failed to rank products")



end



-- Load the returned items into the store. Make sure to filter out any ineligible items from topRankedItems such as developer products the user can no longer purchase



for i, rankedItem in ipairs(topRankedItems) do



local productIdentifier = rankedItem.ProductIdentifier



local productInfo = rankedItem.ProductInfo



-- ...



-- Logic to add products into store



end
```

Provide feedback

---

UserOwnsGamePassAsync

Yields

Returns true if the player with the given [UserId](/docs/reference/engine/classes/Player#UserId)
owns the pass with the given gamePassId.

MarketplaceService:UserOwnsGamePassAsync(

userId:[number](/docs/luau/numbers), gamePassId:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [UserId](/docs/reference/engine/classes/Player#UserId) of the [Player](/docs/reference/engine/classes/Player) whose inventory you're checking. |
| gamePassId:[number](/docs/luau/numbers)  The pass ID you want to check for. Not to be confused with an asset ID. |

Returns

[boolean](/docs/luau/booleans)

Returns true if the user with the given [UserId](/docs/reference/engine/classes/Player#UserId) owns
the [pass](/docs/production/monetization/game-passes) with the given
gamePassId (not to be confused with an asset ID).

#### Caching Behavior

The results of this function are remembered so that repeated calls are
returned faster.

This function always returns true when the user first enters a server
after purchasing the pass.

If the user has purchased the pass inside an experience through
[PromptGamePassPurchase](/docs/reference/engine/classes/MarketplaceService#PromptGamePassPurchase),
the
[UserOwnsGamePassAsync()](/docs/reference/engine/classes/MarketplaceService#UserOwnsGamePassAsync)
function might return false because of caching behavior. Alternatively,
the function might return true even after the user has deleted the pass
from their inventory.

Provide feedback

---

Events

PromptBulkPurchaseFinished

Fires when a purchase prompt for bulk avatar items is closed.

MarketplaceService.PromptBulkPurchaseFinished(

player:[Instance](/docs/reference/engine/datatypes/Instance), status:[Enum.MarketplaceBulkPurchasePromptStatus](/docs/reference/engine/enums/MarketplaceBulkPurchasePromptStatus), results:[Dictionary](/docs/luau/tables#dictionaries)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) who received the prompt. |
| status:[Enum.MarketplaceBulkPurchasePromptStatus](/docs/reference/engine/enums/MarketplaceBulkPurchasePromptStatus)  The status of the bulk purchase. |
| results:[Dictionary](/docs/luau/tables#dictionaries)  The table type containing the line items and their status in the following format:  ```  {  RobuxSpent: number  Items: {  {  type: MarketplaceProductType,  id: string,  status: MarketplaceItemPurchaseStatus  },  ...  }  } ```  Each line item contains the following pairs:   * type: The corresponding [Enum.MarketplaceProductType](/docs/reference/engine/enums/MarketplaceProductType) (Enum). * id: The ID of the asset or bundle (string). * status: The [Enum.MarketplaceItemPurchaseStatus](/docs/reference/engine/enums/MarketplaceItemPurchaseStatus) of the purchase   (Enum) |

This event fires when a purchase prompt for a bulk avatar items closes.
For example, when a user receives the purchase prompt and clicks
Cancel, or when they receive a success or error message and click
OK.

Note: This is not a trusted event from the client. To check if the user
owns the items purchased, use [MarketplaceService.PlayerOwnsAsset](/docs/reference/engine/classes/MarketplaceService#PlayerOwnsAsset)
or [MarketplaceService.PlayerOwnsBundle](/docs/reference/engine/classes/MarketplaceService#PlayerOwnsBundle).

Provide feedback

---

PromptBundlePurchaseFinished

MarketplaceService.PromptBundlePurchaseFinished(

player:[Instance](/docs/reference/engine/datatypes/Instance), bundleId:[number](/docs/luau/numbers), wasPurchased:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance) |
| bundleId:[number](/docs/luau/numbers) |
| wasPurchased:[boolean](/docs/luau/booleans) |

Provide feedback

---

PromptGamePassPurchaseFinished

Fires when a purchase prompt for a pass is closed.

MarketplaceService.PromptGamePassPurchaseFinished(

player:[Instance](/docs/reference/engine/datatypes/Instance), gamePassId:[number](/docs/luau/numbers), wasPurchased:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) who received the prompt. |
| gamePassId:[number](/docs/luau/numbers)  The ID number of the pass shown in the prompt. Not to be confused with an asset ID. |
| wasPurchased:[boolean](/docs/luau/booleans)  Indicates if the user pressed OK (true), Cancel (false) on the purchase prompt, or if the purchase prompt errored (false).  This might not accurately reflect if the purchase itself has been successfully processed. Use [UserOwnsGamePassAsync()](/docs/reference/engine/classes/MarketplaceService#UserOwnsGamePassAsync) as ownership confirmation. |

This event fires when a purchase prompt for a
[pass](/docs/production/monetization/game-passes) closes. For
example, when a user receives the purchase prompt and clicks Cancel,
or when they receive a success or error message and click OK.

##### See also

* For repeatable developer product purchase prompts, use
  [PromptProductPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptProductPurchaseFinished).
* For affiliate gear sales or other assets, use
  [PromptPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptPurchaseFinished).
* For more information on saving and replicating user data like purchases
  and progress, see
  [Implementing player data and purchases](https://devforum.roblox.com/t/implementing-player-data-and-purchasing-systems/2839941).

Code Samples

Handling Gamepass Purchase Finished

```
local MarketplaceService = game:GetService("MarketplaceService")



local function gamepassPurchaseFinished(...)



-- Print all the details of the prompt, for example:



-- PromptGamePassPurchaseFinished PlayerName 123456 false



print("PromptGamePassPurchaseFinished", ...)



end



MarketplaceService.PromptGamePassPurchaseFinished:Connect(gamepassPurchaseFinished)
```

Provide feedback

---

PromptPremiumPurchaseFinished

Fires when a purchase prompt for Roblox Premium is closed.

MarketplaceService.PromptPremiumPurchaseFinished():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when a purchase prompt for
[Roblox Premium](https://www.roblox.com/premium/membership) closes. For
example, when a user receives the purchase prompt and clicks Cancel,
or when they receive a success or error message and click OK.

##### See also

* [PromptPremiumPurchase](/docs/reference/engine/classes/MarketplaceService#PromptPremiumPurchase)
  to prompt a user to purchase Premium.
* [PlayerMembershipChanged](/docs/reference/engine/classes/Players#PlayerMembershipChanged), which
  fires when the server recognizes that a user's membership has changed.

Provide feedback

---

PromptProductPurchaseFinished

Fires when a purchase prompt for a developer product is closed. Do not use
this event to process purchases.

MarketplaceService.PromptProductPurchaseFinished(

userId:[number](/docs/luau/numbers), productId:[number](/docs/luau/numbers), isPurchased:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [UserId](/docs/reference/engine/classes/Player#UserId) of the user who received the developer product prompt. |
| productId:[number](/docs/luau/numbers)  The ID number of the developer product shown in the prompt. Not to be confused with an asset ID. |
| isPurchased:[boolean](/docs/luau/booleans)  Indicates if the user pressed OK (true), Cancel (false) on the purchase prompt, or if the purchase prompt errored (false).  Do not use this parameter to process developer product purchases. |

IMPORTANT: Do not use the PromptProductPurchaseFinished event to
process purchases; instead, use the
[ProcessReceipt](/docs/reference/engine/classes/MarketplaceService#ProcessReceipt) callback. The
firing of PromptProductPurchaseFinished does not mean that a user
has successfully purchased an item.

This event fires when a purchase prompt for a
[developer product](/docs/production/monetization/developer-products)
closes. For example, when a user receives the purchase prompt and clicks
Cancel, or when they receive a success or error message and click
OK. The firing of this event does not mean that a user has
successfully purchased an item.

While you can use the PromptProductPurchaseFinished event to detect when
a user closes a purchase prompt, you should not use it to process
purchases because those purchases might still fail in the backend for
several reasons. For example, if a Roblox system is offline, or if the
product price has changed and the user now doesn't have enough Robux to
make the purchase. To process purchases, you must use
[ProcessReceipt](/docs/reference/engine/classes/MarketplaceService#ProcessReceipt). Using
ProcessReceipt allows you to confirm that the purchase has succeeded
before you grant the user the item they have purchased.

The PromptProductPurchaseFinished event fires with a Player.UserId
instead of a reference to the Player object.

##### See also

* [PromptGamePassPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptGamePassPurchaseFinished)
  to prompt a user to purchase a pass.
* [PromptPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptPurchaseFinished)
  to prompt a user to purchase affiliate gear or other assets.
* For more information on saving and replicating user data like purchases
  and progress, see
  [Implementing player data and purchases](https://devforum.roblox.com/t/implementing-player-data-and-purchasing-systems/2839941).

Provide feedback

---

PromptPurchaseFinished

Fires when a purchase prompt for an affiliate gear sale or other asset is
closed. Does not fire for developer product or pass prompts.

MarketplaceService.PromptPurchaseFinished(

player:[Instance](/docs/reference/engine/datatypes/Instance), assetId:[number](/docs/luau/numbers), isPurchased:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) who received the prompt. |
| assetId:[number](/docs/luau/numbers)  The asset ID of the item shown in the prompt. |
| isPurchased:[boolean](/docs/luau/booleans)  Indicates if the user pressed OK (true), Cancel (false) on the purchase prompt, or if the purchase prompt errored (false).  This might not accurately reflect if the purchase itself has been successfully processed. |

This event fires when a purchase prompt for an affiliate gear sale or
other asset closes. For example, when a user receives the purchase prompt
and clicks Cancel, or when they receive a success or error message and
click OK.

This event does not fire for
[developer product](/docs/production/monetization/developer-products)
or [pass](/docs/production/monetization/game-passes) prompts.

##### See also

* [PromptGamePassPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptGamePassPurchaseFinished)
  to prompt a user to purchase a pass.
* [PromptProductPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptProductPurchaseFinished)
  to prompt a user to purchase a developer product.
* For more information on saving and replicating user data like purchases
  and progress, see
  [Implementing player data and purchases](https://devforum.roblox.com/t/implementing-player-data-and-purchasing-systems/2839941).

Code Samples

Handling PromptPurchaseFinished Event

The below example would print 'Telamon bought an item with AssetID: 1111' to
the output, if they were to complete a transaction in (your) game with an item
that had an AssetID of 1111. Alternatively, it would print 'Telamon didn't buy
an item with AssetID: 1111' if the opposite was true.

```
local MarketplaceService = game:GetService("MarketplaceService")



local function onPromptPurchaseFinished(player, assetId, isPurchased)



if isPurchased then



print(player.Name, "bought an item with AssetID:", assetId)



else



print(player.Name, "didn't buy an item with AssetID:", assetId)



end



end



MarketplaceService.PromptPurchaseFinished:Connect(onPromptPurchaseFinished)
```

Provide feedback

---

PromptSubscriptionPurchaseFinished

Fires when a purchase prompt for a subscription is closed.

MarketplaceService.PromptSubscriptionPurchaseFinished(

user:[Player](/docs/reference/engine/classes/Player), subscriptionId:[string](/docs/luau/strings), didTryPurchasing:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who received the prompt. |
| subscriptionId:[string](/docs/luau/strings)  The ID of the subscription with a status change. |
| didTryPurchasing:[boolean](/docs/luau/booleans)  Whether the user attempted to purchase the subscription. |

This event fires when a purchase prompt for an affiliate gear sale or
other asset closes. For example, when a user receives the purchase prompt
and clicks Cancel, or when they receive a success or error message and
click OK.

##### See also

* [PromptSubscriptionPurchase](/docs/reference/engine/classes/MarketplaceService#PromptSubscriptionPurchase)
  to prompt a user to purchase a subscription.
* [UserSubscriptionStatusChanged](/docs/reference/engine/classes/Players#UserSubscriptionStatusChanged),
  which fires when the server recognizes that a user's membership has
  changed.

Provide feedback

---

Callbacks

ProcessReceipt

A callback to process receipts of developer product purchases.

MarketplaceService.ProcessReceipt(receiptInfo:[Dictionary](/docs/luau/tables#dictionaries)):[Enum.ProductPurchaseDecision](/docs/reference/engine/enums/ProductPurchaseDecision)

Parameters

|  |
| --- |
| receiptInfo:[Dictionary](/docs/luau/tables#dictionaries)  The receiptInfo table passed to this callback contains the following data:   * PurchaseId — A unique identifier for the specific purchase. * PlayerId — The user ID of the user who made the purchase. * ProductId — The ID of the purchased product. * PlaceIdWherePurchased — The place ID in which the purchase   was made. Depending on where the user is during gameplay, the   purchase place's ID can be the same as or different from the current   place's ID. * CurrencySpent — The amount of currency spent in the   transaction. * CurrencyType — The type of currency spent in the purchase;   always [Enum.CurrencyType.Robux](/docs/reference/engine/enums/CurrencyType#Robux). * ProductPurchaseChannel — How the user acquired the developer   product. One of [Enum.ProductPurchaseChannel](/docs/reference/engine/enums/ProductPurchaseChannel). |

Returns

[Enum.ProductPurchaseDecision](/docs/reference/engine/enums/ProductPurchaseDecision)

An enum that represents how the developer product receipt was
processed.

* PurchaseGranted:
  + Indicates that the experience successfully granted the player the
    developer product.
  + Indicates to Roblox that the developer product sale was
    successful.
* NotProcessedYet:
  + Indicates that the experience failed to grant the player the
    developer product.

ProcessReceipt is a callback to process receipts from
[developer product purchases](/docs/production/monetization/developer-products).
You can sell developer products inside an experience using
MarketplaceService functions, or outside an experience on the Store tab
of your experience details page.

You should only set the ProcessReceipt callback one time in a single
server-side [Script](/docs/reference/engine/classes/Script). This callback must handle the receipts
for all developer products you have for sale.

IMPORTANT: We highly recommend that you properly implement the
ProcessReceipt callback in order to sell your developer products. You
should use ProcessReceipt to grant users their purchased product over
any other granting method. If your ProcessReceipt implementation isn't
correct, you will not be able to grant users the products they have
purchased on the Store tab of your experience details page.

##### Guarantees

The ProcessReceipt callback is called for all unresolved developer
product purchases when:

* A user successfully completes the purchase of a developer product.
* A successful developer product purchase prompt appears to the user.
* A user joins the server.

A purchase is considered successfully initiated when:

* The purchase is processed on Roblox's backend.
* The funds are placed in escrow.

A purchase is considered resolved when:

* The ProcessReceipt callback returns a [Enum.ProductPurchaseDecision](/docs/reference/engine/enums/ProductPurchaseDecision)
  enum of [PurchaseGranted](/docs/reference/engine/enums/ProductPurchaseDecision#PurchaseGranted).
* The purchase is successfully recorded on Roblox's backend.

##### Unresolved developer product purchases

An unresolved developer product purchase takes place when a user's
purchase of a developer product has not yet been acknowledged by the
server through the ProcessReceipt function.

Unresolved developer product purchases are not removed or refunded after
the escrow period expires.

##### Retries and timeouts

ProcessReceipt has no time-based retry mechanism. If a user makes a
purchase that returns a [Enum.ProductPurchaseDecision](/docs/reference/engine/enums/ProductPurchaseDecision) enum of
[NotProcessedYet](/docs/reference/engine/enums/ProductPurchaseDecision#PurchaseGranted), the
ProcessReceipt callback is only called again on the same server if:

* The user successfully initiates another developer product purchase.
* The user re-joins any server under the same experience.

ProcessReceipt also has no timeout for yielded callbacks. A
ProcessReceipt callback can yield for as long as the server is running,
and the callback result is still accepted when the result returns.

##### Limitations

* If you don't implement a ProcessReceipt callback, your receipts will
  be auto-acknowledged. You can't get a receipt back after it has been
  acknowledged.
* When there are multiple purchases pending for a user, ProcessReceipt
  callbacks are called in a non-deterministic order.
* The user must be on the server for the ProcessReceipt callback to be
  invoked.
* The user does not have to be on the server for the result of the
  ProcessReceipt callback to be recorded on the backend.
* The ProcessReceipt callback for a specific purchase might run on two
  different servers at the same time if the user joins the second server
  before the callback returns on the first server.
* The ProcessReceipt callback might still fail to be recorded on the
  backend, even if it returns a [Enum.ProductPurchaseDecision](/docs/reference/engine/enums/ProductPurchaseDecision) enum of
  [PurchaseGranted](/docs/reference/engine/enums/ProductPurchaseDecision#PurchaseGranted). When
  this happens, the purchase remains unresolved.

Code Samples

ProcessReceipt Callback

The following code sample:

* Sets up the ProcessReceipt callback function to handle the purchase of two developer products for an experience.
* Checks for and records purchases using a GlobalDataStore called PurchaseHistory.
* Properly returns [PurchaseGranted](/docs/reference/engine/enums/ProductPurchaseDecision#PurchaseGranted) if the transaction completes successfully, or if the function detects that the purchase has already been granted using the PurchaseHistory data store.

After the receipt processing routine, it's possible that the purchase was granted but recording it as granted failed due to a data store error.
This is one unavoidable scenario that leads to duplicate granting of the purchase, because processReceipt() will be called for the purchase again.
You can mitigate this by keeping another in-memory record of purchases so that the same server will not grant the same purchase twice,
but you'll need a [session locking](/docs/cloud-services/data-stores/player-data-purchasing) implementation around your data store to avoid the potential of duplicate grants across servers.

```
local MarketplaceService = game:GetService("MarketplaceService")



local DataStoreService = game:GetService("DataStoreService")



local Players = game:GetService("Players")



-- Data store setup for tracking purchases that were successfully processed



local purchaseHistoryStore = DataStoreService:GetDataStore("PurchaseHistory")



local productIdByName = {



fullHeal = 123123,



gold100 = 456456,



}



-- A dictionary to look up the handler function to grant a purchase corresponding to a product ID



-- These functions return true if the purchase was granted successfully



-- These functions must never yield since they're called later within an UpdateAsync() callback



local grantPurchaseHandlerByProductId = {



[productIdByName.fullHeal] = function(_receipt, player)



local character = player.Character



local humanoid = character and character:FindFirstChild("Humanoid")



-- Ensure the player has a humanoid to heal



if not humanoid then



return false



end



-- Heal the player to full Health



humanoid.Health = humanoid.MaxHealth



-- Indicate a successful grant



return true



end,



[productIdByName.gold100] = function(_receipt, player)



local leaderstats = player:FindFirstChild("leaderstats")



local goldStat = leaderstats and leaderstats:FindFirstChild("Gold")



if not goldStat then



return false



end



-- Add 100 gold to the player's gold stat



goldStat.Value += 100



-- Indicate a successful grant



return true



end,



}



-- The core ProcessReceipt callback function



-- This implementation handles most failure scenarios but does not completely mitigate cross-server data failure scenarios



local function processReceipt(receiptInfo)



local success, result = pcall(



purchaseHistoryStore.UpdateAsync,



purchaseHistoryStore,



receiptInfo.PurchaseId,



function(isPurchased)



if isPurchased then



-- This purchase was already recorded as granted, so it must have previously been handled



-- Avoid calling the grant purchase handler here to prevent granting the purchase twice



-- While the value in the data store is already true, true is returned again so that the pcall result variable is also true



-- This will later be used to return PurchaseGranted from the receipt processor



return true



end



local player = Players:GetPlayerByUserId(receiptInfo.PlayerId)



if not player then



-- Avoids granting the purchase if the player is not in the server



-- When they rejoin, this receipt processor will be called again



return nil



end



local grantPurchaseHandler = grantPurchaseHandlerByProductId[receiptInfo.ProductId]



if not grantPurchaseHandler then



-- If there's no handler defined for this product ID, the purchase cannot be processed



-- This will never happen as long as a handler is set for every product ID sold in the experience



warn(`No purchase handler defined for product ID '{receiptInfo.ProductId}'`)



return nil



end



local handlerSucceeded, handlerResult = pcall(grantPurchaseHandler, receiptInfo, player)



if not handlerSucceeded then



local errorMessage = handlerResult



warn(



`Grant purchase handler errored while processing purchase from '{player.Name}' of product ID '{receiptInfo.ProductId}': {errorMessage}`



)



return nil



end



local didHandlerGrantPurchase = handlerResult == true



if not didHandlerGrantPurchase then



-- The handler did not grant the purchase, so record it as not granted



return nil



end



-- The purchase is now granted to the player, so record it as granted



-- This will later be used to return PurchaseGranted from the receipt processor



return true



end



)



if not success then



local errorMessage = result



warn(`Failed to process receipt due to data store error: {errorMessage}`)



return Enum.ProductPurchaseDecision.NotProcessedYet



end



local didGrantPurchase = result == true



return if didGrantPurchase



then Enum.ProductPurchaseDecision.PurchaseGranted



else Enum.ProductPurchaseDecision.NotProcessedYet



end



-- Set the callback; this can only be done once by one script on the server



MarketplaceService.ProcessReceipt = processReceipt
```

Provide feedback

---