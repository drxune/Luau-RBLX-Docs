# ReplicatedStorage | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ReplicatedStorage
Scraped: 2026-01-11T02:32:10.460882Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- ReplicatedStorage
- Object
- ModuleScript
- RemoteFunction
- RemoteEvent
- Scripts
- LocalScripts
- Workspace
- Enabled
- Player
- StarterPlayerScripts
- StarterCharacterScripts
- StarterGui
- ServerScriptService
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage)

English

Feedback

Engine Class

![ReplicatedStorage](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ReplicatedStorage-Dark.webp)ReplicatedStorage

A container service for objects that are replicated to all clients.

Not Creatable

Service

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage) is a general container service for objects that are
available to both the server and connected clients. It is ideal for
[ModuleScript](/docs/reference/engine/classes/ModuleScript), [RemoteFunction](/docs/reference/engine/classes/RemoteFunction), [RemoteEvent](/docs/reference/engine/classes/RemoteEvent), and other
objects that are useful to both server-side [Scripts](/docs/reference/engine/classes/Script) and
client-side [LocalScripts](/docs/reference/engine/classes/LocalScript).

Objects parented to this service are fully replicated to clients, and normal
replication rules apply. Any changes that are made on the client persist but
aren't replicated to the server. Client changes may be overwritten if the
server does something that overwrites those changes.

Certain changes on the client, such as moving an object from the
[Workspace](/docs/reference/engine/classes/Workspace) to [ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage), can lead to desynchronization
issues (for example, physics updates not being replicated to the object).

[LocalScripts](/docs/reference/engine/classes/LocalScript) do not run when parented to this service,
even if they are [Enabled](/docs/reference/engine/classes/BaseScript#Enabled);
[LocalScripts](/docs/reference/engine/classes/LocalScript) have various other locations where they
eventually run on a [Player](/docs/reference/engine/classes/Player) client such as
[StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts), [StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts), or
[StarterGui](/docs/reference/engine/classes/StarterGui).

Similarly, [Scripts](/docs/reference/engine/classes/Script) do not run when parented to this service
unless you change their [Enum.RunContext](/docs/reference/engine/enums/RunContext) property from the default value of
[Legacy](/docs/reference/engine/enums/RunContext#Legacy). Server [Scripts](/docs/reference/engine/classes/Script) that run on
their own should be parented to [ServerScriptService](/docs/reference/engine/classes/ServerScriptService) instead.

If a [ModuleScript](/docs/reference/engine/classes/ModuleScript) within this service is required by any other script,
it runs as normal. Such modules typically house code that is shared by the
server and client.