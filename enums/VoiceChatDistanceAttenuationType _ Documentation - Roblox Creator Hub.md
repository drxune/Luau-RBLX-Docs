# VoiceChatDistanceAttenuationType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/VoiceChatDistanceAttenuationType
Scraped: 2026-01-11T02:45:43.140293Z

## Inherits
- VoiceChatService
- AudioDeviceInput
- AudioEmitter
1. [Enums](/docs/reference/engine/enums)
2. /
3. [VoiceChatDistanceAttenuationType](/docs/reference/engine/enums/VoiceChatDistanceAttenuationType)

English

Feedback

Engine Enum

VoiceChatDistanceAttenuationType

---

Each value in this enum represents a distance attenuation curve that can be
used by [VoiceChatService](/docs/reference/engine/classes/VoiceChatService) when creating the default voice chat setup
using [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) and [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) objects.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Inverse | 0 | Represents a distance attenuation curve that follows the inverse-squared law. This is identical to the default distance attenuation of an [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) instance. |
| Legacy | 1 | Represents a linear-squared distance attenuation curve with a minimum distance of 7 and a maximum distance of 80. This is identical to the distance attenuation used in the internal-only default voice setup that does not use [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) and [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) objects. |