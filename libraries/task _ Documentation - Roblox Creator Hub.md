# task | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/task
Scraped: 2026-01-11T02:49:43.323012Z

## Inherits
- Heartbeat
- Actor
- ModuleScripts
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [task](/docs/reference/engine/libraries/task)

English

Feedback

Engine Library

task

Allows for functions and threads to be coordinated with the engine's
scheduler.

---

Summary

Functions

|  |
| --- |
| [spawn](#spawn)(functionOrThread: [function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine),...: Variant):[coroutine](/docs/reference/engine/libraries/coroutine) |
| [defer](#defer)(functionOrThread: [function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine),...: Variant):[coroutine](/docs/reference/engine/libraries/coroutine) |
| [delay](#delay)(duration: [number](/docs/luau/numbers),functionOrThread: [function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine),...: Variant):[coroutine](/docs/reference/engine/libraries/coroutine) |
| [desynchronize](#desynchronize)():() |
| [synchronize](#synchronize)():() |
| [wait](#wait)(duration: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [cancel](#cancel)(thread: [coroutine](/docs/reference/engine/libraries/coroutine)):() |

The task library allows for functions and threads to be scheduled with the
engine's scheduler.

The functions available in this library generally support functions and
threads. In most cases using a function is sufficient, but for more advanced
cases it's recommended you familiarize yourself with the [coroutine](/docs/reference/engine/libraries/coroutine)
library.

---

API Reference

Functions

spawn

Calls/resumes a function/coroutine immediately through the engine's
scheduler.

task.spawn(

functionOrThread:[function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine), ...:Variant

):[coroutine](/docs/reference/engine/libraries/coroutine)

Parameters

|  |
| --- |
| functionOrThread:[function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine)  A function or a thread returned by [coroutine.create()](/docs/reference/engine/libraries/coroutine#create). |
| ...:Variant  Arguments to send to the function or thread. |

Returns

[coroutine](/docs/reference/engine/libraries/coroutine)

The scheduled thread.

Accepts a function or a thread (as returned by
[coroutine.create()](/docs/reference/engine/libraries/coroutine#create)) and calls/resumes it immediately through the
engine's scheduler. Arguments after the first are sent to the
function/thread.

If the calling script is currently running in a serial execution phase,
then the spawned function or thread is resumed in the current serial
execution phase. If the calling script is currently running in a parallel
execution phase, then the spawned function or thread is resumed in the
current parallel execution phase. For more information, see
[Parallel Luau](/docs/scripting/multithreading).

Provide feedback

---

defer

Calls/resumes a function/coroutine at the end of the current resumption
cycle.

task.defer(

functionOrThread:[function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine), ...:Variant

):[coroutine](/docs/reference/engine/libraries/coroutine)

Parameters

|  |
| --- |
| functionOrThread:[function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine)  A function or a thread returned by coroutine.create. |
| ...:Variant  Arguments to send to the function or thread. |

Returns

[coroutine](/docs/reference/engine/libraries/coroutine)

The scheduled thread.

Accepts a function or a thread (as returned by
[coroutine.create()](/docs/reference/engine/libraries/coroutine#create)) and defers it until the end of the current
resume point within the current frame.

This function should be used when a similar behavior to
[task.spawn()](/docs/reference/engine/libraries/task#spawn) is desirable, but the thread does not need to run
immediately.

If the calling script is currently running in a serial execution phase,
then the deferred function or thread is resumed in a serial execution
phase. If the calling script is currently running in a parallel execution
phase, then the deferred function or thread is resumed in a parallel
execution phase. For more information, see
[Parallel Luau](/docs/scripting/multithreading).

Provide feedback

---

delay

Schedules a function/coroutine to be called/resumed on the next Heartbeat
after the given duration (in seconds) has passed, without throttling.

task.delay(

duration:[number](/docs/luau/numbers), functionOrThread:[function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine), ...:Variant

):[coroutine](/docs/reference/engine/libraries/coroutine)

Parameters

|  |
| --- |
| duration:[number](/docs/luau/numbers)  The minimum number of seconds that must pass before the function/thread is called/resumed. |
| functionOrThread:[function](/docs/luau/functions) | [coroutine](/docs/reference/engine/libraries/coroutine) |
| ...:Variant  Arguments to be passed to the function/thread when it is due to be called/resumed. |

Returns

[coroutine](/docs/reference/engine/libraries/coroutine)

The scheduled thread.

Accepts a function or a thread (as returned by
[coroutine.create()](/docs/reference/engine/libraries/coroutine#create)) and schedules it to be called/resumed on the
next [Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat) after the given amount of time
in seconds has elapsed. Arguments after the second are sent to the
function/thread.

This function differs from the deprecated global delay() function in
that no throttling occurs: on the very same
[Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat) step in which enough time has
passed, the function is guaranteed to be called/resumed. Providing a
duration of zero (0) will guarantee that the function is called on the
very next [Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat).

You can calculate the actual time passed by calling [os.clock()](/docs/reference/engine/libraries/os#clock)
upon scheduling and in the scheduled function.

If the calling script is currently running in a serial execution phase,
then the delayed function or thread is resumed in a serial execution
phase. If the calling script is currently running in a parallel execution
phase, then the delayed function or thread is resumed in a parallel
execution phase. For more information, see
[Parallel Luau](/docs/scripting/multithreading).

Provide feedback

---

desynchronize

Causes the following code to be run in parallel.

task.desynchronize():()

Returns

()

If the calling script is currently running in a serial execution phase,
desynchronize() suspends the script and the script will be resumed in
the next parallel execution phase. If the calling script is currently
running in a parallel execution phase, desynchronize() returns
immediately and has no effect.

Only scripts which are descendants of an [Actor](/docs/reference/engine/classes/Actor) may call this
method. If a script outside of an [Actor](/docs/reference/engine/classes/Actor) calls this method, an
error will be raised. [ModuleScripts](/docs/reference/engine/classes/ModuleScript) may also call
desynchronize() as long as the instantiation of the module calling it
was required by a script that is a descendant of an [Actor](/docs/reference/engine/classes/Actor).

For more information, see
[Parallel Luau](/docs/scripting/multithreading).

Provide feedback

---

synchronize

Causes the following code to be run in serial.

task.synchronize():()

Returns

()

If the calling script is currently running in a parallel execution phase,
synchronize() suspends the script and the script will be resumed in the
next serial execution phase. If the calling script is currently running in
a serial execution phase, synchronize() returns immediately and has no
effect.

Only scripts which are descendants of an [Actor](/docs/reference/engine/classes/Actor) may call this
method. If a script outside of an [Actor](/docs/reference/engine/classes/Actor) calls this method, an
error will be raised. [ModuleScripts](/docs/reference/engine/classes/ModuleScript) may also call
synchronize() as long as the instantiation of the module calling it was
required by a script that is a descendant of an [Actor](/docs/reference/engine/classes/Actor).

For more information, see
[Parallel Luau](/docs/scripting/multithreading).

Provide feedback

---

wait

Yields the current thread without throttling.

task.wait(duration:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| duration:[number](/docs/luau/numbers) Default Value: 0 The amount of time in seconds that should elapse before the current thread is resumed. |

Returns

[number](/docs/luau/numbers)

Yields the current thread until the given duration (in seconds) has
elapsed, then resumes the thread on the next
[Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat) step. The actual amount of time
elapsed is returned.

If no duration is given, it will default to zero (0). This means the
thread resumes on the very next step, which is equivalent in behavior to
Class.RunService.Heartbeat:Wait()

Unlike the deprecated global wait(), this function does not throttle
and guarantees the resumption of the thread on the first Heartbeat that
occurs when it is due. This function also only returns the elapsed time
and nothing else.

If the calling script is currently running in a serial execution phase,
then the script is resumed in a serial execution phase. If the calling
script is currently running in a parallel execution phase, then the script
is resumed in a parallel execution phase. For more information, see
[Parallel Luau](/docs/scripting/multithreading).

Provide feedback

---

cancel

Cancels a thread, preventing it from being resumed.

task.cancel(thread:[coroutine](/docs/reference/engine/libraries/coroutine)):()

Parameters

|  |
| --- |
| thread:[coroutine](/docs/reference/engine/libraries/coroutine)  The thread that will be cancelled. |

Returns

()

Cancels a thread and closes it, preventing it from being resumed manually
or by the engine's scheduler.

This function can be used with other members of the task library that
return a thread to cancel them before they are resumed. For example:

```
local thread = task.delay(5, function()



print("Hello world!")



end)



task.cancel(thread)
```

Note that threads may be in a state where it is impossible to cancel them.
For example, the currently executing thread and threads that have resumed
another coroutine may not be cancelled. If this is the case, an error will
be generated. However, code should not rely on specific thread states or
conditions causing [task.cancel()](/docs/reference/engine/libraries/task#cancel) to fail. It is possible that
future updates will eliminate these constraints and allow threads in these
states to be successfully cancelled.

Provide feedback

---