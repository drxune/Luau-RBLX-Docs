# AdService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AdService
Scraped: 2026-01-11T02:37:10.412579Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- AdService
- Player
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AdService](/docs/reference/engine/classes/AdService)

English

Feedback

Engine Class

AdService

A class that allows the display of mobile video ads.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [CreateAdRewardFromDevProductId](#CreateAdRewardFromDevProductId)(devProductId: [number](/docs/luau/numbers)):AdReward |
| [GetAdAvailabilityNowAsync](#GetAdAvailabilityNowAsync)(adFormat: [Enum.AdFormat](/docs/reference/engine/enums/AdFormat)):Variant |
| [RegisterAdOpportunityAsync](#RegisterAdOpportunityAsync)(instance: [Instance](/docs/reference/engine/datatypes/Instance),placementId: [number](/docs/luau/numbers)?):() |
| [ShowRewardedVideoAdAsync](#ShowRewardedVideoAdAsync)(player: [Player](/docs/reference/engine/classes/Player),reward: AdReward,placementId: [number](/docs/luau/numbers)?):[Enum.ShowAdResult](/docs/reference/engine/enums/ShowAdResult) |
| [ShowVideoAd](#ShowVideoAd)():()  Deprecated |
| [UnregisterAdOpportunity](#UnregisterAdOpportunity)(instance: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Events

|  |
| --- |
| [VideoAdClosed](#VideoAdClosed)(adShown: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A service for displaying mobile video ads as a form of monetization. Use it to
implement rewarded video ads in your experience.

---

API Reference

Methods

CreateAdRewardFromDevProductId

Creates a reward to give users who watch an entire video ad.

AdService:CreateAdRewardFromDevProductId(devProductId:[number](/docs/luau/numbers)):AdReward

Parameters

|  |
| --- |
| devProductId:[number](/docs/luau/numbers)  The ID of the developer product you want to grant as a reward. |

Returns

AdReward

Creates a reward to give users who watch an entire video ad.

Provide feedback

---

GetAdAvailabilityNowAsync

Yields

Checks if a video ad is available to be played to the current user inside
the experience.

AdService:GetAdAvailabilityNowAsync(adFormat:[Enum.AdFormat](/docs/reference/engine/enums/AdFormat)):Variant

Parameters

|  |
| --- |
| adFormat:[Enum.AdFormat](/docs/reference/engine/enums/AdFormat)  The format of the requested ad. For example, RewardedVideo. |

Returns

Variant

Checks if a video ad is available to be played to the current user inside
the experience.

Code Samples

```
local adAvailabilityResult = AdService:GetAdAvailabilityNow(Enum.AdFormat.RewardedVideo)
```

Provide feedback

---

RegisterAdOpportunityAsync

Yields

Tracks how many times a user had the chance to watch a video ad and the
rate at which they actually watched the ad.

AdService:RegisterAdOpportunityAsync(

instance:[Instance](/docs/reference/engine/datatypes/Instance), placementId:[number](/docs/luau/numbers)?

):()

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance) |
| placementId:[number](/docs/luau/numbers)?  The ID of the placement of the rewarded video ad inside the experience. Allows for reporting on the performance of individual ad placements. |

Returns

()

Code Samples

Track ad opportunities

Tracks ad opportunities for rewarded video ads.

```
local AdService = game:GetService("AdService")



local playerGui = game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui")



-- Create the ScreenGui and the Button



local screenGui = Instance.new("ScreenGui", playerGui)



local adButton = Instance.new("TextButton", screenGui)



-- Register the button with AdService



local success, err = pcall(function()



-- The second parameter is an optional Placement ID (UUID) parameter generated in the Creator Hub.



-- If you choose not to provide a Placement ID, the ad opportunity is tracked under the default placement.



AdService:RegisterAdOpportunityAsync(adButton, "123e4567-e89b-12d3-a456-426614174000")



end)



if not success then



warn("Failed to register ad opportunity:", err)



end
```

Provide feedback

---

ShowRewardedVideoAdAsync

Yields

Plays the video ad to the current user inside the experience.

AdService:ShowRewardedVideoAdAsync(

player:[Player](/docs/reference/engine/classes/Player), reward:AdReward, placementId:[number](/docs/luau/numbers)?

):[Enum.ShowAdResult](/docs/reference/engine/enums/ShowAdResult)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The Player object for whom you are fetching the ad for. |
| reward:AdReward  The reward object for the reward you want to grant the user who watches an ad to completion. |
| placementId:[number](/docs/luau/numbers)?  The ID of the placement of the rewarded video ad inside the experience. Allows for reporting on the performance of individual ad placements. |

Returns

[Enum.ShowAdResult](/docs/reference/engine/enums/ShowAdResult)

Plays the video ad to the current user inside the experience.

Code Samples

```
local reward = AdService:CreateAdRewardFromDevProductId(100)



local result = AdService:ShowRewardedVideoAdAsync(player, reward)
```

Provide feedback

---

ShowVideoAd

Deprecated

Show details

---

UnregisterAdOpportunity

AdService:UnregisterAdOpportunity(instance:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

Provide feedback

---

Events

VideoAdClosed

Deprecated

Show details

---