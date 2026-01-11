# Players | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Players
Scraped: 2026-01-11T02:37:25.637408Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- Players
- Player
- HumanoidDescription
- Model
- BanHistoryPages
- FriendPages
- BanAsync()
- UnbanAsync()
- GetBanHistoryAsync()
- Players:SetChatStyle()
- Players.ClassicChat
- characters
- Player:LoadCharacter()
- Players.CharacterAutoLoads
- Player.Character
- Humanoid.Died
- Players.BubbleChat
- LocalScript
- LocalScripts
- ModuleScripts
- Script
- Players.MaxPlayers
- Players.BanningEnabled
- UserIds
- Players:BanAsync()
- Players:GetBanHistoryAsync()
- UserId
- Chat
- Chat:Chat()
- Players:Chat()
- Humanoid
- Pages
- GetCharacterAppearanceAsync
- InsertService:LoadAsset()
- display name
- Player.UserId
- Players:GetUserIdFromNameAsync()
- Players:GetFriendsAsync()
- Players:GetNameFromUserIdAsync()
- Player.Name
- GetNameFromUserIdAsync()
- Name
- MarketplaceService.ProcessReceipt
- dying
- Instance:GetChildren()
- Players.PlayerAdded
- PlayerAdded
- userId
- GetUserIdFromNameAsync()
- ImageLabel.Image
- Decal.Texture
- Players:GetUserThumbnailAsync()
- Image()
- Size()
- Players.LocalPlayer
- Players:TeamChat()
- GlobalDataStore
- Players.PlayerRemoving
- Player.CharacterAdded
- Player.CharacterRemoving
- MarketplaceService:PromptPremiumPurchase()
- MarketplaceService.PromptPremiumPurchaseFinished
- ChildRemoved
- Instance.DescendantRemoving
- Player.PlayerAdded
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Players](/docs/reference/engine/classes/Players)

English

Feedback

Engine Class

![Players](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Players-Dark.webp)Players

A service that contains presently connected [Player](/docs/reference/engine/classes/Player) objects.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [BanningEnabled](#BanningEnabled):[boolean](/docs/luau/booleans) |
| [BubbleChat](#BubbleChat):[boolean](/docs/luau/booleans) |
| [CharacterAutoLoads](#CharacterAutoLoads):[boolean](/docs/luau/booleans) |
| [ClassicChat](#ClassicChat):[boolean](/docs/luau/booleans) |
| [LocalPlayer](#LocalPlayer):[Player](/docs/reference/engine/classes/Player) |
| [localPlayer](#localPlayer):[Player](/docs/reference/engine/classes/Player)  Deprecated |
| [MaxPlayers](#MaxPlayers):[number](/docs/luau/numbers) |
| [NumPlayers](#NumPlayers):[number](/docs/luau/numbers)  Deprecated |
| [numPlayers](#numPlayers):[number](/docs/luau/numbers)  Deprecated |
| [PreferredPlayers](#PreferredPlayers):[number](/docs/luau/numbers) |
| [RespawnTime](#RespawnTime):[number](/docs/luau/numbers) |
| [UseStrafingAnimations](#UseStrafingAnimations):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [BanAsync](#BanAsync)(config: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [Chat](#Chat)(message: [string](/docs/luau/strings)):() |
| [CreateHumanoidModelFromDescriptionAsync](#CreateHumanoidModelFromDescriptionAsync)(description: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),rigType: [Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType),assetTypeVerification: [Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)):[Model](/docs/reference/engine/classes/Model) |
| [CreateHumanoidModelFromDescription](#CreateHumanoidModelFromDescription)(description: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),rigType: [Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType),assetTypeVerification: [Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)):[Model](/docs/reference/engine/classes/Model)  Deprecated |
| [CreateHumanoidModelFromUserIdAsync](#CreateHumanoidModelFromUserIdAsync)(userId: [number](/docs/luau/numbers)):[Model](/docs/reference/engine/classes/Model) |
| [CreateHumanoidModelFromUserId](#CreateHumanoidModelFromUserId)(userId: [number](/docs/luau/numbers)):[Model](/docs/reference/engine/classes/Model)  Deprecated |
| [GetBanHistoryAsync](#GetBanHistoryAsync)(userId: [number](/docs/luau/numbers)):[BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages) |
| [GetCharacterAppearanceAsync](#GetCharacterAppearanceAsync)(userId: [number](/docs/luau/numbers)):[Model](/docs/reference/engine/classes/Model)  Deprecated |
| [GetCharacterAppearanceInfoAsync](#GetCharacterAppearanceInfoAsync)(userId: [number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetFriendsAsync](#GetFriendsAsync)(userId: [number](/docs/luau/numbers)):[FriendPages](/docs/reference/engine/classes/FriendPages) |
| [GetHumanoidDescriptionFromOutfitIdAsync](#GetHumanoidDescriptionFromOutfitIdAsync)(outfitId: [number](/docs/luau/numbers)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |
| [GetHumanoidDescriptionFromOutfitId](#GetHumanoidDescriptionFromOutfitId)(outfitId: [number](/docs/luau/numbers)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  Deprecated |
| [GetHumanoidDescriptionFromUserIdAsync](#GetHumanoidDescriptionFromUserIdAsync)(userId: [number](/docs/luau/numbers)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |
| [GetHumanoidDescriptionFromUserId](#GetHumanoidDescriptionFromUserId)(userId: [number](/docs/luau/numbers)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  Deprecated |
| [GetNameFromUserIdAsync](#GetNameFromUserIdAsync)(userId: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [GetPlayerByUserId](#GetPlayerByUserId)(userId: [number](/docs/luau/numbers)):[Player](/docs/reference/engine/classes/Player) |
| [GetPlayerFromCharacter](#GetPlayerFromCharacter)(character: [Model](/docs/reference/engine/classes/Model)):[Player](/docs/reference/engine/classes/Player) |
| [GetPlayers](#GetPlayers)():Instances |
| [getPlayers](#getPlayers)():Instances  Deprecated |
| [GetUserIdFromNameAsync](#GetUserIdFromNameAsync)(userName: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [GetUserThumbnailAsync](#GetUserThumbnailAsync)(userId: [number](/docs/luau/numbers),thumbnailType: [Enum.ThumbnailType](/docs/reference/engine/enums/ThumbnailType),thumbnailSize: [Enum.ThumbnailSize](/docs/reference/engine/enums/ThumbnailSize)):[Tuple](/docs/luau/tuples) |
| [playerFromCharacter](#playerFromCharacter)(character: [Model](/docs/reference/engine/classes/Model)):[Player](/docs/reference/engine/classes/Player)  Deprecated |
| [players](#players)():Instances  Deprecated |
| [SetChatStyle](#SetChatStyle)(style: [Enum.ChatStyle](/docs/reference/engine/enums/ChatStyle)):() |
| [TeamChat](#TeamChat)(message: [string](/docs/luau/strings)):() |
| [UnbanAsync](#UnbanAsync)(config: [Dictionary](/docs/luau/tables#dictionaries)):() |

Events

|  |
| --- |
| [PlayerAdded](#PlayerAdded)(player: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PlayerMembershipChanged](#PlayerMembershipChanged)(player: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PlayerRemoving](#PlayerRemoving)(player: [Player](/docs/reference/engine/classes/Player),reason: [Enum.PlayerExitReason](/docs/reference/engine/enums/PlayerExitReason)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [UserSubscriptionStatusChanged](#UserSubscriptionStatusChanged)(user: [Player](/docs/reference/engine/classes/Player),subscriptionId: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [Players](/docs/reference/engine/classes/Players) service contains [Player](/docs/reference/engine/classes/Player) objects for presently
connected clients to a Roblox server. It also contains information about a
place's configuration. It can fetch information about players not connected to
the server, such as character appearances, connections, and avatar thumbnail.

---

API Reference

Properties

BanningEnabled

Not Scriptable

Read Parallel

Enables or disables the three [Players](/docs/reference/engine/classes/Players) methods
([BanAsync()](/docs/reference/engine/classes/Players#BanAsync),
[UnbanAsync()](/docs/reference/engine/classes/Players#UnbanAsync), and
[GetBanHistoryAsync()](/docs/reference/engine/classes/Players#GetBanHistoryAsync)) that constitute
the ban API. This property is not scriptable and can only be modified in
Studio.

Players.BanningEnabled:[boolean](/docs/luau/booleans)

Enables or disables the three [Players](/docs/reference/engine/classes/Players) methods
([BanAsync()](/docs/reference/engine/classes/Players#BanAsync),
[UnbanAsync()](/docs/reference/engine/classes/Players#UnbanAsync), and
[GetBanHistoryAsync()](/docs/reference/engine/classes/Players#GetBanHistoryAsync)) that constitute
the ban API. This property is not scriptable and can only be modified in
Studio.

Provide feedback

---

BubbleChat

Read Only

Not Replicated

Read Parallel

Indicates whether or not bubble chat is enabled. It is set with the
[Players:SetChatStyle()](/docs/reference/engine/classes/Players#SetChatStyle) method.

Players.BubbleChat:[boolean](/docs/luau/booleans)

This property indicates whether or not bubble chat is enabled. It is set
with the [Players:SetChatStyle()](/docs/reference/engine/classes/Players#SetChatStyle) method using the [Enum.ChatStyle](/docs/reference/engine/enums/ChatStyle)
enum.

When this chat mode is enabled, the game displays chats in the chat user
interface at the top-left corner of the screen.

There are two other chat modes, [Players.ClassicChat](/docs/reference/engine/classes/Players#ClassicChat) and a chat
mode where both classic and bubble chat are enabled.

Provide feedback

---

CharacterAutoLoads

Not Replicated

Read Parallel

Indicates whether [characters](/docs/reference/engine/classes/Player#Character) will respawn
automatically.

Players.CharacterAutoLoads:[boolean](/docs/luau/booleans)

This property indicates whether [characters](/docs/reference/engine/classes/Player#Character) will
respawn automatically. The default value is true.

If this property is disabled (false), player
[characters](/docs/reference/engine/classes/Player#Character) will not spawn until the
[Player:LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter) function is called for each [Player](/docs/reference/engine/classes/Player),
including when players join the experience.

This can be useful in experiences where players have finite lives, such as
competitive games in which players do not respawn until a game round ends.

Code Samples

Player Respawn Timer

This example demonstrates one possible usage of the
[Players.CharacterAutoLoads](/docs/reference/engine/classes/Players#CharacterAutoLoads) property.

The example below respawns all players in the game, if dead, once every 10
seconds. This means that players who die 1 second after all players respawn
must wait 9 seconds until the script loads all [Player.Character](/docs/reference/engine/classes/Player#Character) again.

First, this script removes a player's character when they die and the
[Humanoid.Died](/docs/reference/engine/classes/Humanoid#Died) function fires. This is done so that the respawn loop
that executes every 10 seconds reloads that player when it does not find the
player's character in the Workspace.

To work as expected, this example should be run within a Script.

```
local Players = game:GetService("Players")



-- Set CharacterAutoLoads to false



Players.CharacterAutoLoads = false



-- Remove player's character from workspace on death



Players.PlayerAdded:Connect(function(player)



while true do



local char = player.CharacterAdded:Wait()



char.Humanoid.Died:Connect(function()



char:Destroy()



end)



end



end)



-- Respawn all dead players once every 10 seconds



while true do



local players = Players:GetChildren()



-- Check if each player is dead by checking if they have no character, if dead load that player's character



for _, player in pairs(players) do



if not workspace:FindFirstChild(player.Name) then



player:LoadCharacter()



end



end



-- Wait 10 seconds until next respawn check



task.wait(10)



end
```

Provide feedback

---

ClassicChat

Read Only

Not Replicated

Read Parallel

Indicates whether or not classic chat is enabled; set by the
[Players:SetChatStyle()](/docs/reference/engine/classes/Players#SetChatStyle) method.

Players.ClassicChat:[boolean](/docs/luau/booleans)

Indicates whether or not classic chat is enabled. This property is set by
the [Players:SetChatStyle()](/docs/reference/engine/classes/Players#SetChatStyle) method using the [Enum.ChatStyle](/docs/reference/engine/enums/ChatStyle) enum.

When this chat mode is enabled, the game displays chats in a bubble above
the sender's head.

There are two other chat modes, [Players.BubbleChat](/docs/reference/engine/classes/Players#BubbleChat) and a chat mode
where both classic and bubble chat are enabled.

Provide feedback

---

LocalPlayer

Read Only

Not Replicated

Read Parallel

The [Player](/docs/reference/engine/classes/Player) that the [LocalScript](/docs/reference/engine/classes/LocalScript) is running for.

Players.LocalPlayer:[Player](/docs/reference/engine/classes/Player)

This read-only property refers to the [Player](/docs/reference/engine/classes/Player) whose client is
running the experience.

This property is only defined for [LocalScripts](/docs/reference/engine/classes/LocalScript) and
[ModuleScripts](/docs/reference/engine/classes/ModuleScript) required by them, since they run on the
client. For the server, on which [Script](/docs/reference/engine/classes/Script) objects run their code,
this property is nil.

Provide feedback

---

localPlayer

Deprecated

Show details

---

MaxPlayers

Read Only

Not Replicated

Read Parallel

The maximum number of players that can be in a server.

Players.MaxPlayers:[number](/docs/luau/numbers)

This property determines the maximum number of players that can be in a
server. This property can only be set through a specific place's settings
on the [Creator Dashboard](https://create.roblox.com/dashboard/creations)
or through [Game Settings](/docs/studio/game-settings).

Provide feedback

---

NumPlayers

Deprecated

Show details

---

numPlayers

Deprecated

Show details

---

PreferredPlayers

Read Only

Not Replicated

Read Parallel

The preferred number of players for a server.

Players.PreferredPlayers:[number](/docs/luau/numbers)

This property indicates the number of players to which Roblox's matchmaker
will fill servers. This number will be less than the maximum number of
players ([Players.MaxPlayers](/docs/reference/engine/classes/Players#MaxPlayers)) supported by the experience.

Provide feedback

---

RespawnTime

Read Parallel

Controls the amount of time taken for a players character to respawn.

Players.RespawnTime:[number](/docs/luau/numbers)

This property controls the time, in seconds, it takes for a player to
respawn when [Players.CharacterAutoLoads](/docs/reference/engine/classes/Players#CharacterAutoLoads) is true. It defaults to
5.0 seconds.

This is useful when you want to change how long it takes to respawn based
on the type of your experience but don't want to handle spawning players
individually.

Although this property can be set from within a [Script](/docs/reference/engine/classes/Script), you can
more easily set it directly on the [Players](/docs/reference/engine/classes/Players) object in Studio's
[Explorer](/docs/studio/explorer) window.

Provide feedback

---

UseStrafingAnimations

Not Scriptable

Read Parallel

Players.UseStrafingAnimations:[boolean](/docs/luau/booleans)

Provide feedback

---

Methods

BanAsync

Yields

Bans users from your experience, with options to specify duration, reason,
whether the ban applies to the entire universe or just the current place,
and more. This method is enabled and disabled by the
[Players.BanningEnabled](/docs/reference/engine/classes/Players#BanningEnabled) property, which you can toggle in Studio.

Players:BanAsync(config:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| config:[Dictionary](/docs/luau/tables#dictionaries)   * UserIds (required; array) — Array of [UserIds](/docs/reference/engine/classes/Player#UserId)   of players to be banned. Max size is 50. * ApplyToUniverse (optional; boolean) — Whether ban propagates to   all places within the experience universe. Default is true. * Duration (required; integer) — Duration of the ban, in seconds.   Permanent bans should have a value of -1. 0 and all other   negative values are invalid. * DisplayReason (required; string) — The message that will be   displayed to users when they attempt to and fail to join an   experience. Maximum string length is 400. * PrivateReason (required; string) — Internal messaging that will be   returned when querying the user's ban history. Maximum string length   is 1000. * ExcludeAltAccounts (optional; boolean) — When true, Roblox does   not attempt to ban alt accounts. Default is false. |

Returns

()

The [Players:BanAsync()](/docs/reference/engine/classes/Players#BanAsync) method allows you to easily ban users who
violate your experience's guidelines. You can specify the ban duration,
enable the ban to propagate to suspected alternate accounts, and provide a
message to the banned user in accordance with the
[Usage Guidelines](/docs/players#banning-users). You should
also post your experience rules somewhere accessible to all users and
provide a way for them to appeal. This method is enabled and disabled by
the [Players.BanningEnabled](/docs/reference/engine/classes/Players#BanningEnabled) property, which you can toggle in
Studio.

##### Banning and Messaging

Banned users will be immediately evicted and prevented from rejoining your
experiences. They will be presented with an error modal displaying the
time left on their ban and your DisplayReason. Roblox's backend systems
will evict players across all servers from the place(s) that you specify.
DisplayReason can have a maximum length of 400 characters and is subject
to a text filter. For more information on acceptable modal text, see
[ban messaging](/docs/players#message-guidelines).

##### Places and Universe

By default, bans extend to any place within that universe. To limit the
ban to only the place from which this API is called, configure
ApplyToUniverse to false. However, if a user is banned in the start
place of the universe, it effectively results in the user being excluded
from the entirety of the universe, irrespective of whether a universal ban
is in place or not.

##### Alternative Accounts

Users often play under multiple different accounts, known as alternate
accounts or alt accounts, which are sometimes used to circumvent account
bans. To help you keep banned users out, the default behavior of this API
will propagate all bans from the source account you banned to any of their
suspected alt accounts. You can turn off ban propagations to alt accounts
by configuring ExcludeAltAccounts to true.

##### Ban Duration

Not all transgressions are the same, so not all bans should be the same
length. This API lets you configure the duration of the ban, in seconds,
with the Duration field. To specify a permanent ban, set the field to
-1. You may also want to dynamically configure the ban duration based on
the user's ban history, which you can query for using
[Players:GetBanHistoryAsync()](/docs/reference/engine/classes/Players#GetBanHistoryAsync). For example, you may want to
consider the number of bans, the duration of previous bans, or build logic
off of the notes you save under PrivateReason which can be up to 1000
characters and are not text filtered. PrivateReason notes are never
shared with the client and can be considered safe from attackers.

##### Errors and Throttling

This method invokes an HTTP call to backend services which are subject to
throttling and may fail. If you're calling this API with more than one
[UserId](/docs/reference/engine/classes/Player#UserId), this method will attempt to make the HTTP
call for each ID. It will then aggregate any error messages and join them
as a comma separated list. For example, if this method is invoked for five
users and requests for those with [UserIds](/docs/reference/engine/classes/Player#UserId) 2 and 4
fail, the following error message appears:

HTTP failure for UserId 2: Timedout, HTTP 504 (Service unavailable) failure for UserId 4: Service exception

The message will always include failure for UserId {} if it is an HTTP
error.

##### Client-Side Requirement

Because of the risks associated with banning users, this method may only
be called on the backend experience server (client-side calls will result
in an error). You may test this API in Studio, during
[collaborative](/docs/projects/collaboration) creation, or in a
[team test](/docs/studio/testing-modes#collaborative-testing), but
the bans will not apply to production.

This API uses the
[User Restrictions Open Cloud API](/docs/cloud/reference/UserRestriction). You
will be able to utilize these APIs to manage your bans in third party
applications.

Code Samples

Banning Users

The following example bans a user with a duration calculated from their ban history, scoped to the entire universe and all of the user's alternate accounts.

```
local Players = game:GetService("Players")



if shouldBeBanned(player) then



local banHistoryPages = Players:GetBanHistoryAsync(player.UserId)



local duration = getNextBanDuration(banHistoryPages) -- Creator-implemented logic



local config: BanConfigType = {



UserIds = { player.UserId },



Duration = duration,



DisplayReason = "You violated community guideline #5",



PrivateReason = "Put anything here that the user should not know but is helpful for your records",



ExcludeAltAccounts = false,



ApplyToUniverse = true,



}



local success, err = pcall(function()



return Players:BanAsync(config)



end)



print(success, err)



end
```

Provide feedback

---

Chat

Plugin Security

Makes the local player chat the given message.

Players:Chat(message:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings)  The message chatted. |

Returns

()

This function makes the local player chat the given message. Since this
item is protected, attempting to use it in a [Script](/docs/reference/engine/classes/Script) or
[LocalScript](/docs/reference/engine/classes/LocalScript) will cause an error.

Instead, when creating a custom chat system, or a system that needs access
to the chat, you can use the [Chat](/docs/reference/engine/classes/Chat) service's [Chat:Chat()](/docs/reference/engine/classes/Chat#Chat)
function instead.

Code Samples

Players:Chat

This example demonstrates that the [Players:Chat()](/docs/reference/engine/classes/Players#Chat) function executes
without error if using the Command Bar or a Plugin (assuming the local player
can chat freely) and errors if executed in a Script.

```
-- Command bar



game:GetService("Players"):Chat("Hello, world!") --Results in 'Hello, world!' appearing in the Chat log under your Player's name.



-- Script



local Players = game:GetService("Players")



Players:Chat("Hello, world!") --Errors
```

Provide feedback

---

CreateHumanoidModelFromDescriptionAsync

Yields

Returns a character [Model](/docs/reference/engine/classes/Model) equipped with everything specified in
the passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

Players:CreateHumanoidModelFromDescriptionAsync(

description:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType), assetTypeVerification:[Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)

):[Model](/docs/reference/engine/classes/Model)

Parameters

|  |
| --- |
| description:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  Specifies the appearance of the returned character. |
| rigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)  Specifies whether the returned character will be R6 or R15. |
| assetTypeVerification:[Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification) Default Value: "Default" The asset type verification mode. |

Returns

[Model](/docs/reference/engine/classes/Model)

A [Humanoid](/docs/reference/engine/classes/Humanoid) character [Model](/docs/reference/engine/classes/Model).

Returns a character [Model](/docs/reference/engine/classes/Model) equipped with everything specified in
the passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), and is R6 or R15 as specified
by rigType.

Code Samples

Create Humanoid Model From Description

This code sample creates a Humanoid Model from the passed in
HumanoidDescription and parents the Model to the Workspace.

```
game.Players:CreateHumanoidModelFromDescription(Instance.new("HumanoidDescription"), Enum.HumanoidRigType.R15).Parent =



game.Workspace
```

Provide feedback

---

CreateHumanoidModelFromDescription

Deprecated

Show details

---

CreateHumanoidModelFromUserIdAsync

Yields

Returns a character Model set-up with everything equipped to match the
avatar of the user specified by the passed in userId.

Players:CreateHumanoidModelFromUserIdAsync(userId:[number](/docs/luau/numbers)):[Model](/docs/reference/engine/classes/Model)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The userId for a Roblox user. (The UserId is the number in the profile of the user e.g [www.roblox.com/users/1/profile](http://www.roblox.com/users/1/profile)). |

Returns

[Model](/docs/reference/engine/classes/Model)

A Humanoid character Model.

Returns a character Model set-up with everything equipped to match the
avatar of the user specified by the passed in userId. This includes
whether that character is currently R6 or R15.

Code Samples

Create Humanoid Model From A User ID

This code sample creates a Humanoid Model to match the avatar of the passed in
User ID, and parents the Model to the Workspace.

```
game.Players:CreateHumanoidModelFromUserId(1).Parent = game.Workspace
```

Provide feedback

---

CreateHumanoidModelFromUserId

Deprecated

Show details

---

GetBanHistoryAsync

Yields

Retrieves the ban and unban history of any user within the experience's
universe. This method is enabled and disabled by the
[Players.BanningEnabled](/docs/reference/engine/classes/Players#BanningEnabled) property, which you can toggle in Studio.

Players:GetBanHistoryAsync(userId:[number](/docs/luau/numbers)):[BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers) |

Returns

[BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages)

See [BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages) for return reference.

Retrieves the ban and unban history of any user within the experience's
universe. This method returns a [BanHistoryPages](/docs/reference/engine/classes/BanHistoryPages) instance that
inherits from [Pages](/docs/reference/engine/classes/Pages). This method is enabled and disabled by the
[Players.BanningEnabled](/docs/reference/engine/classes/Players#BanningEnabled) property, which you can toggle in Studio.

This function call will only succeed on production game servers and not on
client devices or in Studio.

This API uses the
[User Restrictions Open Cloud API](/docs/cloud/reference/UserRestriction). You
will be able to utilize these APIs to manage your bans in third party
applications.

Provide feedback

---

GetCharacterAppearanceAsync

Deprecated

Show details

---

GetCharacterAppearanceInfoAsync

Yields

Returns information about the character appearance of a given user.

Players:GetCharacterAppearanceInfoAsync(userId:[number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The \**userId* of the specified player. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary containing information about the character appearance of
a given user.

This function returns information about a player's avatar on the Roblox
website in the form of a dictionary. It is not to be confused with
[GetCharacterAppearanceAsync](/docs/reference/engine/classes/Players#GetCharacterAppearanceAsync),
which actually loads the assets described by this method. You can use
[InsertService:LoadAsset()](/docs/reference/engine/classes/InsertService#LoadAsset) to load the assets that are used in the
player's avatar. The structure of the returned dictionary is as follows:

| Name | Type | Description |
| --- | --- | --- |
| assets | table (see below) | Describes the equipped assets (hats, body parts, etc) |
| bodyColors | table (see below) | Describes the BrickColor values for each limb |
| bodyColor3s | table (see below) | Describes the Color3 instance for each limb which may not match perfectly with bodyColors |
| defaultPantsApplied | bool | Describes whether default pants are applied |
| defaultShirtApplied | bool | Describes whether default shirt is applied |
| emotes | table (see below) | Describes the equipped emote animations |
| playerAvatarType | string | Either "R15" or "R6" |
| scales | table (see below) | Describes various body scaling factors |

##### Assets Sub-Table

The assets table is an array of tables containing the following keys
that describe the assets currently equipped by the player:

| Name | Type | Description |
| --- | --- | --- |
| id | number | The asset ID of the equipped asset |
| assetType | table | A table with name and id fields, each describing the kind of asset equipped ("Hat", "Face", etc.) |
| name | string | The name of the equipped asset |

##### Scales Sub-Table

The scales table has the following keys, each a number corresponding to
one [Humanoid](/docs/reference/engine/classes/Humanoid) scaling property: bodyType, head, height,
proportion, depth, width.

##### Body Colors Sub-Table

The bodyColors table has the following keys, each a number corresponding
to a [BrickColor](/docs/reference/engine/datatypes/BrickColor) ID number which can be used with
[BrickColor.new(id)](/docs/reference/engine/datatypes/BrickColor#new): leftArmColorId, torsoColorId,
rightArmColorId, headColorId, leftLegColorId, rightLegColorId.

Code Samples

Example Return Character Appearance Dictionary

Sometimes it is best to see an example of the returned dictionary structure in
pure Lua. Here is one such example of a player whose avatar uses a package and
wears several hats. Can you guess who it is?

```
local result = {



playerAvatarType = "R15",



defaultPantsApplied = false,



defaultShirtApplied = false,



scales = {



bodyType = 0,



head = 1,



height = 1.05,



proportion = 0,



depth = 0.92,



width = 0.85,



},



bodyColors = {



leftArmColorId = 1030,



torsoColorId = 1001,



rightArmColorId = 1030,



headColorId = 1030,



leftLegColorId = 1001,



rightLegColorId = 1001,



},



assets = {



{



id = 1031492,



assetType = {



name = "Hat",



id = 8,



},



name = "Striped Hat",



},



{



id = 13062491,



assetType = {



name = "Face Accessory",



id = 42,



},



name = "Vision Française ",



},



{



id = 16598440,



assetType = {



name = "Neck Accessory",



id = 43,



},



name = "Red Bow Tie",



},



{



id = 28999228,



assetType = {



name = "Face",



id = 18,



},



name = "Joyous Surprise",



},



{



id = 86896488,



assetType = {



name = "Shirt",



id = 11,



},



name = "Expensive Red Tuxedo Jacket",



},



{



id = 86896502,



assetType = {



name = "Pants",



id = 12,



},



name = "Expensive Red Tuxedo Pants",



},



{



id = 376530220,



assetType = {



name = "Left Arm",



id = 29,



},



name = "ROBLOX Boy Left Arm",



},



{



id = 376531012,



assetType = {



name = "Right Arm",



id = 28,



},



name = "ROBLOX Boy Right Arm",



},



{



id = 376531300,



assetType = {



name = "Left Leg",



id = 30,



},



name = "ROBLOX Boy Left Leg",



},



{



id = 376531703,



assetType = {



name = "Right Leg",



id = 31,



},



name = "ROBLOX Boy Right Leg",



},



{



id = 376532000,



assetType = {



name = "Torso",



id = 27,



},



name = "ROBLOX Boy Torso",



},



},



}



print(result)
```

Provide feedback

---

GetFriendsAsync

Yields

Returns a [FriendPages](/docs/reference/engine/classes/FriendPages) object which contains information for all of
the given player's connections.

Players:GetFriendsAsync(userId:[number](/docs/luau/numbers)):[FriendPages](/docs/reference/engine/classes/FriendPages)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The user ID of the player being specified. |

Returns

[FriendPages](/docs/reference/engine/classes/FriendPages)

The GetFriends [Players](/docs/reference/engine/classes/Players) function returns a [FriendPages](/docs/reference/engine/classes/FriendPages)
object which contains information for all of the given user's connections.
The items within the [FriendPages](/docs/reference/engine/classes/FriendPages) object are tables with the
following fields:

| Name | Type | Description |
| --- | --- | --- |
| Id | int64 | The connections's UserId |
| Username | string | The connections's username |
| DisplayName | string | The [display name](/docs/reference/engine/classes/Player#DisplayName) of the connections. |

See the code samples for an easy way to iterate over all a player's
connections.

Code Samples

Print Roblox Connections

This code sample loads the [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the player whose username
is provided at the top of the script by using
[Players:GetUserIdFromNameAsync()](/docs/reference/engine/classes/Players#GetUserIdFromNameAsync). Then, it gets a FriendPages object
by calling [Players:GetFriendsAsync()](/docs/reference/engine/classes/Players#GetFriendsAsync) and iterates over each entry
using the iterPageItems function. The username of each connection is stored in a
table, then printed at the end.

```
local Players = game:GetService("Players")



local USERNAME = "Cozecant"



local function iterPageItems(pages)



return coroutine.wrap(function()



local pagenum = 1



while true do



for _, item in ipairs(pages:GetCurrentPage()) do



coroutine.yield(item, pagenum)



end



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



pagenum = pagenum + 1



end



end)



end



-- First, get the user ID of the player



local userId = Players:GetUserIdFromNameAsync(USERNAME)



-- Then, get a FriendPages object for their connections



local friendPages = Players:GetFriendsAsync(userId)



-- Iterate over the items in the pages. For FriendPages, these



-- are tables of information about the connection, including Username.



-- Collect each username in a table



local usernames = {}



for item, _pageNo in iterPageItems(friendPages) do



table.insert(usernames, item.Username)



end



print("Connections of " .. USERNAME .. ": " .. table.concat(usernames, ", "))
```

Provide feedback

---

GetHumanoidDescriptionFromOutfitIdAsync

Yields

Returns the HumanoidDescription for a specified outfit, which will be set
with the parts/colors/Animations etc of the outfit.

Players:GetHumanoidDescriptionFromOutfitIdAsync(outfitId:[number](/docs/luau/numbers)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Parameters

|  |
| --- |
| outfitId:[number](/docs/luau/numbers)  The ID of the outfit for which the HumanoidDescription is sought. |

Returns

[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

HumanoidDescription initialized with the specification for the passed
in outfitId.

Returns the HumanoidDescription for a specified outfitId, which will be
set with the parts/colors/Animations etc of the outfit. An outfit can be
one created by a user, or it can be the outfit for a bundle created by
Roblox.

Code Samples

Get HumanoidDescription From Outfit ID

Shows how to get the HumanoidDescription for bundle 799 (Fishman).

```
local Players = game:GetService("Players")



local Workspace = game:GetService("Workspace")



local function getOutfitId(bundleId)



if bundleId <= 0 then



return



end



local info = game.AssetService:GetBundleDetailsAsync(bundleId)



if not info then



return



end



for _, item in pairs(info.Items) do



if item.Type == "UserOutfit" then



return item.Id



end



end



return nil



end



local function getHumanoidDescriptionBundle(bundleId)



local itemId = getOutfitId(bundleId)



if itemId and itemId > 0 then



return Players:GetHumanoidDescriptionFromOutfitId(itemId)



end



return nil



end



local humanoidDescription = getHumanoidDescriptionBundle(799)



local humanoidModel = Players:CreateHumanoidModelFromDescription(humanoidDescription, Enum.HumanoidRigType.R15)



humanoidModel.Parent = Workspace
```

Provide feedback

---

GetHumanoidDescriptionFromOutfitId

Deprecated

Show details

---

GetHumanoidDescriptionFromUserIdAsync

Yields

Returns a HumanoidDescription which specifies everything equipped for the
avatar of the user specified by the passed in userId.

Players:GetHumanoidDescriptionFromUserIdAsync(userId:[number](/docs/luau/numbers)):[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The userId for a Roblox user. (The UserId is the number in the profile of the user e.g [www.roblox.com/users/1/profile](http://www.roblox.com/users/1/profile)). |

Returns

[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

HumanoidDescription initialized with the passed in user's avatar
specification.

Returns a HumanoidDescription which specifies everything equipped for the
avatar of the user specified by the passed in userId. Also includes scales
and body colors.

Code Samples

Get HumanoidDescription From User ID

This code sample shows how to use GetHumanoidDescriptionFromUserId() to create
a Humanoid Model.

```
game.Players:CreateHumanoidModelFromDescription(



game.Players:GetHumanoidDescriptionFromUserId(1),



Enum.HumanoidRigType.R15



).Parent =



game.Workspace
```

Provide feedback

---

GetHumanoidDescriptionFromUserId

Deprecated

Show details

---

GetNameFromUserIdAsync

Yields

Sends a query to the Roblox website for the username of an account with a
given [UserId](/docs/reference/engine/classes/Player#UserId).

Players:GetNameFromUserIdAsync(userId:[number](/docs/luau/numbers)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the player being specified. |

Returns

[string](/docs/luau/strings)

The name of a user with the specified [Player.UserId](/docs/reference/engine/classes/Player#UserId).

The GetNameFromUserIdAsync [Players](/docs/reference/engine/classes/Players) function will send a query to
the Roblox website asking what the username is of the account with the
given [UserId](/docs/reference/engine/classes/Player#UserId).

This method errors if no account exists with the given UserId. If you
aren't certain such an account exists, it's recommended to wrap calls to
this function with [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall). In addition, you can
manually cache results to make future calls with the same UserId fast. See
the code samples to learn more.

Code Samples

Get Name from UserId

This code sample demonstrates using the
[Players:GetNameFromUserIdAsync()](/docs/reference/engine/classes/Players#GetNameFromUserIdAsync) method to get a user's
[Player.Name](/docs/reference/engine/classes/Player#Name) from their [Player.UserId](/docs/reference/engine/classes/Player#UserId).

```
local Players = game:GetService("Players")



-- Example Data:



-- UserId: 118271    Name: "RobloxRulez"



-- UserId: 131963979 Name: "docsRule"



local nameOne = Players:GetNameFromUserIdAsync(118271)



local nameTwo = Players:GetNameFromUserIdAsync(131963979)



print(nameOne, nameTwo)



-- prints: "RobloxRulez docsRule"
```

Get Name from UserId using a cache

This code sample demonstrates using the
[Players:GetNameFromUserIdAsync()](/docs/reference/engine/classes/Players#GetNameFromUserIdAsync) method to get a user's
[Player.Name](/docs/reference/engine/classes/Player#Name) from their [Player.UserId](/docs/reference/engine/classes/Player#UserId). Because
[GetNameFromUserIdAsync()](/docs/reference/engine/classes/Players#GetNameFromUserIdAsync) yields, you
can avoid calling it for the same [Name](/docs/reference/engine/classes/Player#Name) using a table to
store each UserId:Name pair found, called a cache.
[pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) is used to catch the failure in case the Name
doesn't exist.

```
local Players = game:GetService("Players")



-- Create a table called 'cache' to store each 'Name' as they are found.



-- If we lookup a 'Name' using the same 'UserId', the 'Name' will come



-- from cache (fast) instead of GetNameFromUserIdAsync() (yields).



local cache = {}



function getNameFromUserId(userId)



-- First, check if the cache contains 'userId'



local nameFromCache = cache[userId]



if nameFromCache then



-- if a value was stored in the cache at key 'userId', then this 'nameFromCache'



-- is the correct Name and we can return it.



return nameFromCache



end



-- If here, 'userId' was not previously looked up and does not exist in the



-- cache. Now we need to use GetNameFromUserIdAsync() to look up the name



local name



local success, _ = pcall(function()



name = Players:GetNameFromUserIdAsync(userId)



end)



if success then



-- if 'success' is true, GetNameFromUserIdAsync() successfully found the



-- name. Store this name in the cache using 'userId' as the key so we



-- never have to look this name up in the future. Then return name.



cache[userId] = name



return name



end



-- If here, 'success' was false, meaning GetNameFromUserIdAsync()



-- was unable to find the 'name' for the 'userId' provided. Warn the user



-- this happened and then return nothing, or nil.



warn("Unable to find Name for UserId:", userId)



return nil



end



-- Example Data:



-- UserId: 118271    Name: "RobloxRulez"



-- UserId: 131963979 Name: "docsRule"



-- The first time a UserId is used, GetNameFromUserIdAsync() will be called



local nameOne = getNameFromUserId(118271)



local nameTwo = getNameFromUserId(131963979)



-- Because 118271 was previously used, get its Name from the cache



local nameOneQuick = getNameFromUserId(118271)



print(nameOne, nameTwo, nameOneQuick)



-- prints: "RobloxRulez docsRule RobloxRulez"
```

Provide feedback

---

GetPlayerByUserId

Write Parallel

Returns the [Player](/docs/reference/engine/classes/Player) with the given [UserId](/docs/reference/engine/classes/Player#UserId) if
they are in-game.

Players:GetPlayerByUserId(userId:[number](/docs/luau/numbers)):[Player](/docs/reference/engine/classes/Player)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the player being specified. |

Returns

[Player](/docs/reference/engine/classes/Player)

This function searches each [Player](/docs/reference/engine/classes/Player) in [Players](/docs/reference/engine/classes/Players) for one
whose [Player.UserId](/docs/reference/engine/classes/Player#UserId) matches the given userId. If such a player
does not exist, it returns nil.

This method is useful in finding the purchaser of a developer product
using [MarketplaceService.ProcessReceipt](/docs/reference/engine/classes/MarketplaceService#ProcessReceipt) which provides a table
that includes the purchaser's [UserId](/docs/reference/engine/classes/Player#UserId) and not a
reference to the [Player](/docs/reference/engine/classes/Player) object itself. Most experiences will
require a reference to the player in order to grant products.

Code Samples

Players:GetPlayerByUserId

```
local Players = game:GetService("Players")



local player = Players:GetPlayerByUserId(1)



if player then



print("Player with userId 1 is in this server! Their name is: " .. player.Name)



else



print("Player with userId 1 is not in this server!")



end
```

Provide feedback

---

GetPlayerFromCharacter

Returns the [Player](/docs/reference/engine/classes/Player) whose [Player.Character](/docs/reference/engine/classes/Player#Character) matches the
given instance, or nil if one cannot be found.

Players:GetPlayerFromCharacter(character:[Model](/docs/reference/engine/classes/Model)):[Player](/docs/reference/engine/classes/Player)

Parameters

|  |
| --- |
| character:[Model](/docs/reference/engine/classes/Model)  A character instance that you want to get the player from. |

Returns

[Player](/docs/reference/engine/classes/Player)

This function returns the [Player](/docs/reference/engine/classes/Player) associated with the given
[Player.Character](/docs/reference/engine/classes/Player#Character), or nil if one cannot be found. It is
equivalent to the following function:

```
local function getPlayerFromCharacter(character)



for _, player in game:GetService("Players"):GetPlayers() do



if player.Character == character then



return player



end



end



end
```

This method is often used when some event in player's character fires
(such as their [Humanoid](/docs/reference/engine/classes/Humanoid) [dying](/docs/reference/engine/classes/Humanoid#Died)). Such an
event might not directly reference the Player object, but this method
provides easy access. The inverse of this function can be described as
getting the Character of a Player. To do this, simply access the Character
property.

Code Samples

Players:GetPlayerFromCharacter

Players:GetPlayerFromCharacter

```
local Players = game:GetService("Players")



local Workspace = game:GetService("Workspace")



local PLAYER_NAME = "Nightriff"



local character = Workspace:FindFirstChild(PLAYER_NAME)



local player = Players:GetPlayerFromCharacter(character)



if player then



print(`Player {player.Name} ({player.UserId}) is in the game`)



else



print(`Player {PLAYER_NAME} is not in the game!`)



end
```

Provide feedback

---

GetPlayers

Write Parallel

Returns a table of all presently connected [Player](/docs/reference/engine/classes/Player) objects.

Players:GetPlayers():Instances

Returns

Instances

A table containing all the players in the server.

This method returns a table of all presently connected [Player](/docs/reference/engine/classes/Player)
objects. It functions the same way [Instance:GetChildren()](/docs/reference/engine/classes/Instance#GetChildren) would
except that it only returns [Player](/docs/reference/engine/classes/Player) objects found under
[Players](/docs/reference/engine/classes/Players). When used with a for loop, it is useful for iterating
over all players in a game.

```
local Players = game:GetService("Players")



for _, player in Players:GetPlayers() do



print(player.Name)



end
```

Scripts that connect to [Players.PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded) are often trying to
process every Player that connects to the game. This method is useful for
iterating over already-connected players that wouldn't fire
[PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded). Using this method ensures that no
player is missed!

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



print("Player: " .. player.Name)



end



for _, player in Players:GetPlayers() do



onPlayerAdded(player)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Code Samples

Give Sparkles to Everyone

This code sample listens for players spawning and gives them Sparkles in their
head. It does this by defining two functions, onPlayerSpawned and
onPlayerAdded.

```
local Players = game:GetService("Players")



local function onCharacterAdded(character)



-- Give them sparkles on their head if they don't have them yet



if not character:FindFirstChild("Sparkles") then



local sparkles = Instance.new("Sparkles")



sparkles.Parent = character:WaitForChild("Head")



end



end



local function onPlayerAdded(player)



-- Check if they already spawned in



if player.Character then



onCharacterAdded(player.Character)



end



-- Listen for the player (re)spawning



player.CharacterAdded:Connect(onCharacterAdded)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

getPlayers

Deprecated

Show details

---

GetUserIdFromNameAsync

Yields

Sends a query to the Roblox website for the [userId](/docs/reference/engine/classes/Player#UserId)
of an account with a given username.

Players:GetUserIdFromNameAsync(userName:[string](/docs/luau/strings)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| userName:[string](/docs/luau/strings)  The username of the player being specified. |

Returns

[number](/docs/luau/numbers)

The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of a user whose name is specified.

This function will send a query to the Roblox website asking what the
[Player.UserId](/docs/reference/engine/classes/Player#UserId) is of the account with the given [Player](/docs/reference/engine/classes/Player)
name.

This method errors if no account exists with the given username. If you
aren't certain such an account exists, it's recommended to wrap calls to
this function with [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall). In addition, you can
manually cache results to quickly make future calls with the same
username. See the code samples to learn more.

Code Samples

Get UserId from Name

This code sample demonstrates using the
[Players:GetUserIdFromNameAsync()](/docs/reference/engine/classes/Players#GetUserIdFromNameAsync) method to get a user's
[Player.UserId](/docs/reference/engine/classes/Player#UserId) from their [Player.Name](/docs/reference/engine/classes/Player#Name).

```
local Players = game:GetService("Players")



-- Example Data:



-- UserId: 118271    Name: "RobloxRulez"



-- UserId: 131963979 Name: "docsRule"



local userIdOne = Players:GetUserIdFromNameAsync("RobloxRulez")



local userIdTwo = Players:GetUserIdFromNameAsync("docsRule")



print(userIdOne, userIdTwo)



-- prints: "118271 131963979"
```

Get UserId from Name using a cache

This code sample demonstrates using the
[Players:GetUserIdFromNameAsync()](/docs/reference/engine/classes/Players#GetUserIdFromNameAsync) method to get a user's
[Player.UserId](/docs/reference/engine/classes/Player#UserId) from their [Player.Name](/docs/reference/engine/classes/Player#Name). Because
[GetUserIdFromNameAsync()](/docs/reference/engine/classes/Players#GetUserIdFromNameAsync) yields, you
can avoid calling it for the same [UserId](/docs/reference/engine/classes/Player#UserId) using a table
to store each Name:UserId pair found, called a cache.
[pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) is used to catch the failure in case the UserId
doesn't exist.

```
local Players = game:GetService("Players")



-- Create a table called 'cache' to store each 'UserId' as they are found.



-- If we lookup a 'UserId' using the same 'Name', the 'UserId' will come



-- from cache (fast) instead of GetUserIdFromNameAsync() (yields).



local cache = {}



function getUserIdFromName(name)



-- First, check if the cache contains 'name'



local userIdFromCache = cache[name]



if userIdFromCache then



-- if a value was stored in the cache at key 'name', then this 'userIdFromCache'



-- is the correct UserId and we can return it.



return userIdFromCache



end



-- If here, 'name' was not previously looked up and does not exist in the



-- cache. Now we need to use GetUserIdFromNameAsync() to look up the userId



local userId



local success, _ = pcall(function()



userId = Players:GetUserIdFromNameAsync(name)



end)



if success then



-- if 'success' is true, GetUserIdFromNameAsync() successfully found the



-- userId. Store this userId in the cache using 'name' as the key so we



-- never have to look this userId up in the future. Then return userId.



cache[name] = userId



return userId



end



-- If here, 'success' was false, meaning GetUserIdFromNameAsync()



-- was unable to find the 'userId' for the 'name' provided. We can warn the



-- user this happened and then return nothing, or nil.



warn("Unable to find UserId for Name:", name)



return nil



end



-- Example Data:



-- UserId: 118271    Name: "RobloxRulez"



-- UserId: 131963979 Name: "docsRule"



-- The first time a Name is used, GetUserIdFromNameAsync() will be called



local userIdOne = getUserIdFromName("RobloxRulez")



local userIdTwo = getUserIdFromName("docsRule")



-- Because "RobloxRulez" was previously used, get its UserId from the cache



local userIdOneQuick = getUserIdFromName("RobloxRulez")



print(userIdOne, userIdTwo, userIdOneQuick)



-- prints: "118271 131963979 118271"
```

Provide feedback

---

GetUserThumbnailAsync

Yields

Returns the content URL of a player thumbnail given the size and type, as
well as a boolean describing if the image is ready to use.

Players:GetUserThumbnailAsync(

userId:[number](/docs/luau/numbers), thumbnailType:[Enum.ThumbnailType](/docs/reference/engine/enums/ThumbnailType), thumbnailSize:[Enum.ThumbnailSize](/docs/reference/engine/enums/ThumbnailSize)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the player being specified. |
| thumbnailType:[Enum.ThumbnailType](/docs/reference/engine/enums/ThumbnailType)  A [Enum.ThumbnailType](/docs/reference/engine/enums/ThumbnailType) describing the type of thumbnail. |
| thumbnailSize:[Enum.ThumbnailSize](/docs/reference/engine/enums/ThumbnailSize)  A [Enum.ThumbnailSize](/docs/reference/engine/enums/ThumbnailSize) specifying the size of the thumbnail. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing the content URL of a user thumbnail based on the
specified parameters, and a bool describing if the image is ready to
be used or not.

This function returns the content URL of an image of a player's avatar
given their [UserId](/docs/reference/engine/classes/Player#UserId), the desired image size as a
[Enum.ThumbnailSize](/docs/reference/engine/enums/ThumbnailSize) enum, and the desired type as a [Enum.ThumbnailType](/docs/reference/engine/enums/ThumbnailType)
enum. It also returns a boolean describing if the image is ready to use.

Most often, this method is used with [ImageLabel.Image](/docs/reference/engine/classes/ImageLabel#Image) or
[Decal.Texture](/docs/reference/engine/classes/Decal#Texture) to display user avatar pictures in an experience.

Code Samples

Display Player Thumbnail

This code sample displays the current player's thumbnail in a parent
ImageLabel by using [Players:GetUserThumbnailAsync()](/docs/reference/engine/classes/Players#GetUserThumbnailAsync) and setting the
[Image()](/docs/reference/engine/classes/ImageLabel#Image) property as well as its
[Size()](/docs/reference/engine/classes/GuiObject#Size).

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local PLACEHOLDER_IMAGE = "rbxassetid://0" -- replace with placeholder image



-- fetch the thumbnail



local userId = player.UserId



local thumbType = Enum.ThumbnailType.HeadShot



local thumbSize = Enum.ThumbnailSize.Size420x420



local content, isReady = Players:GetUserThumbnailAsync(userId, thumbType, thumbSize)



-- set the ImageLabel's content to the user thumbnail



local imageLabel = script.Parent



imageLabel.Image = (isReady and content) or PLACEHOLDER_IMAGE



imageLabel.Size = UDim2.new(0, 420, 0, 420)
```

Provide feedback

---

playerFromCharacter

Deprecated

Show details

---

players

Deprecated

Show details

---

SetChatStyle

Plugin Security

Sets whether BubbleChat and ClassicChat are being used, and tells TeamChat
and [Chat](/docs/reference/engine/classes/Chat) what to do.

Players:SetChatStyle(style:[Enum.ChatStyle](/docs/reference/engine/enums/ChatStyle)):()

Parameters

|  |
| --- |
| style:[Enum.ChatStyle](/docs/reference/engine/enums/ChatStyle) Default Value: "Classic" The specified chat style being set. |

Returns

()

This function sets whether BubbleChat and ClassicChat are being used, and
tells TeamChat and Chat what to do using the [Enum.ChatStyle](/docs/reference/engine/enums/ChatStyle) enum. Since
this item is protected, attempting to use it in a [Script](/docs/reference/engine/classes/Script) or
[LocalScript](/docs/reference/engine/classes/LocalScript) will cause an error.

This function is used internally when the chat mode is set by the game.

Code Samples

Setting a Player's Chat Style

This example demonstrates that the [Players:SetChatStyle()](/docs/reference/engine/classes/Players#SetChatStyle) function
executes without error if using the Command Bar or a Plugin and errors if
executed in a LocalScript.

When executed in the Command Bar, this code sets the chat style to Classic
using the [Enum.ChatStyle](/docs/reference/engine/enums/ChatStyle) enum.

```
-- Command bar



game.Players:SetChatStyle(Enum.ChatStyle.Classic) -- Set's chat style to Classic



-- LocalScript



local Players = game:GetService("Players")



Players:SetChatStyle(Enum.ChatStyle.Classic) -- Errors
```

Provide feedback

---

TeamChat

Plugin Security

Makes the local player chat the given message, which will only be viewable
by users on the same team.

Players:TeamChat(message:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings)  The message being chatted. |

Returns

()

This function makes the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) chat the given
message, which will only be viewable by users on the same team. Since this
item is protected, attempting to use it in a [Script](/docs/reference/engine/classes/Script) or
[LocalScript](/docs/reference/engine/classes/LocalScript) will cause an error.

This function is used internally when the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer)
sends a message to their team.

Code Samples

Sending Team Chat

This example demonstrates that the [Players:TeamChat()](/docs/reference/engine/classes/Players#TeamChat) function
executes without error if using the Command Bar or a Plugin and errors if
executed in a LocalScript.

When executed in the Command Bar, the function sends the specified message to
all players on the same Team as the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer).

```
-- Command bar



game.Players:TeamChat("Hello World") -- Sends a "Hello World" message to all players on the local player's team



-- LocalScript



local Players = game:GetService("Players")



Players:TeamChat("Hello World") -- Errors
```

Provide feedback

---

UnbanAsync

Yields

Unbans players banned from [Players:BanAsync()](/docs/reference/engine/classes/Players#BanAsync) or the User
Restrictions Open Cloud API. This method is enabled and disabled by the
[Players.BanningEnabled](/docs/reference/engine/classes/Players#BanningEnabled) property, which you can toggle in Studio.

Players:UnbanAsync(config:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| config:[Dictionary](/docs/luau/tables#dictionaries)  | Name | Type | Description | | --- | --- | --- | | UserIds | array | UserIDs to be force allowed into the experience(s).    Max size is 50. | | ApplyToUniverse | boolean | Propagates the unban to all places within this universe. | |

Returns

()

Unbans players banned from [Players:BanAsync()](/docs/reference/engine/classes/Players#BanAsync) or the
[User Restrictions Open Cloud API](/docs/cloud/reference/UserRestriction). This
method is enabled and disabled by the [Players.BanningEnabled](/docs/reference/engine/classes/Players#BanningEnabled)
property, which you can toggle in Studio.

Like [Players:BanAsync()](/docs/reference/engine/classes/Players#BanAsync), this method takes in a config
dictionary that will let you bulk unban users. This configures the users
that are unbanned and the scope from which they are unbanned from.

Unbans will only take effect on bans with the same ApplyToUniverse
scope. For example, an unban with ApplyToUniverse set to true will not
invalidate a previous ban with ApplyToUniverse set to false. In other
words, a universe level unban will not invalidate a place level ban. The
opposite also holds true.

This method invokes a HTTP call to backend services, which are throttled
and may fail. If you are calling this API with multiple UserIds, this
method will attempt to make this HTTP call for each UserId. It will then
aggregate any error messages and join them as a comma separated list. For
example, if this method is invoked for five UserIds: {1, 2, 3, 4, 5}
and requests for users 2 and 4 fail then the following error message
appears:
HTTP failure for UserId 2: Timedout, HTTP 504 (Service unavailable) failure for UserId 4: Service exception.
The message will always include failure for UserId {} if it is an HTTP
error. It is undefined behavior if you pass in both valid and invalid
UserIds, i.e. a UserId that is not a positive number, as some network
requests may succeed before all input is validated.

Because of the risks associated with banning users, this method may only
be called on the backend game server. Client side calls will result in an
error. You may test this API in Studio, Team Create, and Team Test, but
the bans will not apply to production. This function call will only
attempt ban requests on production game servers and not in Studio testing.
However, all input validation steps will still work in Studio.

This API uses the
[User Restrictions Open Cloud API](/docs/cloud/reference/UserRestriction). You
will be able to utilize these APIs to manage your bans in third party
applications.

Code Samples

Unbanning Users

The following un-bans a user, as well as another unrelated account with UserId 789.

```
local Players = game:GetService("Players")



if shouldBeUnbanned(player) then



local config: UnbanConfigType = {



UserIds = { player.UserId, 789 },



ApplyToUniverse = false,



}



local success, err = pcall(function()



return Players:UnbanAsync(config)



end)



print(success, err)



end
```

Provide feedback

---

Events

PlayerAdded

Fires when a player enters the game.

Players.PlayerAdded(player:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  An instance of the player that joined the game. |

This event fires when a player enters the game. This is used to fire an
event when a player joins a game, such as loading the player's saved
[GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) data.

This can be used alongside the [Players.PlayerRemoving](/docs/reference/engine/classes/Players#PlayerRemoving) event, which
fires when a player is about to leave the game. For instance, if you would
like print a message every time a new player joins or leaves the game:

```
local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



print(player.Name .. " joined the game!")



end)



Players.PlayerRemoving:Connect(function(player, reason)



print(player.Name .. " left the game! Reason: " .. tostring(exitReason))



end)
```

If you want to track when a player's character is added or removed from
the game, such as when a player respawns or dies, you can use the
[Player.CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) and [Player.CharacterRemoving](/docs/reference/engine/classes/Player#CharacterRemoving)
functions.

Note that this event does not work as expected in a solo playtest mode
because the player is created before scripts run that connect to
[PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded). To handle this case, as well as
cases in which the script is added into the game after a player enters,
create an onPlayerAdded() function that you can call to handle a
player's entrance.

Code Samples

Players.PlayerAdded

This example will print "A player has entered: " followed by the name of the
player that enters/joins a game every time a player joins.

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



print("A player has entered: " .. player.Name)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

PlayerMembershipChanged

Fires when the game server recognizes that a player's membership has
changed.

Players.PlayerMembershipChanged(player:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |

This event fires when the game server recognizes that a player's
membership has changed. Note, however, that the server will only attempt
to check and update the membership after the Premium modal has been
closed. Thus, to account for cases where the user purchases Premium
outside of the game while playing, you must still prompt them to
purchase Premium; this will then show a message telling them they're
already upgraded and, once they close the modal, the game server will
update their membership and trigger this event.

To learn more about and incorporating Premium into your experience and
monetizing with the engagement-based payouts system, see
[Engagement-Based Payouts](/docs/production/monetization/engagement-based-payouts).

See also:

* [MarketplaceService:PromptPremiumPurchase()](/docs/reference/engine/classes/MarketplaceService#PromptPremiumPurchase), used to prompt a
  user to purchase Premium
* [MarketplaceService.PromptPremiumPurchaseFinished](/docs/reference/engine/classes/MarketplaceService#PromptPremiumPurchaseFinished), fires when the
  Premium purchase UI closes

Code Samples

Handling Premium Membership Changes

The function in the code sample runs after the game server confirms a player's
membership has changed. It demonstrates how you can grant players access to
Premium benefits (or revoke them) when their membership status changes.

```
local Players = game:GetService("Players")



local function grantPremiumBenefits(player)



-- Grant the player access to Premium-only areas, items, or anything you can imagine!



print("Giving", player, "premium benefits!")



end



local function playerAdded(player)



if player.MembershipType == Enum.MembershipType.Premium then



grantPremiumBenefits(player)



end



end



local function playerMembershipChanged(player)



print("Received event PlayerMembershipChanged. New membership = " .. tostring(player.MembershipType))



if player.MembershipType == Enum.MembershipType.Premium then



grantPremiumBenefits(player)



end



end



Players.PlayerAdded:Connect(playerAdded)



Players.PlayerMembershipChanged:Connect(playerMembershipChanged)
```

Provide feedback

---

PlayerRemoving

Fires when a player is about to leave the game.

Players.PlayerRemoving(

player:[Player](/docs/reference/engine/classes/Player), reason:[Enum.PlayerExitReason](/docs/reference/engine/enums/PlayerExitReason)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  An instance of the player that is leaving the game. |
| reason:[Enum.PlayerExitReason](/docs/reference/engine/enums/PlayerExitReason)  Enum.PlayerExitReason in attempt to inform why. |

The PlayerRemoving event fires right before a [Player](/docs/reference/engine/classes/Player) leaves the
game. This event fires before [ChildRemoved](/docs/reference/engine/classes/Instance#ChildRemoved)
does on [Players](/docs/reference/engine/classes/Players), and behaves somewhat similarly to
[Instance.DescendantRemoving](/docs/reference/engine/classes/Instance#DescendantRemoving). Since it fires before the actual
removal of a [Player](/docs/reference/engine/classes/Player), this event is useful for storing player data
using a [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore).

This can be used alongside the [Player.PlayerAdded](/docs/reference/engine/classes/Player#PlayerAdded) event, which
fires when a player joins the game. For instance, to print a message every
time a new player joins or leaves the game:

```
local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



print(player.Name .. " joined the game!")



end)



Players.PlayerRemoving:Connect(function(player, exitReason)



print(player.Name .. " left the game! - Reason: " .. tostring(exitReason))



end)
```

If you want to track when a player's character is added or removed from
the game, such as when a player respawns or dies, you can use the
[Player.CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) and [Player.CharacterRemoving](/docs/reference/engine/classes/Player#CharacterRemoving)
functions.

Code Samples

Players.PlayerRemoving

This code will print "A player has left: ", followed by the player's name,
every time a player leaves:

```
local Players = game:GetService("Players")



local function onPlayerRemoving(player)



print("A player has left: " .. player.Name)



end



Players.PlayerRemoving:Connect(onPlayerRemoving)
```

Provide feedback

---

UserSubscriptionStatusChanged

Fires when the game server recognizes that the user's status for a certain
subscription has changed.

Players.UserSubscriptionStatusChanged(

user:[Player](/docs/reference/engine/classes/Player), subscriptionId:[string](/docs/luau/strings)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| user:[Player](/docs/reference/engine/classes/Player)  User whose subscription status has changed. |
| subscriptionId:[string](/docs/luau/strings)  The ID of the subscription with a status change. |

This event fires when the game server recognizes that the user's status
for a certain subscription has changed. Note that the server only attempts
to check and update the status after the Subscription Purchase modal
has been closed. To account for cases in which the user purchases the
subscription outside of the game while playing, you must still prompt
them to purchase the subscription; the prompt shows a message telling the
user they're already subscribed, and after they close the modal, the game
server updates their subscription status and triggers this event.

Note that only server scripts receive this event.

Provide feedback

---