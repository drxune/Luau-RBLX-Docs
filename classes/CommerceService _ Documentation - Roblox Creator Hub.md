# CommerceService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CommerceService
Scraped: 2026-01-11T02:40:04.281081Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- CommerceService
- Player
- Object
- CommerceService:PromptCommerceProductPurchase()
- PolicyService.IsEligibleToPurchaseCommerceProduct
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [CommerceService](/docs/reference/engine/classes/CommerceService)

English

Feedback

Engine Class

CommerceService

Supports real-world purchases that you can bundle with digital benefits.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [GetCommerceProductInfoAsync](#GetCommerceProductInfoAsync)(commerceProductId: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries) |
| [PromptCommerceProductPurchase](#PromptCommerceProductPurchase)(user: [Player](/docs/reference/engine/classes/Player),commerceProductId: [string](/docs/luau/strings)):() |
| [PromptRealWorldCommerceBrowser](#PromptRealWorldCommerceBrowser)(player: [Player](/docs/reference/engine/classes/Player),url: [string](/docs/luau/strings)):() |
| [UserEligibleForRealWorldCommerceAsync](#UserEligibleForRealWorldCommerceAsync)():[boolean](/docs/luau/booleans) |

Events

|  |
| --- |
| [PromptCommerceProductPurchaseFinished](#PromptCommerceProductPurchaseFinished)(user: [Player](/docs/reference/engine/classes/Player),productId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[CommerceService](/docs/reference/engine/classes/CommerceService) is a service that supports real-world purchases that
you can bundle with virtual items. For information on eligibility and
implementation, see
[Commerce products](/docs/production/monetization/commerce-products).

---

API Reference

Methods

GetCommerceProductInfoAsync

Yields

Retrieves information about the commerce products you are selling in
experience.

CommerceService:GetCommerceProductInfoAsync(commerceProductId:[string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| commerceProductId:[string](/docs/luau/strings) |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Retrieves information about the products that you are selling and surface
them within your experience. How you surface products to your users is
entirely up to you.

| Name | string | Localized name of of the physical item |
| --- | --- | --- |
| Description | string | Localized description of the physical item |
| IconImageAssetId | number | The image asset ID of main default image of the physical item |
| DisplayPrice | string | Localized price string with currency symbol of the physical item. e.g. “$4.99“ |
| IsPurchasable | bool | If the item can be added to a merchant checkout session, i.e. item is in stock, or can be backordered |

Provide feedback

---

PromptCommerceProductPurchase

Prompts a user to purchase a commerce product using the provided
commerceProductId. Opens a webview that guides the user through the
purchasing flow.

CommerceService:PromptCommerceProductPurchase(

user:[Player](/docs/reference/engine/classes/Player), commerceProductId:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player) |
| commerceProductId:[string](/docs/luau/strings) |

Returns

()

Prompts a user to purchase a commerce product using the provided
commerceProductId. Opens a webview that guides the user through the
purchasing flow.

Provide feedback

---

PromptRealWorldCommerceBrowser

CommerceService:PromptRealWorldCommerceBrowser(

player:[Player](/docs/reference/engine/classes/Player), url:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |
| url:[string](/docs/luau/strings) |

Returns

()

This is a legacy endpoint that is not meant for use. To open the webview
to the purchasing flow for real world commerce, see
[CommerceService:PromptCommerceProductPurchase()](/docs/reference/engine/classes/CommerceService#PromptCommerceProductPurchase). For more
information, see
[Commerce products](/docs/production/monetization/commerce-products)

Provide feedback

---

UserEligibleForRealWorldCommerceAsync

Yields

CommerceService:UserEligibleForRealWorldCommerceAsync():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

This is a legacy endpoint that is not meant for use. To check if a user is
eligible for real world commerce, see
[PolicyService.IsEligibleToPurchaseCommerceProduct](/docs/reference/engine/classes/PolicyService#IsEligibleToPurchaseCommerceProduct). For more
information, see
[Commerce products](/docs/production/monetization/commerce-products)

Provide feedback

---

Events

PromptCommerceProductPurchaseFinished

Fires when commerce purchase webview has closed - not an indicator that a
purchase was successful.

CommerceService.PromptCommerceProductPurchaseFinished(

user:[Player](/docs/reference/engine/classes/Player), productId:[string](/docs/luau/strings)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player) |
| productId:[string](/docs/luau/strings) |

Use this signal to detect when a user has completed the purchasing flow
and the webview has closed to resume gameplay within the experience.
This signal does not indicate a successful purchase, so do not grant
virtual items solely from this signal.

While optional, it is recommended to use this signal to reorient your
users on Android, as the commerce purchasing flow will have forced them
into portrait mode.

Provide feedback

---