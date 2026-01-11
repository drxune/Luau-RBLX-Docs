# ServerScriptService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ServerScriptService
Scraped: 2026-01-11T02:39:17.504334Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- ServerScriptService
- Script
- Object
- ModuleScript
- Disabled
- LoadStringEnabled
- cloned
- ServerStorage
- ReplicatedStorage
- Folders
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ServerScriptService](/docs/reference/engine/classes/ServerScriptService)

English

Feedback

Engine Class

![ServerScriptService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ServerScriptService-Dark.webp)ServerScriptService

A container service for server-only [Script](/docs/reference/engine/classes/Script) objects.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [LoadStringEnabled](#LoadStringEnabled):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

ServerScriptService is a container service for [Script](/docs/reference/engine/classes/Script),
[ModuleScript](/docs/reference/engine/classes/ModuleScript) and other scripting-related assets that are only meant
for server use. The contents are never replicated to player clients at all,
which allows for a secure storage of important game logic. Script objects will
run if they are within this service and not
[Disabled](/docs/reference/engine/classes/BaseScript#Disabled).

This service houses just one property,
[LoadStringEnabled](/docs/reference/engine/classes/ServerScriptService#LoadStringEnabled), which
determines whether the loadstring function in Luau is enabled. It's
recommended to keep this disabled for security reasons, as misusing this
function can lead to remote code execution vulnerabilities.

Scripts running in ServerScriptService may need access to various other assets
which are not scripting-related, such as prefabricated models to be
[cloned](/docs/reference/engine/classes/Instance#Clone). Such assets should go in
[ServerStorage](/docs/reference/engine/classes/ServerStorage), which behaves similarly to this service except that
[Script](/docs/reference/engine/classes/Script) objects will not run even if they are not
[Disabled](/docs/reference/engine/classes/BaseScript#Disabled). Assets and [ModuleScript](/docs/reference/engine/classes/ModuleScript) that are
useful to both the server and clients should go in [ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage)
instead. Finally, you can further organize objects within this service through
the use of [Folders](/docs/reference/engine/classes/Folder) without affecting the way it behaves.

---

API Reference

Properties

LoadStringEnabled

Not Replicated

Not Scriptable

Read Parallel

Toggles whether or not the loadstring function can be used by server
scripts. Defaults to false.

ServerScriptService.LoadStringEnabled:[boolean](/docs/luau/booleans)

Toggles whether or not the loadstring function can be used by server
scripts. Defaults to false.

Provide feedback

---