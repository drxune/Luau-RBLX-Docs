# ControllerPartSensor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ControllerPartSensor
Scraped: 2026-01-11T02:38:03.292441Z

## Inherits
- ControllerSensor
- ControllerPartSensor
- SensorBase
- BasePart
- Humanoid
- Instance
- Object
- BaseParts
- ControllerPartSensor.SensedPart
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ControllerSensor](/docs/reference/engine/classes/ControllerSensor)
6. /
7. [ControllerPartSensor](/docs/reference/engine/classes/ControllerPartSensor)

English

Feedback

Engine Class

ControllerPartSensor

A [SensorBase](/docs/reference/engine/classes/SensorBase) that outputs data about another [BasePart](/docs/reference/engine/classes/BasePart) based on
[Humanoid](/docs/reference/engine/classes/Humanoid) floor and ladder detection logic.

---

Summary

Properties

|  |
| --- |
| [HitFrame](#HitFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [HitNormal](#HitNormal):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [SearchDistance](#SearchDistance):[number](/docs/luau/numbers) |
| [SensedPart](#SensedPart):[BasePart](/docs/reference/engine/classes/BasePart) |
| [SensorMode](#SensorMode):[Enum.SensorMode](/docs/reference/engine/enums/SensorMode) |

Inherited Members

3 inherited from [SensorBase](/docs/reference/engine/classes/SensorBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [SensorBase](/docs/reference/engine/classes/SensorBase) that outputs data about another [BasePart](/docs/reference/engine/classes/BasePart) based on
[Humanoid](/docs/reference/engine/classes/Humanoid) floor and ladder detection logic. It is primarily used for
sending data to a character controller. Using a [ControllerPartSensor](/docs/reference/engine/classes/ControllerPartSensor)
allows you to detect [BaseParts](/docs/reference/engine/classes/BasePart) in the same manner as the
[Humanoid](/docs/reference/engine/classes/Humanoid) uses for detecting floors and ladders.

---

API Reference

Properties

HitFrame

Read Parallel

The position in world space where the sensor hit the
[ControllerPartSensor.SensedPart](/docs/reference/engine/classes/ControllerPartSensor#SensedPart).

ControllerPartSensor.HitFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

The position in world space where the sensor hit the
[ControllerPartSensor.SensedPart](/docs/reference/engine/classes/ControllerPartSensor#SensedPart).

Provide feedback

---

HitNormal

Read Parallel

The surface normal at the position where the sensor hit the
[ControllerPartSensor.SensedPart](/docs/reference/engine/classes/ControllerPartSensor#SensedPart).

ControllerPartSensor.HitNormal:[Vector3](/docs/reference/engine/datatypes/Vector3)

The surface normal at the position where the sensor hit the SensedPart.

Provide feedback

---

SearchDistance

Read Parallel

The distance from the sensor's parent [BasePart](/docs/reference/engine/classes/BasePart) to use when sensing
other parts.

ControllerPartSensor.SearchDistance:[number](/docs/luau/numbers)

The distance from the sensor's parent [BasePart](/docs/reference/engine/classes/BasePart) to use when sensing
other parts.

Provide feedback

---

SensedPart

Read Parallel

A reference to the [BasePart](/docs/reference/engine/classes/BasePart) hit by the sensor.

ControllerPartSensor.SensedPart:[BasePart](/docs/reference/engine/classes/BasePart)

A reference to the [BasePart](/docs/reference/engine/classes/BasePart) hit by the sensor.

Provide feedback

---

SensorMode

Read Parallel

Determines what behavior this [SensorBase](/docs/reference/engine/classes/SensorBase) uses when sensing other
parts.

ControllerPartSensor.SensorMode:[Enum.SensorMode](/docs/reference/engine/enums/SensorMode)

Determines what behavior this [SensorBase](/docs/reference/engine/classes/SensorBase) uses when sensing other
parts.

A setting of [Enum.SensorMode.Ladder](/docs/reference/engine/enums/SensorMode#Ladder) performs the same ladder detection
logic used by a [Humanoid](/docs/reference/engine/classes/Humanoid) to populate sensor output. It currently
always senses along the forward vector of its parent [BasePart](/docs/reference/engine/classes/BasePart).

A setting of [Enum.SensorMode.Floor](/docs/reference/engine/enums/SensorMode#Floor) performs the same floor detection
logic used by a [Humanoid](/docs/reference/engine/classes/Humanoid) to populate sensor output. It currently
always senses along the negative up vector of the world.

Provide feedback

---