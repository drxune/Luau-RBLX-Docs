# FluidForceSensor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/FluidForceSensor
Scraped: 2026-01-11T02:37:46.099083Z

## Tags
- Not Replicated

## Inherits
- SensorBase
- FluidForceSensor
- Force
- Torque
- CenterOfPressure
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SensorBase](/docs/reference/engine/classes/SensorBase)
6. /
7. [FluidForceSensor](/docs/reference/engine/classes/FluidForceSensor)

English

Feedback

Engine Class

FluidForceSensor

A [SensorBase](/docs/reference/engine/classes/SensorBase) that outputs [Force](/docs/reference/engine/classes/FluidForceSensor#Force),
[Torque](/docs/reference/engine/classes/FluidForceSensor#Torque) and
[CenterOfPressure](/docs/reference/engine/classes/FluidForceSensor#CenterOfPressure).

---

Summary

Properties

|  |
| --- |
| [CenterOfPressure](#CenterOfPressure):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Force](#Force):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Torque](#Torque):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [EvaluateAsync](#EvaluateAsync)(linearVelocity: [Vector3](/docs/reference/engine/datatypes/Vector3),angularVelocity: [Vector3](/docs/reference/engine/datatypes/Vector3),cframe: [CFrame](/docs/reference/engine/datatypes/CFrame)):[Tuple](/docs/luau/tuples) |

Inherited Members

3 inherited from [SensorBase](/docs/reference/engine/classes/SensorBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

FluidForceSensor is a [SensorBase](/docs/reference/engine/classes/SensorBase) which outputs the results of fluid
force simulation from the last physics frame for the part it is attached to.
The sensor outputs the [Force](/docs/reference/engine/classes/FluidForceSensor#Force),
[Torque](/docs/reference/engine/classes/FluidForceSensor#Torque) and
[CenterOfPressure](/docs/reference/engine/classes/FluidForceSensor#CenterOfPressure) which were computed
by the fluid force simulation on the last physics frame.

---

API Reference

Properties

CenterOfPressure

Read Only

Not Replicated

Read Parallel

Assembly center of pressure offset from its center of mass in world
coordinates.

FluidForceSensor.CenterOfPressure:[Vector3](/docs/reference/engine/datatypes/Vector3)

Assembly center of pressure offset from its center of mass in world
coordinates.

Provide feedback

---

Force

Read Only

Not Replicated

Read Parallel

Assembly fluid force in world coordinates.

FluidForceSensor.Force:[Vector3](/docs/reference/engine/datatypes/Vector3)

Assembly fluid force in world coordinates.

Provide feedback

---

Torque

Read Only

Not Replicated

Read Parallel

Assembly fluid torque in world coordinates.

FluidForceSensor.Torque:[Vector3](/docs/reference/engine/datatypes/Vector3)

Assembly fluid torque in world coordinates.

Provide feedback

---

Methods

EvaluateAsync

Yields

Asynchronously computes force, torque, and center of pressure for the
parent part of a sensor given provided inputs.

FluidForceSensor:EvaluateAsync(

linearVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3), angularVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3), cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| linearVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)  Linear velocity in world coordinates. |
| angularVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)  Angular velocity in world coordinates. |
| cframe:[CFrame](/docs/reference/engine/datatypes/CFrame)  [CFrame](/docs/reference/engine/datatypes/CFrame) to be used for evaluation. |

Returns

[Tuple](/docs/luau/tuples)

Tuple of [Force](/docs/reference/engine/classes/FluidForceSensor#Force),
[Torque](/docs/reference/engine/classes/FluidForceSensor#Torque) and
[CenterOfPressure](/docs/reference/engine/classes/FluidForceSensor#CenterOfPressure) calculated
given the input parameters.

Asynchronously computes force, torque, and center of pressure for the
parent part of a sensor given provided inputs.

Provide feedback

---