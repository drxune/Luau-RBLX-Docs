# Script | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Script
Scraped: 2026-01-11T02:39:42.990803Z

## Inherits
- BaseScript
- Script
- Instance
- Object
- LocalScript
- BadgeService
- LocalScripts
- Enabled
- Workspace
- ServerScriptService
- Parent
- ScriptEditorService
- ScriptEditorService:UpdateSourceAsync()
- ScriptEditorService:GetEditorSource()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BaseScript](/docs/reference/engine/classes/BaseScript)
6. /
7. [Script](/docs/reference/engine/classes/Script)

English

Feedback

Engine Class

![Script](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Script-Dark.webp)Script

An object that contains and runs Luau code on the server.

---

Summary

Properties

|  |
| --- |
| [Source](#Source):[string](/docs/luau/strings) |

Inherited Members

4 inherited from [BaseScript](/docs/reference/engine/classes/BaseScript)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[LocalScript](/docs/reference/engine/classes/LocalScript)

A [Script](/docs/reference/engine/classes/Script) is a Luau source container that can access server-side
objects, properties, and events, such as to award badges to players using
[BadgeService](/docs/reference/engine/classes/BadgeService), while [LocalScripts](/docs/reference/engine/classes/LocalScript) on the client
cannot.

The instant that the following conditions are met, a script's code is run in a
new thread:

* Its [Enabled](/docs/reference/engine/classes/Script#Enabled) property is true.
* The [Script](/docs/reference/engine/classes/Script) object is a descendant of the [Workspace](/docs/reference/engine/classes/Workspace) or
  [ServerScriptService](/docs/reference/engine/classes/ServerScriptService).

The script will continue to run until the above conditions are not met, it
terminates, or it raises an error (unless that error is raised by a function
connected to some event that is firing). Additionally, the thread will be
stopped if the script or one of its ancestors is destroyed. A script will
continue to run even if the [Parent](/docs/reference/engine/classes/Instance#Parent) property is set to
nil and the [Script](/docs/reference/engine/classes/Script) is not destroyed.

---

API Reference

Properties

Source

Read Parallel

The code to be executed.

Script.Source:[string](/docs/luau/strings)

Represents the code to be executed. It's protected and discouraged for
editing directly. Attempting to access this property in a [Script](/docs/reference/engine/classes/Script)
or [LocalScript](/docs/reference/engine/classes/LocalScript) causes errors.

If you want to read or modify the source of a script that a user has open,
use [ScriptEditorService](/docs/reference/engine/classes/ScriptEditorService) to interact with the
[Script Editor](/docs/studio/script-editor) rather than directly
modifying this property. Both
[ScriptEditorService:UpdateSourceAsync()](/docs/reference/engine/classes/ScriptEditorService#UpdateSourceAsync) and
[ScriptEditorService:GetEditorSource()](/docs/reference/engine/classes/ScriptEditorService#GetEditorSource) can read or modify script
content from the script editor if the script is opened. You can also read
the source from the
[command line](/docs/studio/ui-overview#command-bar).

Provide feedback

---