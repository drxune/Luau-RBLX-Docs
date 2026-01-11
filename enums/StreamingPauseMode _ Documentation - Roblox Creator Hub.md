# StreamingPauseMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/StreamingPauseMode
Scraped: 2026-01-11T02:43:27.486306Z

## Inherits
- Workspace.StreamingIntegrityMode
- Workspace.StreamingPauseMode
- Workspace.StreamingEnabled
- Workspace.StreamingMinRadius
- Workspace.StreamingTargetRadius
1. [Enums](/docs/reference/engine/enums)
2. /
3. [StreamingPauseMode](/docs/reference/engine/enums/StreamingPauseMode)

English

Feedback

Engine Enum

StreamingPauseMode

Deprecated

Please use [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode) instead.

---

The StreamingPauseMode enum is used to control
[Workspace.StreamingPauseMode](/docs/reference/engine/classes/Workspace#StreamingPauseMode) behavior.

Default behavior is currently equivalent to disabled, but may change in the
future.

The disabled mode indicates that gameplay continues unchanged even if player
does not have the minimum streaming radius available.

In ClientPhysicsPause mode client-side physics is paused when the player
doesn't have the minimum radius present, and resumed when the minimum radius
is available.

See also:

* [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled), controls whether network streaming is
  enabled for the place or not
* [Workspace.StreamingMinRadius](/docs/reference/engine/classes/Workspace#StreamingMinRadius), the minimum distance that parts will
  be streamed to players with high priority
* [Workspace.StreamingTargetRadius](/docs/reference/engine/classes/Workspace#StreamingTargetRadius), the maximum distance that parts
  will be streamed to players

Items

| Name | Value | Summary |
| --- | --- | --- |
| Default | 0 | Deprecated |
| Disabled | 1 | Deprecated |
| ClientPhysicsPause | 2 | Deprecated |