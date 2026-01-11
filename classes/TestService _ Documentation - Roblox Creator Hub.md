# TestService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TestService
Scraped: 2026-01-11T02:34:18.350665Z

## Tags
- Service
- Not Replicated

## Inherits
- Object
- Instance
- TestService
- TestService:Run()
- TestService:Check()
- TestService:Require()
- TestService:Warn()
- TestService:Error()
- TestService:Fail()
- TestService:Message()
- NumberOfPlayers
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TestService](/docs/reference/engine/classes/TestService)

English

Feedback

Engine Class

![TestService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TestService-Dark.webp)TestService

A service used by Roblox to run controlled tests of the engine. It is
available for developers to use, to a limited degree.

Service

---

Summary

Properties

|  |
| --- |
| [AutoRuns](#AutoRuns):[boolean](/docs/luau/booleans) |
| [Description](#Description):[string](/docs/luau/strings) |
| [ErrorCount](#ErrorCount):[number](/docs/luau/numbers) |
| [ExecuteWithStudioRun](#ExecuteWithStudioRun):[boolean](/docs/luau/booleans) |
| [Is30FpsThrottleEnabled](#Is30FpsThrottleEnabled):[boolean](/docs/luau/booleans)  Deprecated |
| [IsPhysicsEnvironmentalThrottled](#IsPhysicsEnvironmentalThrottled):[boolean](/docs/luau/booleans) |
| [IsSleepAllowed](#IsSleepAllowed):[boolean](/docs/luau/booleans) |
| [NumberOfPlayers](#NumberOfPlayers):[number](/docs/luau/numbers) |
| [SimulateSecondsLag](#SimulateSecondsLag):[number](/docs/luau/numbers) |
| [TestCount](#TestCount):[number](/docs/luau/numbers) |
| [ThrottlePhysicsToRealtime](#ThrottlePhysicsToRealtime):[boolean](/docs/luau/booleans) |
| [Timeout](#Timeout):[number](/docs/luau/numbers) |
| [WarnCount](#WarnCount):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Check](#Check)(condition: [boolean](/docs/luau/booleans),description: [string](/docs/luau/strings),source: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):() |
| [Checkpoint](#Checkpoint)(text: [string](/docs/luau/strings),source: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):() |
| [Done](#Done)():() |
| [Error](#Error)(description: [string](/docs/luau/strings),source: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):() |
| [Fail](#Fail)(description: [string](/docs/luau/strings),source: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):() |
| [isFeatureEnabled](#isFeatureEnabled)(name: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [Message](#Message)(text: [string](/docs/luau/strings),source: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):() |
| [Require](#Require)(condition: [boolean](/docs/luau/booleans),description: [string](/docs/luau/strings),source: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):() |
| [RunAsync](#RunAsync)():() |
| [Run](#Run)():()  Deprecated |
| [ScopeTime](#ScopeTime)():[Dictionary](/docs/luau/tables#dictionaries) |
| [TakeSnapshot](#TakeSnapshot)(snapshotname: [string](/docs/luau/strings)):() |
| [Warn](#Warn)(condition: [boolean](/docs/luau/booleans),description: [string](/docs/luau/strings),source: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):() |

Events

|  |
| --- |
| [ServerCollectConditionalResult](#ServerCollectConditionalResult)(condition: [boolean](/docs/luau/booleans),text: [string](/docs/luau/strings),script: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ServerCollectResult](#ServerCollectResult)(text: [string](/docs/luau/strings),script: [Instance](/docs/reference/engine/datatypes/Instance),line: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

TestService is a service used by Roblox internally to run analytical tests
on the engine.

Scripts that are executed inside of TestService (via
[TestService:Run()](/docs/reference/engine/classes/TestService#Run)) have access to special macros that directly invoke
functions under the service. Macros are essentially substitutions for large
blocks of code that shouldn't need to be rewritten each time you want to call
them.

#### RBX\_CHECK

This macro does tests with calls to the [TestService:Check()](/docs/reference/engine/classes/TestService#Check) function.

| Macro | Test Condition |
| --- | --- |
| RBX\_CHECK(cond) | cond == true |
| RBX\_CHECK\_MESSAGE(cond, failMsg) | cond == true |
| RBX\_CHECK\_THROW(CODE) | pcall(function() CODE end) == false |
| RBX\_CHECK\_NO\_THROW(CODE) | pcall(function() CODE end) == true |
| RBX\_CHECK\_EQUAL(a, b) | a == b |
| RBX\_CHECK\_NE(a, b) | a ~= b |
| RBX\_CHECK\_GE(a, b) | a >= b |
| RBX\_CHECK\_LE(a, b) | a <= b |
| RBX\_CHECK\_GT(a, b) | a > b |
| RBX\_CHECK\_LT(a, b) | a < b |

#### RBX\_REQUIRE

This macro does tests with calls to the [TestService:Require()](/docs/reference/engine/classes/TestService#Require)
function.

| Macro | Test Condition |
| --- | --- |
| RBX\_REQUIRE(cond) | cond == true |
| RBX\_REQUIRE\_MESSAGE(cond, failMsg) | cond == true |
| RBX\_REQUIRE\_THROW(CODE) | pcall(function() CODE end) == false |
| RBX\_REQUIRE\_NO\_THROW(CODE) | pcall(function() CODE end) == true |
| RBX\_REQUIRE\_EQUAL(a, b) | a == b |
| RBX\_REQUIRE\_NE(a, b) | a ~= b |
| RBX\_REQUIRE\_GE(a, b) | a >= b |
| RBX\_REQUIRE\_LE(a, b) | a <= b |
| RBX\_REQUIRE\_GT(a, b) | a > b |
| RBX\_REQUIRE\_LT(a, b) | a < b |

#### RBX\_WARN

This macro does tests with calls to the [TestService:Warn()](/docs/reference/engine/classes/TestService#Warn) function.

| Macro | Test Condition |
| --- | --- |
| RBX\_WARN(cond) | cond == true |
| RBX\_WARN\_MESSAGE(cond, failMsg) | cond == true |
| RBX\_WARN\_THROW(CODE) | pcall(function() CODE end) == false |
| RBX\_WARN\_NO\_THROW(CODE) | pcall(function() CODE end) == true |
| RBX\_WARN\_EQUAL(a, b) | a == b |
| RBX\_WARN\_NE(a, b) | a ~= b |
| RBX\_WARN\_GE(a, b) | a >= b |
| RBX\_WARN\_LE(a, b) | a <= b |
| RBX\_WARN\_GT(a, b) | a > b |
| RBX\_WARN\_LT(a, b) | a < b |

#### Additional Macros

| Macro | Description |
| --- | --- |
| RBX\_ERROR(msg) | Directly calls the [TestService:Error()](/docs/reference/engine/classes/TestService#Error) function. |
| RBX\_FAIL(msg) | Directly calls the [TestService:Fail()](/docs/reference/engine/classes/TestService#Fail) function. |
| RBX\_MESSAGE(msg) | Directly calls the [TestService:Message()](/docs/reference/engine/classes/TestService#Message) function. |

---

API Reference

Properties

AutoRuns

Read Parallel

If set to true, the game will start running when the service's
[TestService:Run()](/docs/reference/engine/classes/TestService#Run) method is called.

TestService.AutoRuns:[boolean](/docs/luau/booleans)

If set to true, the game will start running when the service's
[TestService:Run()](/docs/reference/engine/classes/TestService#Run) method is called.

Provide feedback

---

Description

Read Parallel

A description of the test being executed.

TestService.Description:[string](/docs/luau/strings)

A description of the test being executed.

Provide feedback

---

ErrorCount

Read Only

Not Replicated

Read Parallel

Measures how many errors have been recorded in the test session.

TestService.ErrorCount:[number](/docs/luau/numbers)

Measures how many errors have been recorded in the test session.

Provide feedback

---

ExecuteWithStudioRun

Read Parallel

When set to true, TestService will be executed when using the Run
action in Roblox Studio.

TestService.ExecuteWithStudioRun:[boolean](/docs/luau/booleans)

When set to true, TestService will be executed when using the Run
action in Roblox Studio.

Note that if the [NumberOfPlayers](/docs/reference/engine/classes/TestService#NumberOfPlayers)
property is set to a value above 0, running the game will open
NumberOfPlayers + 1 Studio windows where one window is a server and the
rest are players connected to that server. Try to keep this value within a
rational range (1 to 8 players) or else your computer's CPU will get
overloaded.

Provide feedback

---

Is30FpsThrottleEnabled

Deprecated

Show details

---

IsPhysicsEnvironmentalThrottled

Read Parallel

Sets whether or not the physics environment should be throttled while
running this test.

TestService.IsPhysicsEnvironmentalThrottled:[boolean](/docs/luau/booleans)

Sets whether or not the physics environment should be throttled while
running this test.

Provide feedback

---

IsSleepAllowed

Read Parallel

Sets whether or not physics objects will be allowed to fall asleep while
the test simulation is running.

TestService.IsSleepAllowed:[boolean](/docs/luau/booleans)

Sets whether or not physics objects will be allowed to fall asleep while
the test simulation is running.

Provide feedback

---

NumberOfPlayers

Read Parallel

The number of players expected in this test, if any.

TestService.NumberOfPlayers:[number](/docs/luau/numbers)

The number of players expected in this test, if any.

Provide feedback

---

SimulateSecondsLag

Read Parallel

Sets a specific amount of additional latency experienced by players during
the test session.

TestService.SimulateSecondsLag:[number](/docs/luau/numbers)

Sets a specific amount of additional latency experienced by players during
the test session.

Provide feedback

---

TestCount

Read Only

Not Replicated

Read Parallel

Measures how many test calls have been recorded in the test session.

TestService.TestCount:[number](/docs/luau/numbers)

Measures how many test calls have been recorded in the test session.

Provide feedback

---

ThrottlePhysicsToRealtime

Read Parallel

Sets whether the test should be throttled to simulate time according to
real world time or as fast as possible.

TestService.ThrottlePhysicsToRealtime:[boolean](/docs/luau/booleans)

Sets whether the test should be throttled to simulate time according to
real world time or as fast as possible.

Provide feedback

---

Timeout

Read Parallel

The maximum amount of time that tests are allowed to run for.

TestService.Timeout:[number](/docs/luau/numbers)

The maximum amount of time that tests are allowed to run for.

Provide feedback

---

WarnCount

Read Only

Not Replicated

Read Parallel

Measures how many warning calls have been recorded in the test session.

TestService.WarnCount:[number](/docs/luau/numbers)

Measures how many warning calls have been recorded in the test session.

Provide feedback

---

Methods

Check

Prints result of a condition to the output.

TestService:Check(

condition:[boolean](/docs/luau/booleans), description:[string](/docs/luau/strings), source:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| condition:[boolean](/docs/luau/booleans) |
| description:[string](/docs/luau/strings) |
| source:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |
| line:[number](/docs/luau/numbers) Default Value: 0 |

Returns

()

If condition is true, prints Check passed: followed by description
to the output in blue text. Otherwise, prints Check failed: followed by
description in red text.

Provide feedback

---

Checkpoint

Prints Test checkpoint: followed by a string to the output in blue text.

TestService:Checkpoint(

text:[string](/docs/luau/strings), source:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| text:[string](/docs/luau/strings) |
| source:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |
| line:[number](/docs/luau/numbers) Default Value: 0 |

Returns

()

Prints Test checkpoint: followed by text to the output in blue text.

Provide feedback

---

Done

Prints Testing Done to the output in blue text.

TestService:Done():()

Returns

()

Prints Testing Done to the output in blue text.

Provide feedback

---

Error

Prints a red error message to the output, prefixed by TestService: .

TestService:Error(

description:[string](/docs/luau/strings), source:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| description:[string](/docs/luau/strings) |
| source:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |
| line:[number](/docs/luau/numbers) Default Value: 0 |

Returns

()

Prints a red error message (description) to the output, prefixed by
TestService: .

Provide feedback

---

Fail

Indicates a fatal error in a TestService run.

TestService:Fail(

description:[string](/docs/luau/strings), source:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| description:[string](/docs/luau/strings) |
| source:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |
| line:[number](/docs/luau/numbers) Default Value: 0 |

Returns

()

Indicates a fatal error in a TestService run. If this is called inside
of a script running inside the service, it will initiate a breakpoint on
the line that invoked the error.

Provide feedback

---

isFeatureEnabled

TestService:isFeatureEnabled(name:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

Provide feedback

---

Message

Prints TestService: followed by a string to the output in blue text.

TestService:Message(

text:[string](/docs/luau/strings), source:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| text:[string](/docs/luau/strings) |
| source:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |
| line:[number](/docs/luau/numbers) Default Value: 0 |

Returns

()

Prints TestService: followed by text to the output in blue text.

Provide feedback

---

Require

Prints whether a condition is true along with a description string.

TestService:Require(

condition:[boolean](/docs/luau/booleans), description:[string](/docs/luau/strings), source:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| condition:[boolean](/docs/luau/booleans) |
| description:[string](/docs/luau/strings) |
| source:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |
| line:[number](/docs/luau/numbers) Default Value: 0 |

Returns

()

If condition is true, prints Require passed: followed by
description to the output in blue text. Otherwise prints
Require failed. Test ended: followed by description in red text.

Provide feedback

---

RunAsync

Yields

Plugin Security

Runs scripts which are parented to TestService.

TestService:RunAsync():()

Returns

()

Runs scripts which are parented to TestService.

Provide feedback

---

Run

Deprecated

Show details

---

ScopeTime

TestService:ScopeTime():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Provide feedback

---

TakeSnapshot

TestService:TakeSnapshot(snapshotname:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| snapshotname:[string](/docs/luau/strings) |

Returns

()

Provide feedback

---

Warn

Prints if a condition is true, otherwise prints a warning.

TestService:Warn(

condition:[boolean](/docs/luau/booleans), description:[string](/docs/luau/strings), source:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| condition:[boolean](/docs/luau/booleans) |
| description:[string](/docs/luau/strings) |
| source:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |
| line:[number](/docs/luau/numbers) Default Value: 0 |

Returns

()

If condition is true, prints Warning passed: followed by
description to the output in blue text. Otherwise prints Warning:
followed by description to the output in yellow text.

Provide feedback

---

Events

ServerCollectConditionalResult

Fires when the server should collect a conditional test result.

TestService.ServerCollectConditionalResult(

condition:[boolean](/docs/luau/booleans), text:[string](/docs/luau/strings), script:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| condition:[boolean](/docs/luau/booleans) |
| text:[string](/docs/luau/strings) |
| script:[Instance](/docs/reference/engine/datatypes/Instance) |
| line:[number](/docs/luau/numbers) |

Fires when the server should collect a conditional test result.

Provide feedback

---

ServerCollectResult

Fires when the server should collect a test result.

TestService.ServerCollectResult(

text:[string](/docs/luau/strings), script:[Instance](/docs/reference/engine/datatypes/Instance), line:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| text:[string](/docs/luau/strings) |
| script:[Instance](/docs/reference/engine/datatypes/Instance) |
| line:[number](/docs/luau/numbers) |

Fires when the server should collect a test result.

Provide feedback

---