# StudioTestService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StudioTestService
Scraped: 2026-01-11T02:40:24.957913Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- StudioTestService
- Object
- StudioTestService:ExecutePlayModeAsync()
- StudioTestService:ExecuteRunModeAsync()
- DataModel
- StudioTestService:EndTest()
- StudioTestService:GetTestArgs()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StudioTestService](/docs/reference/engine/classes/StudioTestService)

English

Feedback

Engine Class

StudioTestService

Service allowing plugins to automate and customize Test and Run mode testing.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [EndTest](#EndTest)(value: Variant):() |
| [ExecutePlayModeAsync](#ExecutePlayModeAsync)(args: Variant):Variant |
| [ExecuteRunModeAsync](#ExecuteRunModeAsync)(args: Variant):Variant |
| [GetTestArgs](#GetTestArgs)():Variant |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

StudioTestService allows plugins to automate and customize Test and Run mode
testing. With StudioTestService, your plugins can launch tests that jump
straight to a specific part of your game, or run complex code tests
automatically.

The following is an example of automated unit testing:

```
--Plugin Script



local StudioTestService = game:GetService("StudioTestService")



local testResult = StudioTestService:ExecuteRunModeAsync("MyTestSuite")



print("Test finished. Result:", testResult)
```

```
--Server Script



local StudioTestService = game:GetService("StudioTestService")



local RunService = game:GetService("RunService")



if not RunService:IsStudio() or not RunService:IsRunMode() then



return



end



local suiteName = StudioTestService:GetTestArgs()



if suiteName then



local tests = getTestsArrayByName(SuiteName)



if tests then



local result = "SUCCESS!"



for name, test in tests do



if not pcall(test) then



result = name .. " failed!"



break



end



end



StudioTestService:EndTest(result)



else



StudioTestService:EndTest("Suite not found")



end



else



print("Starting manual playtest")



end
```

---

API Reference

Methods

EndTest

StudioTestService:EndTest(value:Variant):()

Parameters

|  |
| --- |
| value:Variant  Value returned to the calling [StudioTestService:ExecutePlayModeAsync()](/docs/reference/engine/classes/StudioTestService#ExecutePlayModeAsync) or [StudioTestService:ExecuteRunModeAsync()](/docs/reference/engine/classes/StudioTestService#ExecuteRunModeAsync) method. |

Returns

()

Ends the current Studio test session if called from the server
[DataModel](/docs/reference/engine/classes/DataModel), even if the test was not started by this service.

If the test was started by
[StudioTestService:ExecutePlayModeAsync()](/docs/reference/engine/classes/StudioTestService#ExecutePlayModeAsync) or
[StudioTestService:ExecuteRunModeAsync()](/docs/reference/engine/classes/StudioTestService#ExecuteRunModeAsync), the value passed here is
returned by that method.

This method returns immediately and ends the test session asynchronously.
It errors if called from any [DataModel](/docs/reference/engine/classes/DataModel) other than that of the
server during a running Studio test session.

Provide feedback

---

ExecutePlayModeAsync

Yields

Plugin Security

StudioTestService:ExecutePlayModeAsync(args:Variant):Variant

Parameters

|  |
| --- |
| args:Variant  Argument passed to the test session, or nil. |

Returns

Variant

Value passed from [StudioTestService:EndTest()](/docs/reference/engine/classes/StudioTestService#EndTest), or nil.

Starts a solo Test session and yields until that session ends.

The args parameter can be retrieved using
[StudioTestService:GetTestArgs()](/docs/reference/engine/classes/StudioTestService#GetTestArgs). Returns the value passed to
[StudioTestService:EndTest()](/docs/reference/engine/classes/StudioTestService#EndTest), or nil if the test ended by other
means.

This method errors if a test session is already running.

Provide feedback

---

ExecuteRunModeAsync

Yields

Plugin Security

StudioTestService:ExecuteRunModeAsync(args:Variant):Variant

Parameters

|  |
| --- |
| args:Variant  Argument passed to the test session, or nil. |

Returns

Variant

Value passed from [StudioTestService:EndTest()](/docs/reference/engine/classes/StudioTestService#EndTest), or nil.

Starts a Run test session and yields until that session ends.

The args parameter can be retrieved using
[StudioTestService:GetTestArgs()](/docs/reference/engine/classes/StudioTestService#GetTestArgs). Returns the value passed to
[StudioTestService:EndTest()](/docs/reference/engine/classes/StudioTestService#EndTest), or nil if the test ended by other
means.

This method errors if a test session is already running.

Provide feedback

---

GetTestArgs

StudioTestService:GetTestArgs():Variant

Returns

Variant

Arguments passed to the test, or nil.

Returns the argument passed to
[StudioTestService:ExecutePlayModeAsync()](/docs/reference/engine/classes/StudioTestService#ExecutePlayModeAsync) or
[StudioTestService:ExecuteRunModeAsync()](/docs/reference/engine/classes/StudioTestService#ExecuteRunModeAsync) for the current test
session, or nil if the session was not started by those methods.

Provide feedback

---