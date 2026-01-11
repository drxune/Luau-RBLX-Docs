# coroutine | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/coroutine
Scraped: 2026-01-11T02:49:48.604652Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [coroutine](/docs/reference/engine/libraries/coroutine)

English

Feedback

Engine Library

coroutine

A function that executes alongside the main thread.

---

Summary

Functions

|  |
| --- |
| [close](#close)(co: [coroutine](/docs/reference/engine/libraries/coroutine)):[boolean](/docs/luau/booleans),Variant<[string](/docs/luau/strings), ()> |
| [create](#create)(f: [function](/docs/luau/functions)):[coroutine](/docs/reference/engine/libraries/coroutine) |
| [isyieldable](#isyieldable)():[boolean](/docs/luau/booleans) |
| [resume](#resume)(co: [coroutine](/docs/reference/engine/libraries/coroutine),...: Variant):[boolean](/docs/luau/booleans),Variant<[Tuple](/docs/luau/tuples), [string](/docs/luau/strings)> |
| [running](#running)():[coroutine](/docs/reference/engine/libraries/coroutine) |
| [status](#status)(co: [coroutine](/docs/reference/engine/libraries/coroutine)):[string](/docs/luau/strings) |
| [wrap](#wrap)(f: [function](/docs/luau/functions)):[function](/docs/luau/functions) |
| [yield](#yield)(...: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples)<Variant> |

A coroutine is used to perform multiple tasks at the same time from within
the same script. Such tasks might include producing values from inputs or
performing work on a subroutine when solving a larger problem. A task doesn't
even need to have a defined ending point, but it does need to define
particular times at which it yields (pause) to let other things be worked
on.

Using Coroutines
----------------

A new coroutine can be created by providing a function to
[coroutine.create()](/docs/reference/engine/libraries/coroutine#create). Once created, a coroutine doesn't begin running
until the first call to [coroutine.resume()](/docs/reference/engine/libraries/coroutine#resume) which passes the
arguments to the function. This call returns when the function either halts or
calls [coroutine.yield()](/docs/reference/engine/libraries/coroutine#yield) and, when this happens,
[coroutine.resume()](/docs/reference/engine/libraries/coroutine#resume) returns either the values returned by the
function, the values sent to [coroutine.yield()](/docs/reference/engine/libraries/coroutine#yield), or an error message.
If it does error, the second return value is the thrown error.

```
local function task(...)



-- This function might do some work for a bit then yield some value



coroutine.yield("first")  -- To be returned by coroutine.resume()



-- The function continues once it is resumed again



return "second"



end



local taskCoro = coroutine.create(task)



-- Call resume for the first time, which runs the function from the beginning



local success, result = coroutine.resume(taskCoro, ...)



print(success, result)  --> true, first (task called coroutine.yield())



-- Continue running the function until it yields or halts



success, result = coroutine.resume(taskCoro)



print(success, result)  --> true, second (task halted because it returned "second")
```

During the lifetime of the coroutine, you can call
[coroutine.status()](/docs/reference/engine/libraries/coroutine#status) to inspect its status:

| Status | Meaning |
| --- | --- |
| **suspended** | The coroutine is waiting to be resumed. Coroutines begin in this state and enter it when their function calls coroutine.yield(). |
| **running** | The coroutine is running right now. |
| **normal** | The coroutine is awaiting the yield of another coroutine; in other words, it has resumed another coroutine. |
| **dead** | The function has halted (returned or thrown an error). The coroutine cannot be used further. |

### Wrapping Coroutines

When working with coroutines, you can also forgo the use of the coroutine
object and instead use a wrapper function. Such a wrapper function will resume
a particular coroutine when it is called and will return only the yielded
values. You can do this using [coroutine.wrap()](/docs/reference/engine/libraries/coroutine#wrap):

```
-- Create coroutine and return a wrapper function that resumes it



local f = coroutine.wrap(task)



-- Resume the coroutine as if we called coroutine.resume()



local result = f()



-- If an error occurs it will be raised here!



-- This differs from coroutine.resume() which acts similar to pcall()
```

The first value returned from [coroutine.resume()](/docs/reference/engine/libraries/coroutine#resume) describes whether a
coroutine ran without errors. However, functions returned by
[coroutine.wrap()](/docs/reference/engine/libraries/coroutine#wrap) will not do this: instead they directly return the
values returned or passed to [coroutine.yield()](/docs/reference/engine/libraries/coroutine#yield), if any. Should an
error have occurred while running the coroutine function, the error is raised
on the call of the returned function.

### Producer Pattern Example

Imagine a task that produces repetitions of a word: each time it produces a
repetition, the next one will produce one more. For example, providing Hello
will produce Hello, HelloHello, HelloHelloHello, etc. To do this, you
can define repeatThis():

```
-- This function repeats a word every time its coroutine is resumed



local function repeatThis(word)



local repetition = ""



while true do



-- Do one repetition then yield the result



repetition = repetition .. word



coroutine.yield(repetition)



end



end
```

To run this function as a coroutine, you can use [coroutine.create()](/docs/reference/engine/libraries/coroutine#create)
followed by multiple calls to [coroutine.resume()](/docs/reference/engine/libraries/coroutine#resume):

```
local repetitionCoro = coroutine.create(repeatThis)



print(coroutine.resume(repetitionCoro, "Hello"))  -- true, Hello



print(coroutine.resume(repetitionCoro))           -- true, HelloHello



print(coroutine.resume(repetitionCoro))           -- true, HelloHelloHello
```

For this producer function, you can also use [coroutine.wrap()](/docs/reference/engine/libraries/coroutine#wrap) to get
a function that produces values:

```
local f = coroutine.wrap(repeatThis)



print(f("Hello"))  -- Hello



print(f())         -- HelloHello



print(f())         -- HelloHelloHello
```

---

API Reference

Functions

close

Closes and puts the provided coroutine in a dead state.

coroutine.close(co:[coroutine](/docs/reference/engine/libraries/coroutine)):[boolean](/docs/luau/booleans),Variant<[string](/docs/luau/strings), ()>

Parameters

|  |
| --- |
| co:[coroutine](/docs/reference/engine/libraries/coroutine) |

Returns

[boolean](/docs/luau/booleans), Variant<[string](/docs/luau/strings), ()>

true unless the coroutine being closed is in an error state.

The error message, if any.

Closes and puts the provided coroutine in a dead state. This function
returns true unless the coroutine is in an error state, in which case it
returns false and the error message. A coroutine that is currently
running cannot be closed. A coroutine cannot be resumed after it is
closed.

Provide feedback

---

create

Creates a new coroutine, with body f. f must be a Luau function.

coroutine.create(f:[function](/docs/luau/functions)):[coroutine](/docs/reference/engine/libraries/coroutine)

Parameters

|  |
| --- |
| f:[function](/docs/luau/functions) |

Returns

[coroutine](/docs/reference/engine/libraries/coroutine)

Creates a new coroutine, with body f. f must be a Luau function.

Provide feedback

---

isyieldable

Returns true if the coroutine this function is called within can safely
yield.

coroutine.isyieldable():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether or not the coroutine can safely yield at this point.

Returns true if the coroutine this function is called within can safely
yield. Yielding a coroutine inside metamethods or C functions is
prohibited, with the exception of pcall and xpcall.

Provide feedback

---

resume

Starts or continues the execution of coroutine co.

coroutine.resume(

co:[coroutine](/docs/reference/engine/libraries/coroutine), ...:Variant

):[boolean](/docs/luau/booleans),Variant<[Tuple](/docs/luau/tuples), [string](/docs/luau/strings)>

Parameters

|  |
| --- |
| co:[coroutine](/docs/reference/engine/libraries/coroutine) |
| ...:Variant |

Returns

[boolean](/docs/luau/booleans), Variant<[Tuple](/docs/luau/tuples), [string](/docs/luau/strings)>

Starts or continues the execution of coroutine co. The first time you
resume a coroutine, it starts running its body. The values ... are
passed as the arguments to the body function. If the coroutine has
yielded, resume restarts it; the values ... are passed as the results
from the yield. If the coroutine runs without any errors, resume returns
true plus any values passed to yield (if the coroutine yields) or any
values returned by the body function (if the coroutine terminates). If
there is any error, resume returns false plus the error message.

Provide feedback

---

running

Returns the running coroutine.

coroutine.running():[coroutine](/docs/reference/engine/libraries/coroutine)

Returns

[coroutine](/docs/reference/engine/libraries/coroutine)

Returns the running coroutine.

Provide feedback

---

status

Returns the status of coroutine co as a string.

coroutine.status(co:[coroutine](/docs/reference/engine/libraries/coroutine)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| co:[coroutine](/docs/reference/engine/libraries/coroutine) |

Returns

[string](/docs/luau/strings)

Returns the status of coroutine co, as a string: 'running', if the
coroutine is running (that is, it called status); 'suspended', if the
coroutine is suspended in a call to yield, or if it has not started
running yet; 'normal' if the coroutine is active but not running (that is,
it has resumed another coroutine); and 'dead' if the coroutine has
finished its body function, or if it has stopped with an error.

Provide feedback

---

wrap

Creates a new coroutine and returns a function that, when called, resumes
the coroutine.

coroutine.wrap(f:[function](/docs/luau/functions)):[function](/docs/luau/functions)

Parameters

|  |
| --- |
| f:[function](/docs/luau/functions) |

Returns

[function](/docs/luau/functions)

Creates a new coroutine, with body f. f must be a Luau function. Returns a
function that resumes the coroutine each time it is called. Any arguments
passed to the function behave as the extra arguments to resume. Returns
the same values returned by resume, except the first boolean. In case of
error, propagates the error.

Provide feedback

---

yield

Suspends execution of the coroutine.

coroutine.yield(...:[Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples)<Variant>

Parameters

|  |
| --- |
| ...:[Tuple](/docs/luau/tuples) |

Returns

[Tuple](/docs/luau/tuples)<Variant>

Suspends the execution of the calling coroutine. Any arguments to yield
are passed as extra results to resume. Yielding a coroutine inside
metamethods or C functions is prohibited, with the exception of pcall
and xpcall.

Provide feedback

---