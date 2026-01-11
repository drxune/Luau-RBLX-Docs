# ConfigService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ConfigService
Scraped: 2026-01-11T02:34:44.784663Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- ConfigService
- ConfigSnapshot
- Player
- SetTestingValue()
- ConfigSnapshot:Refresh()
- ConfigSnapshot:GetValue()
- ClearTestingValue()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ConfigService](/docs/reference/engine/classes/ConfigService)

English

Feedback

Engine Class

ConfigService

A game service that gives access to in-experience configuration with updates
in real time.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [ClearTestingValue](#ClearTestingValue)(key: [string](/docs/luau/strings)):() |
| [GetConfigAsync](#GetConfigAsync)():[ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot) |
| [GetConfigForPlayerAsync](#GetConfigForPlayerAsync)(player: [Player](/docs/reference/engine/classes/Player)):[ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot) |
| [SetTestingValue](#SetTestingValue)(key: [string](/docs/luau/strings),value: Variant):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

ConfigService exposes methods for getting [ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot) objects.
Configs can only be accessed by game servers, so you can't use
[ConfigService](/docs/reference/engine/classes/ConfigService) within client scripts.

See [Experience configs](/docs/production/configs) for an in-depth guide
on managing keys, deploying real-time updates, error handling, limits, and
more.

---

API Reference

Methods

ClearTestingValue

Clears current testing value for the given key.

ConfigService:ClearTestingValue(key:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key of the configuration to clear testing value for. |

Returns

()

Removes a testing override created by the
[SetTestingValue()](/docs/reference/engine/classes/ConfigService#SetTestingValue) function. The
actual configured value will be returned after calling this function.

Provide feedback

---

GetConfigAsync

Yields

Retrieves a snapshot of the latest configuration.

ConfigService:GetConfigAsync():[ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot)

Returns

[ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot)

A [ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot) instance with the latest configuration.

This function retrieves the latest available configuration as a
[ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot) instance without player targeting. Snapshots can be
refreshed to the latest values by calling
[ConfigSnapshot:Refresh()](/docs/reference/engine/classes/ConfigSnapshot#Refresh).

Experiments are not applied since there is no player context.

If configuration fails to load and there is no previously available
configuration, this function throws an error.

Provide feedback

---

GetConfigForPlayerAsync

Yields

Retrieves a snapshot of the latest configuration for a specific player.

ConfigService:GetConfigForPlayerAsync(player:[Player](/docs/reference/engine/classes/Player)):[ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The player to get the configuration for. |

Returns

[ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot)

A [ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot) instance with the latest configuration
targeted to the player.

Retrieves the latest available configuration as a [ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot)
instance targeting to the given player. Snapshots can be refreshed to the
latest values by calling [ConfigSnapshot:Refresh()](/docs/reference/engine/classes/ConfigSnapshot#Refresh).

This function applies all experiments running for the player.

If configuration fails to load and there is no previously available
configuration, this function throws an error.

Provide feedback

---

SetTestingValue

Sets a testing override for the given key.

ConfigService:SetTestingValue(

key:[string](/docs/luau/strings), value:Variant

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key of the configuration to override with a testing value. |
| value:Variant  Value to set as the testing override. |

Returns

()

Sets a testing override for the specified configuration key in the current
server instance. When a testing value is set, calls to
[ConfigSnapshot:GetValue()](/docs/reference/engine/classes/ConfigSnapshot#GetValue) for that key will return the testing
value instead of the actual configured value.

Testing values can be cleared by calling the
[ClearTestingValue()](/docs/reference/engine/classes/ConfigService#ClearTestingValue) function.

Provide feedback

---