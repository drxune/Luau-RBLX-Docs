# ServerStorage | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ServerStorage
Scraped: 2026-01-11T02:31:21.897373Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- ServerStorage
- LocalScripts
- DataModel.GetService
- Scripts
- ModuleScripts
- ServerScriptService
- Workspace
- ReplicatedStorage
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ServerStorage](/docs/reference/engine/classes/ServerStorage)

English

Feedback

Engine Class

![ServerStorage](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ServerStorage-Dark.webp)ServerStorage

A container whose contents are only accessible on the server. Objects
descending from ServerStorage will not replicate to the client and will not be
accessible from [LocalScripts](/docs/reference/engine/classes/LocalScript).

Not Creatable

Service

Not Replicated

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A container whose contents are only accessible on the server. Objects
descending from ServerStorage will not replicate to the client and will not be
accessible from [LocalScripts](/docs/reference/engine/classes/LocalScript).

As ServerStorage is a service it can only be accessed using the
[DataModel.GetService](/docs/reference/engine/classes/DataModel#GetService) method.

By storing large objects such as maps in ServerStorage until they are needed,
network traffic will not be used up transmitting these objects to the client
when they join the game.

[Scripts](/docs/reference/engine/classes/Script) will not run when they are parented to ServerStorage,
although [ModuleScripts](/docs/reference/engine/classes/ModuleScript) contained within can be accessed
and ran. It is recommended developers use [ServerScriptService](/docs/reference/engine/classes/ServerScriptService) to hold
[Scripts](/docs/reference/engine/classes/Script) they wish the server to execute.

Note that as the contents of ServerStorage can only be accessed by the server,
its contents will need to be parented elsewhere (such as [Workspace](/docs/reference/engine/classes/Workspace))
before clients can access them. Developers who require a container that is
accessible by both the server and client are advised to use
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage) instead.

Code Samples

ServerStorage Map Rotation

This is a very simple example of how a multiple map system can be made using
ServerStorage.

It creates three dummy models (to take the place of maps), that are parented
to ServerStorage. Then, it will load a random map (different to the previous
map) and wait a specified duration on a loop.

Developers wishing to integrate something similar into their games should
consider measures to ensure players respawn correctly, or go to a lobby during
intermission periods.

```
local ServerStorage = game:GetService("ServerStorage")



local ROUND_TIME = 5



local map1 = Instance.new("Model")



map1.Name = "Map1"



map1.Parent = ServerStorage



local map2 = Instance.new("Model")



map2.Name = "Map2"



map2.Parent = ServerStorage



local map3 = Instance.new("Model")



map3.Name = "Map3"



map3.Parent = ServerStorage



local maps = { map1, map2, map3 }



local RNG = Random.new()



local currentMap = nil



local lastPick = nil



while true do



print("New map!")



-- remove current map



if currentMap then



currentMap:Destroy()



end



-- pick a map



local randomPick = nil



if #maps > 1 then



repeat



randomPick = RNG:NextInteger(1, #maps)



until randomPick ~= lastPick



lastPick = randomPick



end



-- fetch new map



local map = maps[randomPick]



currentMap = map:Clone()



currentMap.Parent = workspace



task.wait(ROUND_TIME)



end
```