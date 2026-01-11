# StreamOutBehavior | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/StreamOutBehavior
Scraped: 2026-01-11T02:43:03.856293Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [StreamOutBehavior](/docs/reference/engine/enums/StreamOutBehavior)

English

Feedback

Engine Enum

StreamOutBehavior

---

Determines how content is streamed out from Player clients. This is a
temporary rollout API. In the future, streaming will always run on
Opportunistic mode.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Currently equivalent to LowMemory. This will eventually change to Opportunistic. |
| LowMemory | 1 | Only stream out when memory is low. |
| Opportunistic | 2 | Stream out content that is significantly outside of the current StreamingRadius. |