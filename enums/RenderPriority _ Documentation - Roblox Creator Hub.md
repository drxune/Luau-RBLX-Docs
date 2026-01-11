# RenderPriority | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/RenderPriority
Scraped: 2026-01-11T02:44:44.976416Z

## Inherits
- RunService:BindToRenderStep()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [RenderPriority](/docs/reference/engine/enums/RenderPriority)

English

Feedback

Engine Enum

RenderPriority

---

A list of standard reserved values in BindToRenderStep.

See [RunService:BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep) for the proper usage, as the enum
itself isn't used.

Items

| Name | Value | Summary |
| --- | --- | --- |
| First | 0 | This should run first. |
| Input | 100 | This should run as second. |
| Camera | 200 | This should run after Input. |
| Character | 300 | This should run after Camera. |
| Last | 2000 | This should run as last, after Character. |