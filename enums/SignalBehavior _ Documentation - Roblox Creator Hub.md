# SignalBehavior | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/SignalBehavior
Scraped: 2026-01-11T02:45:59.550631Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [SignalBehavior](/docs/reference/engine/enums/SignalBehavior)

English

Feedback

Engine Enum

SignalBehavior

---

Determines when the engine resumes event handlers. At some future point, the
default mode will be Deferred but opt-out will still be possible through use
of Immediate.

For more information, see
[Deferred Events](/docs/scripting/events/deferred).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | The default behavior; currently equivalent to Immediate but this will eventually change to Deferred. |
| Immediate | 1 | Event handlers are resumed immediately when the event occurs. |
| Deferred | 2 | All events are deferred and their handlers resumed at specific resumptions points each frame. |
| AncestryDeferred | 3 | Equivalent to Deferred but only for events triggered by changes in ancestry. |