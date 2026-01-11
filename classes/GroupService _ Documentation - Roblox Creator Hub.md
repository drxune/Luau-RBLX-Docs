# GroupService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GroupService
Scraped: 2026-01-11T02:29:49.057644Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- GroupService
- StandardPages
- GroupService:GetGroupInfoAsync()
- GroupService:GetAlliesAsync()
- GroupService:GetEnemiesAsync()
- GroupService:GetGroupsAsync()
- Player:IsInGroup()
- GroupService:PromptJoinAsync()
- Player.UserId
- Player
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [GroupService](/docs/reference/engine/classes/GroupService)

English

Feedback

Engine Class

GroupService

GroupService is a service that allows developers to fetch information about a
Roblox group from within a game.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetAlliesAsync](#GetAlliesAsync)(groupId: [number](/docs/luau/numbers)):[StandardPages](/docs/reference/engine/classes/StandardPages) |
| [GetEnemiesAsync](#GetEnemiesAsync)(groupId: [number](/docs/luau/numbers)):[StandardPages](/docs/reference/engine/classes/StandardPages) |
| [GetGroupInfoAsync](#GetGroupInfoAsync)(groupId: [number](/docs/luau/numbers)):Variant |
| [GetGroupsAsync](#GetGroupsAsync)(userId: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [PromptJoinAsync](#PromptJoinAsync)(groupId: [number](/docs/luau/numbers)):[Enum.GroupMembershipStatus](/docs/reference/engine/enums/GroupMembershipStatus) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

GroupService is a service that allows developers to fetch information about
a Roblox group from within a game.

Basic information on the group, including its name, description, owner, roles
and emblem can be fetched using [GroupService:GetGroupInfoAsync()](/docs/reference/engine/classes/GroupService#GetGroupInfoAsync).
Lists of a group's allies and enemies can be fetched using
[GroupService:GetAlliesAsync()](/docs/reference/engine/classes/GroupService#GetAlliesAsync) and
[GroupService:GetEnemiesAsync()](/docs/reference/engine/classes/GroupService#GetEnemiesAsync).

GroupService can also be used to fetch a list of groups a player is a member
of, using [GroupService:GetGroupsAsync()](/docs/reference/engine/classes/GroupService#GetGroupsAsync). If you wish to verify if a
player is in a group, use the [Player:IsInGroup()](/docs/reference/engine/classes/Player#IsInGroup) method rather than
[GroupService:GetGroupsAsync()](/docs/reference/engine/classes/GroupService#GetGroupsAsync).

The service has a number of useful applications, such as detecting if a player
is an ally or enemy upon joining the game, or prompting a player to join a
group using the [GroupService:PromptJoinAsync()](/docs/reference/engine/classes/GroupService#PromptJoinAsync) method.

Code Samples

Group Ally/Enemy Checker

This code sample demonstrates how GroupService and
[Player:IsInGroup()](/docs/reference/engine/classes/Player#IsInGroup) can be used to determine whether a player is a
member of a group, or any of its allies or enemies.

Note as [GroupService:GetAlliesAsync()](/docs/reference/engine/classes/GroupService#GetAlliesAsync) and
[GroupService:GetEnemiesAsync()](/docs/reference/engine/classes/GroupService#GetEnemiesAsync) use StandardPages objects a utility
function is used to convert them to allies.

```
local GroupService = game:GetService("GroupService")



local Players = game:GetService("Players")



-- Define group ID here



local GROUP_ID = 271454



-- Utility function for dealing with pages



local function pagesToArray(pages)



local array = {}



while true do



for _, v in ipairs(pages:GetCurrentPage()) do



table.insert(array, v)



end



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



end



return array



end



-- Get lists of allies and enemies



local alliesPages = GroupService:GetAlliesAsync(GROUP_ID)



local enemiesPages = GroupService:GetEnemiesAsync(GROUP_ID)



-- Convert to array



local allies = pagesToArray(alliesPages)



local enemies = pagesToArray(enemiesPages)



local function playerAdded(player)



-- Check to see if the player is in the group



if player:IsInGroup(GROUP_ID) then



print(player.Name .. " is a member!")



else



local isAlly, isEnemy = false, false



-- Check to see if the player is in any ally groups



for _, groupInfo in ipairs(allies) do



local groupId = groupInfo.Id



if player:IsInGroup(groupId) then



isAlly = true



break



end



end



-- Check to see if the player is in any enemy groups



for _, groupInfo in ipairs(enemies) do



local groupId = groupInfo.Id



if player:IsInGroup(groupId) then



isEnemy = true



break



end



end



if isAlly and not isEnemy then



print(player.Name .. " is an ally!")



elseif isEnemy and not isAlly then



print(player.Name .. " is an enemy!")



elseif isEnemy and isAlly then



print(player.Name .. " is both an ally and an enemy!")



else



print(player.Name .. " is neither an ally or an enemy!")



end



end



end



-- Listen for new players being added



Players.PlayerAdded:Connect(playerAdded)



-- Handle players already in game



for _, player in ipairs(Players:GetPlayers()) do



playerAdded(player)



end
```

---

API Reference

Methods

GetAlliesAsync

Yields

Returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object including information on all of the
specified group's allies.

GroupService:GetAlliesAsync(groupId:[number](/docs/luau/numbers)):[StandardPages](/docs/reference/engine/classes/StandardPages)

Parameters

|  |
| --- |
| groupId:[number](/docs/luau/numbers)  The group's ID. |

Returns

[StandardPages](/docs/reference/engine/classes/StandardPages)

Returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object including information on all of the
specified group's allies.

This pages does not include a list of group IDs but instead a list of
group information tables, mirroring the format of those returned by
[GroupService:GetGroupInfoAsync()](/docs/reference/engine/classes/GroupService#GetGroupInfoAsync). See below for the structure of
these tables.

```
group = {



Name = "Knights of the Seventh Sanctum",



Id = 377251,



Owner = {



Name = "Vilicus",



Id = 23415609



},



EmblemUrl = "http://www.roblox.com/asset/?id=60428602",



Description = "We fight alongside the balance to make sure no one becomes to powerful",



Roles = {



[1] = {



Name = "Apprentice",



Rank = 1



},



[2] = {



Name = "Warrior",



Rank = 2



},



[3] = {



Name = "Earth Walker",



Rank = 255



}



}



}
```

Note, as this function returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object rather than
an array, developers may wish to convert it to an array for ease of use
(see examples).

This function has a number of useful applications, including detecting if
a player is a member of an allied group.

For enemies, use [GroupService:GetEnemiesAsync()](/docs/reference/engine/classes/GroupService#GetEnemiesAsync).

Code Samples

GroupService:GetAlliesAsync

```
local Players = game:GetService("Players")



local GroupService = game:GetService("GroupService")



local GROUP_ID = 57



-- creates a table of all of the allies of a given group



local allies = {}



local pages = GroupService:GetAlliesAsync(GROUP_ID)



while true do



for _, group in pairs(pages:GetCurrentPage()) do



table.insert(allies, group)



end



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



end



function onPlayerAdded(player)



for _, group in pairs(allies) do



if player:IsInGroup(group.Id) then



print("Player is an ally!")



break



end



end



end



Players.PlayerAdded:Connect(onPlayerAdded)



-- handle players who joined while the allies list was still loading



for _, player in pairs(Players:GetPlayers()) do



onPlayerAdded(player)



end
```

Group Ally/Enemy Checker

This code sample demonstrates how GroupService and
[Player:IsInGroup()](/docs/reference/engine/classes/Player#IsInGroup) can be used to determine whether a player is a
member of a group, or any of its allies or enemies.

Note as [GroupService:GetAlliesAsync()](/docs/reference/engine/classes/GroupService#GetAlliesAsync) and
[GroupService:GetEnemiesAsync()](/docs/reference/engine/classes/GroupService#GetEnemiesAsync) use StandardPages objects a utility
function is used to convert them to allies.

```
local GroupService = game:GetService("GroupService")



local Players = game:GetService("Players")



-- Define group ID here



local GROUP_ID = 271454



-- Utility function for dealing with pages



local function pagesToArray(pages)



local array = {}



while true do



for _, v in ipairs(pages:GetCurrentPage()) do



table.insert(array, v)



end



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



end



return array



end



-- Get lists of allies and enemies



local alliesPages = GroupService:GetAlliesAsync(GROUP_ID)



local enemiesPages = GroupService:GetEnemiesAsync(GROUP_ID)



-- Convert to array



local allies = pagesToArray(alliesPages)



local enemies = pagesToArray(enemiesPages)



local function playerAdded(player)



-- Check to see if the player is in the group



if player:IsInGroup(GROUP_ID) then



print(player.Name .. " is a member!")



else



local isAlly, isEnemy = false, false



-- Check to see if the player is in any ally groups



for _, groupInfo in ipairs(allies) do



local groupId = groupInfo.Id



if player:IsInGroup(groupId) then



isAlly = true



break



end



end



-- Check to see if the player is in any enemy groups



for _, groupInfo in ipairs(enemies) do



local groupId = groupInfo.Id



if player:IsInGroup(groupId) then



isEnemy = true



break



end



end



if isAlly and not isEnemy then



print(player.Name .. " is an ally!")



elseif isEnemy and not isAlly then



print(player.Name .. " is an enemy!")



elseif isEnemy and isAlly then



print(player.Name .. " is both an ally and an enemy!")



else



print(player.Name .. " is neither an ally or an enemy!")



end



end



end



-- Listen for new players being added



Players.PlayerAdded:Connect(playerAdded)



-- Handle players already in game



for _, player in ipairs(Players:GetPlayers()) do



playerAdded(player)



end
```

Provide feedback

---

GetEnemiesAsync

Yields

Returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object including information on all of the
specified group's enemies.

GroupService:GetEnemiesAsync(groupId:[number](/docs/luau/numbers)):[StandardPages](/docs/reference/engine/classes/StandardPages)

Parameters

|  |
| --- |
| groupId:[number](/docs/luau/numbers)  The group's ID. |

Returns

[StandardPages](/docs/reference/engine/classes/StandardPages)

Returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object including information on all of the
specified group's enemies.

This pages does not include a list of group IDs but instead a list of
group information tables, mirroring the format of those returned by
[GroupService:GetGroupInfoAsync()](/docs/reference/engine/classes/GroupService#GetGroupInfoAsync). See below for the structure of
these tables.

```
group = {



Name = "Knights of the Seventh Sanctum",



Id = 377251,



Owner = {



Name = "Vilicus",



Id = 23415609



},



EmblemUrl = "http://www.roblox.com/asset/?id=60428602",



Description = "We fight alongside the balance to make sure no one becomes to powerful",



Roles = {



[1] = {



Name = "Apprentice",



Rank = 1



},



[2] = {



Name = "Warrior",



Rank = 2



},



[3] = {



Name = "Earth Walker",



Rank = 255



}



}



}
```

Note, as this function returns a [StandardPages](/docs/reference/engine/classes/StandardPages) object rather than
an array, developers may wish to convert it to an array for ease of use
(see examples).

This function has a number of useful applications, including detecting if
a player is a member of an enemy group.

For allies, use [GroupService:GetAlliesAsync()](/docs/reference/engine/classes/GroupService#GetAlliesAsync).

Code Samples

GroupService:GetEnemiesAsync

```
local Players = game:GetService("Players")



local GroupService = game:GetService("GroupService")



local GROUP_ID = 57



-- creates a list of all of the enemies of a given group



local enemies = {}



local pages = GroupService:GetEnemiesAsync(GROUP_ID)



while true do



for _, group in pairs(pages:GetCurrentPage()) do



table.insert(enemies, group)



end



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



end



function onPlayerAdded(player)



for _, enemyGroup in pairs(enemies) do



if player:IsInGroup(enemyGroup.Id) then



print("Player is an enemy!")



break



end



end



end



Players.PlayerAdded:Connect(onPlayerAdded)



-- handle players who joined while the enemies list was still loading



for _, player in pairs(Players:GetPlayers()) do



onPlayerAdded(player)



end
```

Group Ally/Enemy Checker

This code sample demonstrates how GroupService and
[Player:IsInGroup()](/docs/reference/engine/classes/Player#IsInGroup) can be used to determine whether a player is a
member of a group, or any of its allies or enemies.

Note as [GroupService:GetAlliesAsync()](/docs/reference/engine/classes/GroupService#GetAlliesAsync) and
[GroupService:GetEnemiesAsync()](/docs/reference/engine/classes/GroupService#GetEnemiesAsync) use StandardPages objects a utility
function is used to convert them to allies.

```
local GroupService = game:GetService("GroupService")



local Players = game:GetService("Players")



-- Define group ID here



local GROUP_ID = 271454



-- Utility function for dealing with pages



local function pagesToArray(pages)



local array = {}



while true do



for _, v in ipairs(pages:GetCurrentPage()) do



table.insert(array, v)



end



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



end



return array



end



-- Get lists of allies and enemies



local alliesPages = GroupService:GetAlliesAsync(GROUP_ID)



local enemiesPages = GroupService:GetEnemiesAsync(GROUP_ID)



-- Convert to array



local allies = pagesToArray(alliesPages)



local enemies = pagesToArray(enemiesPages)



local function playerAdded(player)



-- Check to see if the player is in the group



if player:IsInGroup(GROUP_ID) then



print(player.Name .. " is a member!")



else



local isAlly, isEnemy = false, false



-- Check to see if the player is in any ally groups



for _, groupInfo in ipairs(allies) do



local groupId = groupInfo.Id



if player:IsInGroup(groupId) then



isAlly = true



break



end



end



-- Check to see if the player is in any enemy groups



for _, groupInfo in ipairs(enemies) do



local groupId = groupInfo.Id



if player:IsInGroup(groupId) then



isEnemy = true



break



end



end



if isAlly and not isEnemy then



print(player.Name .. " is an ally!")



elseif isEnemy and not isAlly then



print(player.Name .. " is an enemy!")



elseif isEnemy and isAlly then



print(player.Name .. " is both an ally and an enemy!")



else



print(player.Name .. " is neither an ally or an enemy!")



end



end



end



-- Listen for new players being added



Players.PlayerAdded:Connect(playerAdded)



-- Handle players already in game



for _, player in ipairs(Players:GetPlayers()) do



playerAdded(player)



end
```

Provide feedback

---

GetGroupInfoAsync

Yields

Returns a table containing information about the given group.

GroupService:GetGroupInfoAsync(groupId:[number](/docs/luau/numbers)):Variant

Parameters

|  |
| --- |
| groupId:[number](/docs/luau/numbers)  The group ID of the group. |

Returns

Variant

A dictionary of information about the group.

Returns a table containing information about the given group.

The table returned is the same format as that returned in
[GroupService:GetAlliesAsync()](/docs/reference/engine/classes/GroupService#GetAlliesAsync) and
[GroupService:GetEnemiesAsync()](/docs/reference/engine/classes/GroupService#GetEnemiesAsync). This format can be seen below.

```
group = {



Name = "Knights of the Seventh Sanctum",



Id = 377251,



Owner = {



Name = "Vilicus",



Id = 23415609



},



EmblemUrl = "http://www.roblox.com/asset/?id=60428602",



Description = "We fight alongside the balance to make sure no one becomes to powerful",



Roles = {



[1] = {



Name = "Apprentice",



Rank = 1



},



[2] = {



Name = "Warrior",



Rank = 2



},



[3] = {



Name = "Earth Walker",



Rank = 255



}



}



}
```

Note, if a group has no owner the Owner field will be set to nil.

This function has a number of useful applications, including loading the
latest description and logo of a group for display in a group base.

Code Samples

GroupService:GetGroupInfoAsync

```
local GroupService = game:GetService("GroupService")



local GROUP_ID = 377251



local group = GroupService:GetGroupInfoAsync(GROUP_ID)



print(group.Name .. " has the following roles:")



for _, role in ipairs(group.Roles) do



print("Rank " .. role.Rank .. ": " .. role.Name)



end
```

Load Group Emblem

The code in this sample spawns a Part in the Workspace that includes a
texture of the given group's emblem.

```
local GroupService = game:GetService("GroupService")



local function getEmblemAsync(groupId)



local groupInfo = GroupService:GetGroupInfoAsync(groupId)



return groupInfo.EmblemUrl



end



local part = Instance.new("Part")



part.Anchored = true



part.CanCollide = false



part.Size = Vector3.new(5, 5, 1)



part.Position = Vector3.new(0, 5, 0)



local decal = Instance.new("Decal")



decal.Parent = part



part.Parent = workspace



decal.ColorMapContent = getEmblemAsync(377251)
```

Provide feedback

---

GetGroupsAsync

Yields

Returns a list of tables containing information on all of the groups a
given player is a member of.

GroupService:GetGroupsAsync(userId:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the user. |

Returns

[Array](/docs/luau/tables#arrays)

An array of dictionaries containing information on the group's the
[Player](/docs/reference/engine/classes/Player) is a member of.

Warning: The IsInClan property in the returned table will always
return false and exists for backwards compatibility. The Clans feature
was sunset from the Roblox platform in 2016.

This function returns a list of tables containing information on all of
the groups a given [Player](/docs/reference/engine/classes/Player) is a member of.

The list returned will include an entry for every group the player is a
member of. These entries are tables with the following fields.

| Name | Description |
| --- | --- |
| **Name** | The group's name |
| **Id** | The group ID |
| **EmblemUrl** | An asset url linking to the group's thumbnail (for example: http://www.roblox.com/asset/?id=276165514) |
| **EmblemId** | The assetId of the emblem, the same which is used in the EmblemUrl |
| **Rank** | The rankId the player has (for example: 255 for the owner) |
| **Role** | The name of the player's grouprank (for example: Group Owner) |
| **IsPrimary** | A boolean indicating if this is the player's primary group |
| **IsInClan** | A boolean indicating if the player is in this group's clan |

Note unlike [GroupService:GetAlliesAsync()](/docs/reference/engine/classes/GroupService#GetAlliesAsync) and
[GroupService:GetEnemiesAsync()](/docs/reference/engine/classes/GroupService#GetEnemiesAsync), GetGroupsAsync returns a table
rather than a [StandardPages](/docs/reference/engine/classes/StandardPages) object.

Code Samples

Getting the Groups that a User is A Member Of

This code sample will print information on all of the groups a player is a
member of when they join the game, using
[GroupService:GetGroupsAsync()](/docs/reference/engine/classes/GroupService#GetGroupsAsync).

```
local GroupService = game:GetService("GroupService")



local Players = game:GetService("Players")



local function playerAdded(player)



-- load a list of info on all groups the player is a member of



local groups = GroupService:GetGroupsAsync(player.UserId)



for _, groupInfo in pairs(groups) do



for key, value in pairs(groupInfo) do



print(key .. ": " .. tostring(value))



end



print("--")



end



end



Players.PlayerAdded:Connect(playerAdded)



-- go through existing players



for _, player in pairs(Players:GetPlayers()) do



playerAdded(player)



end
```

Provide feedback

---

PromptJoinAsync

Yields

Prompts the local [Player](/docs/reference/engine/classes/Player) to join a specified Roblox group via a
native modal.

GroupService:PromptJoinAsync(groupId:[number](/docs/luau/numbers)):[Enum.GroupMembershipStatus](/docs/reference/engine/enums/GroupMembershipStatus)

Parameters

|  |
| --- |
| groupId:[number](/docs/luau/numbers)  ID of the group to prompt the player to join. This must be a valid group ID. |

Returns

[Enum.GroupMembershipStatus](/docs/reference/engine/enums/GroupMembershipStatus)

[Enum.GroupMembershipStatus](/docs/reference/engine/enums/GroupMembershipStatus) indicating the player's group membership
status after the prompt is closed. If the player closes the prompt
without joining, this will return [Enum.GroupMembershipStatus.None](/docs/reference/engine/enums/GroupMembershipStatus#None) or
their previous status if they were already a member.

PromptJoinAsync() displays a prompt to the local player through which
they may join the specified Roblox group. The group must exist and the
player must meet the eligibility criteria to join. If the player is
ineligible, this method will return [Enum.GroupMembershipStatus.None](/docs/reference/engine/enums/GroupMembershipStatus#None).

Note that you can use [Player:IsInGroup()](/docs/reference/engine/classes/Player#IsInGroup) to check the player's
current membership status before calling this method.

Code Samples

Prompting a player to join a group

This code sample demonstrates how to prompt a player to join a group, using [GroupService:PromptJoinAsync()](/docs/reference/engine/classes/GroupService#PromptJoinAsync).

```
local GroupService = game:GetService("GroupService")



local GROUP_ID = 377251



-- This should be done in a script running on the client



local success, result = pcall(function()



return GroupService:PromptJoinAsync(GROUP_ID)



end)



if success then



if result == Enum.GroupMembershipStatus.Joined then



print("Player joined the group!")



elseif result == Enum.GroupMembershipStatus.JoinRequestPending then



print("Join request sent")



elseif result == Enum.GroupMembershipStatus.AlreadyMember then



print("Already a member")



else



print("Did not join or not eligible")



end



else



warn("Prompt failed:", result)



end
```

Provide feedback

---