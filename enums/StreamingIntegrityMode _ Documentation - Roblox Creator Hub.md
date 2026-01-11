# StreamingIntegrityMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/StreamingIntegrityMode
Scraped: 2026-01-11T02:43:15.084232Z

## Inherits
- Workspace.StreamingIntegrityMode
- Player.ReplicationFocus
- Player.GameplayPaused
1. [Enums](/docs/reference/engine/enums)
2. /
3. [StreamingIntegrityMode](/docs/reference/engine/enums/StreamingIntegrityMode)

English

Feedback

Engine Enum

StreamingIntegrityMode

---

This enum is used to control [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode)
behavior. The default behavior is currently equivalent to Disabled but may
change in the future. For all modes, the replication focus defaults to be the
local character model unless explicitly set via
[Player.ReplicationFocus](/docs/reference/engine/classes/Player#ReplicationFocus).

Most experiences should use PauseOutsideLoadedArea, however if your
experience relies on raycasts, or otherwise requires a certain amount of
content to be loaded in, then MinimumRadiusPause might be a better choice.

Note that MinimumRadiusPause and PauseOutsideLoadedArea both set the
[Player.GameplayPaused](/docs/reference/engine/classes/Player#GameplayPaused) property when their respective pause logic is
triggered, and a default message is displayed on the client. The default pause
UI can be overridden as outlined in
[Instance streaming](/docs/workspace/streaming#customize-the-pause-screen).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Default behavior (currently equivalent to Disabled). |
| Disabled | 1 | Simulation of the replication focus is never paused, regardless of the amount of content streamed in on the client. |
| MinimumRadiusPause | 2 | All client-side simulation is paused when content is not streamed in up to the minimum radius. |
| PauseOutsideLoadedArea | 3 | Simulation of the replication focus is paused when any part of its bounding box is not in a streamed-in area. |