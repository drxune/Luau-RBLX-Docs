# debug | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/debug
Scraped: 2026-01-11T02:49:52.909851Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [debug](/docs/reference/engine/libraries/debug)

English

Feedback

Engine Library

debug

This library provides functions useful for debugging and profiling code.

---

Summary

Functions

|  |
| --- |
| [traceback](#traceback)(message: [string](/docs/luau/strings),level: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [traceback](#traceback-thread-mes)(thread: [coroutine](/docs/reference/engine/libraries/coroutine),message: [string](/docs/luau/strings),level: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [info](#info)(level: [number](/docs/luau/numbers),options: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [info](#info-function-o)(function: [function](/docs/luau/functions),options: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [info](#info-thread-lev)(thread: [coroutine](/docs/reference/engine/libraries/coroutine),level: [number](/docs/luau/numbers),options: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [profilebegin](#profilebegin)(label: [string](/docs/luau/strings)):() |
| [profileend](#profileend)():() |
| [getmemorycategory](#getmemorycategory)():[string](/docs/luau/strings) |
| [setmemorycategory](#setmemorycategory)(tag: [string](/docs/luau/strings)):[string](/docs/luau/strings) |
| [resetmemorycategory](#resetmemorycategory)():() |
| [dumpcodesize](#dumpcodesize)():() |

Provides a few basic functions for debugging code in Roblox. Unlike the
[debug](/docs/reference/engine/libraries/debug) library found in Lua natively, this version has been heavily
sandboxed.

---

API Reference

Functions

traceback

Returns a string of undefined format that describes the current function
call stack.

debug.traceback(

message:[string](/docs/luau/strings), level:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings)  The first line of the returned string. |
| level:[number](/docs/luau/numbers) Default Value: 1 The number of calls "up" the call stack to return. |

Returns

[string](/docs/luau/strings)

Traceback of the current function call stack.

Returns a traceback of the current function call stack as a string; in
other words, a description of the functions that have been called up to
this point. During debugging, this behaves like an error stack trace but
does not stop execution of the script.

The level parameter specifies what level of the call stack to consider,
with 1 being the call of [debug.traceback()](/docs/reference/engine/libraries/debug#traceback) itself, 2 being
the call of the function calling [debug.traceback()](/docs/reference/engine/libraries/debug#traceback), and so on.
See the code sample below for an example of sequential function calls.

Note that this function will often return inaccurate results (compared to
the original source code) and that the format of the returned traceback
may change at any time. You should not parse the return value for
specific information such as script names or line numbers.

The following example includes sequential function calls; fnB() is
called, and it calls fnA() which then calls [debug.traceback()](/docs/reference/engine/libraries/debug#traceback).

```
local function fnA()



print(debug.traceback("Specific moment during fnA()"))



end



local function fnB()



fnA()



end



-- Call function fnB() to begin traceback



fnB()
```

Provide feedback

---

traceback

Returns a string of undefined format that describes the current function
call stack.

debug.traceback(

thread:[coroutine](/docs/reference/engine/libraries/coroutine), message:[string](/docs/luau/strings), level:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| thread:[coroutine](/docs/reference/engine/libraries/coroutine)  A thread as returned by [coroutine.create()](/docs/reference/engine/libraries/coroutine#create). |
| message:[string](/docs/luau/strings)  The first line of the returned string. |
| level:[number](/docs/luau/numbers) Default Value: 1 The number of calls "up" the call stack to return. |

Returns

[string](/docs/luau/strings)

Traceback of the current function call stack.

Returns a traceback of the current function call stack as a string; in
other words, a description of the functions that have been called up to
this point. During debugging, this behaves like an error stack trace but
does not stop execution of the script.

The level parameter specifies what level of the call stack to consider,
with 1 being the call of [debug.traceback()](/docs/reference/engine/libraries/debug#traceback) itself, 2 being
the call of the function calling [debug.traceback()](/docs/reference/engine/libraries/debug#traceback), and so on.
See the code sample below for an example of sequential function calls.

Note that this function will often return inaccurate results (compared to
the original source code) and that the format of the returned traceback
may change at any time. You should not parse the return value for
specific information such as script names or line numbers.

The following example includes sequential function calls; fnB() is
called, and it calls fnA() which then calls [debug.traceback()](/docs/reference/engine/libraries/debug#traceback).

```
local function fnA()



print(debug.traceback("Specific moment during fnA()"))



end



local function fnB()



fnA()



end



-- Call function fnB() to begin traceback



fnB()
```

Provide feedback

---

info

Traverses the entire stack of current thread and returns a string
containing the call stack of target level details.

debug.info(

level:[number](/docs/luau/numbers), options:[string](/docs/luau/strings)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| level:[number](/docs/luau/numbers)  Determines at what level of the call stack the information returned should describe. A value of 1 represents the function which is calling [debug.info()](/docs/reference/engine/libraries/debug#info), a value of 2 represents the function that called that function, and so on. |
| options:[string](/docs/luau/strings)  A string that describes what the returned information should represent. It must only contain 0 or 1 instances of the characters slnaf, each representing a piece of information:   * s ([string](/docs/luau/strings)) — The function source identifier,   equal to the full name of the script the function is defined in. * l ([number](/docs/luau/numbers)) — The line number of the function   call represented by level. * n ([string](/docs/luau/strings)) — The name of the function; may be   nil for anonymous functions and C functions without an assigned   debug name. * a ([number](/docs/luau/numbers), [boolean](/docs/luau/booleans)) —   Arity of the function, which refers to the parameter count and   whether the function is variadic. * f ([function](/docs/luau/functions)) — The function which was   inspected. |

Returns

[Tuple](/docs/luau/tuples)

Allows programmatic inspection of the call stack. This function differs
from [debug.traceback()](/docs/reference/engine/libraries/debug#traceback) in that it guarantees the format of the
data it returns. This is useful for general logging and filtering purposes
as well as for sending the data to systems expecting structured input,
such as crash aggregation.

```
local function fnA()



-- Output source identifier ("s") and line ("l") at levels 1 and 2



print(debug.info(1, "sl"))  --> fnA() 3



print(debug.info(2, "sl"))  --> fnA() 7



end



fnA()
```

Note that this function is similar to
[debug.getinfo](https://www.lua.org/pil/23.1.html), an unavailable part of
the standard Lua library which serves a similar purpose.

Provide feedback

---

info

Traverses the entire stack of current thread and returns a string
containing the call stack of target function details.

debug.info(

function:[function](/docs/luau/functions), options:[string](/docs/luau/strings)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| function:[function](/docs/luau/functions)  The function of the call stack which the information returned should describe. |
| options:[string](/docs/luau/strings)  A string that describes what the returned information should represent. It must only contain 0 or 1 instances of the characters slnaf, each representing a piece of information:   * s ([string](/docs/luau/strings)) — The function source identifier,   equal to the full name of the script the function is defined in. * l ([number](/docs/luau/numbers)) — The line that function is   defined on. * n ([string](/docs/luau/strings)) — The name of the function; may be   nil for anonymous functions and C functions without an assigned   debug name. * a ([number](/docs/luau/numbers), [boolean](/docs/luau/booleans)) —   Arity of the function, which refers to the parameter count and   whether the function is variadic. * f ([function](/docs/luau/functions)) — The function which was   inspected. |

Returns

[Tuple](/docs/luau/tuples)

Allows programmatic inspection of the call stack. This function differs
from [debug.traceback()](/docs/reference/engine/libraries/debug#traceback) in that it guarantees the format of the
data it returns. This is useful for general logging and filtering purposes
as well as for sending the data to systems expecting structured input,
such as crash aggregation.

```
local function fnA()



end



local function fnB()



end



-- Output line ("l"), name ("n"), and identifier ("f") for both fnA() and fnB()



print(debug.info(fnA, "lnf"))  --> 1 fnA function: 0x75e3d3c398a81252



print(debug.info(fnB, "lnf"))  --> 5 fnB function: 0x6022a6dc5ccf4ab2
```

Note that this function is similar to
[debug.getinfo](https://www.lua.org/pil/23.1.html), an unavailable part of
the standard Lua library which serves a similar purpose.

Provide feedback

---

info

Traverses the entire stack of target thread and returns a string
containing the call stack of target level details.

debug.info(

thread:[coroutine](/docs/reference/engine/libraries/coroutine), level:[number](/docs/luau/numbers), options:[string](/docs/luau/strings)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| thread:[coroutine](/docs/reference/engine/libraries/coroutine)  A thread as returned by [coroutine.create()](/docs/reference/engine/libraries/coroutine#create). |
| level:[number](/docs/luau/numbers)  Determines at what level of the call stack the information returned should describe. A value of 1 represents the function which is calling [debug.info()](/docs/reference/engine/libraries/debug#info), a value of 2 represents the function that called that function, and so on. |
| options:[string](/docs/luau/strings)  A string that describes what the returned information should represent. It must only contain 0 or 1 instances of the characters slnaf, each representing a piece of information:   * s ([string](/docs/luau/strings)) — The function source identifier,   equal to the full name of the script the function is defined in. * l ([number](/docs/luau/numbers)) — The line number of the function   call represented by level. * n ([string](/docs/luau/strings)) — The name of the function; may be   nil for anonymous functions and C functions without an assigned   debug name. * a ([number](/docs/luau/numbers), [boolean](/docs/luau/booleans)) —   Arity of the function, which refers to the parameter count and   whether the function is variadic. * f ([function](/docs/luau/functions)) — The function which was   inspected. |

Returns

[Tuple](/docs/luau/tuples)

Allows programmatic inspection of the call stack. This function differs
from [debug.traceback()](/docs/reference/engine/libraries/debug#traceback) in that it guarantees the format of the
data it returns. This is useful for general logging and filtering purposes
as well as for sending the data to systems expecting structured input,
such as crash aggregation.

```
local function fnA()



-- Output source identifier ("s") and line ("l") at levels 1 and 2



print(debug.info(1, "sl"))  --> fnA() 3



print(debug.info(2, "sl"))  --> fnA() 7



end



fnA()
```

Note that this function is similar to
[debug.getinfo](https://www.lua.org/pil/23.1.html), an unavailable part of
the standard Lua library which serves a similar purpose.

Provide feedback

---

profilebegin

Starts profiling for a label.

debug.profilebegin(label:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| label:[string](/docs/luau/strings)  The text that this [MicroProfiler](/docs/studio/microprofiler) label displays. |

Returns

()

Starts profiling for a
[MicroProfiler](/docs/studio/microprofiler) label.

Provide feedback

---

profileend

Stops profiling for the most recent label that
[debug.profilebegin()](/docs/reference/engine/libraries/debug#profilebegin) opened.

debug.profileend():()

Returns

()

Stops profiling for the most recent
[MicroProfiler](/docs/studio/microprofiler) label that
[debug.profilebegin()](/docs/reference/engine/libraries/debug#profilebegin) opened.

Provide feedback

---

getmemorycategory

Returns the name of the current thread's active memory category.

debug.getmemorycategory():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

The current thread's active memory category.

Returns the name of the current thread's active memory category.

Provide feedback

---

setmemorycategory

Assigns a custom tag to the current thread's memory category.

debug.setmemorycategory(tag:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings) |

Returns

[string](/docs/luau/strings)

The current thread's previous memory category.

Assigns a custom tag name to the current thread's memory category in the
[Developer Console](/docs/studio/developer-console). Useful for
analyzing memory usage of multiple threads in the same script which would
otherwise be grouped together under the same tag/name. Returns the name of
the current thread's previous memory category.

Provide feedback

---

resetmemorycategory

Resets the tag assigned by [debug.setmemorycategory()](/docs/reference/engine/libraries/debug#setmemorycategory) to the
automatically assigned value (typically, the script name).

debug.resetmemorycategory():()

Returns

()

Resets the tag assigned by [debug.setmemorycategory()](/docs/reference/engine/libraries/debug#setmemorycategory) to the
automatically assigned value (typically, the script name).

Provide feedback

---

dumpcodesize

Displays a table of native code size of individual functions and scripts.

debug.dumpcodesize():()

Returns

()

Displays a table of native code size of individual functions and scripts.
This function is only available in the Command Bar in Studio. More details
can be found on the
[Native Code Generation](/docs/luau/native-code-gen) page.

Provide feedback

---