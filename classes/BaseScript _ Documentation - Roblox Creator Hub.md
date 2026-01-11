# BaseScript | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BaseScript
Scraped: 2026-01-11T02:33:16.364449Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- LuaSourceContainer
- BaseScript
- Instance
- Object
- Script
- Disabled
- Enabled
- LocalScript
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)
6. /
7. [BaseScript](/docs/reference/engine/classes/BaseScript)

English

Feedback

Engine Class

BaseScript

The base class for all script objects which run automatically.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Disabled](#Disabled):[boolean](/docs/luau/booleans) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [LinkedSource](#LinkedSource):ContentId  Deprecated |
| [RunContext](#RunContext):[Enum.RunContext](/docs/reference/engine/enums/RunContext) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Script](/docs/reference/engine/classes/Script)

The base class for all script objects which run automatically.

---

API Reference

Properties

Disabled

Read Parallel

Determines whether a [BaseScript](/docs/reference/engine/classes/BaseScript) will run or not.

BaseScript.Disabled:[boolean](/docs/luau/booleans)

Determines whether a [BaseScript](/docs/reference/engine/classes/BaseScript) will run or not.

If a script is disabled by changing this property to true while the script
is running, the current running thread of the script will be terminated.

If this property is changed from true to false, the script will run again.
This means that [Disabled](/docs/reference/engine/classes/BaseScript#Disabled) can be toggled to
restart a script:

```
scriptObject.Disabled = true



scriptObject.Disabled = false
```

Note that the above code snippet cannot be used within the script itself,
since disabling the script from within itself will terminate the thread
and the line to reenable it will never execute.

Provide feedback

---

Enabled

Not Replicated

Read Parallel

Determines whether a [BaseScript](/docs/reference/engine/classes/BaseScript) will run or not.

BaseScript.Enabled:[boolean](/docs/luau/booleans)

Determines whether a [BaseScript](/docs/reference/engine/classes/BaseScript) will run or not. This should be
used in favor of the similar but opposite
[Disabled](/docs/reference/engine/classes/BaseScript#Disabled) property.

If a script is disabled by changing this property to false while the
script is running, the current running thread of the script will be
terminated.

If this property is changed from false to true, the script will run again.
This means that [Enabled](/docs/reference/engine/classes/BaseScript#Enabled) can be toggled to
restart a script:

```
scriptObject.Enabled = false



scriptObject.Enabled = true
```

Note that the above code snippet cannot be used within the script itself,
since disabling the script from within itself will terminate the thread
and the line to reenable it will never execute.

Provide feedback

---

LinkedSource

Deprecated

Show details

---

RunContext

Plugin Security

Read Parallel

Determines the context under which the script will run.

BaseScript.RunContext:[Enum.RunContext](/docs/reference/engine/enums/RunContext)

Determines the context under which the script will run.

When using the Legacy RunContext scripts will only run when parented to
certain containers dependent on whether they are a [Script](/docs/reference/engine/classes/Script) or
[LocalScript](/docs/reference/engine/classes/LocalScript).

If RunContext is assigned while the script is running any threads created
by the script will be terminated and the script will start running under
the new context if possible.

Note, RunContext cannot be used from a LocalScript.

Provide feedback

---