# PlaybackState | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/PlaybackState
Scraped: 2026-01-11T02:45:00.089747Z

## Inherits
- Tween
- Tween.PlaybackState
1. [Enums](/docs/reference/engine/enums)
2. /
3. [PlaybackState](/docs/reference/engine/enums/PlaybackState)

English

Feedback

Engine Enum

PlaybackState

---

Describes the current state of a [Tween](/docs/reference/engine/classes/Tween) in its
[Tween.PlaybackState](/docs/reference/engine/classes/Tween#PlaybackState) property.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Begin | 0 | The tween has been created, but has yet to be played. After exiting this state, the tween never enters it again. |
| Delayed | 1 | The tween is waiting for the duration specified in its [TweenInfo.DelayTime](/docs/reference/engine/datatypes/TweenInfo#DelayTime). After the delay elapses, the tween plays. |
| Playing | 2 | The tween is currently in progress. |
| Paused | 3 | The tween is paused in the middle of playing. |
| Completed | 4 | The tween completed successfully. |
| Cancelled | 5 | The tween was cancelled before completion. |