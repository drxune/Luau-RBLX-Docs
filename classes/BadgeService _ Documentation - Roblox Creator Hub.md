# BadgeService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BadgeService
Scraped: 2026-01-11T02:36:05.128059Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- BadgeService
- Player.UserId
- Player
- UserId
- Script
- ModuleScript
- LocalScript
- BadgeService:GetBadgeInfoAsync()
- BadgeService:UserHasBadgeAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [BadgeService](/docs/reference/engine/classes/BadgeService)

English

Feedback

Engine Class

BadgeService

Provides information on badges and awards them.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [AwardBadgeAsync](#AwardBadgeAsync)(userId: [number](/docs/luau/numbers),badgeId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [AwardBadge](#AwardBadge)(userId: [number](/docs/luau/numbers),badgeId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [CheckUserBadgesAsync](#CheckUserBadgesAsync)(userId: [number](/docs/luau/numbers),badgeIds: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |
| [GetBadgeInfoAsync](#GetBadgeInfoAsync)(badgeId: [number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries) |
| [IsDisabled](#IsDisabled)(badgeId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [IsLegal](#IsLegal)(badgeId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [UserHasBadge](#UserHasBadge)(userId: [number](/docs/luau/numbers),badgeId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [UserHasBadgeAsync](#UserHasBadgeAsync)(userId: [number](/docs/luau/numbers),badgeId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

BadgeService provides information and functionality related to
[badges](/docs/production/publishing/badges). Badges are used across the
platform to recognize a player's achievements and activity. Upon awarding a
badge to a player, it is added to their inventory and displayed on their
profile page.

---

API Reference

Methods

AwardBadgeAsync

Yields

Award a badge to a player given the ID of each.

BadgeService:AwardBadgeAsync(

userId:[number](/docs/luau/numbers), badgeId:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the user the badge is to be awarded to. |
| badgeId:[number](/docs/luau/numbers)  The ID of the badge to be awarded. |

Returns

[boolean](/docs/luau/booleans)

Boolean of true if the badge was awarded successfully.

Grants a [Player](/docs/reference/engine/classes/Player) a badge with the [UserId](/docs/reference/engine/classes/Player#UserId) and
the badge ID.

In order to successfully award a badge:

* The player must be presently connected to the experience.
* The player must not already have the badge (note that a player may
  delete an awarded badge from their profile and be awarded the badge
  again).
* The badge must be awarded from a server-side [Script](/docs/reference/engine/classes/Script) or a
  [ModuleScript](/docs/reference/engine/classes/ModuleScript) eventually required by a [Script](/docs/reference/engine/classes/Script), not from a
  [LocalScript](/docs/reference/engine/classes/LocalScript).
* The badge must be awarded in a place that is part of the experience
  associated with the badge.
* The badge must be enabled; check this using the IsEnabled property of
  the badge fetched through [BadgeService:GetBadgeInfoAsync()](/docs/reference/engine/classes/BadgeService#GetBadgeInfoAsync).

Rate limit is 50 + 35 \* [number of users] per minute.

Code Samples

Awarding a Badge

The following example creates an awardBadge() function that handles
potential errors that may occur when awarding a badge.

```
local BadgeService = game:GetService("BadgeService")



local Players = game:GetService("Players")



local BADGE_ID = 0



local function awardBadge(player, badgeId)



-- Fetch badge information



local success, badgeInfo = pcall(function()



return BadgeService:GetBadgeInfoAsync(badgeId)



end)



if success then



-- Confirm that badge can be awarded



if badgeInfo.IsEnabled then



-- Award badge



local awarded, errorMessage = pcall(BadgeService.AwardBadgeAsync, BadgeService, player.UserId, badgeId)



if not awarded then



warn("Error while awarding badge:", errorMessage)



end



end



else



warn("Error while fetching badge info: " .. badgeInfo)



end



end



local function onPlayerAdded(player)



awardBadge(player, BADGE_ID)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

AwardBadge

Deprecated

Show details

---

CheckUserBadgesAsync

Yields

Checks a list of badge IDs against a [UserId](/docs/reference/engine/classes/Player#UserId) and
returns a list of badge IDs that the player owns.

BadgeService:CheckUserBadgesAsync(

userId:[number](/docs/luau/numbers), badgeIds:[Array](/docs/luau/tables#arrays)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [UserId](/docs/reference/engine/classes/Player#UserId) of the player to check for ownership of the specified badges. |
| badgeIds:[Array](/docs/luau/tables#arrays)  The list of IDs of the badges to check ownership of. Maximum length of 10. |

Returns

[Array](/docs/luau/tables#arrays)

The list of badge IDs the given user owns out of the provided badge
IDs. Empty if none of the provided badges are owned by the given user.
Not guaranteed to be in the same order as the input list.

Checks a list of badge IDs against a [UserId](/docs/reference/engine/classes/Player#UserId) and
returns a list of badge IDs that the player owns. This method supports
batches of up to 10 badges; use [BadgeService:UserHasBadgeAsync()](/docs/reference/engine/classes/BadgeService#UserHasBadgeAsync)
for single badge lookups.

Any set of badges for any experience can be queried, no matter who created
the badges or which experiences they are for. Any
[UserId](/docs/reference/engine/classes/Player#UserId) can be used in a [Script](/docs/reference/engine/classes/Script), but in a
[LocalScript](/docs/reference/engine/classes/LocalScript), only the [UserId](/docs/reference/engine/classes/Player#UserId) of the local
user whose client is running the script can be used.

Rate limit is 10 + 5 \* [number of players] per minute in each server.

Code Samples

Checking Earned Badges in Batches

This script checks which badges a user owns when they join the experience.

```
local BadgeService = game:GetService("BadgeService")



local Players = game:GetService("Players")



local badgeIds = { 0000000000, 1111111111, 2222222222 } -- Change this to a list of your badge IDs



local function onPlayerAdded(player)



-- Check if the player has any of the badges



local success, result = pcall(function()



return BadgeService:CheckUserBadgesAsync(player.UserId, badgeIds)



end)



-- If there's an error, issue a warning and exit the function



if not success then



warn("Error while checking if player", player.Name, "has badges:", result)



return



end



local ownedBadgeIds = result



if #ownedBadgeIds == 0 then



print(player.Name, "does not have any of the badges")



else



print(player.Name, "has the following badges:", table.concat(ownedBadgeIds, ", "))



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

GetBadgeInfoAsync

Yields

Fetch information about a badge given its ID.

BadgeService:GetBadgeInfoAsync(badgeId:[number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| badgeId:[number](/docs/luau/numbers)  The badge ID of the badge whose information should be fetched. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary of information about the specified badge.

This method fetches information about a badge given its ID and returns a
dictionary with the following fields:

| Key | Type | Description |
| --- | --- | --- |
| Name | string | The name of the badge. |
| Description | string | The description of the badge. |
| IconImageId | int64 | The asset ID of the image for the badge. |
| IsEnabled | boolean | Indicates whether the badge is available to be awarded. |

This method takes a brief moment to load the information from Roblox;
repeated calls will cache for a short duration.

Code Samples

Getting Badge Info

This sample prints badge information fetched via
[BadgeService:GetBadgeInfoAsync()](/docs/reference/engine/classes/BadgeService#GetBadgeInfoAsync).

```
local BadgeService = game:GetService("BadgeService")



-- Fetch badge information



local success, result = pcall(function()



return BadgeService:GetBadgeInfoAsync(00000000) -- Change this to desired badge ID



end)



-- Output the information



if success then



print("Badge:", result.Name)



print("Enabled:", result.IsEnabled)



print("Description:", result.Description)



print("Icon:", "rbxassetid://" .. result.IconImageId)



else



warn("Error while fetching badge info:", result)



end
```

Provide feedback

---

IsDisabled

Deprecated

Show details

---

IsLegal

Deprecated

Show details

---

UserHasBadge

Deprecated

Show details

---

UserHasBadgeAsync

Yields

Checks whether a player has the badge given the [Player.UserId](/docs/reference/engine/classes/Player#UserId) and
the badge ID.

BadgeService:UserHasBadgeAsync(

userId:[number](/docs/luau/numbers), badgeId:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the player to check for ownership of the specified badge. |
| badgeId:[number](/docs/luau/numbers)  The badge ID of the badge whose ownership will be checked. |

Returns

[boolean](/docs/luau/booleans)

Indicates if the specified user has the specified badge.

Checks and returns whether a [Player](/docs/reference/engine/classes/Player) owns a badge given their
[UserId](/docs/reference/engine/classes/Player#UserId) and the badge ID. You can call this method
from the server in a [Script](/docs/reference/engine/classes/Script) or [ModuleScript](/docs/reference/engine/classes/ModuleScript) eventually
required by a [Script](/docs/reference/engine/classes/Script), and the user in question must be present in
the server for the query to run. When calling this method from the client
in a [LocalScript](/docs/reference/engine/classes/LocalScript), it only works for the local user whose client is
running the script.

Any badge for any experience can be queried, no matter who created the
badge or which experience it is used for.

Rate limit is 50 + 35 \* [number of players] per minute.

Code Samples

Checking Earned Badges

The following script waits for any player to enter the game and checks if they
own a specific badge. This is useful for creating a restricted area with [collision filtering](/docs/workspace/collisions#collision-filtering) or [teleportation](/docs/projects/teleporting) that only works if a player owns a special badge.

```
local BadgeService = game:GetService("BadgeService")



local Players = game:GetService("Players")



local badgeId = 00000000 -- Change this to your badge ID



local function onPlayerAdded(player)



-- Check if the player has the badge



local success, hasBadge = pcall(function()



return BadgeService:UserHasBadgeAsync(player.UserId, badgeId)



end)



-- If there's an error, issue a warning and exit the function



if not success then



warn("Error while checking if player has badge!")



return



end



if hasBadge then



-- Handle player's badge ownership as needed



print(player.Name, "has badge", badgeId)



end



end



-- Connect "PlayerAdded" events to the "onPlayerAdded()" function



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---