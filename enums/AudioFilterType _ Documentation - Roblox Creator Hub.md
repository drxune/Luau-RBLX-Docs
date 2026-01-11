# AudioFilterType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AudioFilterType
Scraped: 2026-01-11T02:42:57.810675Z

## Inherits
- AudioFilter
- Frequency
- Gain
- Q
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AudioFilterType](/docs/reference/engine/enums/AudioFilterType)

English

Feedback

Engine Enum

AudioFilterType

---

Families of curves that [AudioFilter](/docs/reference/engine/classes/AudioFilter) can use to process incoming audio.
Each filter type is applied at a specified
[Frequency](/docs/reference/engine/classes/AudioFilter#Frequency) and may be shaped by additional
[Gain](/docs/reference/engine/classes/AudioFilter#Gain) or [Q](/docs/reference/engine/classes/AudioFilter#Q) parameters.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Peak | 0 | Filter that boosts or reduces sound near a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency). |
| LowShelf | 1 | Filter that boosts or reduces sound below a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency). |
| HighShelf | 2 | Filter that boosts or reduces sound above a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency). |
| Lowpass12dB | 3 | Filter that cuts sound above a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency), at a slope of -12dB/octave. |
| Lowpass24dB | 4 | Filter that cuts sound above a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency), at a slope of -24dB/octave. |
| Lowpass48dB | 5 | Filter that cuts sound above a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency), at a slope of -48dB/octave. |
| Highpass12dB | 6 | Filter that cuts sound below a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency), at a slope of -12dB/octave. |
| Highpass24dB | 7 | Filter that cuts sound below a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency), at a slope of -24dB/octave. |
| Highpass48dB | 8 | Filter that cuts sound below a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency), at a slope of -48dB/octave. |
| Bandpass | 9 | Filter that only allows sound near a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency) to be heard. |
| Notch | 10 | Filter that cuts sound near a specified [Frequency](/docs/reference/engine/classes/AudioFilter#Frequency). |
| Lowpass6dB | 11 |  |