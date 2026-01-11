# ContextActionResult | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ContextActionResult
Scraped: 2026-01-11T02:45:23.643385Z

## Inherits
- ContextActionService:BindAction()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ContextActionResult](/docs/reference/engine/enums/ContextActionResult)

English

Feedback

Engine Enum

ContextActionResult

---

ContextActionResult controls the behavior of multiple bound actions. It
gives the option of controlling whether or not a bound action should sink or
pass the input event, meaning other things (including other bound actions) can
process it.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Sink | 0 | If functionToBind from [ContextActionService:BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction) returns [Enum.ContextActionResult.Sink](/docs/reference/engine/enums/ContextActionResult#Sink), the input event will stop at that function and no other bound actions under it will be processed. This is the default behavior if functionToBind does not return anything or yields in any way. |
| Pass | 1 | If functionToBind from [ContextActionService:BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction) returns [Enum.ContextActionResult.Pass](/docs/reference/engine/enums/ContextActionResult#Pass), the input event is considered to have not been handled by functionToBind and will continue being passed to actions bound to the same input type. |