# Motor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Motor
Scraped: 2026-01-11T02:31:14.418035Z

## Tags
- Not Replicated

## Inherits
- JointInstance
- Motor
- Instance
- Object
- Motor6D
- Motor.MaxVelocity
- Motor.DesiredAngle
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [JointInstance](/docs/reference/engine/classes/JointInstance)
6. /
7. [Motor](/docs/reference/engine/classes/Motor)

English

Feedback

Engine Class

Motor

Makes a movable [JointInstance](/docs/reference/engine/classes/JointInstance) between two parts.

---

Summary

Properties

|  |
| --- |
| [CurrentAngle](#CurrentAngle):[number](/docs/luau/numbers) |
| [DesiredAngle](#DesiredAngle):[number](/docs/luau/numbers) |
| [MaxVelocity](#MaxVelocity):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [SetDesiredAngle](#SetDesiredAngle)(value: [number](/docs/luau/numbers)):() |

Inherited Members

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Motor6D](/docs/reference/engine/classes/Motor6D)

An object used to make movable [JointInstance](/docs/reference/engine/classes/JointInstance) between two Parts.

---

API Reference

Properties

CurrentAngle

Not Replicated

Read Parallel

Displays the current rotation of the motor in radians.

Motor.CurrentAngle:[number](/docs/luau/numbers)

Displays the current rotation of the motor in radians.

Provide feedback

---

DesiredAngle

Read Parallel

The desired angle to turn the motor to in radians.

Motor.DesiredAngle:[number](/docs/luau/numbers)

The desired angle to turn the motor to in radians. The motor will attempt
to reach this angle (provided [Motor.MaxVelocity](/docs/reference/engine/classes/Motor#MaxVelocity) is greater than 0.

Provide feedback

---

MaxVelocity

Read Parallel

The maximum velocity the motor can use to reach [Motor.DesiredAngle](/docs/reference/engine/classes/Motor#DesiredAngle)
measured in radians per physics frame (1/60th of a second).

Motor.MaxVelocity:[number](/docs/luau/numbers)

The maximum velocity the motor can use to reach [Motor.DesiredAngle](/docs/reference/engine/classes/Motor#DesiredAngle)
measured in radians per physics frame (1/60th of a second).

Provide feedback

---

Methods

SetDesiredAngle

Sets [Motor.DesiredAngle](/docs/reference/engine/classes/Motor#DesiredAngle) of the motor.

Motor:SetDesiredAngle(value:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| value:[number](/docs/luau/numbers) |

Returns

()

Sets [Motor.DesiredAngle](/docs/reference/engine/classes/Motor#DesiredAngle) of the motor.

Provide feedback

---