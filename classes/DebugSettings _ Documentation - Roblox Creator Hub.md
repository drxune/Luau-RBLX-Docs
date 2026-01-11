# DebugSettings | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DebugSettings
Scraped: 2026-01-11T02:27:54.821603Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- DebugSettings
- DataModel
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DebugSettings](/docs/reference/engine/classes/DebugSettings)

English

Feedback

Engine Class

DebugSettings

Collection of various developer-facing diagnostics information.

Not Creatable

Service

Not Replicated

Not Browsable

---

Summary

Properties

|  |
| --- |
| [DataModel](#DataModel):[number](/docs/luau/numbers) |
| [InstanceCount](#InstanceCount):[number](/docs/luau/numbers) |
| [IsScriptStackTracingEnabled](#IsScriptStackTracingEnabled):[boolean](/docs/luau/booleans) |
| [JobCount](#JobCount):[number](/docs/luau/numbers) |
| [PlayerCount](#PlayerCount):[number](/docs/luau/numbers) |
| [ReportSoundWarnings](#ReportSoundWarnings):[boolean](/docs/luau/booleans) |
| [RobloxVersion](#RobloxVersion):[string](/docs/luau/strings) |
| [TickCountPreciseOverride](#TickCountPreciseOverride):[Enum.TickCountSampleMethod](/docs/reference/engine/enums/TickCountSampleMethod) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The DebugSettings allows you to view diagnostics information regarding Roblox.
It is labeled as Diagnostics in the Roblox Studio Settings menu.

---

API Reference

Properties

DataModel

Read Only

Not Replicated

Read Parallel

Describes whether a [DataModel](/docs/reference/engine/classes/DataModel) is actively in memory, as an integer
(where 1 = true, and 0 = false).

DebugSettings.DataModel:[number](/docs/luau/numbers)

Describes whether a [DataModel](/docs/reference/engine/classes/DataModel) is actively in memory, as an integer
(where 1 = true, and 0 = false).

Provide feedback

---

InstanceCount

Read Only

Not Replicated

Read Parallel

The number of instances active in the simulation.

DebugSettings.InstanceCount:[number](/docs/luau/numbers)

The number of instances active in the simulation.

Provide feedback

---

IsScriptStackTracingEnabled

Read Parallel

Whether or not a stacktrace is displayed in the output for an error.

DebugSettings.IsScriptStackTracingEnabled:[boolean](/docs/luau/booleans)

Whether or not a stacktrace is displayed in the output for an error.

Provide feedback

---

JobCount

Read Only

Not Replicated

Read Parallel

Returns the number of internal DataModel jobs actively being processed.

DebugSettings.JobCount:[number](/docs/luau/numbers)

Returns the number of internal DataModel jobs actively being processed.

Provide feedback

---

PlayerCount

Read Only

Not Replicated

Read Parallel

The number of players currently in the active game-instance.

DebugSettings.PlayerCount:[number](/docs/luau/numbers)

The number of players currently in the active game-instance.

Provide feedback

---

ReportSoundWarnings

Read Parallel

Whether or not sound warnings should be reported.

DebugSettings.ReportSoundWarnings:[boolean](/docs/luau/booleans)

Whether or not sound warnings should be reported.

Provide feedback

---

RobloxVersion

Read Only

Not Replicated

Read Parallel

The current client version of Roblox. Can also be retrieved by using the
version() function.

DebugSettings.RobloxVersion:[string](/docs/luau/strings)

The current client version of Roblox. Can also be retrieved by using the
version() function.

Provide feedback

---

TickCountPreciseOverride

Read Parallel

Sets the internal sampling method used to measure elapsed time with
consistency across platforms.

DebugSettings.TickCountPreciseOverride:[Enum.TickCountSampleMethod](/docs/reference/engine/enums/TickCountSampleMethod)

Sets the internal sampling method used to measure elapsed time with
consistency across platforms.

Provide feedback

---