# RollOffMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/RollOffMode
Scraped: 2026-01-11T02:42:32.462202Z

## Inherits
- Sounds
- BasePart
- Attachment
- Sound.RollOffMinDistance
- Sound.RollOffMaxDistance
1. [Enums](/docs/reference/engine/enums)
2. /
3. [RollOffMode](/docs/reference/engine/enums/RollOffMode)

English

Feedback

Engine Enum

RollOffMode

---

Enum which determines how [Sounds](/docs/reference/engine/classes/Sound) parented to a [BasePart](/docs/reference/engine/classes/BasePart)
or [Attachment](/docs/reference/engine/classes/Attachment) attenuate (fade out) as the distance between the
listener and the parent increases.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Inverse | 0 | Volume attenuates from [Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance) in an inverse manner, mirroring how sounds attenuate in the real world. This is done through [Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance)/distance, where distance is the [Vector3.Magnitude](/docs/reference/engine/datatypes/Vector3#Magnitude) between the audio source and the audio listener. |
| Linear | 1 | Volume attenuates between [Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance) and [Sound.RollOffMaxDistance](/docs/reference/engine/classes/Sound#RollOffMaxDistance) with a linear relationship. This is done through ([Sound.RollOffMaxDistance](/docs/reference/engine/classes/Sound#RollOffMaxDistance)/distance)/([Sound.RollOffMaxDistance](/docs/reference/engine/classes/Sound#RollOffMaxDistance)-[Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance)), where distance is the [Vector3.Magnitude](/docs/reference/engine/datatypes/Vector3#Magnitude) between the audio source and the audio listener. |
| LinearSquare | 2 | Volume attenuates between [Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance) and [Sound.RollOffMaxDistance](/docs/reference/engine/classes/Sound#RollOffMaxDistance) with a linear squared relationship. This is done through squaring Linear. |
| InverseTapered | 3 | A hybrid model which follows the Inverse model when close to [Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance) and the LinearSquare model when close to [Sound.RollOffMaxDistance](/docs/reference/engine/classes/Sound#RollOffMaxDistance). This is done by taking the lesser of Inverse and LinearSquare. |