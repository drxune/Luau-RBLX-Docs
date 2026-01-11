# AnalyticsService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AnalyticsService
Scraped: 2026-01-11T02:42:06.875485Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- AnalyticsService
- Player
- Object
- AnalyticsService:LogCustomEvent()
- HttpService:GenerateGUID()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AnalyticsService](/docs/reference/engine/classes/AnalyticsService)

English

Feedback

Engine Class

AnalyticsService

Collection of methods that allows developers to track how users interact with
their experiences.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [ApiKey](#ApiKey):[string](/docs/luau/strings)  Deprecated |

Methods

|  |
| --- |
| [FireCustomEvent](#FireCustomEvent)(player: [Instance](/docs/reference/engine/datatypes/Instance),eventCategory: [string](/docs/luau/strings),customData: Variant):()  Deprecated |
| [FireEvent](#FireEvent)(category: [string](/docs/luau/strings),value: Variant):()  Deprecated |
| [FireInGameEconomyEvent](#FireInGameEconomyEvent)(player: [Instance](/docs/reference/engine/datatypes/Instance),itemName: [string](/docs/luau/strings),economyAction: [Enum.AnalyticsEconomyAction](/docs/reference/engine/enums/AnalyticsEconomyAction),itemCategory: [string](/docs/luau/strings),amount: [number](/docs/luau/numbers),currency: [string](/docs/luau/strings),location: Variant,customData: Variant):()  Deprecated |
| [FireLogEvent](#FireLogEvent)(player: [Instance](/docs/reference/engine/datatypes/Instance),logLevel: [Enum.AnalyticsLogLevel](/docs/reference/engine/enums/AnalyticsLogLevel),message: [string](/docs/luau/strings),debugInfo: Variant,customData: Variant):()  Deprecated |
| [FirePlayerProgressionEvent](#FirePlayerProgressionEvent)(player: [Instance](/docs/reference/engine/datatypes/Instance),category: [string](/docs/luau/strings),progressionStatus: [Enum.AnalyticsProgressionStatus](/docs/reference/engine/enums/AnalyticsProgressionStatus),location: Variant,statistics: Variant,customData: Variant):()  Deprecated |
| [LogCustomEvent](#LogCustomEvent)(player: [Player](/docs/reference/engine/classes/Player),eventName: [string](/docs/luau/strings),value: [number](/docs/luau/numbers),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogEconomyEvent](#LogEconomyEvent)(player: [Player](/docs/reference/engine/classes/Player),flowType: [Enum.AnalyticsEconomyFlowType](/docs/reference/engine/enums/AnalyticsEconomyFlowType),currencyType: [string](/docs/luau/strings),amount: [number](/docs/luau/numbers),endingBalance: [number](/docs/luau/numbers),transactionType: [string](/docs/luau/strings),itemSku: [string](/docs/luau/strings),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogFunnelStepEvent](#LogFunnelStepEvent)(player: [Player](/docs/reference/engine/classes/Player),funnelName: [string](/docs/luau/strings),funnelSessionId: [string](/docs/luau/strings),step: [number](/docs/luau/numbers),stepName: [string](/docs/luau/strings),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogOnboardingFunnelStepEvent](#LogOnboardingFunnelStepEvent)(player: [Player](/docs/reference/engine/classes/Player),step: [number](/docs/luau/numbers),stepName: [string](/docs/luau/strings),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogProgressionCompleteEvent](#LogProgressionCompleteEvent)(player: [Player](/docs/reference/engine/classes/Player),progressionPathName: [string](/docs/luau/strings),level: [number](/docs/luau/numbers),levelName: [string](/docs/luau/strings),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogProgressionEvent](#LogProgressionEvent)(player: [Player](/docs/reference/engine/classes/Player),progressionPathName: [string](/docs/luau/strings),status: [Enum.AnalyticsProgressionType](/docs/reference/engine/enums/AnalyticsProgressionType),level: [number](/docs/luau/numbers),levelName: [string](/docs/luau/strings),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogProgressionFailEvent](#LogProgressionFailEvent)(player: [Player](/docs/reference/engine/classes/Player),progressionPathName: [string](/docs/luau/strings),level: [number](/docs/luau/numbers),levelName: [string](/docs/luau/strings),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogProgressionStartEvent](#LogProgressionStartEvent)(player: [Player](/docs/reference/engine/classes/Player),progressionPathName: [string](/docs/luau/strings),level: [number](/docs/luau/numbers),levelName: [string](/docs/luau/strings),customFields: [Dictionary](/docs/luau/tables#dictionaries)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

AnalyticsService is a collection of methods that allows developers to
track how users interact with their experiences, specifically player
progression, in-experience economy, funnels, and custom events.

---

API Reference

Properties

ApiKey

Deprecated

Show details

---

Methods

FireCustomEvent

Deprecated

Show details

---

FireEvent

Deprecated

Show details

---

FireInGameEconomyEvent

Deprecated

Show details

---

FireLogEvent

Deprecated

Show details

---

FirePlayerProgressionEvent

Deprecated

Show details

---

LogCustomEvent

Logs an event used to track custom metrics of a user in experience.

AnalyticsService:LogCustomEvent(

player:[Player](/docs/reference/engine/classes/Player), eventName:[string](/docs/luau/strings), value:[number](/docs/luau/numbers), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The user who triggered the event. |
| eventName:[string](/docs/luau/strings)  The name of the custom event. |
| value:[number](/docs/luau/numbers) Default Value: 1 The value of the event that will be used in aggregation. |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Optional dictionary of custom fields that will provide breakdowns in Roblox-provided charts. Only specific keys, provided by [Enum.AnalyticsCustomFieldKeys](/docs/reference/engine/enums/AnalyticsCustomFieldKeys), will be used for these breakdowns. Limited to 8,000 unique combinations of values across the three custom fields per experience. |

Returns

()

Logs an event used to track custom metrics of a user in experience. For
additional information, see
[Custom Events](/docs/production/analytics/custom-events).

Code Samples

Log Custom Event

This example uses [AnalyticsService:LogCustomEvent()](/docs/reference/engine/classes/AnalyticsService#LogCustomEvent) to log two custom events: MissionStarted and MissionCompletedDuration.

```
local AnalyticsService = game:GetService("AnalyticsService")



-- Log when the mission starts



AnalyticsService:LogCustomEvent(



player,



"MissionStarted" -- Custom event name



)



-- Log when the mission is completed with the time it took



AnalyticsService:LogCustomEvent(



player,



"MissionCompletedDuration", -- Custom event name



120 -- Event value used in aggregation



)
```

Provide feedback

---

LogEconomyEvent

Logs an event used to track player actions related in experience.

AnalyticsService:LogEconomyEvent(

player:[Player](/docs/reference/engine/classes/Player), flowType:[Enum.AnalyticsEconomyFlowType](/docs/reference/engine/enums/AnalyticsEconomyFlowType), currencyType:[string](/docs/luau/strings), amount:[number](/docs/luau/numbers), endingBalance:[number](/docs/luau/numbers), transactionType:[string](/docs/luau/strings), itemSku:[string](/docs/luau/strings), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The user who triggered the event. |
| flowType:[Enum.AnalyticsEconomyFlowType](/docs/reference/engine/enums/AnalyticsEconomyFlowType)  Should specify the direction that currency is flowing using [Enum.AnalyticsEconomyFlowType](/docs/reference/engine/enums/AnalyticsEconomyFlowType). |
| currencyType:[string](/docs/luau/strings)  The name of the currency being added or removed, for example "gold", "gems", or "energy". Limited to 5 unique currency types per experience. |
| amount:[number](/docs/luau/numbers)  The amount of currency being added or removed. This value should always be positive. |
| endingBalance:[number](/docs/luau/numbers)  The user's balance after the currency has been added or removed. This value should always be greater than or equal to 0. |
| transactionType:[string](/docs/luau/strings)  The type of transaction that occurred. While you're free to use any transaction type, it's recommended to use the provided types from [Enum.AnalyticsEconomyTransactionType](/docs/reference/engine/enums/AnalyticsEconomyTransactionType) such as "IAP" or "ContextualPurchase" to enable future insights from Roblox tools and charts.  Because this field type is a string, you'll need to pass the Name value of the enum. For example [Enum.AnalyticsEconomyTransactionType.IAP.Name](/docs/reference/engine/enums/AnalyticsEconomyTransactionType).  Limited to 20 unique types per experience. |
| itemSku:[string](/docs/luau/strings)  Optional SKU of the item or bundle being purchased. This is a unique identifier for the item being purchased. Limited to 100 unique SKUs per experience. |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Optional dictionary of custom fields that will provide breakdowns in Roblox-provided charts. Only specific keys, provided by [Enum.AnalyticsCustomFieldKeys](/docs/reference/engine/enums/AnalyticsCustomFieldKeys), will be used for these breakdowns. Limited to 8,000 unique combinations of values across the three custom fields per experience. |

Returns

()

Logs an event used to track player actions related in experience.

Code Samples

Tracking an in-app purchase

The following sample tracks a Robux purchase of a 1000-coin bundle, using the IAP (in-app purchase) transaction type. Note the item name provided as an optional parameter when compared to the previous sample.

```
local AnalyticsService = game:GetService("AnalyticsService")



AnalyticsService:LogEconomyEvent(



player,



Enum.AnalyticsEconomyFlowType.Source,



"Coins",



1000, -- How many coins are in the bundle



1020, -- balance after transaction



Enum.AnalyticsEconomyTransactionType.IAP.Name,



"1000CoinBundle" -- Unique identifier of the coin bundle



)
```

Provide feedback

---

LogFunnelStepEvent

Logs an event used to track user actions stepping through a pre-planned
funnel.

AnalyticsService:LogFunnelStepEvent(

player:[Player](/docs/reference/engine/classes/Player), funnelName:[string](/docs/luau/strings), funnelSessionId:[string](/docs/luau/strings), step:[number](/docs/luau/numbers), stepName:[string](/docs/luau/strings), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The user who triggered the event. |
| funnelName:[string](/docs/luau/strings)  The name of the funnel. This should be the same for all steps in the funnel. Limited to 10 unique funnels per experience. |
| funnelSessionId:[string](/docs/luau/strings)  Optional unique identifier for the funnel session. This should be the same for all steps in the funnel.  Note that this field is only necessary for recurring funnels, for example a purchase flow funnel or an item upgrade funnel. If you don't have a natural funnel session identifier, it's recommended to use [HttpService:GenerateGUID()](/docs/reference/engine/classes/HttpService#GenerateGUID). |
| step:[number](/docs/luau/numbers) Default Value: 1 The step number in the funnel. This should be unique for each step in the funnel. All funnels start at step 1. Limited to steps 1-100.  Repeated steps by the same user in the same funnel session, or when funnelSessionId is nil will be ignored.  Note that if any steps are skipped, the intermediate steps will be considered completed. |
| stepName:[string](/docs/luau/strings)  Optional name of the step in the funnel. This field is only used for display purposes in Roblox-provided charts. |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Optional dictionary of custom fields that will provide breakdowns in Roblox-provided charts. Only specific keys, provided by [Enum.AnalyticsCustomFieldKeys](/docs/reference/engine/enums/AnalyticsCustomFieldKeys), will be used for these breakdowns. Limited to 8,000 unique combinations of values across the three custom fields per experience. |

Returns

()

Logs an event used to track user actions stepping through a pre-planned
funnel. Funnel breakdowns will only consider the user and event values
from the first step in a funnel session.

Code Samples

Tracking Shop steps

The following sample tracks some basic events for each user beginning the process to buy an item from an "armory" shop. Note the funnelSessionId used to distinguish between different sessions of the same user opening the shop.

```
local AnalyticsService = game:GetService("AnalyticsService")



local HttpService = game:GetService("HttpService")



funnelSessionId = HttpService:GenerateGUID()



-- Log when the user opens the store



AnalyticsService:LogFunnelStepEvent(



player,



"ArmoryCheckout", -- Funnel name used to group steps together



funnelSessionId, -- Funnel session ID for this unique checkout session



1, -- Step number



"Opened Store" -- Step name



)



-- Log when the user views an item



AnalyticsService:LogFunnelStepEvent(



player,



"ArmoryCheckout", -- Funnel name used to group steps together



funnelSessionId, -- Funnel session ID for this unique checkout session



2, -- Step number



"Viewed Item" -- Step name



)



-- Log when the user views adds to cart



AnalyticsService:LogFunnelStepEvent(



player,



"ArmoryCheckout", -- Funnel name used to group steps together



funnelSessionId, -- Funnel session ID for this unique checkout session



3, -- Step number



"Added to Cart" -- Step name



)
```

Provide feedback

---

LogOnboardingFunnelStepEvent

Logs an event used to track user actions stepping through an onboarding
funnel.

AnalyticsService:LogOnboardingFunnelStepEvent(

player:[Player](/docs/reference/engine/classes/Player), step:[number](/docs/luau/numbers), stepName:[string](/docs/luau/strings), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The user who triggered the event. |
| step:[number](/docs/luau/numbers)  The step number in the funnel. This should be unique for each step in the funnel. All funnels start at step 1. Limited to steps 1-100.  Note that if any steps are skipped, the intermediate steps will be considered completed. |
| stepName:[string](/docs/luau/strings)  Optional name of the step in the funnel. This field is only used for display purposes in Roblox-provided charts. |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Optional dictionary of custom fields that will provide breakdowns in Roblox-provided charts. Only specific keys, provided by [Enum.AnalyticsCustomFieldKeys](/docs/reference/engine/enums/AnalyticsCustomFieldKeys), will be used for these breakdowns. Limited to 8,000 unique combinations of values across the three custom fields per experience. |

Returns

()

Logs an event used to track user actions stepping through an onboarding
funnel. Funnel breakdowns will only consider the user and event values
from the first step in a funnel session.

Code Samples

Tracking onboarding steps

The following sample demonstrates how to log two steps of an onboarding funnel. An onboarding funnel typically introduces players to the game's core loop.

```
local AnalyticsService = game:GetService("AnalyticsService")



-- Log the first step of the FTUE



AnalyticsService:LogOnboardingFunnelStepEvent(



player,



1, -- Step number



"Joined Game" -- Step name



)



-- Log the second step of the FTUE



AnalyticsService:LogOnboardingFunnelStepEvent(



player,



2, -- Step number



"Choose Class" -- Step name



)
```

Provide feedback

---

LogProgressionCompleteEvent

Logs an event for when a user has completed a level attempt.

AnalyticsService:LogProgressionCompleteEvent(

player:[Player](/docs/reference/engine/classes/Player), progressionPathName:[string](/docs/luau/strings), level:[number](/docs/luau/numbers), levelName:[string](/docs/luau/strings), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The player who triggered the event. |
| progressionPathName:[string](/docs/luau/strings) |
| level:[number](/docs/luau/numbers) |
| levelName:[string](/docs/luau/strings) |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" |

Returns

()

Logs an event for when a user has completed a level attempt. This event
does not currently display in any Roblox-provided charts.

Provide feedback

---

LogProgressionEvent

Logs an event for when a user has started, completed, or failed a level
attempt.

AnalyticsService:LogProgressionEvent(

player:[Player](/docs/reference/engine/classes/Player), progressionPathName:[string](/docs/luau/strings), status:[Enum.AnalyticsProgressionType](/docs/reference/engine/enums/AnalyticsProgressionType), level:[number](/docs/luau/numbers), levelName:[string](/docs/luau/strings), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The player who triggered the event. |
| progressionPathName:[string](/docs/luau/strings) |
| status:[Enum.AnalyticsProgressionType](/docs/reference/engine/enums/AnalyticsProgressionType) |
| level:[number](/docs/luau/numbers) |
| levelName:[string](/docs/luau/strings) |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" |

Returns

()

Logs an event for when a user has started, completed, or failed a level
attempt. This event does not currently display in any Roblox-provided
charts.

Provide feedback

---

LogProgressionFailEvent

Logs an event for when a user has failed a level attempt.

AnalyticsService:LogProgressionFailEvent(

player:[Player](/docs/reference/engine/classes/Player), progressionPathName:[string](/docs/luau/strings), level:[number](/docs/luau/numbers), levelName:[string](/docs/luau/strings), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The user who triggered the event. |
| progressionPathName:[string](/docs/luau/strings) |
| level:[number](/docs/luau/numbers) |
| levelName:[string](/docs/luau/strings) |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" |

Returns

()

Logs an event for when a user has failed a level attempt. This event does
not currently display in any Roblox-provided charts.

Provide feedback

---

LogProgressionStartEvent

Logs an event for when a user has started a level attempt.

AnalyticsService:LogProgressionStartEvent(

player:[Player](/docs/reference/engine/classes/Player), progressionPathName:[string](/docs/luau/strings), level:[number](/docs/luau/numbers), levelName:[string](/docs/luau/strings), customFields:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The player who triggered the event. |
| progressionPathName:[string](/docs/luau/strings) |
| level:[number](/docs/luau/numbers) |
| levelName:[string](/docs/luau/strings) |
| customFields:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" |

Returns

()

Logs an event for when a user has started a level attempt. This event does
not currently display in any Roblox-provided charts.

Provide feedback

---