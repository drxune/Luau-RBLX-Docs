# Luau globals | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/globals/LuaGlobals#xpcall
Scraped: 2026-01-11T02:50:02.563937Z

## Inherits
- ModuleScript
- ServerScriptService
- ReplicatedStorage
- LocalScript
- Script
1. [Globals](/docs/reference/engine/globals)
2. /
3. [Luau globals](/docs/reference/engine/globals/Luau%20globals)
4. /
5. [xpcall](/docs/reference/engine/globals/Luau%20globals#xpcall)

English

Feedback

Engine Global

Luau globals

A list of functions and variables that are native to Luau.

---

Summary

Functions

|  |
| --- |
| [assert](#assert)(value: Variant,errorMessage: [string](/docs/luau/strings)):Variant |
| [collectgarbage](#collectgarbage)(operation: [string](/docs/luau/strings)):Variant  Deprecated |
| [error](#error)(message: Variant,level: [number](/docs/luau/numbers)):() |
| [gcinfo](#gcinfo)():[number](/docs/luau/numbers) |
| [getfenv](#getfenv)(stack: Variant):[table](/docs/luau/tables)  Deprecated |
| [getmetatable](#getmetatable)(t: Variant):Variant |
| [ipairs](#ipairs)(t: [Array](/docs/luau/tables#arrays)):[function](/docs/luau/functions),[Array](/docs/luau/tables#arrays),[number](/docs/luau/numbers) |
| [loadstring](#loadstring)(contents: [string](/docs/luau/strings),chunkname: [string](/docs/luau/strings)):Variant |
| [newproxy](#newproxy)(addMetatable: [boolean](/docs/luau/booleans)):[userdata](/docs/luau/userdata) |
| [next](#next)(t: [table](/docs/luau/tables),lastKey: Variant):Variant,Variant |
| [pairs](#pairs)(t: [table](/docs/luau/tables)):[function](/docs/luau/functions),[table](/docs/luau/tables) |
| [pcall](#pcall)(func: [function](/docs/luau/functions),args: [Tuple](/docs/luau/tuples)):[boolean](/docs/luau/booleans),Variant |
| [print](#print)(params: [Tuple](/docs/luau/tuples)):() |
| [rawequal](#rawequal)(v1: Variant,v2: Variant):[boolean](/docs/luau/booleans) |
| [rawget](#rawget)(t: [table](/docs/luau/tables),index: Variant):Variant |
| [rawlen](#rawlen)(t: [table](/docs/luau/tables)):[table](/docs/luau/tables) |
| [rawset](#rawset)(t: [table](/docs/luau/tables),index: Variant,value: Variant):[table](/docs/luau/tables) |
| [require](#require)(module: [ModuleScript](/docs/reference/engine/classes/ModuleScript) | [string](/docs/luau/strings) | [number](/docs/luau/numbers)):Variant |
| [select](#select)(index: Variant,args: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |
| [setfenv](#setfenv)(f: Variant,fenv: [table](/docs/luau/tables)):Variant  Deprecated |
| [setmetatable](#setmetatable)(t: [table](/docs/luau/tables),newMeta: Variant):[table](/docs/luau/tables) |
| [tonumber](#tonumber)(arg: Variant,base: [number](/docs/luau/numbers)):Variant |
| [tostring](#tostring)(e: Variant):[string](/docs/luau/strings) |
| [type](#type)(v: Variant):[string](/docs/luau/strings) |
| [unpack](#unpack)(list: [table](/docs/luau/tables),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):Variant |
| [xpcall](#xpcall)(f: [function](/docs/luau/functions),err: [function](/docs/luau/functions),args: [Tuple](/docs/luau/tuples)):[boolean](/docs/luau/booleans),Variant |

Properties

|  |
| --- |
| [\_G](#_G):[Array](/docs/luau/tables#arrays) |
| [\_VERSION](#_VERSION):[string](/docs/luau/strings) |

The following is a list of functions and variables that are native to Luau.
These functions can be used in a standard installation of both
[Luau](https://luau.org) and [Lua 5.1.4](https://www.lua.org/manual/5.1/),
though there are some differences in how some of these work on Roblox.

---

API Reference

Functions

assert

Throws an error if the provided value resolves to false or nil.

assert(

value:Variant, errorMessage:[string](/docs/luau/strings)

):Variant

Parameters

|  |
| --- |
| value:Variant  The value that will be asserted against. |
| errorMessage:[string](/docs/luau/strings) Default Value: assertion failed! The text that will be shown in the error if the assertion fails. |

Returns

Variant

Throws an error if the provided value is false or nil. If the
assertion passes, it returns all values passed to it.

```
local product = 90 * 4



assert(product == 360, "Oh dear, multiplication is broken")



-- The line above does nothing, because 90 times 4 is 360
```

Provide feedback

---

collectgarbage

Deprecated

Show details

---

error

Halts thread execution and throws an error.

error(

message:Variant, level:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| message:Variant  The error message to display. |
| level:[number](/docs/luau/numbers) Default Value: 1 The level of information that should be printed. Defaults to 1. |

Returns

()

Terminates the last protected function called and outputs message as an
error message. If the function containing the error is not called in a
protected function such as pcall(), then the script which called the
function will terminate. The error function itself never returns and acts
like a script error.

The level argument specifies how to get the error position. With level
1 (the default), the error position is where the error function was
called. Level 2 points the error to where the function that called error
was called; and so on. Passing a level 0 avoids the addition of error
position information to the message.

Provide feedback

---

gcinfo

Returns the total memory heap size in kilobytes.

gcinfo():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the total memory heap size in kilobytes. The number reflects the
current heap consumption from the operating system perspective, which
fluctuates over time as garbage collector frees objects.

Provide feedback

---

getfenv

Deprecated

Show details

---

getmetatable

Returns the metatable of the given table.

getmetatable(t:Variant):Variant

Parameters

|  |
| --- |
| t:Variant  The object to fetch the metatable of. |

Returns

Variant

Returns the metatable of the given table t if it has one, otherwise
returns nil. If t does have a metatable, and the \_\_metatable
metamethod is set, it returns that value instead.

```
-- Demonstrate getmetatable:



local meta = {}



local t = setmetatable({}, meta)



print(getmetatable(t) == meta) --> true



-- Make the original metatable unrecoverable by setting the __metatable metamethod:



meta.__metatable = "protected"



print(getmetatable(t)) --> protected
```

Provide feedback

---

ipairs

Returns an iterator function and the table for use in a for loop.

ipairs(t:[Array](/docs/luau/tables#arrays)):[function](/docs/luau/functions),[Array](/docs/luau/tables#arrays),[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| t:[Array](/docs/luau/tables#arrays)  A table whose elements are to be iterated over. |

Returns

[function](/docs/luau/functions), [Array](/docs/luau/tables#arrays), [number](/docs/luau/numbers)

Returns three values: an iterator function, the table t and the number
0. Each time the iterator function is called, it returns the next
numerical index-value pair in the table. When used in a generic for-loop,
the return values can be used to iterate over each numerical index in the
table:

```
local fruits = {"apples", "oranges", "kiwi"}



for index, fruit in ipairs(fruits) do



print(index, fruit) --> 1 apples, 2 oranges, 3 kiwi, etc...



end
```

Provide feedback

---

loadstring

Returns the provided code as a function that can be executed.

loadstring(

contents:[string](/docs/luau/strings), chunkname:[string](/docs/luau/strings)

):Variant

Parameters

|  |
| --- |
| contents:[string](/docs/luau/strings)  The specified string to be loaded as Luau code. |
| chunkname:[string](/docs/luau/strings)  An optional chunk name for error messages and debug information. If unspecified, Luau uses the contents string. |

Returns

Variant

Loads Luau code from a string and returns it as a function.

Unlike standard Lua 5.1, Roblox's Luau cannot load the compiled bytecode
using loadstring().

loadstring() is disabled by default. For guidance around enabling it,
see [ServerScriptService](/docs/reference/engine/classes/ServerScriptService).

WARNING: This method disables certain Luau optimizations on the
returned function. Extreme caution should be taken when using
[loadstring()](/docs/reference/engine/globals/LuaGlobals#loadstring); if your intention is to allow users to
run code in your experience, make sure to protect the returned function's
environment by using [getfenv()](/docs/reference/engine/globals/LuaGlobals#getfenv) and
[setfenv()](/docs/reference/engine/globals/LuaGlobals#setfenv).

Provide feedback

---

newproxy

Creates a blank userdata, with the option for it to have a metatable.

newproxy(addMetatable:[boolean](/docs/luau/booleans)):[userdata](/docs/luau/userdata)

Parameters

|  |
| --- |
| addMetatable:[boolean](/docs/luau/booleans) Default Value: false |

Returns

[userdata](/docs/luau/userdata)

Creates a blank userdata, with the option for it to have a metatable.

Provide feedback

---

next

An iterator function for use in for loops.

next(

t:[table](/docs/luau/tables), lastKey:Variant

):Variant,Variant

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The array to be traversed. |
| lastKey:Variant Default Value: nil The last key that was previously retrieved from a call to next. |

Returns

Variant, Variant

Returns the first key/value pair in the array. If a lastKey argument was
specified then returns the next element in the array based on the key that
provided. The order in which the indices are enumerated is not specified,
even for numeric indices. To traverse a table in numeric order, use a
numerical for loop or ipairs.

The behavior of next is undefined if, during the traversal, you assign any
value to a non-existent field in the table. You may, however, modify
existing fields. In particular, you may clear existing fields.

Provide feedback

---

pairs

Returns an iterator function and the provided table for use in a for
loop.

pairs(t:[table](/docs/luau/tables)):[function](/docs/luau/functions),[table](/docs/luau/tables)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  An array or dictionary table to iterate over. |

Returns

[function](/docs/luau/functions), [table](/docs/luau/tables)

Returns an iterator function, the passed table t, and nil, so that the
construction will iterate over all key/value pairs of that table when used
in a generic for loop:

```
local scores = {



["John"] = 5,



["Sally"] = 10



}



for name, score in pairs(scores) do



print(name .. " has score: " .. score)



end
```

Provide feedback

---

pcall

Runs the provided function and catches any error it throws, returning the
function's success and its results.

pcall(

func:[function](/docs/luau/functions), args:[Tuple](/docs/luau/tuples)

):[boolean](/docs/luau/booleans),Variant

Parameters

|  |
| --- |
| func:[function](/docs/luau/functions)  The function to be called in protected mode. |
| args:[Tuple](/docs/luau/tuples)  The arguments to send to func when executing. |

Returns

[boolean](/docs/luau/booleans), Variant

Calls the function func with the given arguments in protected mode. This
means that any error inside func is not propagated; instead, pcall()
catches the error and returns a status code. Its first result is the
status code (a boolean), which is true if the call succeeds without
errors. In such case, pcall() also returns all results from the call,
after this first result. In case of any error, pcall() returns false
plus the error message.

```
local function divideByFive(n: number): number



return n / 5



end



local success, errorMessage = pcall(divideByFive, "notANumber")  -- Results in error...



if success then



-- Handle successful response...



else



warn("Error message:", errorMessage)



end
```

Provide feedback

---

print

Prints all provided values to the output.

print(params:[Tuple](/docs/luau/tuples)):()

Parameters

|  |
| --- |
| params:[Tuple](/docs/luau/tuples)  Any number of arguments to be outputted. |

Returns

()

Receives any number of arguments, and prints their values to the output.
print is not intended for formatted output, but only as a quick way to
show a value, typically for debugging. For a formatted output, use
[string.format()](/docs/reference/engine/libraries/string#format). On Roblox, print does not call tostring,
but the \_\_tostring metamethod still fires if the table has one.

Provide feedback

---

rawequal

Returns whether v1 is equal to v2, bypassing their metamethods.

rawequal(

v1:Variant, v2:Variant

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| v1:Variant  The first variable to compare. |
| v2:Variant  The second variable to compare. |

Returns

[boolean](/docs/luau/booleans)

Checks whether v1 is equal to v2, without invoking any metamethods.

Provide feedback

---

rawget

Gets the real value of table[index], bypassing any metamethods.

rawget(

t:[table](/docs/luau/tables), index:Variant

):Variant

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The table to be referenced. |
| index:Variant  The index to get from t. |

Returns

Variant

Gets the real value of table[index], without invoking any metamethods.

Provide feedback

---

rawlen

Returns the length of the string or table, bypassing any metamethods.

rawlen(t:[table](/docs/luau/tables)):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The table to be referenced. |

Returns

[table](/docs/luau/tables)

Returns the length of the string or table, without invoking any
metamethods.

Provide feedback

---

rawset

Sets the real value of table[index], bypassing any metamethods.

rawset(

t:[table](/docs/luau/tables), index:Variant, value:Variant

):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The table to be referenced. |
| index:Variant  The index to set in t to a specified value. Must be different from nil. |
| value:Variant  The value to be set to a specified index in table t. |

Returns

[table](/docs/luau/tables)

Sets the real value of table[index] to a given value, without invoking
any metamethod.

Provide feedback

---

require

Returns the value that was returned by the given ModuleScript, running it
if it has not been run yet.

require(module:[ModuleScript](/docs/reference/engine/classes/ModuleScript) | [string](/docs/luau/strings) | [number](/docs/luau/numbers)):Variant

Parameters

|  |
| --- |
| module:[ModuleScript](/docs/reference/engine/classes/ModuleScript) | [string](/docs/luau/strings) | [number](/docs/luau/numbers)  The [ModuleScript](/docs/reference/engine/classes/ModuleScript) that will be executed to retrieve the return value it provides, or a reference to one (a string path or asset ID). |

Returns

Variant

What the [ModuleScript](/docs/reference/engine/classes/ModuleScript) returned (usually a table or a
function).

Runs the supplied [ModuleScript](/docs/reference/engine/classes/ModuleScript) and returns what the
[ModuleScript](/docs/reference/engine/classes/ModuleScript) returned (usually a table or a function). If the
[ModuleScript](/docs/reference/engine/classes/ModuleScript) has not been run yet, it will be executed.

If a string path is provided instead, it is first resolved to a
[ModuleScript](/docs/reference/engine/classes/ModuleScript) relative to the script that called
[require()](/docs/reference/engine/globals/LuaGlobals#require), mimicking the Unix-like semantics of Luau's
require() expression.

Specifically, require-by-string's resolution semantics are as follows:

* Paths with the ./ prefix begin resolution at script.Parent.
* Paths with the ../ prefix begin resolution at script.Parent.Parent.
* Paths with the @self/ prefix begin resolution at script.
* Each non-prefix component in a given path corresponds to a child
  instance of the previous component. The exception to this is the ..
  component, which corresponds to the parent of the previous component.
* If the desired [ModuleScript](/docs/reference/engine/classes/ModuleScript) is not present at the time that
  [require()](/docs/reference/engine/globals/LuaGlobals#require) is called, the call will fail and throw an
  error. In other words, require-by-string is non-blocking: it does not
  implicitly wait for a [ModuleScript](/docs/reference/engine/classes/ModuleScript) to be created.

To illustrate this, each pair of [require()](/docs/reference/engine/globals/LuaGlobals#require) expressions
in the example below contains two functionally equivalent calls. Redundant
parentheses have been added to clarify exactly how each path component
maps onto an instance.

```
-- "./" prefix is equivalent to script.Parent



require("./MySibling")



require((script.Parent).(MySibling))



-- "../" prefix is equivalent to script.Parent.Parent



require("../SiblingOfMyParent")



require((script.Parent.Parent).(SiblingOfMyParent))



-- "../" can be chained to go up multiple levels



require("../../SiblingOfMyGrandparent")



require((script.Parent.Parent).(Parent).(SiblingOfMyGrandparent))



-- "@self" prefix corresponds to the script itself



require("@self/MyChild")



require((script).(MyChild))
```

Once the return object is created by an initial
[require()](/docs/reference/engine/globals/LuaGlobals#require) call of a [ModuleScript](/docs/reference/engine/classes/ModuleScript), future
[require()](/docs/reference/engine/globals/LuaGlobals#require) calls for the same [ModuleScript](/docs/reference/engine/classes/ModuleScript) (on
the same side of the client-server boundary) will not run the code again.
Instead, a reference to the same return object created by the initial
[require()](/docs/reference/engine/globals/LuaGlobals#require) call will be supplied. This behavior allows
for the sharing of values across different scripts, as multiple
[require()](/docs/reference/engine/globals/LuaGlobals#require) calls from different scripts will reference
the same returned object. If the returned object is a table, any values
stored within the table are shared and accessible by any script requiring
that [ModuleScript](/docs/reference/engine/classes/ModuleScript).

As noted above, the "object sharing" behavior does not cross the
client-server boundary. This means that if a [ModuleScript](/docs/reference/engine/classes/ModuleScript) is
accessible to both the client and server (such as by being placed in
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage)) and [require()](/docs/reference/engine/globals/LuaGlobals#require) is called
from both a [LocalScript](/docs/reference/engine/classes/LocalScript) as well as a [Script](/docs/reference/engine/classes/Script), the code in
the [ModuleScript](/docs/reference/engine/classes/ModuleScript) will be run twice, and the [LocalScript](/docs/reference/engine/classes/LocalScript)
will receive a distinct return object from the one received by the
[Script](/docs/reference/engine/classes/Script).

Also note that if the [ModuleScript](/docs/reference/engine/classes/ModuleScript) the user wants to run has been
uploaded to Roblox (with the instance's name being MainModule), it can
be loaded by using the [require()](/docs/reference/engine/globals/LuaGlobals#require) function on the asset
ID of the [ModuleScript](/docs/reference/engine/classes/ModuleScript), though only on the server.

Provide feedback

---

select

Returns all arguments after the given index.

select(

index:Variant, args:[Tuple](/docs/luau/tuples)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| index:Variant  The index of the argument to return all arguments after in args. If it's set to "#", the number of arguments that were passed after it is returned. |
| args:[Tuple](/docs/luau/tuples)  A tuple of arguments. |

Returns

[Tuple](/docs/luau/tuples)

Returns all arguments after argument number index. If negative, it will
return from the end of the argument list.

```
print(select(2, "A", "B", "C")) --> B C



print(select(-1, "A", "B", "C")) --> C
```

If the index argument is set to "#", the number of arguments that were
passed after it is returned.

```
print(select("#", "A", "B", "C")) --> 3
```

Provide feedback

---

setfenv

Deprecated

Show details

---

setmetatable

Sets the given table's metatable.

setmetatable(

t:[table](/docs/luau/tables), newMeta:Variant

):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The table to set the metatable of. |
| newMeta:Variant  If nil, the metatable of the given table t is removed. Otherwise, the metatable to set for the given table t. |

Returns

[table](/docs/luau/tables)

Sets the metatable for the given table t to newMeta. If newMeta is
nil, the metatable of t is removed. Finally, this function returns the
table t which was passed to it. If t already has a metatable whose
\_\_metatable metamethod is set, calling this on t raises an error.

```
local meta = {__metatable = "protected"}



local t = {}



setmetatable(t, meta) -- This sets the metatable of t



-- We now have a table, t, with a metatable. If we try to change it...



setmetatable(t, {}) --> Error: cannot change a protected metatable
```

Provide feedback

---

tonumber

Returns the provided value converted to a number, or nil if impossible.

tonumber(

arg:Variant, base:[number](/docs/luau/numbers)

):Variant

Parameters

|  |
| --- |
| arg:Variant  The object to be converted into a number. |
| base:[number](/docs/luau/numbers) Default Value: 10 The numerical base to convert arg into. |

Returns

Variant

Attempts to convert the arg into a number with a specified base to
interpret the value in. If it cannot be converted, this function returns
nil.

The base may be any integer between 2 and 36, inclusive. In bases above
10, the letter 'A' (in either upper or lower case) represents 10, 'B'
represents 11, and so forth, with 'Z' representing 35. In base 10 (the
default), the number may have a decimal part, as well as an optional
exponent part. In other bases, only unsigned integers are accepted.

If a string begins with 0x and a base is not provided, the 0x is
trimmed and the base is assumed to be 16, or hexadecimal.

```
print(tonumber("1337")) --> 1337 (assumes base 10, decimal)



print(tonumber("1.25")) --> 1.25 (base 10 may have decimal portions)



print(tonumber("3e2")) --> 300 (base 10 may have exponent portion, 3 &times; 10 ^ 2)



print(tonumber("25", 8)) --> 21 (base 8, octal)



print(tonumber("0x100")) --> 256 (assumes base 16, hexadecimal)



print(tonumber("roblox")) --> nil (does not raise an error)



-- Tip: use with assert if you would like unconvertable numbers to raise an error



print(assert(tonumber("roblox"))) --> Error: assertion failed
```

Provide feedback

---

tostring

Returns the provided value converted to a string, or nil if impossible.

tostring(e:Variant):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| e:Variant  The object to be converted into a string. |

Returns

[string](/docs/luau/strings)

Receives an argument of any type and converts it to a string in a
reasonable format. For complete control of how numbers are converted, use
string.format. If the metatable of e has a \_\_tostring metamethod, then
it will be called with e as the only argument and will return the
result.

```
local isRobloxCool = true



-- Convert the boolean to a string then concatenate:



print("Roblox is cool: " .. tostring(isRobloxCool)) --> Roblox is cool: true
```

Provide feedback

---

type

Returns the basic type of the provided object.

type(v:Variant):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| v:Variant  The object to return the type of. |

Returns

[string](/docs/luau/strings)

Returns the type of its only argument, coded as a string. The possible
results of this function are "nil" (a string, not the value nil),
"number", "string", "boolean", "table", "vector", "function",
"thread", "userdata", and "buffer". The buffer and vector
primitives are additions from Luau, not from Lua.

Provide feedback

---

unpack

Returns all elements from the given list as a tuple.

unpack(

list:[table](/docs/luau/tables), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):Variant

Parameters

|  |
| --- |
| list:[table](/docs/luau/tables)  The list of elements to be unpacked. |
| i:[number](/docs/luau/numbers) Default Value: 1 The index of the first element to unpack. |
| j:[number](/docs/luau/numbers) Default Value: #list The index of the last element to unpack. |

Returns

Variant

Returns the elements from the given table. By default, i is 1 and j is
the length of list, as defined by the length operator.

Provide feedback

---

xpcall

Similar to [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) except it uses a custom error
handler.

xpcall(

f:[function](/docs/luau/functions), err:[function](/docs/luau/functions), args:[Tuple](/docs/luau/tuples)

):[boolean](/docs/luau/booleans),Variant

Parameters

|  |
| --- |
| f:[function](/docs/luau/functions)  The function to be called in protected mode. |
| err:[function](/docs/luau/functions)  The function to be used as an error handle if xpcall catches an error. |
| args:[Tuple](/docs/luau/tuples) |

Returns

[boolean](/docs/luau/booleans), Variant

This function is similar to [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall), except that you
can set a new error handler.

xpcall() calls function f in protected mode, using err as the error
handler, and passes a list of arguments. Any error inside f is not
propagated; instead, xpcall() catches the error, calls the err
function with the original error object, and returns a status code. Its
first result is the status code (a boolean), which is true if the call
succeeds without errors. In this case, xpcall() also returns all results
from the call, after this first result. In case of any error, xpcall()
returns false plus the result from err.

Unlike [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall), the err function preserves the stack
trace of function f, which can be inspected using [debug.info()](/docs/reference/engine/libraries/debug#info)
or [debug.traceback()](/docs/reference/engine/libraries/debug#traceback).

Provide feedback

---

Properties

\_G

A table that is shared between all scripts of the same context level.

\_G:[Array](/docs/luau/tables#arrays)

A table that is shared between all scripts of the same context level.

Provide feedback

---

\_VERSION

A global variable that holds a string containing the current interpreter
version.

\_VERSION:[string](/docs/luau/strings)

A global variable (not a function) that holds a string containing the
current interpreter version.

Provide feedback

---