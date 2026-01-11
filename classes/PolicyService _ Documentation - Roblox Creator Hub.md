# PolicyService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PolicyService
Scraped: 2026-01-11T02:28:09.889337Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- PolicyService
- Player
- Players
- LocalizationService:GetCountryRegionForPlayerAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PolicyService](/docs/reference/engine/classes/PolicyService)

English

Feedback

Engine Class

PolicyService

Helps you query information regarding policy compliance for players around the
world based on age range, location, and platform type.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [CanViewBrandProjectAsync](#CanViewBrandProjectAsync)(player: [Player](/docs/reference/engine/classes/Player),brandProjectId: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [GetPolicyInfoForPlayerAsync](#GetPolicyInfoForPlayerAsync)(player: [Instance](/docs/reference/engine/datatypes/Instance)):[Dictionary](/docs/luau/tables#dictionaries) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

PolicyService helps you query information regarding policy compliance for
players around the world based on age range, location, and platform type.

---

API Reference

Methods

CanViewBrandProjectAsync

Yields

Determines if a user can see brand project assets inside your experience.

PolicyService:CanViewBrandProjectAsync(

player:[Player](/docs/reference/engine/classes/Player), brandProjectId:[string](/docs/luau/strings)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The Player object you're trying to show the brand project to. |
| brandProjectId:[string](/docs/luau/strings)  The brand project ID provided by Roblox. Represents all assets associated with a brand project. |

Returns

[boolean](/docs/luau/booleans)

Whether or not the brand project can be shown to the specific user.

Determines if a user can see brand project assets inside your experience.
This method lets you work with brands to only show commercial assets to
brand-compliant audiences.

To use CanViewBrandProjectAsync, you must use a brand project ID
provided by Roblox. To request a brand project ID,
[contact
us](https://docs.google.com/forms/d/e/1FAIpQLSfGTRQwATB2wUg0P4HUSTtyXrhptFahJifo1ew84SyqtfSBfg/viewform).

You must call this method on a server-side Script and wrap it in a
[pcall()](/docs/reference/engine/globals/LuaGlobals#pcall).

Code Samples

Server-side code sample

You must call CanViewBrandProjectAsync from the server-side and then fire an event on the client. Calling this method from the client-side returns an error.

```
-- In ServerScriptService



local Players = game:GetService("Players")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local PolicyService = game:GetService("PolicyService")



-- Pre-created RemoteEvent in ReplicatedStorage



local RemoteEvent = ReplicatedStorage:WaitForChild("RemoteEvent")



local brandedAsset = ReplicatedStorage:WaitForChild("BrandedAsset")



local defaultAsset = Instance.new("Part")



Players.PlayerAdded:Connect(function(player)



-- PolicyService:CanViewBrandProjectAsync can only be called from the Server



local success, canView = pcall(function()



return PolicyService:CanViewBrandProjectAsync(player, "BRP-0123456789")



end)



if success and canView then



RemoteEvent:FireClient(player, brandedAsset)



else



RemoteEvent:FireClient(player, defaultAsset)



end



end)
```

Client-side code sample

```
-- In StarterPlayerScripts



local Players = game:GetService("Players")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



-- Pre-created RemoteEvent in ReplicatedStorage



local RemoteEvent = ReplicatedStorage:WaitForChild("RemoteEvent")



RemoteEvent.OnClientEvent:Connect(function(partToLoad)



local clonedPart = partToLoad:Clone()



clonedPart.Parent = workspace



end)
```

Provide feedback

---

GetPolicyInfoForPlayerAsync

Yields

Returns policy information about a player based on geolocation, age group,
and platform.

PolicyService:GetPolicyInfoForPlayerAsync(player:[Instance](/docs/reference/engine/datatypes/Instance)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) to get policy information for. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary containing information about the policy information of
the requested player; see above for the dictionary structure.

Returns policy information about a player based on geolocation, age group,
and platform. The structure of the returned dictionary is as follows:

| Name | Type | Required for | Description |
| --- | --- | --- | --- |
| AreAdsAllowed | Boolean | Any experience that includes [immersive ads](/docs/production/monetization/immersive-ads). | When true, the player might see immersive ads within an experience. |
| ArePaidRandomItemsRestricted | Boolean | Any experience that has paid random items. | When true, the player can **not** interact with paid random item generators, either via in‑experience currency bought with Robux or Robux directly. |
| AllowedExternalLinkReferences | Array | Any experience that references external links. | A list of external link references such as social media links, handles, or iconography that a player is permitted to see. Possible values include "Discord", "Facebook", "Twitch", "YouTube", "X", "GitHub", and "Guilded". |
| IsContentSharingAllowed | Boolean | Any feature in the experience that enables users to create content (e.g. text, images, video, audio) that other users can see in the experience or allows user to share content within experiences. | When true, the player can use features related to sharing UGC within an experience, such as uploading a screen capture, sharing a video, or posting an image to a content feed that other users can see. |
| IsEligibleToPurchaseCommerceProduct | Boolean | Any experience that wants to sell [commerce products](/docs/production/monetization/commerce-products). | When true, the player is eligible to purchase commerce products within an experience. |
| IsEligibleToPurchaseSubscription | Boolean | Any experience that wants to sell subscriptions. | When true, the player is eligible to purchase subscriptions within an experience. |
| IsPaidItemTradingAllowed | Boolean | Any experience that allows users to purchase virtual items that they can trade with other players. | When true, the player can trade virtual items that they purchased with in-experience currency or Robux. |
| IsPhotoToAvatarAllowed | Boolean | Any experience that uses the Photo-to-Avatar APIs. | When true, the Photo-to-Avatar API `Class.AvatarCreationService: PromptSelectAvatarGenerationImageAsync()` is available to the player. |
| IsSubjectToChinaPolicies | Boolean | Any experience that is available in China. | When true, an experience should enforce compliance changes. See [this forum post](https://devforum.roblox.com/t/new-programs-available-roblox-china-licensed-to-operate/1023361) for more information. |

##### Exceptions

Like any async call, this method needs to be wrapped in
[pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) and error-handled properly. A full list of
possible error messages and their reasons is:

| Message | Reason |
| --- | --- |
| Instance was not a player | The player parameter is not a [Player](/docs/reference/engine/classes/Player) instance. |
| Players not found | Internal error that the [Players](/docs/reference/engine/classes/Players) object is missing. |
| This method cannot be called on the client for a non-local player | This method cannot be called on the client for a non-local [Player](/docs/reference/engine/classes/Player). |
| GetPolicyInfoForPlayerAsync is called too many times | Internal error that GetPolicyInfoForPlayerAsync() is called more than 100 (current setting) times before an HTTP response comes back. |

See also [LocalizationService:GetCountryRegionForPlayerAsync()](/docs/reference/engine/classes/LocalizationService#GetCountryRegionForPlayerAsync)
which returns a country/region code string according to the player's
client IP geolocation.

Code Samples

Getting Policy Information for a Player

This code sample gets policy information for the local player and warns if
they cannot interact with paid random item generators.

```
local PolicyService = game:GetService("PolicyService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local success, result = pcall(function()



return PolicyService:GetPolicyInfoForPlayerAsync(player)



end)



if not success then



warn("PolicyService error: " .. result)



elseif result.ArePaidRandomItemsRestricted then



warn("Player cannot interact with paid random item generators")



end
```

Getting Policy Information for a Player

This code sample gets policy information for the local player and warns if
they cannot purchase a real-world commerce product.

```
local PolicyService = game:GetService("PolicyService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local success, result = pcall(function()



return PolicyService:GetPolicyInfoForPlayerAsync(player)



end)



if not success then



warn("PolicyService error: " .. result)



elseif not result.IsEligibleToPurchaseCommerceProduct then



warn("Player is not eligible to purchase commerce products")



end
```

Provide feedback

---