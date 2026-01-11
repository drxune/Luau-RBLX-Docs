# HapticEffectType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/HapticEffectType
Scraped: 2026-01-11T02:45:29.893728Z

## Inherits
- HapticEffect.Type
- HapticEffect:SetWaveformKeys()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [HapticEffectType](/docs/reference/engine/enums/HapticEffectType)

English

Feedback

Engine Enum

HapticEffectType

---

Enum used alongside [HapticEffect.Type](/docs/reference/engine/classes/HapticEffect#Type).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Custom | 0 | Allows for application of a custom haptic waveform through the [HapticEffect:SetWaveformKeys()](/docs/reference/engine/classes/HapticEffect#SetWaveformKeys) method. |
| UIHover | 1 | Useful for when a player browses over an object (often a UI object) without the intention of triggering its action; it can also alert the player that they have browsed over an interactable object. This effect type is subtle and does not disrupt the gameplay experience. |
| UIClick | 2 | Useful for when a player has selected an object (often a UI object) with the intention of triggering its action. This effect type is crisp and it provides immediate feedback without being overwhelming. |
| UINotification | 3 | Useful for when there is an inbound message that should draw the player's attention away from their current gameplay and prompt them that the notification requires immediate attention or action. |
| GameplayExplosion | 4 | Useful to signify a large-scale physics event that triggers impact across a large portion of a given scene. This effect is high intensity in order to represent the magnitude of the impact and it lingers for a longer period of time than GameplayCollision. |
| GameplayCollision | 5 | This effect is a large immediate rumble that dies down quickly, useful to signify a clear and purposeful impact between objects. |