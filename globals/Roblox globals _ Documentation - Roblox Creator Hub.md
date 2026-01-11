# Roblox globals | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/globals/RobloxGlobals#delay
Scraped: 2026-01-11T02:49:20.090233Z

## Inherits
- PluginManager
- GlobalSettings
- Stats
- UserSettings
- DataModel
- Plugin
- LuaSourceContainer
- Workspace
- Workspace.AuthorityMode
- Script
- ModuleScripts
- ModuleScript
- LocalScript
1. [Globals](/docs/reference/engine/globals)
2. /
3. [Roblox globals](/docs/reference/engine/globals/Roblox%20globals)
4. /
5. [Functions](/docs/reference/engine/globals/Roblox%20globals#functions)

English

Feedback

Engine Global

Roblox globals

Built-in functions and constants unique to Roblox.

---

Summary

Functions

|  |
| --- |
| [delay](#delay)(delayTime: [number](/docs/luau/numbers),callback: [function](/docs/luau/functions)):()  Deprecated |
| [DebuggerManager](#DebuggerManager)():DebuggerManager  Deprecated |
| [elapsedTime](#elapsedTime)():[number](/docs/luau/numbers) |
| [PluginManager](#PluginManager)():[PluginManager](/docs/reference/engine/classes/PluginManager) |
| [printidentity](#printidentity)(prefix: [string](/docs/luau/strings)):()  Deprecated |
| [settings](#settings)():[GlobalSettings](/docs/reference/engine/classes/GlobalSettings) |
| [spawn](#spawn)(callback: [function](/docs/luau/functions)):()  Deprecated |
| [stats](#stats)():[Stats](/docs/reference/engine/classes/Stats)  Deprecated |
| [tick](#tick)():[number](/docs/luau/numbers) |
| [time](#time)():[number](/docs/luau/numbers) |
| [typeof](#typeof)(object: Variant):[string](/docs/luau/strings) |
| [UserSettings](#UserSettings)():[UserSettings](/docs/reference/engine/classes/UserSettings) |
| [version](#version)():[string](/docs/luau/strings) |
| [wait](#wait)(seconds: [number](/docs/luau/numbers)):[number](/docs/luau/numbers),[number](/docs/luau/numbers)  Deprecated |
| [warn](#warn)(params: [Tuple](/docs/luau/tuples)):() |
| [ypcall](#ypcall)(f: [function](/docs/luau/functions),args: [Tuple](/docs/luau/tuples)):[boolean](/docs/luau/booleans),Variant  Deprecated |

Properties

|  |
| --- |
| [Enum](#Enum):[Enums](/docs/reference/engine/datatypes/Enums) |
| [game](#game):[DataModel](/docs/reference/engine/classes/DataModel) |
| [plugin](#plugin):[Plugin](/docs/reference/engine/classes/Plugin) |
| [shared](#shared):[Array](/docs/luau/tables#arrays) |
| [script](#script):[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) |
| [workspace](#workspace):[Workspace](/docs/reference/engine/classes/Workspace) |

Roblox provides several unique built-in functions and variables in its
embedding of Luau. These are only found on Roblox and are not packaged by
default with Luau or Lua.

---

API Reference

Functions

delay

Deprecated

Show details

---

DebuggerManager

Deprecated

Show details

---

elapsedTime

Returns the amount of time in seconds that the current instance of Roblox
has been running for.

elapsedTime():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns how much time has elapsed since the current instance of Roblox was
started. In Roblox Studio, this begins counting up from the moment Roblox
Studio starts running, not just when opening a place.

Provide feedback

---

PluginManager

Refers to the [PluginManager](/docs/reference/engine/classes/PluginManager), a deprecated singleton that was
previously required to create plugins.

PluginManager():[PluginManager](/docs/reference/engine/classes/PluginManager)

Returns

[PluginManager](/docs/reference/engine/classes/PluginManager)

Returns the [PluginManager](/docs/reference/engine/classes/PluginManager) which is a deprecated singleton that was
previously required to create plugins. It still has some applicable uses,
such as if you need to create a [Plugin](/docs/reference/engine/classes/Plugin) object from Studio's
[Command Bar](/docs/studio/ui-overview#command-bar).

Provide feedback

---

printidentity

Deprecated

Show details

---

settings

Returns the [GlobalSettings](/docs/reference/engine/classes/GlobalSettings) object, which can be used to access
settings objects that configure Roblox Studio's behavior.

settings():[GlobalSettings](/docs/reference/engine/classes/GlobalSettings)

Returns

[GlobalSettings](/docs/reference/engine/classes/GlobalSettings)

Returns the [GlobalSettings](/docs/reference/engine/classes/GlobalSettings) object, which can be used to access the
settings objects that are used in Roblox Studio's settings menu.

Provide feedback

---

spawn

Deprecated

Show details

---

stats

Deprecated

Show details

---

tick

Returns the amount of time in seconds since the Unix epoch according to
this device's time.

tick():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns how much time has elapsed, in seconds, since the Unix epoch, on
the current local session's computer. The Unix epoch is represented by
00:00:00 on 1 January 1970.

tick() isn't officially deprecated, but has a variety of issues. It can
be off by up to one second and returns inconsistent results across time
zones and operating systems. Use [os.time()](/docs/reference/engine/libraries/os#time),
[os.clock()](/docs/reference/engine/libraries/os#clock), or [time()](/docs/reference/engine/globals/RobloxGlobals#time) instead. Also
consider [DateTime.UnixTimestamp](/docs/reference/engine/datatypes/DateTime#UnixTimestamp) and
[DateTime.UnixTimestampMillis](/docs/reference/engine/datatypes/DateTime#UnixTimestampMillis).

Provide feedback

---

time

Returns the amount of time in seconds that has elapsed since the current
game instance started running.

time():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the amount of time, in seconds, that has elapsed since the current
game instance started running. If the current game instance is not
running, this will be 0.

If [Workspace.AuthorityMode](/docs/reference/engine/classes/Workspace#AuthorityMode) is [Enum.AuthorityMode.Server](/docs/reference/engine/enums/AuthorityMode#Server), this
value is synchronized between client and server.

Provide feedback

---

typeof

Returns the type of the given object as a string, also supporting
Roblox-specific types (e.g. Vector3).

typeof(object:Variant):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| object:Variant  The Luau type that will have its type checked. |

Returns

[string](/docs/luau/strings)

Returns the type of the object specified, as a string. This function is
more accurate than Luau's native type function, as it does not denote
Roblox-specific types as userdata.

Provide feedback

---

UserSettings

Returns the UserSettings object, which is used to read information from
the current user's game menu settings.

UserSettings():[UserSettings](/docs/reference/engine/classes/UserSettings)

Returns

[UserSettings](/docs/reference/engine/classes/UserSettings)

Returns the [UserSettings](/docs/reference/engine/classes/UserSettings) object, which is used to read information
from the current user's game menu settings.

Provide feedback

---

version

Returns the current version of Roblox as a string, which includes the
generation, version, patch and commit.

version():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

Returns the current version of Roblox as a string. The integers in the
version string are separated by periods, and each integers represent the
following, in order:

* Generation - The current generation of the application shell that is
  hosting the client.
* Version - The current release version of Roblox.
* Patch - The current patch number for this version of Roblox.
* Commit - The ID of the last internal commit that was accepted into this
  version of the client.

Provide feedback

---

wait

Deprecated

Show details

---

warn

Behaves similarly to print, except with more distinct formatting (yellow);
intended for messages which describe potential problems.

warn(params:[Tuple](/docs/luau/tuples)):()

Parameters

|  |
| --- |
| params:[Tuple](/docs/luau/tuples)  This function accepts any number of arguments, and will attempt to convert them into strings which will then be joined together with spaces between them. |

Returns

()

Behaves identically to Luau's print function, except the output is styled
as a warning, with yellow text and a timestamp. This function accepts any
number of arguments, and will attempt to convert them into strings which
will then be joined together with spaces between them.

Provide feedback

---

ypcall

Deprecated

Show details

---

Properties

Enum

Contains all Enum objects.

Enum:[Enums](/docs/reference/engine/datatypes/Enums)

A reference to the Enums data type, which stores all of the available
enums that can be used on Roblox.

Provide feedback

---

game

Refers to the DataModel singleton, the root instance of a place's
hierarchy.

game:[DataModel](/docs/reference/engine/classes/DataModel)

A reference to the [DataModel](/docs/reference/engine/classes/DataModel), which is the root Instance of
Roblox's parent/child hierarchy.

Provide feedback

---

plugin

Refers to a Plugin singleton when the code is run in the context of a
Studio plugin.

plugin:[Plugin](/docs/reference/engine/classes/Plugin)

A reference to the [Plugin](/docs/reference/engine/classes/Plugin) object that represents the plugin being
run from this [Script](/docs/reference/engine/classes/Script). This reference exists only in the context
where a script is executed as a plugin and is not passed to
[ModuleScripts](/docs/reference/engine/classes/ModuleScript) within the plugin. To use this
reference in a [ModuleScript](/docs/reference/engine/classes/ModuleScript), you must explicitly pass it.

```
assert(plugin, "This script must be run as a plugin!")



-- Code beyond this point will execute only if the script is run as a plugin
```

Provide feedback

---

shared

A table shared between all code running at the same execution context
level.

shared:[Array](/docs/luau/tables#arrays)

A table that is shared across all scripts that share the same execution
context level. This serves the exact same purpose as \_G.

Provide feedback

---

script

A reference to the LuaSourceContainer object (Script, LocalScript, or
ModuleScript) that is executing this code.

script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)

A reference to the script object that is executing the code you are
writing. It can be either a [Script](/docs/reference/engine/classes/Script), a [LocalScript](/docs/reference/engine/classes/LocalScript), or a
[ModuleScript](/docs/reference/engine/classes/ModuleScript). This variable is not available when executing code
from Roblox Studio's command bar.

Provide feedback

---

workspace

A reference to the Workspace service, which contains all of the physical
components of a place.

workspace:[Workspace](/docs/reference/engine/classes/Workspace)

A reference to the [Workspace](/docs/reference/engine/classes/Workspace) service, which contains all of the
physical components of a Roblox world.

Provide feedback

---