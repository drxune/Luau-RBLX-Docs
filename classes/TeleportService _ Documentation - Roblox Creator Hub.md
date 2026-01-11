# TeleportService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TeleportService
Scraped: 2026-01-11T02:42:39.838561Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- TeleportService
- Players
- Player
- LocalPlayer
- CoreGui
- loading screen
- parented
- PlayerGui
- Players.LocalPlayer
- DataStoreService
- PlaceId
- JobId
- UserId
- Player.UserId
- TeleportService:TeleportToPlaceInstance()
- TeleportService:ReserveServer()
- TeleportService:SetTeleportSetting()
- GlobalDataStore:SetAsync()
- GlobalDataStore
- GlobalDataStores
- DataModel.UniverseId
- TeleportService.TeleportInitFailed
- DataModel.PrivateServerId
- DataModel.PlaceId
- TeleportService:TeleportToPrivateServer()
- TeleportService:TeleportAsync()
- TeleportOptions.ReservedServerAccessCode
- DataModel.JobId
- PrivateServerId
- DataModel.MatchmakingType
- teleport GUI
- ScreenGui
- RemoteEvent
- TeleportService:GetArrivingTeleportGui()
- parent
- LocalPlayer()
- TeleportService:SetTeleportGui()
- TeleportService:GetTeleportSetting()
- TeleportService:GetLocalPlayerTeleportData()
- TeleportAsync()
- TeleportOptions
- TeleportAsyncResult
- TeleportService:TeleportPartyAsync()
- SpawnLocation
- TeleportService:Teleport()
- LocalScript
- ReplicatedFirst
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TeleportService](/docs/reference/engine/classes/TeleportService)

English

Feedback

Engine Class

TeleportService

Enables transporting [Players](/docs/reference/engine/classes/Player) between places and servers.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [CustomizedTeleportUI](#CustomizedTeleportUI):[boolean](/docs/luau/booleans)  Deprecated |

Methods

|  |
| --- |
| [GetArrivingTeleportGui](#GetArrivingTeleportGui)():[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetLocalPlayerTeleportData](#GetLocalPlayerTeleportData)():Variant |
| [GetPlayerPlaceInstanceAsync](#GetPlayerPlaceInstanceAsync)(userId: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |
| [GetTeleportSetting](#GetTeleportSetting)(setting: [string](/docs/luau/strings)):Variant |
| [PromptExperienceDetailsAsync](#PromptExperienceDetailsAsync)(player: [Player](/docs/reference/engine/classes/Player),universeId: [number](/docs/luau/numbers)):PromptExperienceDetailsResult |
| [ReserveServerAsync](#ReserveServerAsync)(placeId: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |
| [ReserveServer](#ReserveServer)(placeId: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples)  Deprecated |
| [SetTeleportGui](#SetTeleportGui)(gui: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [SetTeleportSetting](#SetTeleportSetting)(setting: [string](/docs/luau/strings),value: Variant):() |
| [Teleport](#Teleport)(placeId: [number](/docs/luau/numbers),player: [Instance](/docs/reference/engine/datatypes/Instance),teleportData: Variant,customLoadingScreen: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [TeleportAsync](#TeleportAsync)(placeId: [number](/docs/luau/numbers),players: Instances,teleportOptions: [Instance](/docs/reference/engine/datatypes/Instance)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [TeleportPartyAsync](#TeleportPartyAsync)(placeId: [number](/docs/luau/numbers),players: Instances,teleportData: Variant,customLoadingScreen: [Instance](/docs/reference/engine/datatypes/Instance)):[string](/docs/luau/strings) |
| [TeleportToPlaceInstance](#TeleportToPlaceInstance)(placeId: [number](/docs/luau/numbers),instanceId: [string](/docs/luau/strings),player: [Instance](/docs/reference/engine/datatypes/Instance),spawnName: [string](/docs/luau/strings),teleportData: Variant,customLoadingScreen: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [TeleportToPrivateServer](#TeleportToPrivateServer)(placeId: [number](/docs/luau/numbers),reservedServerAccessCode: [string](/docs/luau/strings),players: Instances,spawnName: [string](/docs/luau/strings),teleportData: Variant,customLoadingScreen: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [TeleportToSpawnByName](#TeleportToSpawnByName)(placeId: [number](/docs/luau/numbers),spawnName: [string](/docs/luau/strings),player: [Instance](/docs/reference/engine/datatypes/Instance),teleportData: Variant,customLoadingScreen: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Events

|  |
| --- |
| [LocalPlayerArrivedFromTeleport](#LocalPlayerArrivedFromTeleport)(loadingGui: [Instance](/docs/reference/engine/datatypes/Instance),dataTable: Variant):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TeleportInitFailed](#TeleportInitFailed)(player: [Instance](/docs/reference/engine/datatypes/Instance),teleportResult: [Enum.TeleportResult](/docs/reference/engine/enums/TeleportResult),errorMessage: [string](/docs/luau/strings),placeId: [number](/docs/luau/numbers),teleportOptions: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

TeleportService is responsible for transporting [Players](/docs/reference/engine/classes/Player)
between different places and servers.

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

---

API Reference

Properties

CustomizedTeleportUI

Deprecated

Show details

---

Methods

GetArrivingTeleportGui

Returns the *customLoadingScreen* the
[LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) arrived into the place with.

TeleportService:GetArrivingTeleportGui():[Instance](/docs/reference/engine/datatypes/Instance)

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The *customLoadingScreen* the [LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer)
arrived into the place with.

This function returns the *customLoadingScreen* the
[LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) arrived into the place with.

Note, the *customLoadingScreen* will not be used if the destination place
is in a different game.

#### Loading Screen

During a teleport, while the destination place is loading, the
*customLoadingScreen* is parented to the [CoreGui](/docs/reference/engine/classes/CoreGui). Once the place
has loaded the [loading screen](/docs/reference/engine/classes/ScreenGui) is
[parented](/docs/reference/engine/classes/Instance#Parent) to *nil*.

If you wish to preserve the *customLoadingScreen* and perform your own
transitions, you will need to parent it to the local player's
[PlayerGui](/docs/reference/engine/classes/PlayerGui). For an example of this, see the code sample below.

#### Studio Limitation

Note that this service does not work during playtesting in Roblox Studio;
to test aspects of your experience using it, you must publish the
experience and play it in the Roblox application.

Code Samples

Handling a Teleport Loading GUI

The following code, when placed inside a LocalScript in ReplicatedFirst
will preserve a custom teleport loading screen for five seconds before
destroying it.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



local ReplicatedFirst = game:GetService("ReplicatedFirst")



local customLoadingScreen = TeleportService:GetArrivingTeleportGui()



if customLoadingScreen then



local playerGui = Players.LocalPlayer:WaitForChild("PlayerGui")



ReplicatedFirst:RemoveDefaultLoadingScreen()



customLoadingScreen.Parent = playerGui



task.wait(5)



customLoadingScreen:Destroy()



end
```

Provide feedback

---

GetLocalPlayerTeleportData

Returns the *teleportData* the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) arrived into
the place with.

TeleportService:GetLocalPlayerTeleportData():Variant

Returns

Variant

The teleport data the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) arrived into the
place with.

This function returns the teleport data the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer)
arrived with. It can only be called from the client.

Exploiters can spoof teleport data. Send secure data such as player
currency through a server-side service such as [DataStoreService](/docs/reference/engine/classes/DataStoreService) to
prevent tampering.

Code Samples

Getting LocalPlayer Teleport Data

When put into StarterPlayerScripts, this example runs when the player joins
the game, and prints any teleport data provided by the player's previous
server.

```
local TeleportService = game:GetService("TeleportService")



local teleportData = TeleportService:GetLocalPlayerTeleportData()



print("Local player arrived with this data:", teleportData)
```

Provide feedback

---

GetPlayerPlaceInstanceAsync

Yields

Returns the [PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) and
[JobId](/docs/reference/engine/classes/DataModel#JobId) of the server the user with the given
[UserId](/docs/reference/engine/classes/Player#UserId) is in provided it is in the same game as the
current place.

TeleportService:GetPlayerPlaceInstanceAsync(userId:[number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the [Player](/docs/reference/engine/classes/Player). |

Returns

[Tuple](/docs/luau/tuples)

See the table above.

This function returns the [PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) and
[JobId](/docs/reference/engine/classes/DataModel#JobId) of the server the user with the given
[UserId](/docs/reference/engine/classes/Player#UserId) is in, provided it is in the same game as the
current place.

Then, [TeleportService:TeleportToPlaceInstance()](/docs/reference/engine/classes/TeleportService#TeleportToPlaceInstance) can be called with
this information to allow a user to join the target user's server.

Upon a successful lookup, the function returns the following values:

| # | Name | Type | Description |
| --- | --- | --- | --- |
| **1** | currentInstance | bool | A bool indicating if the user was found in the current instance |
| **2** | error | string | An error message in the event of the lookup failing |
| **3** | placeId | int64 | The PlaceId of the server the user is in |
| **4** | instanceId | string | The JobId of the server the user is in |

If there is a problem during lookup, such as the user being offline, an
error is thrown. It is recommended that you wrap calls to this function in
pcall.

#### Limitations

You should be aware of the following limitations when using this function:

* This function can only be called by the server.
* This function may fail to return the correct information if the user is
  teleporting.
* It is possible for this function to throw an error, hence developers
  should wrap it in a [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) (see example below)
* As this function returns the JobId of the server and not the access code
  returned by [TeleportService:ReserveServer()](/docs/reference/engine/classes/TeleportService#ReserveServer), the ID returned is
  not appropriate for use with reserved servers.

#### Studio Limitation

Note that this service does not work during playtesting in Roblox Studio;
to test aspects of your experience using it, you must publish the
experience and play it in the Roblox application.

Code Samples

Following Another Player

The code sample below, when placed inside a Script within
ServerScriptService, will teleport a player who's following another player
to the associated place/server. Note that this will not work if the player
being followed is in a reserved server.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



-- Is this player following anyone?



local followId = player.FollowUserId



-- If so, find out where they are



if followId and followId ~= 0 then



local _currentInstance, placeId, jobId



local success, errorMessage, _currentInstance, placeId, jobId = pcall(function()



-- followId is the user ID of the player that you want to retrieve the place and job ID for



return TeleportService:GetPlayerPlaceInstanceAsync(followId)



end)



if success then



-- Teleport player



TeleportService:TeleportToPlaceInstance(placeId, jobId, player)



else



warn(errorMessage)



end



else



warn("Player " .. player.UserId .. " is not following another player!")



end



end)
```

Provide feedback

---

GetTeleportSetting

Retrieves a teleport setting saved using
[TeleportService:SetTeleportSetting()](/docs/reference/engine/classes/TeleportService#SetTeleportSetting) using the given key.

TeleportService:GetTeleportSetting(setting:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| setting:[string](/docs/luau/strings)  The key the value was stored under using [TeleportService:SetTeleportSetting()](/docs/reference/engine/classes/TeleportService#SetTeleportSetting). |

Returns

Variant

The value stored under the given key.

This function retrieves a teleport setting saved using
[TeleportService:SetTeleportSetting()](/docs/reference/engine/classes/TeleportService#SetTeleportSetting) using the given key.

This method is intended for use on the client only and should not be used
on the server.

Teleport settings are preserved across teleportations within the same
game. This means data can be saved using
[TeleportService:SetTeleportSetting()](/docs/reference/engine/classes/TeleportService#SetTeleportSetting) in one place and retrieved
using GetTeleportSetting in another place the user has been teleported to.

For example, in a game that allowed crouching you could save whether the
user is currently crouching prior to teleporting as a teleport setting.
This could then be retrieved in the destination place after the
teleportation:

```
local TeleportService = game:GetService("TeleportService")



local isCrouching = TeleportService:GetTeleportSetting("isCrouching")
```

If no teleport setting exists under the given key, this function will
return *nil*.

#### Differences from GlobalDataStores

Although they share some similarities, there are some key differences
between teleport settings and datastores:

* [GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) stores the data on Roblox servers
  whereas SetTeleportSetting stores the data locally
* Data stored in a [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) is preserved after the user
  leaves the game universe whereas teleport settings are not
* [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) can only be accessed on the
  server, whereas teleport settings can only be accessed on the client
* [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) have usage limits, whereas
  teleport settings do not

In general teleport settings should be used to preserve client side
information within a single play session across different places in a
game. [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) should be used to save
important player data that needs to be accessed across player sessions.

#### Teleport settings and security

As teleport settings are stored locally, it is possible they can be
manipulated by malicious users. This risk can be mitigated by employing
server side validation.

#### Studio Limitation

Note that this service does not work during playtesting in Roblox Studio;
to test aspects of your experience using it, you must publish the
experience and play it in the Roblox application.

Provide feedback

---

PromptExperienceDetailsAsync

Yields

Prompts a [Player](/docs/reference/engine/classes/Player) with information about the specified experience.
The player can choose to teleport to the target experience through the
prompt.

TeleportService:PromptExperienceDetailsAsync(

player:[Player](/docs/reference/engine/classes/Player), universeId:[number](/docs/luau/numbers)

):PromptExperienceDetailsResult

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) to be presented the prompt. |
| universeId:[number](/docs/luau/numbers)  [DataModel.UniverseId](/docs/reference/engine/classes/DataModel#UniverseId) of the experience to be presented to the [Player](/docs/reference/engine/classes/Player) |

Returns

PromptExperienceDetailsResult

Enum.PromptExperienceDetailsResult

Prompts the specified [Player](/docs/reference/engine/classes/Player) with information of the specified
experience. The prompt includes the experience name, creator name,
maturity rating, etc. The prompt also includes a Join button which the
player can use to be teleported to the target experience. If the player is
ineligible to join the target experience, the button will be disabled.

Any teleport failures after the player clicks the Join button will
also fire [TeleportService.TeleportInitFailed](/docs/reference/engine/classes/TeleportService#TeleportInitFailed) providing a reason
for the failure.

#### Limitations

* For security purposes, teleporting a user from your experience to
  another experience owned by others fails by default. See
  [here](/docs/projects/teleport#enable-cross-experience-teleportation)
  for steps to enable cross-experience teleportation.
* This function currently can only be called from the client with
  [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) as the player parameter.
* The join button will always be disabled during Studio playtesting; to
  test aspects of your experience using it, you must publish the
  experience and play it in the Roblox application.

Code Samples

Show Experience Details to Player

The code sample below, when placed inside a Script with Client RunContext, will display a system dialog to the player showing details about a specified experience.
Player can choose to teleport to the experience or close the dialog.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local success, result = pcall(function()



TeleportService:PromptExperienceDetailsAsync(player, 8357232245)



end)



if not success then



warn("Error prompting experience details: " .. tostring(result))



end



if result == Enum.PromptExperienceDetailsResult.PromptClosed then



print("Player closed the experience details prompt")



elseif result == Enum.PromptExperienceDetailsResult.TeleportAttempted then



print("Player chose to teleport to the experience")



end
```

Provide feedback

---

ReserveServerAsync

Yields

Returns an access code that can be used to teleport players to a reserved
server, along with the [DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) for it.

TeleportService:ReserveServerAsync(placeId:[number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the place the reserved server is being created for. |

Returns

[Tuple](/docs/luau/tuples)

The server access code required by
[TeleportService:TeleportToPrivateServer()](/docs/reference/engine/classes/TeleportService#TeleportToPrivateServer) and the
[DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) for the reserved server.

This function returns an access code that can be used to teleport players
to a reserved server, along with the server's
[DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId). It can only be called on the server.

#### Reserved Servers

You can access reserved servers using:

* [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync) with the
  [TeleportOptions.ReservedServerAccessCode](/docs/reference/engine/classes/TeleportOptions#ReservedServerAccessCode) parameter.
* [TeleportService:TeleportToPrivateServer()](/docs/reference/engine/classes/TeleportService#TeleportToPrivateServer), with the access code
  ReserveServer returns.
  + A server is started when the access code is first used.
  + Access codes remain valid indefinitely, meaning reserved servers can
    still be joined if no game server is running (in this case a new
    server will be started).

You can see if the current server is a reserved server by using the
following code:

```
local isReserved = game.PrivateServerId ~= "" and game.PrivateServerOwnerId == 0
```

The [DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) is constant across all server
instances associated with the server access code, the
[DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) is not.

#### Studio Limitation

Note that this service does not work during playtesting in Roblox Studio;
to test aspects of your experience using it, you must publish the
experience and play it in the Roblox application.

#### Cross-Platform Play

Players on Xbox and PlayStation with cross‑play disabled will arrive in a
different server than players with cross‑play enabled. This can cause
multiple game servers with the same
[PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) to exist. You can use
[DataModel.MatchmakingType](/docs/reference/engine/classes/DataModel#MatchmakingType) to differentiate these game servers.

Code Samples

TeleportService: Teleport to a Reserved Server

The following code would send everyone in the current game to a reserved
server. Since reserved servers can only be joined by using
[TeleportService:TeleportToPrivateServer()](/docs/reference/engine/classes/TeleportService#TeleportToPrivateServer), nobody will join the
reserved server afterwards.

Mind that, since everyone will be teleported, the current server will
(probably) shutdown as nobody would be left in it.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



local code = TeleportService:ReserveServer(game.PlaceId)



local players = Players:GetPlayers()



TeleportService:TeleportToPrivateServer(game.PlaceId, code, players)



-- You could add extra arguments to this function: spawnName, teleportData and customLoadingScreen
```

TeleportService: Teleport to a Reserved Server via Chat

The following code would reserve one server, if it hasn't be reserved before.
Whenever someone says "reserved", they will be teleported to the private
server.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



local DataStoreService = game:GetService("DataStoreService")



local dataStore = DataStoreService:GetGlobalDataStore()



-- Get the saved code



local code = dataStore:GetAsync("ReservedServer")



if typeof(code) ~= "string" then -- None saved, create one



code = TeleportService:ReserveServer(game.PlaceId)



dataStore:SetAsync("ReservedServer", code)



end



local function joined(player)



player.Chatted:Connect(function(message)



if message == "reserved" then



TeleportService:TeleportToPrivateServer(game.PlaceId, code, { player })



end



end)



end



Players.PlayerAdded:Connect(joined)
```

Provide feedback

---

ReserveServer

Deprecated

Show details

---

SetTeleportGui

Sets the custom [teleport GUI](/docs/reference/engine/classes/ScreenGui) that will be shown to the
local user during teleportation, prior to the teleport being invoked.

TeleportService:SetTeleportGui(gui:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| gui:[Instance](/docs/reference/engine/datatypes/Instance)  The loading [ScreenGui](/docs/reference/engine/classes/ScreenGui) that is to be displayed during teleportation. |

Returns

()

This function sets the custom [teleport GUI](/docs/reference/engine/classes/ScreenGui) that will be
shown to the local user during teleportation, prior to the teleport being
invoked.

Note, the [teleport GUI](/docs/reference/engine/classes/ScreenGui) will not be used if the
destination place is in a different game. It will also not persist across
multiple teleports and will need to be set prior to each one.

This function should only be used on the client. If the teleportation
function is called from the server (as is the case with
[TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync)) then this function should be
called on the client prior to this. One way of doing this is listening to
a [RemoteEvent](/docs/reference/engine/classes/RemoteEvent) that fires several seconds before teleportation.

#### Loading screen

During a teleport, while the destination place is loading, the
*customLoadingScreen* is parented to the [CoreGui](/docs/reference/engine/classes/CoreGui). Once the place
has loaded the [loading screen](/docs/reference/engine/classes/ScreenGui) is
[parented](/docs/reference/engine/classes/Instance#Parent) to *nil*.

This [ScreenGui](/docs/reference/engine/classes/ScreenGui) can be fetched at the destination place using
[TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui), allowing you to parent
it to the [PlayerGui](/docs/reference/engine/classes/PlayerGui) and perform your own transitions.

You are advised to also [parent](/docs/reference/engine/classes/Instance#Parent) the
[ScreenGui](/docs/reference/engine/classes/ScreenGui) to the [PlayerGui](/docs/reference/engine/classes/PlayerGui) in the start place while the
teleport is initiating.

#### Studio Limitation

Note that this service does not work during playtesting in Roblox Studio;
to test aspects of your experience using it, you must publish the
experience and play it in the Roblox application.

Code Samples

Teleporting the local player

This snippet demonstrates how TeleportService can be used to teleport the
[LocalPlayer()](/docs/reference/engine/classes/Players#LocalPlayer) from the client.

It also shows how [TeleportService:SetTeleportGui()](/docs/reference/engine/classes/TeleportService#SetTeleportGui) can be used to
define a custom loading GUI. Note, this ScreenGui will need to be retrieved
at the destination place using
[TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui) and be parented to the
PlayerGui.

```
local TeleportService = game:GetService("TeleportService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local Players = game:GetService("Players")



local playerGui = Players.LocalPlayer:WaitForChild("PlayerGui")



local PLACE_ID = 0 -- replace here



local loadingGui = ReplicatedStorage:FindFirstChild("LoadingGui")



-- parent the loading gui for this place



loadingGui.Parent = playerGui



-- set the loading gui for the destination place



TeleportService:SetTeleportGui(loadingGui)



TeleportService:Teleport(PLACE_ID)
```

Provide feedback

---

SetTeleportSetting

Stores a value under a given key that persists across all teleportations
in the same game.

TeleportService:SetTeleportSetting(

setting:[string](/docs/luau/strings), value:Variant

):()

Parameters

|  |
| --- |
| setting:[string](/docs/luau/strings)  The key to store the *value* under. This key can be used to retrieve the value using [TeleportService:GetTeleportSetting()](/docs/reference/engine/classes/TeleportService#GetTeleportSetting). |
| value:Variant  The value to store. |

Returns

()

This function stores a value under a given key that persists across all
teleportations in the same game.

This method is intended for use on the client only and should not be used
on the server.

The stored value can later be retrieved using
[TeleportService:GetTeleportSetting()](/docs/reference/engine/classes/TeleportService#GetTeleportSetting). This will work in the
current place and any subsequent places the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer)
teleports to, provided they are in the same game.

For example, in a game that allowed crouching you could save whether the
user is currently crouching prior to teleporting as a teleport setting:

```
local TeleportService = game:GetService("TeleportService")



local isCrouching = false



TeleportService:SetTeleportSetting("isCrouching", isCrouching)
```

The stored value can take one of the following forms:

* A table without mixed keys (all strings or all integers)
* A string
* A number
* A bool

If data is already stored under the given key, the previous value will be
overwritten by the new value.

#### Differences from GlobalDataStores

Although they share some similarities, there are some key differences
between teleport settings and datastores:

* [GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) stores the data on Roblox servers
  whereas SetTeleportSetting stores the data locally
* Data stored in a [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore) is preserved after the user
  leaves the game universe whereas teleport settings are not
* [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) can only be accessed on the
  server, whereas teleport settings can only be accessed on the client
* [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) have usage limits, whereas
  teleport settings do not

In general teleport settings should be used to preserve client side
information within a single play session across different places in a
game. [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) should be used to save
important player data that needs to be accessed across player sessions.

#### Teleport settings and security

As teleport settings are stored locally, it is possible they can be
manipulated by malicious users. This risk can be mitigated by employing
server side validation.

#### Studio Limitation

Note that this service does not work during playtesting in Roblox Studio;
to test aspects of your experience using it, you must publish the
experience and play it in the Roblox application.

Provide feedback

---

Teleport

Teleports a [Player](/docs/reference/engine/classes/Player) to the place associated with the given
placeId.

TeleportService:Teleport(

placeId:[number](/docs/luau/numbers), player:[Instance](/docs/reference/engine/datatypes/Instance), teleportData:Variant, customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance)

):()

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The ID of the place to teleport to. |
| player:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" The [Player](/docs/reference/engine/classes/Player) to teleport, if this function is being called from the client this defaults to the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer). |
| teleportData:Variant  Optional data to be passed to the destination place. Can be retrieved using [TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData). |
| customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" Optional custom loading screen to be placed in the [CoreGui](/docs/reference/engine/classes/CoreGui) at the destination place. Can be retrieved using [TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui). |

Returns

()

This method should not be used for new work; the numerous teleport
functions have been combined into a single method,
[TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync), which should be
used instead.

Code Samples

Teleporting the local player

This snippet demonstrates how TeleportService can be used to teleport the
[LocalPlayer()](/docs/reference/engine/classes/Players#LocalPlayer) from the client.

It also shows how [TeleportService:SetTeleportGui()](/docs/reference/engine/classes/TeleportService#SetTeleportGui) can be used to
define a custom loading GUI. Note, this ScreenGui will need to be retrieved
at the destination place using
[TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui) and be parented to the
PlayerGui.

```
local TeleportService = game:GetService("TeleportService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local Players = game:GetService("Players")



local playerGui = Players.LocalPlayer:WaitForChild("PlayerGui")



local PLACE_ID = 0 -- replace here



local loadingGui = ReplicatedStorage:FindFirstChild("LoadingGui")



-- parent the loading gui for this place



loadingGui.Parent = playerGui



-- set the loading gui for the destination place



TeleportService:SetTeleportGui(loadingGui)



TeleportService:Teleport(PLACE_ID)
```

Teleporting from the server

This snippet demonstrates how TeleportService can be used to teleport a
Player from the server.

```
local Players = game:GetService("Players")



local TeleportService = game:GetService("TeleportService")



local PLACE_ID = 0 -- replace here



local USER_ID = 1 -- replace with player's UserId



local player = Players:GetPlayerByUserId(USER_ID)



TeleportService:Teleport(PLACE_ID, player)
```

Provide feedback

---

TeleportAsync

Yields

The all-encompassing method to teleport a player or group of players from
one server to another.

TeleportService:TeleportAsync(

placeId:[number](/docs/luau/numbers), players:Instances, teleportOptions:[Instance](/docs/reference/engine/datatypes/Instance)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The place ID the player(s) should be teleported to. |
| players:Instances  An array of the player(s) to teleport. |
| teleportOptions:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" An optional [TeleportOptions](/docs/reference/engine/classes/TeleportOptions) object containing additional arguments to the [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync) call. If this is not passed, no result will be returned. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

If a [TeleportOptions](/docs/reference/engine/classes/TeleportOptions) parameter is passed, this will be a
[TeleportAsyncResult](/docs/reference/engine/classes/TeleportAsyncResult) object that provides information about the
final teleport destination.

This function serves as the all-encompassing method to teleport a player
or group of players from one server to another. It can be used to:

* Teleport players to a different place.
* Teleport players to a specific server.
* Teleport players to a reserved server.

#### Group Teleport Limitations

* Groups of players can only be teleported within a single experience.
* No more than 50 players can be teleported with a single
  [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync) call.

#### Potential Errors

This is a list of potential reasons a teleport may fail, ranging from
invalid teleports to network issues.

| Error | Description |
| --- | --- |
| Invalid placeId | The provided place ID is below 0. |
| Players empty | The provided list of players to teleport is empty. |
| List of players instances is incorrect | Any of the provided players is not a Player object. |
| TeleportOptions not of correct type | The provided teleportOption is not a TeleportOptions object. |
| TeleportAsync called from Client | The client called TeleportAsync, which can only be called from the server. |
| Incompatible Parameters | Conflicting teleport options were used and TeleportService doesn't know where to send the player.   Conflicting TeleportOption parameters:  \* ReservedServerAccessCode and ServerInstanceId  \* ShouldReserveServer and ServerInstanceId  \* ShouldReserveServer and ReservedServerAccessCode |

For more information on how to teleport players between servers and
receive user data from a teleport, see
[Teleporting Between Places](/docs/projects/teleport#sending-user-data-along-with-teleports).

Provide feedback

---

TeleportPartyAsync

Yields

Teleports a group of [Players](/docs/reference/engine/classes/Player) to the same server of the
place with the given [PlaceId](/docs/reference/engine/classes/DataModel#PlaceId), returning the
[JobId](/docs/reference/engine/classes/DataModel#JobId) of the server instance they were teleported
to.

TeleportService:TeleportPartyAsync(

placeId:[number](/docs/luau/numbers), players:Instances, teleportData:Variant, customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The ID of the place to teleport to. |
| players:Instances  An array containing the [Players](/docs/reference/engine/classes/Player) to teleport. |
| teleportData:Variant  Optional data to be passed to the destination place. Can be retrieved using [TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData). |
| customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" Optional custom loading screen to be placed in the [CoreGui](/docs/reference/engine/classes/CoreGui) at the destination place. Can be retrieved using [TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui). |

Returns

[string](/docs/luau/strings)

The [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of the server instance the
[Players](/docs/reference/engine/classes/Player) were teleported to.

This method should not be used for new work; the numerous teleport
functions have been combined into a single method,
[TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync), which should be
used instead.

Code Samples

Teleport all players in the server

This code sample is an example of how
[TeleportService:TeleportPartyAsync()](/docs/reference/engine/classes/TeleportService#TeleportPartyAsync) can be used to teleport a group
of Player|Players.

In this case, all Player|Players will be teleported to the specified
*placeId* as a party. The [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of the destination server is
then printed.

```
local Players = game:GetService("Players")



local TeleportService = game:GetService("TeleportService")



local PLACE_ID = 0 -- replace



local playerList = Players:GetPlayers()



local success, result = pcall(function()



return TeleportService:TeleportPartyAsync(PLACE_ID, playerList)



end)



if success then



local jobId = result



print("Players teleported to", jobId)



else



warn(result)



end
```

Provide feedback

---

TeleportToPlaceInstance

Teleports a [Player](/docs/reference/engine/classes/Player) to the server instance associated with the
given *placeId* and *instanceId*.

TeleportService:TeleportToPlaceInstance(

placeId:[number](/docs/luau/numbers), instanceId:[string](/docs/luau/strings), player:[Instance](/docs/reference/engine/datatypes/Instance), spawnName:[string](/docs/luau/strings), teleportData:Variant, customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance)

):()

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The ID of the place to teleport to. |
| instanceId:[string](/docs/luau/strings)  The [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of the server instance to teleport to. |
| player:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" The [Player](/docs/reference/engine/classes/Player) to teleport, if this function is being called from the client this defaults to the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer). |
| spawnName:[string](/docs/luau/strings)  Optional name of the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) to spawn at. |
| teleportData:Variant  Optional data to be passed to the destination place. Can be retrieved using [TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData). |
| customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" Optional custom loading screen to be placed in the [CoreGui](/docs/reference/engine/classes/CoreGui) at the destination place. Can be retrieved using [TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui). |

Returns

()

This method should not be used for new work; the numerous teleport
functions have been combined into a single method,
[TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync), which should be
used instead.

Code Samples

Following Another Player

The code sample below, when placed inside a Script within
ServerScriptService, will teleport a player who's following another player
to the associated place/server. Note that this will not work if the player
being followed is in a reserved server.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



-- Is this player following anyone?



local followId = player.FollowUserId



-- If so, find out where they are



if followId and followId ~= 0 then



local _currentInstance, placeId, jobId



local success, errorMessage, _currentInstance, placeId, jobId = pcall(function()



-- followId is the user ID of the player that you want to retrieve the place and job ID for



return TeleportService:GetPlayerPlaceInstanceAsync(followId)



end)



if success then



-- Teleport player



TeleportService:TeleportToPlaceInstance(placeId, jobId, player)



else



warn(errorMessage)



end



else



warn("Player " .. player.UserId .. " is not following another player!")



end



end)
```

Provide feedback

---

TeleportToPrivateServer

Teleport a group of [Players](/docs/reference/engine/classes/Player) to a reserved server created
using [TeleportService:ReserveServer()](/docs/reference/engine/classes/TeleportService#ReserveServer).

TeleportService:TeleportToPrivateServer(

placeId:[number](/docs/luau/numbers), reservedServerAccessCode:[string](/docs/luau/strings), players:Instances, spawnName:[string](/docs/luau/strings), teleportData:Variant, customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance)

):()

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The ID of the place to teleport to. |
| reservedServerAccessCode:[string](/docs/luau/strings)  The reserved server access code returned by [TeleportService:ReserveServer()](/docs/reference/engine/classes/TeleportService#ReserveServer). |
| players:Instances  An array of [Players](/docs/reference/engine/classes/Player) to teleport. |
| spawnName:[string](/docs/luau/strings)  Optional name of the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) to spawn at. |
| teleportData:Variant  Optional data to be passed to the destination place. Can be retrieved using [TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData). |
| customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" Optional custom loading screen to be placed in the [CoreGui](/docs/reference/engine/classes/CoreGui) at the destination place. Can be retrieved using [TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui). |

Returns

()

This method should not be used for new work; the numerous teleport
functions have been combined into a single method,
[TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync), which should be
used instead.

Code Samples

TeleportService: Teleport to a Reserved Server via Chat

The following code would reserve one server, if it hasn't be reserved before.
Whenever someone says "reserved", they will be teleported to the private
server.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



local DataStoreService = game:GetService("DataStoreService")



local dataStore = DataStoreService:GetGlobalDataStore()



-- Get the saved code



local code = dataStore:GetAsync("ReservedServer")



if typeof(code) ~= "string" then -- None saved, create one



code = TeleportService:ReserveServer(game.PlaceId)



dataStore:SetAsync("ReservedServer", code)



end



local function joined(player)



player.Chatted:Connect(function(message)



if message == "reserved" then



TeleportService:TeleportToPrivateServer(game.PlaceId, code, { player })



end



end)



end



Players.PlayerAdded:Connect(joined)
```

TeleportService: Teleport to a Reserved Server

The following code would send everyone in the current game to a reserved
server. Since reserved servers can only be joined by using
[TeleportService:TeleportToPrivateServer()](/docs/reference/engine/classes/TeleportService#TeleportToPrivateServer), nobody will join the
reserved server afterwards.

Mind that, since everyone will be teleported, the current server will
(probably) shutdown as nobody would be left in it.

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



local code = TeleportService:ReserveServer(game.PlaceId)



local players = Players:GetPlayers()



TeleportService:TeleportToPrivateServer(game.PlaceId, code, players)



-- You could add extra arguments to this function: spawnName, teleportData and customLoadingScreen
```

Provide feedback

---

TeleportToSpawnByName

A variant of [TeleportService:Teleport()](/docs/reference/engine/classes/TeleportService#Teleport) that causes the
[Player](/docs/reference/engine/classes/Player) to spawn at a [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) of the given name at
the destination place.

TeleportService:TeleportToSpawnByName(

placeId:[number](/docs/luau/numbers), spawnName:[string](/docs/luau/strings), player:[Instance](/docs/reference/engine/datatypes/Instance), teleportData:Variant, customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance)

):()

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The ID of the place to teleport to. |
| spawnName:[string](/docs/luau/strings)  The name of the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) to spawn at. |
| player:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" The [Player](/docs/reference/engine/classes/Player) to teleport, if this function is being called from the client this defaults to the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer). |
| teleportData:Variant  Optional data to be passed to the destination place. Can be retrieved using [TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData). |
| customLoadingScreen:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" Optional custom loading screen to be placed in the [CoreGui](/docs/reference/engine/classes/CoreGui) at the destination place. Can be retrieved using [TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui). |

Returns

()

This method should not be used for new work; the numerous teleport
functions have been combined into a single method,
[TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync), which should be
used instead.

Code Samples

TeleportService:TeleportToSpawnByName

This code will teleport a player to Crossroads, and if there is a spawn named
"TeleportSpawn" then the player would spawn on it. This assumes it's being
used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

```
local TeleportService = game:GetService("TeleportService")



TeleportService:TeleportToSpawnByName(1818, "TeleportSpawn")
```

Provide feedback

---

Events

LocalPlayerArrivedFromTeleport

Fires when the [LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) enters the place
following a teleport.

TeleportService.LocalPlayerArrivedFromTeleport(

loadingGui:[Instance](/docs/reference/engine/datatypes/Instance), dataTable:Variant

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| loadingGui:[Instance](/docs/reference/engine/datatypes/Instance)  The *customLoadingScreen* the [LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) arrived into the place with. |
| dataTable:Variant  The *teleportData* the [LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) arrived into the place with. |

This function fires when the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) enters the place
following a teleport. The teleportData and customLoadingScreen are
provided as arguments.

When fetching *teleportData* and the *customLoadingScreen* you are advised
to use [TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData) and
[TeleportService:GetArrivingTeleportGui()](/docs/reference/engine/classes/TeleportService#GetArrivingTeleportGui) instead. This is because
these functions can be called immediately without having to wait for this
event to fire.

This event should be connected immediately in a [LocalScript](/docs/reference/engine/classes/LocalScript)
parented to [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst). Otherwise, when the connection is
made the event may have already fired.

#### Loading Screen

During a teleport, while the destination place is loading, the
*customLoadingScreen* is parented to the [CoreGui](/docs/reference/engine/classes/CoreGui). Once the place
has loaded the [loading screen](/docs/reference/engine/classes/ScreenGui) is
[parented](/docs/reference/engine/classes/Instance#Parent) to *nil*.

If you wish to preserve the *customLoadingScreen* and perform your own
transitions, you will need to parent it to the local player's
[PlayerGui](/docs/reference/engine/classes/PlayerGui). For example, using the following code inside a
[LocalScript](/docs/reference/engine/classes/LocalScript) in [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst):

```
local TeleportService = game:GetService("TeleportService")



local Players = game:GetService("Players")



local ReplicatedFirst = game:GetService("ReplicatedFirst")



TeleportService.LocalPlayerArrivedFromTeleport:Connect(function(customLoadingScreen, teleportData)



local playerGui = Players.LocalPlayer:WaitForChild("PlayerGui")



ReplicatedFirst:RemoveDefaultLoadingScreen()



customLoadingScreen.Parent = playerGui



-- animate screen here



wait(5)



-- destroy screen



customLoadingScreen:Destroy()



end)
```

The *customLoadingScreen* will not be used if the destination place is in
a different game.

#### Studio Limitation

Note that this service does not work during playtesting in Roblox Studio;
to test aspects of your experience using it, you must publish the
experience and play it in the Roblox application.

Provide feedback

---

TeleportInitFailed

Fires when a teleport fails to start, leaving the player in their current
server.

TeleportService.TeleportInitFailed(

player:[Instance](/docs/reference/engine/datatypes/Instance), teleportResult:[Enum.TeleportResult](/docs/reference/engine/enums/TeleportResult), errorMessage:[string](/docs/luau/strings), placeId:[number](/docs/luau/numbers), teleportOptions:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) instance that failed to teleport. |
| teleportResult:[Enum.TeleportResult](/docs/reference/engine/enums/TeleportResult)  The reason for the teleport failure. |
| errorMessage:[string](/docs/luau/strings)  The message provided to the player explaining the teleport failure. |
| placeId:[number](/docs/luau/numbers)  The original target place ID of the teleport. |
| teleportOptions:[Instance](/docs/reference/engine/datatypes/Instance)  A [TeleportOptions](/docs/reference/engine/classes/TeleportOptions) object that can be passed back to [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync) to retry the failed teleport. |

This event fires on both the client and the server when a request to
teleport from a function such as [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync)
fails and the player does not leave the current server. It provides a
reason for the failure, as well as all of the information necessary to
retry the teleport. If a group teleport fails, the event will fire once
per player.

#### TeleportOptions

The [TeleportOptions](/docs/reference/engine/classes/TeleportOptions) object provided by this event is not identical
to the one passed to the original [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync)
call. It is a new object populated with the necessary parameters to retry
the teleport and send the player to the exact same destination. This is
especially important for facilitating group teleports when they fail.

| Original Teleport Type | Teleport Data | ReservedServerAccessCode | ServerInstanceId | ShouldReserveServer |
| --- | --- | --- | --- | --- |
| Individual player to place | Original value | None | None | false |
| Player(s) to reserved server | Original value | Original value, or the code generated if ShouldReserveServer was originally true | None | false |
| Player(s) to specific server | Original value | None | Original value | false |
| Players to place | Original value | None | Same destination ID as the other players in the original teleport | false |

For more information on how to teleport players between servers, see
[Teleporting Between Places](/docs/projects/teleport).

Provide feedback

---