# AudioApiRollout | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AudioApiRollout
Scraped: 2026-01-11T02:46:32.213661Z

## Inherits
- AudioDeviceInput
- AudioDeviceInputs
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AudioApiRollout](/docs/reference/engine/enums/AudioApiRollout)

English

Feedback

Engine Enum

AudioApiRollout

---

Used to determine whether voice chat is represented and controlled by
[AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) objects.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Disabled | 0 | Voice chat will use an internal voice chat implementation that is automatic and hidden. |
| Automatic | 1 | Currently means the same thing as Disabled, but will be updated to mean Enabled in the future. |
| Enabled | 2 | Voice chat can be customized or controlled via [AudioDeviceInputs](/docs/reference/engine/classes/AudioDeviceInput). |