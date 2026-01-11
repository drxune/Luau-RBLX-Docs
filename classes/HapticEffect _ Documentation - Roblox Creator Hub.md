# HapticEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HapticEffect
Scraped: 2026-01-11T02:39:16.031020Z

## Inherits
- Object
- Instance
- HapticEffect
- FloatCurve
- Radius
- Position
- SetWaveformKeys()
- Looped
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [HapticEffect](/docs/reference/engine/classes/HapticEffect)

English

Feedback

Engine Class

![HapticEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/HapticEffect-Dark.webp)HapticEffect

---

Summary

Properties

|  |
| --- |
| [Looped](#Looped):[boolean](/docs/luau/booleans) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Radius](#Radius):[number](/docs/luau/numbers) |
| [Type](#Type):[Enum.HapticEffectType](/docs/reference/engine/enums/HapticEffectType) |
| [Waveform](#Waveform):[FloatCurve](/docs/reference/engine/classes/FloatCurve)  Deprecated |

Methods

|  |
| --- |
| [Play](#Play)():() |
| [SetWaveformKeys](#SetWaveformKeys)(keys: [Array](/docs/luau/tables#arrays)):() |
| [Stop](#Stop)():() |

Events

|  |
| --- |
| [Ended](#Ended)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Modern controllers and devices have motors built‑in to provide haptic
feedback. Adding rumbles and vibrations can provide subtle feedback that is
hard to convey through visuals or audio.

Roblox supports haptics for the following devices:

* Android and iOS phones supporting haptics including most iPhone, Pixel, and
  Samsung Galaxy devices
* PlayStation gamepads
* Xbox gamepads
* Quest Touch controller

---

API Reference

Properties

Looped

Read Parallel

Whether the haptic effect loops continuously.

HapticEffect.Looped:[boolean](/docs/luau/booleans)

Whether the haptic effect loops continuously.

```
local Workspace = game:GetService("Workspace")



local effect = Instance.new("HapticEffect")



effect.Type = Enum.HapticEffectType.GameplayExplosion



effect.Looped = true



effect.Parent = Workspace



-- Start the haptic effect



effect:Play()



-- After two seconds, stop the effect



task.wait(2)



effect:Stop()
```

Provide feedback

---

Position

Read Parallel

Along with [Radius](/docs/reference/engine/classes/HapticEffect#Radius), specifies the impact
position relative to the input device and, effectively, how broadly that
impact effects nearby motors.

HapticEffect.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

Along with [Radius](/docs/reference/engine/classes/HapticEffect#Radius), specifies the impact
position relative to the input device and, effectively, how broadly that
impact effects nearby motors. Note that some gamepads do not have both
"small" and "large" motors, and that "gamepad large left/right" is not
supported on PC.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/HapticEffect/Position-Radius.png)

```
local Workspace = game:GetService("Workspace")



local effect = Instance.new("HapticEffect")



-- Set the position and radius of impact



effect.Position = Vector3.new(0.5, 0.5, 0)



effect.Radius = 1



effect.Parent = Workspace



effect:Play()
```

Provide feedback

---

Radius

Read Parallel

Along with [Position](/docs/reference/engine/classes/HapticEffect#Position), specifies the impact
radius relative to the input device and, effectively, how broadly that
impact effects nearby motors.

HapticEffect.Radius:[number](/docs/luau/numbers)

Along with [Position](/docs/reference/engine/classes/HapticEffect#Position), specifies the impact
radius relative to the input device and, effectively, how broadly that
impact effects nearby motors. Note that some gamepads do not have both
"small" and "large" motors, and that "gamepad large left/right" is not
supported on PC.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/HapticEffect/Position-Radius.png)

```
local Workspace = game:GetService("Workspace")



local effect = Instance.new("HapticEffect")



-- Set the position and radius of impact



effect.Position = Vector3.new(0.5, 0.5, 0)



effect.Radius = 1



effect.Parent = Workspace



-- Play the haptic effect



effect:Play()
```

Provide feedback

---

Type

Read Parallel

[Enum.HapticEffectType](/docs/reference/engine/enums/HapticEffectType) describing the haptic type.

HapticEffect.Type:[Enum.HapticEffectType](/docs/reference/engine/enums/HapticEffectType)

The haptic type, such as [Enum.HapticEffectType.GameplayCollision](/docs/reference/engine/enums/HapticEffectType#GameplayCollision) for a
large immediate rumble that dies down quickly. The
[Enum.HapticEffectType.Custom](/docs/reference/engine/enums/HapticEffectType#Custom) value lets you specify a haptic with custom
waveform keys defined through
[SetWaveformKeys()](/docs/reference/engine/classes/HapticEffect#SetWaveformKeys).

Provide feedback

---

Waveform

Deprecated

Show details

---

Methods

Play

Plays the haptic effect.

HapticEffect:Play():()

Returns

()

Plays the haptic effect.

```
local Workspace = game:GetService("Workspace")



local effect = Instance.new("HapticEffect")



effect.Type = Enum.HapticEffectType.GameplayExplosion



effect.Parent = Workspace



-- Play the haptic effect



effect:Play()
```

Provide feedback

---

SetWaveformKeys

Method used to define a custom waveform as a table and apply it to the
haptic.

HapticEffect:SetWaveformKeys(keys:[Array](/docs/luau/tables#arrays)):()

Parameters

|  |
| --- |
| keys:[Array](/docs/luau/tables#arrays) |

Returns

()

This method lets you define a custom waveform as a table and apply it to
the haptic.

```
local Workspace = game:GetService("Workspace")



local effect = Instance.new("HapticEffect")



-- Set effect type to custom in order to define a waveform



effect.Type = Enum.HapticEffectType.Custom



effect.Parent = Workspace



-- Define the custom waveform curve through a table



local rampUpWaveform = {



FloatCurveKey.new(0, 0.3),



FloatCurveKey.new(100, 0.4),



FloatCurveKey.new(300, 0.8),



FloatCurveKey.new(400, 1.0)



}



-- Set waveform through the effect's method



effect:SetWaveformKeys(rampUpWaveform)
```

Provide feedback

---

Stop

Stops the haptic effect.

HapticEffect:Stop():()

Returns

()

Stops the haptic effect.

```
local Workspace = game:GetService("Workspace")



local effect = Instance.new("HapticEffect")



effect.Type = Enum.HapticEffectType.GameplayExplosion



effect.Looped = true



effect.Parent = Workspace



-- Start the haptic effect



effect:Play()



-- After two seconds, stop the effect



task.wait(2)



effect:Stop()
```

Provide feedback

---

Events

Ended

Fires when the [HapticEffect](/docs/reference/engine/classes/HapticEffect) has completed playback and stopped.

HapticEffect.Ended():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the [HapticEffect](/docs/reference/engine/classes/HapticEffect) has completed playback and stopped.
Note this event will not fire for haptics with
[Looped](/docs/reference/engine/classes/HapticEffect#Looped) set to true since they continue
playing upon reaching the end. This event will also not fire when the
haptic is stopped before playback has completed.

This event is often used to destroy an [HapticEffect](/docs/reference/engine/classes/HapticEffect) when it has
completed playback.

Provide feedback

---