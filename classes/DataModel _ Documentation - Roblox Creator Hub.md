# DataModel | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataModel
Scraped: 2026-01-11T02:29:23.524800Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- ServiceProvider
- DataModel
- Workspace
- Lighting
- Instance
- Object
- DataModel.CreatorType
- Player.UserId
- DataModel.CreatorId
- UserId
- DataModel.PlaceId
- DataModel.JobId
- TeleportService
- Players
- TeleportService:GetPlayerPlaceInstanceAsync()
- TeleportService:TeleportToPlaceInstance()
- Player
- DataModel.PrivateServerId
- HttpService:GenerateGUID()
- MatchmakingTypes
- Script
- DataModel.GameId
- ScreenGui
- reserved server
- TeleportService:ReserveServer()
- JobId
- DataModel.PrivateServerOwnerId
- reserved servers
- BindToClose()
- RunService:IsStudio()
- DataStoreService
- DataStores
- PluginGui:BindToClose()
- PluginGui
- DataModel:BindToClose()
- UserIds
- TaskScheduler
- Instances
- ReplicatedFirst
- LocalScripts
- LocalScript
- DataModel.Loaded
- Instance:WaitForChild()
- DataModel:SetUniverseId()
- DataModel:SetPlaceId()
- UserGameSettings
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ServiceProvider](/docs/reference/engine/classes/ServiceProvider)
6. /
7. [DataModel](/docs/reference/engine/classes/DataModel)

English

Feedback

Engine Class

DataModel

The root of Roblox's parent-child hierarchy. Its direct children are services,
such as [Workspace](/docs/reference/engine/classes/Workspace) and [Lighting](/docs/reference/engine/classes/Lighting), that act as the fundamental
components of a Roblox game.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [CreatorId](#CreatorId):[number](/docs/luau/numbers) |
| [CreatorType](#CreatorType):[Enum.CreatorType](/docs/reference/engine/enums/CreatorType) |
| [Environment](#Environment):[string](/docs/luau/strings) |
| [GameId](#GameId):[number](/docs/luau/numbers) |
| [GearGenreSetting](#GearGenreSetting):[Enum.GearGenreSetting](/docs/reference/engine/enums/GearGenreSetting)  Deprecated |
| [Genre](#Genre):[Enum.Genre](/docs/reference/engine/enums/Genre)  Deprecated |
| [JobId](#JobId):[string](/docs/luau/strings) |
| [lighting](#lighting):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [MatchmakingType](#MatchmakingType):[Enum.MatchmakingType](/docs/reference/engine/enums/MatchmakingType) |
| [PlaceId](#PlaceId):[number](/docs/luau/numbers) |
| [PlaceVersion](#PlaceVersion):[number](/docs/luau/numbers) |
| [PrivateServerId](#PrivateServerId):[string](/docs/luau/strings) |
| [PrivateServerOwnerId](#PrivateServerOwnerId):[number](/docs/luau/numbers) |
| [VIPServerId](#VIPServerId):[string](/docs/luau/strings)  Deprecated |
| [VIPServerOwnerId](#VIPServerOwnerId):[number](/docs/luau/numbers)  Deprecated |
| [Workspace](#Workspace):[Workspace](/docs/reference/engine/classes/Workspace) |
| [workspace](#workspace):[Workspace](/docs/reference/engine/classes/Workspace)  Deprecated |

Methods

|  |
| --- |
| [BindToClose](#BindToClose)(function: [function](/docs/luau/functions)):() |
| [GetJobsInfo](#GetJobsInfo)():[Array](/docs/luau/tables#arrays) |
| [GetMessage](#GetMessage)():[string](/docs/luau/strings)  Deprecated |
| [GetObjects](#GetObjects)(url: ContentId):Instances  Deprecated |
| [GetRemoteBuildMode](#GetRemoteBuildMode)():[boolean](/docs/luau/booleans)  Deprecated |
| [IsGearTypeAllowed](#IsGearTypeAllowed)(gearType: [Enum.GearType](/docs/reference/engine/enums/GearType)):[boolean](/docs/luau/booleans)  Deprecated |
| [IsLoaded](#IsLoaded)():[boolean](/docs/luau/booleans) |
| [SavePlace](#SavePlace)(saveFilter: [Enum.SaveFilter](/docs/reference/engine/enums/SaveFilter)):[boolean](/docs/luau/booleans)  Deprecated |
| [SetPlaceId](#SetPlaceId)(placeId: [number](/docs/luau/numbers)):() |
| [SetUniverseId](#SetUniverseId)(universeId: [number](/docs/luau/numbers)):() |

Events

|  |
| --- |
| [AllowedGearTypeChanged](#AllowedGearTypeChanged)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [GraphicsQualityChangeRequest](#GraphicsQualityChangeRequest)(betterQuality: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ItemChanged](#ItemChanged)(object: [Instance](/docs/reference/engine/datatypes/Instance),descriptor: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [Loaded](#Loaded)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Callbacks

|  |
| --- |
| [OnClose](#OnClose)():[Tuple](/docs/luau/tuples)  Deprecated |

Inherited Members

7 inherited from [ServiceProvider](/docs/reference/engine/classes/ServiceProvider)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [Data Model](/docs/projects/data-model) (commonly known as game
after the global variable used to access it) is the root of Roblox's
parent-child hierarchy. Its direct children are services, such as
[Workspace](/docs/reference/engine/classes/Workspace) and [Lighting](/docs/reference/engine/classes/Lighting), that act as the fundamental components
of a Roblox game.

Code Samples

GetService()

Demonstrates using game, the root instance of [DataModel](/docs/reference/engine/classes/DataModel), to get services such as [Workspace](/docs/reference/engine/classes/Workspace) and [Lighting](/docs/reference/engine/classes/Lighting).

```
local Workspace = game:GetService("Workspace")



local Lighting = game:GetService("Lighting")



-- Examples of modifying properties of these services



Workspace.Gravity = 20



Lighting.ClockTime = 4
```

---

API Reference

Properties

CreatorId

Read Only

Not Replicated

Read Parallel

Describes the ID of the user or group that owns the place.

DataModel.CreatorId:[number](/docs/luau/numbers)

This property describes the ID of the user or group that owns the place.
If the [DataModel.CreatorType](/docs/reference/engine/classes/DataModel#CreatorType) property is User then CreatorId
will be the [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the place's owner. If the
[DataModel.CreatorType](/docs/reference/engine/classes/DataModel#CreatorType) is Group then CreatorId will be the ID
of the group that owns the place.

Code Samples

Detect when the place owner joins the game

This code sample will print an output when the user that owns the game, or a
member of the group that owns the game joins the server.

To run this script, place it inside a Script in ServerScriptService

```
local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



if game.CreatorType == Enum.CreatorType.User then



if player.UserId == game.CreatorId then



print("The place owner has joined the game!")



end



elseif game.CreatorType == Enum.CreatorType.Group then



if player:IsInGroup(game.CreatorId) then



print("A member of the group that owns the place has joined the game!")



end



end



end)
```

Provide feedback

---

CreatorType

Read Only

Not Replicated

Read Parallel

Describes the [Enum.CreatorType](/docs/reference/engine/enums/CreatorType) of the place, whether the place is owned
by a user or a group.

DataModel.CreatorType:[Enum.CreatorType](/docs/reference/engine/enums/CreatorType)

This property describes the [Enum.CreatorType](/docs/reference/engine/enums/CreatorType) of the place, whether the
place is owned by a user or a group. If User, then the
[DataModel.CreatorId](/docs/reference/engine/classes/DataModel#CreatorId) property will describe the
[UserId](/docs/reference/engine/classes/Player#UserId) of the account that owns the game. If
Group, then it will describe the group ID.

Code Samples

Detect when the place owner joins the game

This code sample will print an output when the user that owns the game, or a
member of the group that owns the game joins the server.

To run this script, place it inside a Script in ServerScriptService

```
local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



if game.CreatorType == Enum.CreatorType.User then



if player.UserId == game.CreatorId then



print("The place owner has joined the game!")



end



elseif game.CreatorType == Enum.CreatorType.Group then



if player:IsInGroup(game.CreatorId) then



print("A member of the group that owns the place has joined the game!")



end



end



end)
```

Provide feedback

---

Environment

Read Only

Not Replicated

Roblox Script Security

Read Parallel

DataModel.Environment:[string](/docs/luau/strings)

Provide feedback

---

GameId

Read Only

Not Replicated

Read Parallel

Describes the ID of the experience that the place running on the server
belongs to.

DataModel.GameId:[number](/docs/luau/numbers)

This property describes the ID of the experience that the place running on
the server belongs to.

#### See Also

* [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId), which describes the ID of the place running
  on the server
* [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId), which is a unique identifier for the server
  game instance running
* [TeleportService](/docs/reference/engine/classes/TeleportService), which is a service that can be used to
  transport [Players](/docs/reference/engine/classes/Player) between games

Provide feedback

---

GearGenreSetting

Deprecated

Show details

---

Genre

Deprecated

Show details

---

JobId

Read Only

Not Replicated

Read Parallel

A unique identifier for the running game server instance.

DataModel.JobId:[string](/docs/luau/strings)

This property is a unique identifier for the running game server instance.
It is a universally unique identifier (UUID), meaning that no two servers,
past or present, will ever have the same ID.

Defaults to an empty string in Studio.

#### See Also

* [TeleportService:GetPlayerPlaceInstanceAsync()](/docs/reference/engine/classes/TeleportService#GetPlayerPlaceInstanceAsync) which can be used
  to retrieve the [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of a user's current server.
* [TeleportService:TeleportToPlaceInstance()](/docs/reference/engine/classes/TeleportService#TeleportToPlaceInstance) which can be used to
  teleport a [Player](/docs/reference/engine/classes/Player) to a specific server.
* [DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) describes the ID of the private server
  the game server instance belongs to.
* [HttpService:GenerateGUID()](/docs/reference/engine/classes/HttpService#GenerateGUID), a function that can be used to
  generate your own UUIDs.

Provide feedback

---

lighting

Deprecated

Show details

---

MatchmakingType

Read Only

Not Replicated

Read Parallel

Represents how players in the server are handled by matchmaking.

DataModel.MatchmakingType:[Enum.MatchmakingType](/docs/reference/engine/enums/MatchmakingType)

This property represents how players in the server are handled by
matchmaking. Players with different
[MatchmakingTypes](/docs/reference/engine/classes/DataModel#MatchmakingType) cannot be in or
teleport to the same server.

Note that this property is only valid on the server [DataModel](/docs/reference/engine/classes/DataModel) and
it will be the [Enum.MatchmakingType.Default](/docs/reference/engine/enums/MatchmakingType#Default) value for all clients, so
only reference this property inside of a server‑side [Script](/docs/reference/engine/classes/Script).

Provide feedback

---

PlaceId

Read Only

Not Replicated

Read Parallel

Describes the ID of the place running on the server.

DataModel.PlaceId:[number](/docs/luau/numbers)

This property describes the ID of the place running on the server.

If the place has not been published to Roblox, this ID will correspond
with the template being used.

#### See Also

* [DataModel.GameId](/docs/reference/engine/classes/DataModel#GameId), which describes the ID of the experience that
  the current place belongs to
* [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId), which is a unique identifier for the server
  game instance running
* [TeleportService](/docs/reference/engine/classes/TeleportService), which is a service that can be used to
  transport [Players](/docs/reference/engine/classes/Player) between places

Provide feedback

---

PlaceVersion

Read Only

Not Replicated

Read Parallel

Describes the version of the place the server is running on.

DataModel.PlaceVersion:[number](/docs/luau/numbers)

This property describes the version of the place the server is running on.

This version number corresponds with the version number shown under the
Version History section of the place's settings. It is not the current
version of the Roblox client. This property is 0 for all unpublished
experiences.

When a server instance is created for a place, it uses the place's current
version. If the place is later updated while this server is running, the
server will remain at its current version.

This property can be used to display a [ScreenGui](/docs/reference/engine/classes/ScreenGui) showing the
current version of the game to [Players](/docs/reference/engine/classes/Player) to assist with
debugging.

Code Samples

Server version number GUI

This code sample will place a simple GUI in the StarterGui showing the place
version the server is running at.

To use this sample, place it inside a Script in ServerScriptService.

```
local StarterGui = game:GetService("StarterGui")



local versionGui = Instance.new("ScreenGui")



local textLabel = Instance.new("TextLabel")



textLabel.Position = UDim2.new(1, -10, 1, 0)



textLabel.AnchorPoint = Vector2.new(1, 1)



textLabel.Size = UDim2.new(0, 150, 0, 40)



textLabel.BackgroundTransparency = 1



textLabel.TextColor3 = Color3.new(1, 1, 1)



textLabel.TextStrokeTransparency = 0



textLabel.TextXAlignment = Enum.TextXAlignment.Right



textLabel.TextScaled = true



local placeVersion = game.PlaceVersion



textLabel.Text = string.format("Server version: %s", placeVersion)



textLabel.Parent = versionGui



versionGui.Parent = StarterGui
```

Provide feedback

---

PrivateServerId

Read Only

Not Replicated

Read Parallel

Describes the private server ID of the server, if the server is a private
server or a [reserved server](/docs/reference/engine/classes/TeleportService#ReserveServer).

DataModel.PrivateServerId:[string](/docs/luau/strings)

This property describes the private server ID of the server, if the server
is a private server.

If the server is not a private server, then this property will be an empty
string.

#### Private servers

Private servers refer to the following:

* [Private servers](/docs/production/monetization/private-servers)
  that users can purchase from the games page
* Reserved servers, private servers created by the developer using
  [TeleportService:ReserveServer()](/docs/reference/engine/classes/TeleportService#ReserveServer)

#### PrivateServerId vs JobId

The PrivateServerId of a server is different from the
[DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId). The [JobId](/docs/reference/engine/classes/DataModel#JobId) is the unique
identifier of the current server instance.

Private servers (private or reserved servers) can have multiple server
instances associated with them over time. This is because, although only
one server instance can be running at once for a private server, new
server instances can open and close as players join and leave the game.
For example, no server instance is running when nobody is playing in the
server. The PrivateServerId will be consistent across all of these server
instances, and the [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) will be unique for each one.

See also:

* [DataModel.PrivateServerOwnerId](/docs/reference/engine/classes/DataModel#PrivateServerOwnerId), a property describing the owner
  of a private server
* [TeleportService:ReserveServer()](/docs/reference/engine/classes/TeleportService#ReserveServer), a function which creates a
  reserved server

Code Samples

Detecting Private Servers

[DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) and [DataModel.PrivateServerOwnerId](/docs/reference/engine/classes/DataModel#PrivateServerOwnerId)
can be used to detect if the current server instance is a standard server, a
VIP server or a reserved server.

```
local function getServerType()



if game.PrivateServerId ~= "" then



if game.PrivateServerOwnerId ~= 0 then



return "VIPServer"



else



return "ReservedServer"



end



else



return "StandardServer"



end



end



print(getServerType())
```

Provide feedback

---

PrivateServerOwnerId

Read Only

Not Replicated

Read Parallel

Describes the [UserId](/docs/reference/engine/classes/Player#UserId) of the [Player](/docs/reference/engine/classes/Player) that owns
the private server if the server is private.

DataModel.PrivateServerOwnerId:[number](/docs/luau/numbers)

This property describes the [UserId](/docs/reference/engine/classes/Player#UserId) of the
[Player](/docs/reference/engine/classes/Player) that owns the
[private server](/docs/production/monetization/private-servers) if
the server is private.

If the server is a standard or reserved server then this property will be
set to 0.

This property could be used to identify if a [Player](/docs/reference/engine/classes/Player) is the owner
of the private server, for example:

```
local Players = game:GetService("Players")



-- is this a private server?



if game.PrivateServerId ~= "" and game.PrivateServerOwnerId ~= 0 then



-- listen for new players being added



Players.PlayerAdded:Connect(function(player)



-- check if the player is the server owner



if player.UserId == game.PrivateServerOwnerId then



print("The private server owner has joined the game")



end



end)



end
```

See also:

* [DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId), a property describing the unique ID
  of private and [reserved servers](/docs/reference/engine/classes/TeleportService#ReserveServer)

Code Samples

Detecting Private Servers

[DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) and [DataModel.PrivateServerOwnerId](/docs/reference/engine/classes/DataModel#PrivateServerOwnerId)
can be used to detect if the current server instance is a standard server, a
VIP server or a reserved server.

```
local function getServerType()



if game.PrivateServerId ~= "" then



if game.PrivateServerOwnerId ~= 0 then



return "VIPServer"



else



return "ReservedServer"



end



else



return "StandardServer"



end



end



print(getServerType())
```

Provide feedback

---

VIPServerId

Deprecated

Show details

---

VIPServerOwnerId

Deprecated

Show details

---

Workspace

Read Only

Not Replicated

Read Parallel

A reference to the [Workspace](/docs/reference/engine/classes/Workspace) service.

DataModel.Workspace:[Workspace](/docs/reference/engine/classes/Workspace)

This property is a reference to the [Workspace](/docs/reference/engine/classes/Workspace) service. It always
points to [Workspace](/docs/reference/engine/classes/Workspace) and will never be nil.

Provide feedback

---

workspace

Deprecated

Show details

---

Methods

BindToClose

Binds a function to be called before the server shuts down.

DataModel:BindToClose(function:[function](/docs/luau/functions)):()

Parameters

|  |
| --- |
| function:[function](/docs/luau/functions)  A function called before the experience server shuts down. If the bound function accepts a parameter, it passes [Enum.CloseReason](/docs/reference/engine/enums/CloseReason) specifying the reason for the server shutdown. |

Returns

()

Binds a function to be called before the server shuts down. If the bound
function accepts a parameter, it passes [Enum.CloseReason](/docs/reference/engine/enums/CloseReason) specifying the
reason for the server shutdown.

You can bind multiple functions by calling
[BindToClose()](/docs/reference/engine/classes/DataModel#BindToClose) repeatedly. Bound functions
are called in parallel and run at the same time.

The experience server waits 30 seconds for all bound functions to stop
running before it shuts down. After 30 seconds, the server shuts down even
if functions are still running.

To verify that the current session is not in Roblox Studio, use
[RunService:IsStudio()](/docs/reference/engine/classes/RunService#IsStudio). This prevents bound functions from
completing their run in offline testing sessions.

When you use [DataStoreService](/docs/reference/engine/classes/DataStoreService), you should also use BindToClose
to bind a function saving all unsaved data to
[DataStores](/docs/reference/engine/classes/GlobalDataStore). This prevents data loss if the server
shuts down unexpectedly.

See also:

* [Enum.CloseReason](/docs/reference/engine/enums/CloseReason) for reasons for the experience server shutdown.
* [PluginGui:BindToClose()](/docs/reference/engine/classes/PluginGui#BindToClose), which binds a function to a
  [PluginGui](/docs/reference/engine/classes/PluginGui) close button.

Code Samples

Saving player data before shutting down

The following code sample is an example of how [DataModel:BindToClose()](/docs/reference/engine/classes/DataModel#BindToClose)
can be used to save player data in the event of a server shutdown. In this
example, player data is stored in a dictionary named *playerData* with
[UserIds](/docs/reference/engine/classes/Player#UserId) as keys.

```
local DataStoreService = game:GetService("DataStoreService")



local RunService = game:GetService("RunService")



local playerDataStore = DataStoreService:GetDataStore("PlayerData")



local allPlayerSessionDataCache = {}



local function savePlayerDataAsync(userId, data)



return playerDataStore:UpdateAsync(userId, function(oldData)



return data



end)



end



local function onServerShutdown(closeReason)



if RunService:IsStudio() then



-- Avoid writing studio data to production and stalling test session closing



return



end



-- Reference for yielding and resuming later



local mainThread = coroutine.running()



-- Counts up for each new thread, down when the thread finishes. When 0 is reached,



-- the individual thread knows it's the last thread to finish and should resume the main thread



local numThreadsRunning = 0



-- Calling this function later starts on a new thread because of coroutine.wrap



local startSaveThread = coroutine.wrap(function(userId, sessionData)



-- Perform the save operation



local success, result = pcall(savePlayerDataAsync, userId, sessionData)



if not success then



-- Could implement a retry



warn(string.format("Failed to save %d's data: %s", userId, result))



end



-- Thread finished, decrement counter



numThreadsRunning -= 1



if numThreadsRunning == 0 then



-- This was the last thread to finish, resume main thread



coroutine.resume(mainThread)



end



end)



-- This assumes playerData gets cleared from the data table during a final save on PlayerRemoving,



-- so this is iterating over all the data of players still in the game that hasn't been saved



for userId, sessionData in pairs(allPlayerSessionDataCache) do



numThreadsRunning += 1



-- This loop finishes running and counting numThreadsRunning before any of



-- the save threads start because coroutine.wrap has built-in deferral on start



startSaveThread(userId, sessionData)



end



if numThreadsRunning > 0 then



-- Stall shutdown until save threads finish. Resumed by the last save thread when it finishes



coroutine.yield()



end



end



game:BindToClose(onServerShutdown)
```

Binding to and Handling Game Shutdown

The following example prints the close reason to the output.
It prints Done after three seconds, and then allows
Roblox to shut down the experience server.

The close reason matches one of the values in [Enum.CloseReason](/docs/reference/engine/enums/CloseReason).

```
game:BindToClose(function(closeReason)



print(`Closing with reason {closeReason}`)



task.wait(3)



print("Done")



end)
```

Provide feedback

---

GetJobsInfo

Plugin Security

Returns a table containing basic information about the jobs performed by
the task scheduler.

DataModel:GetJobsInfo():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

A table containing information about the jobs performed by the task
scheduler, see above for the format.

Returns a table containing basic information about the jobs performed by
the task scheduler.

In computing, a task scheduler is a system responsible for executing key
tasks at the appropriate intervals.

You can also find live task scheduler statistics in the Task Scheduler
window in Roblox Studio.

The first entry in the table returned is a reference dictionary containing
the statistics (or headings) available. It is in the following format:

```
{



["name"] = "name",



["averageDutyCycle"] = "averageDutyCycle",



["averageStepsPerSecond"] = "averageStepsPerSecond",



["averageStepTime"] = "averageStepTime",



["averageError"] = "averageError",



["isRunning"] = "isRunning",



}
```

The subsequent entries in the table returned are dictionaries containing
the above statistics for jobs performed by the task scheduler. For
example:

```
{



["name"] = "Heartbeat",



["averageDutyCycle"] = 0,



["averageStepsPerSecond"] = 0,



["averageStepTime"] = 0,



["averageError"] = 0,



["isRunning"] = false,



}
```

See also:

* [TaskScheduler](/docs/reference/engine/classes/TaskScheduler)

Code Samples

Getting Jobs Info

Here is an example of iterating over the job info.

```
local jobInfo = game:GetJobsInfo()



local jobTitles = jobInfo[1]



table.remove(jobInfo, 1)



local divider = string.rep("-", 120)



print(divider)



warn("JOB INFO:")



print(divider)



for _, job in pairs(jobInfo) do



for jobIndex, jobValue in pairs(job) do



local jobTitle = jobTitles[jobIndex]



warn(jobTitle, "=", jobValue)



end



print(divider)



end
```

Provide feedback

---

GetMessage

Deprecated

Show details

---

GetObjects

Deprecated

Show details

---

GetRemoteBuildMode

Deprecated

Show details

---

IsGearTypeAllowed

Deprecated

Show details

---

IsLoaded

Returns true if the client has finished loading the game for the first
time.

DataModel:IsLoaded():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the client has finished loading the game for the first time.

When all initial [Instances](/docs/reference/engine/classes/Instance) in the game have finished
replicating to the client, this function returns true.

Unless they are parented to [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst),
[LocalScripts](/docs/reference/engine/classes/LocalScript) do not run until the game has loaded. The
following snippet, run from a [LocalScript](/docs/reference/engine/classes/LocalScript) in
[ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst) yields until the game has loaded:

```
if not game:IsLoaded() then



game.Loaded:Wait()



end
```

See also:

* [Replication order](/docs/scripting/attributes#replication-order)
  for a more detailed summary of the loading process.
* [DataModel.Loaded](/docs/reference/engine/classes/DataModel#Loaded), an event that fires when the game has loaded
* [Instance:WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild), a function which can be used to wait
  for an individual [Instance](/docs/reference/engine/classes/Instance) to replicate without having to wait
  for the whole game to finish loading.

Code Samples

Custom Loading Screen

This sample demonstrates a custom loading screen with a basic TextLabel. The
code should be placed in a LocalScript within ReplicatedFirst. To expand
on this sample with loading screen animations, see the
[Custom Loading Screens](/docs/ui/customizing-loading-screens)
article.

```
local Players = game:GetService("Players")



local ReplicatedFirst = game:GetService("ReplicatedFirst")



local player = Players.LocalPlayer



local playerGui = player:WaitForChild("PlayerGui")



-- Create a basic loading screen



local screenGui = Instance.new("ScreenGui")



screenGui.IgnoreGuiInset = true



local textLabel = Instance.new("TextLabel")



textLabel.Size = UDim2.new(1, 0, 1, 0)



textLabel.BackgroundColor3 = Color3.fromRGB(0, 20, 40)



textLabel.Font = Enum.Font.GothamMedium



textLabel.TextColor3 = Color3.new(0.8, 0.8, 0.8)



textLabel.Text = "Loading"



textLabel.TextSize = 28



textLabel.Parent = screenGui



-- Parent entire screen GUI to player GUI



screenGui.Parent = playerGui



-- Remove the default loading screen



ReplicatedFirst:RemoveDefaultLoadingScreen()



--task.wait(3)  -- Optionally force screen to appear for a minimum number of seconds



if not game:IsLoaded() then



game.Loaded:Wait()



end



screenGui:Destroy()
```

Provide feedback

---

SavePlace

Deprecated

Show details

---

SetPlaceId

Plugin Security

Sets the [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the current game instance.

DataModel:SetPlaceId(placeId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| placeId:[number](/docs/luau/numbers)  The ID to set the [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) to. |

Returns

()

This function sets the [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the game instance to
the given placeId.

Provide feedback

---

SetUniverseId

Plugin Security

Sets the [DataModel.GameId](/docs/reference/engine/classes/DataModel#GameId) of the current game instance to the
given universeId.

DataModel:SetUniverseId(universeId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| universeId:[number](/docs/luau/numbers)  The ID to set the [DataModel.GameId](/docs/reference/engine/classes/DataModel#GameId) to. |

Returns

()

This function sets the [DataModel.GameId](/docs/reference/engine/classes/DataModel#GameId) of the current game
instance to the given universeId. This is useful when testing local
.rbxl files that have not been published to Roblox.

To access the [DataStoreService](/docs/reference/engine/classes/DataStoreService) in an unpublished place, both
[DataModel:SetUniverseId()](/docs/reference/engine/classes/DataModel#SetUniverseId) and [DataModel:SetPlaceId()](/docs/reference/engine/classes/DataModel#SetPlaceId) must
be set.

Provide feedback

---

Events

AllowedGearTypeChanged

Deprecated

Show details

---

GraphicsQualityChangeRequest

Fires when the user prompts and increase or decrease in graphics quality
using the hotkeys.

DataModel.GraphicsQualityChangeRequest(betterQuality:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| betterQuality:[boolean](/docs/luau/booleans)  Whether the user has prompted an increase (*true*) or a decrease (*false*) in graphics quality. |

Fires when the user prompts an increase or decrease in graphics quality
using the hotkeys.

This event fires under the following conditions:

* If the user presses F10, this event fires with a
  betterQuality argument of true.
* If the user presses ShiftF10, this event fires
  with a betterQuality argument of false.

This event does not provide the current graphics quality level or cover
all updates to the graphics quality. For example, changes made in the core
GUI escape menu are not registered.

You can retrieve a user's [Enum.SavedQualitySetting](/docs/reference/engine/enums/SavedQualitySetting) using
[UserGameSettings](/docs/reference/engine/classes/UserGameSettings) with the following snippet:

```
UserSettings():GetService("UserGameSettings").SavedQualityLevel
```

If the user's graphics settings are set to automatic then the
[Enum.SavedQualitySetting](/docs/reference/engine/enums/SavedQualitySetting) will be
[Automatic](/docs/reference/engine/enums/SavedQualitySetting#Automatic). There is currently no way
for developers to reliably get the current graphics quality level of a
user's machine.

Code Samples

Handling User Changes in Graphics Quality

```
game.GraphicsQualityChangeRequest:Connect(function(betterQuality)



if betterQuality then



print("The user has requested an increase in graphics quality!")



else



print("The user has requested a decrease in graphics quality!")



end



end)
```

Provide feedback

---

ItemChanged

Deprecated

Show details

---

Loaded

Fires on the client when the game finishes loading for the first time.

DataModel.Loaded():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires on the client when all initial [Instances](/docs/reference/engine/classes/Instance)
in the game have finished replicating to the client.

Unless they are parented to [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst),
[LocalScripts](/docs/reference/engine/classes/LocalScript) do not run until the game has loaded. The
following snippet, run from a [LocalScript](/docs/reference/engine/classes/LocalScript) in
[ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst) yields until the game has loaded:

```
if not game:IsLoaded() then



game.Loaded:Wait()



end
```

See also:

* [Replication order](/docs/scripting/attributes#replication-order)
  for a more detailed summary of the loading process.
* [DataModel.Loaded](/docs/reference/engine/classes/DataModel#Loaded), an event that fires when the game has loaded
* [Instance:WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild), a function which can be used to wait
  for an individual [Instance](/docs/reference/engine/classes/Instance) to replicate without having to wait
  for the whole game to finish loading.

Provide feedback

---

Callbacks

OnClose

Deprecated

Show details

---