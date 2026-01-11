# LocalScript | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LocalScript
Scraped: 2026-01-11T02:34:51.723043Z

## Inherits
- Script
- LocalScript
- BaseScript
- Instance
- Object
- Camera
- LocalScripts
- LocalPlayer
- Players
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Script](/docs/reference/engine/classes/Script)
6. /
7. [LocalScript](/docs/reference/engine/classes/LocalScript)

English

Feedback

Engine Class

![LocalScript](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/LocalScript-Dark.webp)LocalScript

An object that contains and runs Luau code on the client (player's device)
instead of the server.

---

Summary

Inherited Members

1 inherited from [Script](/docs/reference/engine/classes/Script)

4 inherited from [BaseScript](/docs/reference/engine/classes/BaseScript)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [LocalScript](/docs/reference/engine/classes/LocalScript) is a Luau source container that runs its contents on the
client (player's device) instead of the server. It is used to access
client-only objects such as the player's [Camera](/docs/reference/engine/classes/Camera).

For code run through [LocalScripts](/docs/reference/engine/classes/LocalScript), the
[LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) property of the [Players](/docs/reference/engine/classes/Players)
service will return the player whose client is running the script.

See [here](/docs/projects/data-model#client) for a table of valid
container services from which [LocalScripts](/docs/reference/engine/classes/LocalScript) will execute.