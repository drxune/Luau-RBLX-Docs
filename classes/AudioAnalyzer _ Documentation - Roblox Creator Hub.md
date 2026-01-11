# AudioAnalyzer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioAnalyzer
Scraped: 2026-01-11T02:28:20.023124Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- AudioAnalyzer
- Wires
- Wire
- PeakLevel
- GetSpectrum
- GetSpectrum()
- AudioDeviceInput
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer)

English

Feedback

Engine Class

![AudioAnalyzer](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioAnalyzer-Dark.webp)AudioAnalyzer

Takes measurements from audio streams that are connected to it via one or more
[Wires](/docs/reference/engine/classes/Wire).

---

Summary

Properties

|  |
| --- |
| [PeakLevel](#PeakLevel):[number](/docs/luau/numbers) |
| [RmsLevel](#RmsLevel):[number](/docs/luau/numbers) |
| [SpectrumEnabled](#SpectrumEnabled):[boolean](/docs/luau/booleans) |
| [WindowSize](#WindowSize):[Enum.AudioWindowSize](/docs/reference/engine/enums/AudioWindowSize) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |
| [GetSpectrum](#GetSpectrum)():[Array](/docs/luau/tables#arrays) |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) takes measurements from audio streams that are wired to
it through [Wire](/docs/reference/engine/classes/Wire). It provides a single Input pin but does not
produce any output streams. Note that all audio processing is disabled on the
server in order to conserve resources; Properties and methods of
[AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) return empty or zero results when used from server
scripts.

---

API Reference

Properties

PeakLevel

Read Only

Not Replicated

Read Parallel

The loudest volume observed during the last audio buffer.

AudioAnalyzer.PeakLevel:[number](/docs/luau/numbers)

The loudest volume observed during the last audio buffer. This property
changes more often than the framerate and does not fire changed events. On
the server, this property is always 0.

Provide feedback

---

RmsLevel

Read Only

Not Replicated

Read Parallel

The root-mean-square average volume observed during the last audio buffer.

AudioAnalyzer.RmsLevel:[number](/docs/luau/numbers)

The root-mean-square average volume observed during the last audio buffer.
This property is generally more stable than
[PeakLevel](/docs/reference/engine/classes/AudioAnalyzer#PeakLevel) but it may not capture momentary
volume spikes. This property changes more often than the framerate and
does not fire changed events. On the server, this property is always 0.

Provide feedback

---

SpectrumEnabled

Read Parallel

Enables usage of [GetSpectrum](/docs/reference/engine/classes/AudioAnalyzer#GetSpectrum).

AudioAnalyzer.SpectrumEnabled:[boolean](/docs/luau/booleans)

Enables usage of [GetSpectrum()](/docs/reference/engine/classes/AudioAnalyzer#GetSpectrum). If
false, [GetSpectrum()](/docs/reference/engine/classes/AudioAnalyzer#GetSpectrum) returns an empty
array, but the CPU overhead of the [AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) is dramatically
reduced. This means that if you are only analyzing the volume of an
audio stream, you can disable this property to improve performance.

Provide feedback

---

WindowSize

Read Parallel

AudioAnalyzer.WindowSize:[Enum.AudioWindowSize](/docs/reference/engine/enums/AudioWindowSize)

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioAnalyzer:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) has one "Input" pin.

Provide feedback

---

GetInputPins

AudioAnalyzer:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioAnalyzer:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetSpectrum

Returns the frequency spectrum of the last audio buffer.

AudioAnalyzer:GetSpectrum():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns the frequency spectrum of the last audio buffer, as an array of
numbers. The elements of the array are root-mean-square volume levels,
evenly spaced from 0 hertz to 24,000 hertz. If any of the analyzer's
inputs come from an [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput), or this method is used from
a server script, it returns an empty array.

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) via a [Wire](/docs/reference/engine/classes/Wire).

AudioAnalyzer.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer) and to some other wirable instance.

Provide feedback

---