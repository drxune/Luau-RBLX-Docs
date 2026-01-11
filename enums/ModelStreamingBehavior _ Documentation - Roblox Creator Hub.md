# ModelStreamingBehavior | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ModelStreamingBehavior
Scraped: 2026-01-11T02:42:48.472161Z

## Inherits
- Models
- ModelStreamingMode
- BasePart
- Workspace.PersistentLoaded
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ModelStreamingBehavior](/docs/reference/engine/enums/ModelStreamingBehavior)

English

Feedback

Engine Enum

ModelStreamingBehavior

---

Controls how [Models](/docs/reference/engine/classes/Model) are replicated in experiences when instance
[streaming](/docs/workspace/streaming) is enabled. Only affects models
with [ModelStreamingMode](/docs/reference/engine/classes/Model#ModelStreamingMode) set to
[Default](/docs/reference/engine/enums/ModelStreamingMode)/[Nonatomic](/docs/reference/engine/enums/ModelStreamingMode).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Engine determines best behavior. Currently equivalent to Legacy. |
| Legacy | 1 | Models are sent when their parent is sent, typically during player join. Models are never streamed out unless an ancestor of the model is streamed out. |
| Improved | 2 | Models are never sent during player join. Models that are "non-spatial" (containing no [BasePart](/docs/reference/engine/classes/BasePart) descendants) are sent soon after join, but before the [Workspace.PersistentLoaded](/docs/reference/engine/classes/Workspace#PersistentLoaded) event fires. Models that are "spatial" (containing [BasePart](/docs/reference/engine/classes/BasePart) descendants) are sent when any [BasePart](/docs/reference/engine/classes/BasePart) descendant needs to be streamed to a client, and may stream out when all [BasePart](/docs/reference/engine/classes/BasePart) descendants are eligible to stream out. |