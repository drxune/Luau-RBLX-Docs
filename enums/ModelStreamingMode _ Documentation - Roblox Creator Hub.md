# ModelStreamingMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ModelStreamingMode
Scraped: 2026-01-11T02:45:29.950630Z

## Inherits
- Model
- BasePart
- BaseParts
- Workspace.PersistentLoaded
- Model:AddPersistentPlayer()
- Model:RemovePersistentPlayer()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ModelStreamingMode](/docs/reference/engine/enums/ModelStreamingMode)

English

Feedback

Engine Enum

ModelStreamingMode

---

Controls how model is streamed in and out when used in an experience that is
streaming enabled. Has no effect when experience is not streaming enabled.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Engine determines best behavior. Currently equivalent to Nonatomic. |
| Atomic | 1 | The [Model](/docs/reference/engine/classes/Model) and all of its descendants are streamed in/out together. For streaming in, this applies when any descendant [BasePart](/docs/reference/engine/classes/BasePart) is eligible for streaming in. For streaming out, this applies when all descendant [BaseParts](/docs/reference/engine/classes/BasePart) are eligible for streaming out. |
| Persistent | 2 | Persistent models are sent as a complete atomic unit soon after the player joins and before the [Workspace.PersistentLoaded](/docs/reference/engine/classes/Workspace#PersistentLoaded) event fires. Persistent models and their descendants are never streamed out. |
| PersistentPerPlayer | 3 | Behaves as a persistent model for players that have been added using [Model:AddPersistentPlayer()](/docs/reference/engine/classes/Model#AddPersistentPlayer). For other players, behavior is the same as Atomic. You can revert a model from player persistence via [Model:RemovePersistentPlayer()](/docs/reference/engine/classes/Model#RemovePersistentPlayer). |
| Nonatomic | 4 | When a nonatomic model is streamed, descendants are also sent, except for part descendants. Nonatomic models that are not descendants of parts are sent during experience loading. |