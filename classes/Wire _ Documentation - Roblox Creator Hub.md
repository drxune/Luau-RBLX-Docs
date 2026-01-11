# Wire | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Wire
Scraped: 2026-01-11T02:30:47.563280Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Wire
- Instances
- Wires
- AudioAnalyzer
- AudioChannelMixer
- AudioChannelSplitter
- AudioCompressor
- AudioDeviceInput
- AudioDeviceOutput
- AudioDistortion
- AudioEcho
- AudioEmitter
- AudioEqualizer
- AudioFader
- AudioFilter
- AudioFlanger
- AudioLimiter
- AudioListener
- AudioPitchShifter
- AudioPlayer
- AudioRecorder
- AudioReverb
- AudioSpeechToText
- AudioTextToSpeech
- SourceInstance
- TargetInstance
- SourceName
- TargetName
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Wire](/docs/reference/engine/classes/Wire)

English

Feedback

Engine Class

![Wire](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Wire-Dark.webp)Wire

Connects one or more [Instances](/docs/reference/engine/classes/Instance) to form a processing graph of
their streams. At the moment, only audio streams are supported, but this may
expand in the future.

---

Summary

Properties

|  |
| --- |
| [Connected](#Connected):[boolean](/docs/luau/booleans) |
| [SourceInstance](#SourceInstance):[Instance](/docs/reference/engine/datatypes/Instance) |
| [SourceName](#SourceName):[string](/docs/luau/strings) |
| [TargetInstance](#TargetInstance):[Instance](/docs/reference/engine/datatypes/Instance) |
| [TargetName](#TargetName):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[Wire](/docs/reference/engine/classes/Wire) connects one or more [Instances](/docs/reference/engine/classes/Instance) to form a
processing graph of their streams. Each [Wire](/docs/reference/engine/classes/Wire) connects a source and
target instance, and a source and target "pin" within each of those instances.
Pins are string identifiers that select which stream is to be carried by the
wire.

At the moment, only audio streams are supported, but this may expand in the
future.

The following instances may be connected by [Wires](/docs/reference/engine/classes/Wire):

* [AudioAnalyzer](/docs/reference/engine/classes/AudioAnalyzer)
* [AudioChannelMixer](/docs/reference/engine/classes/AudioChannelMixer)
* [AudioChannelSplitter](/docs/reference/engine/classes/AudioChannelSplitter)
* [AudioCompressor](/docs/reference/engine/classes/AudioCompressor)
* [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput)
* [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput)
* [AudioDistortion](/docs/reference/engine/classes/AudioDistortion)
* [AudioEcho](/docs/reference/engine/classes/AudioEcho)
* [AudioEmitter](/docs/reference/engine/classes/AudioEmitter)
* [AudioEqualizer](/docs/reference/engine/classes/AudioEqualizer)
* [AudioFader](/docs/reference/engine/classes/AudioFader)
* [AudioFilter](/docs/reference/engine/classes/AudioFilter)
* [AudioFlanger](/docs/reference/engine/classes/AudioFlanger)
* [AudioLimiter](/docs/reference/engine/classes/AudioLimiter)
* [AudioListener](/docs/reference/engine/classes/AudioListener)
* [AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter)
* [AudioPlayer](/docs/reference/engine/classes/AudioPlayer)
* [AudioRecorder](/docs/reference/engine/classes/AudioRecorder)
* [AudioReverb](/docs/reference/engine/classes/AudioReverb)
* [AudioSpeechToText](/docs/reference/engine/classes/AudioSpeechToText)
* [AudioTextToSpeech](/docs/reference/engine/classes/AudioTextToSpeech)

---

API Reference

Properties

Connected

Read Only

Not Replicated

Read Parallel

Denotes whether the [Wire](/docs/reference/engine/classes/Wire) is carrying a stream of data.

Wire.Connected:[boolean](/docs/luau/booleans)

Denotes whether the [Wire](/docs/reference/engine/classes/Wire) is connected, meaning its
[SourceInstance](/docs/reference/engine/classes/Wire#SourceInstance),
[TargetInstance](/docs/reference/engine/classes/Wire#TargetInstance),
[SourceName](/docs/reference/engine/classes/Wire#SourceName), and [TargetName](/docs/reference/engine/classes/Wire#TargetName)
properties are all assigned, the connection is valid, and the connection
does not result in a cyclic processing graph. Cyclic processing graphs are
invalid since they can result in infinite computation; attempting to
create one will log an error.

Provide feedback

---

SourceInstance

Read Parallel

The [Instance](/docs/reference/engine/classes/Instance) producing a stream to be carried over the wire.

Wire.SourceInstance:[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) producing a stream to be carried over the wire. At
the moment, only audio streams are wirable.

Provide feedback

---

SourceName

Read Parallel

The name of the pin on [SourceInstance](/docs/reference/engine/classes/Wire#SourceInstance) that is
producing a stream.

Wire.SourceName:[string](/docs/luau/strings)

The name of the pin on [SourceInstance](/docs/reference/engine/classes/Wire#SourceInstance) that is
producing a stream. At the moment, various audio instances only have an
Output pin, but this may expand in the future. The default value of
this property is Output so it is not yet necessary to change.

Provide feedback

---

TargetInstance

Read Parallel

The [Instance](/docs/reference/engine/classes/Instance) to receive a stream from
[SourceInstance](/docs/reference/engine/classes/Wire#SourceInstance).

Wire.TargetInstance:[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) intended to receive a stream from
[SourceInstance](/docs/reference/engine/classes/Wire#SourceInstance). Currently, only audio streams
are wirable.

Provide feedback

---

TargetName

Read Parallel

The name of the pin on [TargetInstance](/docs/reference/engine/classes/Wire#TargetInstance) that is
receiving a stream.

Wire.TargetName:[string](/docs/luau/strings)

The name of the pin on [TargetInstance](/docs/reference/engine/classes/Wire#TargetInstance) that is
receiving a stream. At the moment, audio instances typically have an
Input pin, but [AudioCompressor](/docs/reference/engine/classes/AudioCompressor) has an additional Sidechain
pin. This may expand in the future.

Provide feedback

---