# os | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/os
Scraped: 2026-01-11T02:49:41.077316Z

## Inherits
- Workspace:GetServerTimeNow()
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [os](/docs/reference/engine/libraries/os)

English

Feedback

Engine Library

os

This library provides functions related to time and date.

---

Summary

Functions

|  |
| --- |
| [clock](#clock)():[number](/docs/luau/numbers) |
| [date](#date)(formatString: [string](/docs/luau/strings),time: [number](/docs/luau/numbers)):[Dictionary](/docs/luau/tables#dictionaries) |
| [difftime](#difftime)(t2: [number](/docs/luau/numbers),t1: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [time](#time)(time: [table](/docs/luau/tables)):[number](/docs/luau/numbers) |

This library currently serves the purpose of providing information about the
system time under the UTC format. It has been heavily sandboxed from the
standard Lua [os](/docs/reference/engine/libraries/os) library and does not allow you to perform any
system-altering operations.

---

API Reference

Functions

clock

Returns elapsed time in seconds since an arbitrary baseline with
sub-microsecond precision.

os.clock():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns elapsed time in seconds since an arbitrary baseline with
sub-microsecond precision. This function is useful for comparing durations
between two events that occur on the same computer, and is the best option
for benchmarking.

Unlike with functions such as [os.time()](/docs/reference/engine/libraries/os#time) or
[DateTime.now()](/docs/reference/engine/datatypes/DateTime#now), adjustments to the system clock (such as by the
user or [NTP](https://en.wikipedia.org/wiki/Network_Time_Protocol)) do not
cause time to jump forwards or backwards.

```
-- Record the initial time:



local startTime = os.clock()



-- Do something you want to measure the performance of:



local a, b = 0, 1



for _ = 1, 5000000 do



a, b = b, a



end



-- Measure amount of time this took:



local deltaTime = os.clock() - startTime



print("Elapsed time: " .. deltaTime)



-->  Elapsed time: 0.044425600033719 (actual number may vary)
```

Provide feedback

---

date

Formats the given string with date/time information based on the given
time.

os.date(

formatString:[string](/docs/luau/strings), time:[number](/docs/luau/numbers)

):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| formatString:[string](/docs/luau/strings)  Must be either "\*t" or "!\*t". |
| time:[number](/docs/luau/numbers)  The time value to format. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Formats the given formatString with date/time information based on the
given time, or if not provided, the value returned by [os.time()](/docs/reference/engine/libraries/os#time).

This function should be avoided in new work. Instead, use the
[DateTime](/docs/reference/engine/datatypes/DateTime) API, which supports localized formatting.

The following specifiers (based on the C function strftime) are supported:

| Specifier | Meaning | Example† |
| --- | --- | --- |
| %a | Abbreviated weekday name \* | Mon |
| %A | Full weekday name \* | Monday |
| %b | Abbreviated month name \* | Feb |
| %B | Full month name \* | February |
| %c | Date and time \* | Mon Feb 12 14:14:35 2024 |
| %d | Day of the month | 12 |
| %H | Hour, using 24-hour clock | 14 |
| %I | Hour, using 12-hour clock | 02 |
| %j | Day of year | 043 |
| %m | Month | 02 |
| %M | Minute | 14 |
| %p | Either "AM" or "PM" | PM |
| %S | Second | 35 |
| %U | Week number (first Sunday as the first day of week one) | 06 |
| %w | Weekday | 1 |
| %W | Week number (first Monday as the first day of week one) | 07 |
| %x | Date \* | 02/12/24 |
| %X | Time \* | 14:14:35 |
| %y | Two-digit year | 24 |
| %Y | Full year | 2024 |
| %z | ISO 8601 offset from UTC in timezone (1 minute = 1, 1 hour = 100) | -0800 |
| %Z | Timezone name or abbreviation \* | PST |
| %% | The % character | % |

\* This value can vary depending on the current locale.

† The example provided is for February 12th, 2024 (Monday) at
2:14:35 PM (14:14:35), run using locale "en-us" in Pacific Standard Time
(PST).

If the provided formatString is exactly "\*t" (local time) or "!\*t"
(UTC time), this function instead returns a dictionary containing the
following components, which are normally available in the specifiers
above.

| Field | Type | Description |
| --- | --- | --- |
| year | int | An integer that describes the current year of the Current Era (ex. 2017) |
| month | int | An integer between 1 and 12 (starting from January) that describes the current month. |
| wday | int | An integer between 1 and 7 (starting from Sunday) that describes the current week day. |
| yday | int | An integer between 1 and 366 describing how many days we are into the year. There can be 366 days if it is a leap year. |
| day | int | An integer between 1 and 31 describing the current day of the month. |
| hour | int | An integer between 1 and 24 describing the current hour of the day. |
| min | int | An integer between 0 and 59 describing the current minute of the hour. |
| sec | int | An integer between 0 and 60 describing the current second of the hour. (60 because the function is described to indicate leap seconds, but in practice it probably doesn't). |
| isdst | bool | A boolean describing if daylight savings time is currently active. |

Provide feedback

---

difftime

Returns the number of seconds from one time to another.

os.difftime(

t2:[number](/docs/luau/numbers), t1:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| t2:[number](/docs/luau/numbers) |
| t1:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the number of seconds from t1 to t2. The difference is
computed assuming that t1 and t2 are correctly casted to the
[time\_t](http://en.cppreference.com/w/cpp/chrono/c/time_t) format.

Provide feedback

---

time

Returns how many seconds have passed since the Unix epoch (1 January 1970,
00:00:00) under current UTC time.

os.time(time:[table](/docs/luau/tables)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| time:[table](/docs/luau/tables) Default Value: UTC time A dictionary table describing a specific time, similar to that returned by [os.date()](/docs/reference/engine/libraries/os#date). If not provided, uses the current UTC time. |

Returns

[number](/docs/luau/numbers)

Returns how many seconds have passed since the Unix epoch (1 January 1970,
00:00:00), under current UTC time. If provided a table formatted similarly
to that returned by [os.date()](/docs/reference/engine/libraries/os#date), it returns the number of seconds
from the Unix epoch to that time instead.

Note that the returned time uses the device's local clock. Most operating
systems automatically sync their local time against online time servers,
so this should be within a few hundred milliseconds. However, users can
easily disable sync behavior and set the system time to anything they
want; for synchronized time between client and server, use
[Workspace:GetServerTimeNow()](/docs/reference/engine/classes/Workspace#GetServerTimeNow) instead.

This function should be avoided in new work. Instead, use the
[DateTime](/docs/reference/engine/datatypes/DateTime) API, which supports localized formatting.

When you need to precisely measure the time elapsed between two points in
time, like when testing performance, use [os.clock()](/docs/reference/engine/libraries/os#clock) instead.

Provide feedback

---