# SensorBase | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SensorBase
Scraped: 2026-01-11T02:30:51.333776Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- SensorBase
- AtmosphereSensor
- BuoyancySensor
- ControllerSensor
- FluidForceSensor
- BasePart
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [SensorBase](/docs/reference/engine/classes/SensorBase)

English

Feedback

Engine Class

SensorBase

An abstract class for various sensor instance types.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [UpdateType](#UpdateType):[Enum.SensorUpdateType](/docs/reference/engine/enums/SensorUpdateType) |

Methods

|  |
| --- |
| [Sense](#Sense)():()  Deprecated |

Events

|  |
| --- |
| [OnSensorOutputChanged](#OnSensorOutputChanged)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[AtmosphereSensor](/docs/reference/engine/classes/AtmosphereSensor), [BuoyancySensor](/docs/reference/engine/classes/BuoyancySensor), [ControllerSensor](/docs/reference/engine/classes/ControllerSensor), [FluidForceSensor](/docs/reference/engine/classes/FluidForceSensor)

A [SensorBase](/docs/reference/engine/classes/SensorBase) is an instance that, when parented to a [BasePart](/docs/reference/engine/classes/BasePart),
outputs additional data about the world around that part. This data is
presented in the sensor's "output" property category. Often, other systems
will consume the sensor's output data.

---

API Reference

Properties

UpdateType

Read Parallel

Determines how the sensor will update its output data.

SensorBase.UpdateType:[Enum.SensorUpdateType](/docs/reference/engine/enums/SensorUpdateType)

Determines how the sensor will update its output data.

With [Enum.SensorUpdateType.OnRead](/docs/reference/engine/enums/SensorUpdateType#OnRead), internal sensor logic is run so that
the output properties are always up to date. In this mode, the sensor will
only run if you read the properties and they are currently outdated.

With [Enum.SensorUpdateType.Manual](/docs/reference/engine/enums/SensorUpdateType#Manual), the output properties will never
change. Instead, you can write your own scripts to set the output
properties as you like.

Provide feedback

---

Methods

Sense

Deprecated

Show details

---

Events

OnSensorOutputChanged

SensorBase.OnSensorOutputChanged():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Provide feedback

---