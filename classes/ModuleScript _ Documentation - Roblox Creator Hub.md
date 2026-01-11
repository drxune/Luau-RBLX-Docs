# ModuleScript | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ModuleScript
Scraped: 2026-01-11T02:31:42.440903Z

## Inherits
- LuaSourceContainer
- ModuleScript
- Instance
- Object
- ModuleScripts
- Scripts
- LocalScripts
- LocalScript
- Script
- ScriptEditorService
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)
6. /
7. [ModuleScript](/docs/reference/engine/classes/ModuleScript)

English

Feedback

Engine Class

![ModuleScript](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ModuleScript-Dark.webp)ModuleScript

A script type that runs once when [require()](/docs/reference/engine/globals/LuaGlobals#require) is called with
it. Returns exactly one value, usually a table of functions, to used by other
scripts. Useful for compartmentalizing code.

---

Summary

Properties

|  |
| --- |
| [LinkedSource](#LinkedSource):ContentId  Deprecated |
| [Source](#Source):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [ModuleScript](/docs/reference/engine/classes/ModuleScript) is a script type that returns exactly one value by a
call to [require()](/docs/reference/engine/globals/LuaGlobals#require). [ModuleScripts](/docs/reference/engine/classes/ModuleScript) run
once and only once per Luau environment and return the exact same value for
subsequent calls to [require()](/docs/reference/engine/globals/LuaGlobals#require).

[ModuleScripts](/docs/reference/engine/classes/ModuleScript) are essential objects for adhering to the
"Don't Repeat Yourself" (DRY) principle, allowing you to write a function only
once and use it everywhere. Having multiple copies of a function is
problematic when you need to change their behavior, so you should define
functions or groups of functions in [ModuleScripts](/docs/reference/engine/classes/ModuleScript) and
have your [Scripts](/docs/reference/engine/classes/Script) and [LocalScripts](/docs/reference/engine/classes/LocalScript) call
[require()](/docs/reference/engine/globals/LuaGlobals#require) on those modules.

It's important to know that return values from
[ModuleScripts](/docs/reference/engine/classes/ModuleScript) are independent with regards to
[Scripts](/docs/reference/engine/classes/Script) and [LocalScripts](/docs/reference/engine/classes/LocalScript), and other
environments like the
[Command Bar](/docs/studio/ui-overview#command-bar). Using
[require()](/docs/reference/engine/globals/LuaGlobals#require) on a [ModuleScript](/docs/reference/engine/classes/ModuleScript) in a
[LocalScript](/docs/reference/engine/classes/LocalScript) will run the code on the client, even if a [Script](/docs/reference/engine/classes/Script)
did so already on the server. Therefore, be careful if you're using a
[ModuleScript](/docs/reference/engine/classes/ModuleScript) on the client and server at the same time, or debugging
it within Studio.

Note that the first call to [require()](/docs/reference/engine/globals/LuaGlobals#require) will not yield
(halt) unless the [ModuleScript](/docs/reference/engine/classes/ModuleScript) yields (calls [task.wait()](/docs/reference/engine/libraries/task#wait) for
example), in which case the current thread that called
[require()](/docs/reference/engine/globals/LuaGlobals#require) will yield until the [ModuleScript](/docs/reference/engine/classes/ModuleScript)
returns a value. If a [ModuleScript](/docs/reference/engine/classes/ModuleScript) is attempting to
[require()](/docs/reference/engine/globals/LuaGlobals#require) another [ModuleScript](/docs/reference/engine/classes/ModuleScript) that in turn tries
to [require()](/docs/reference/engine/globals/LuaGlobals#require) it, the thread will hang and never halt
(cyclic [require()](/docs/reference/engine/globals/LuaGlobals#require) calls do not generate errors). Be
mindful of your module dependencies in large projects!

If a [ModuleScript](/docs/reference/engine/classes/ModuleScript) is uploaded to Roblox and the root module has the
name set to MainModule, it can be uploaded as a model and required using
[require()](/docs/reference/engine/globals/LuaGlobals#require) with the model's asset ID. Then it can be loaded
into your experience, although this logic only works on the server and will
error on the client. If other users want to use the module, it must be public.

Code Samples

Simple ModuleScript Example

The code sample starts by creating a local variable holding an empty table. It
then fills the table with two placeholder functions, and then finally returns
the table. Using this code in a ModuleScript would make the my\_functions
table (and thus any functions, tables or other values within it) available to
any Script, LocalScript or other ModuleScript.

```
-- Tables store multiple values in one variable



local MyFunctions = {}



-- Add a few functions to the table



function MyFunctions.foo()



print("Foo!")



end



function MyFunctions.bar()



print("Bar!")



end



-- ModuleScripts must return exactly one value



return MyFunctions
```

Simple ModuleScript Usage

This code sample shows how to use the require function on a ModuleScript, then
use the value that it returned. See the "Simple ModuleScript Example" for the
code to go with this sample.

```
-- The require function is provided a ModuleScript, then runs



-- the code, waiting until it returns a singular value.



local MyFunctions = require(script.Parent.MyFunctions)



-- These are some dummy functions defined in another code sample



MyFunctions.foo()



MyFunctions.bar()
```

---

API Reference

Properties

LinkedSource

Deprecated

Show details

---

Source

Read Parallel

The code to be executed.

ModuleScript.Source:[string](/docs/luau/strings)

The code to be executed.

If you want to read or modify a script that the user has open, consider
using the [ScriptEditorService](/docs/reference/engine/classes/ScriptEditorService) to interact with the Script Editor
instead.

Provide feedback

---