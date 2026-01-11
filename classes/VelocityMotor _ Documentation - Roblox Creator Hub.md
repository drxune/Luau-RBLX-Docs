# VelocityMotor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VelocityMotor
Scraped: 2026-01-11T02:38:03.145929Z

## Inherits
- JointInstance
- VelocityMotor
- Hole
- Instance
- Object
- Motor
- MotorFeature
- BasePart
- VelocityMotor.Hole
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [JointInstance](/docs/reference/engine/classes/JointInstance)
6. /
7. [VelocityMotor](/docs/reference/engine/classes/VelocityMotor)

English

Feedback

Engine Class

VelocityMotor

---

Summary

Properties

|  |
| --- |
| [CurrentAngle](#CurrentAngle):[number](/docs/luau/numbers) |
| [DesiredAngle](#DesiredAngle):[number](/docs/luau/numbers) |
| [Hole](#Hole):[Hole](/docs/reference/engine/classes/Hole) |
| [MaxVelocity](#MaxVelocity):[number](/docs/luau/numbers) |

Inherited Members

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The VelocityMotor is a special type of joint that works similarly to a
[Motor](/docs/reference/engine/classes/Motor), but it uses a [MotorFeature](/docs/reference/engine/classes/MotorFeature) and a [Hole](/docs/reference/engine/classes/Hole) to create
the connection. In order for this object to work correctly:

* The VelocityMotor must be parented inside of a [MotorFeature](/docs/reference/engine/classes/MotorFeature)
* The [MotorFeature](/docs/reference/engine/classes/MotorFeature) needs to be parented inside of a [BasePart](/docs/reference/engine/classes/BasePart)
* A [Hole](/docs/reference/engine/classes/Hole) needs to be parented inside of another [BasePart](/docs/reference/engine/classes/BasePart)
* The VelocityMotor's [VelocityMotor.Hole](/docs/reference/engine/classes/VelocityMotor#Hole) property should be assigned
  to the hole you parented inside of the other part.

---

API Reference

Properties

CurrentAngle

Read Parallel

Displays the angle that the motor is at in radians.

VelocityMotor.CurrentAngle:[number](/docs/luau/numbers)

Displays the angle that the motor is at in radians.

Provide feedback

---

DesiredAngle

Read Parallel

The desired angle to be reached. The motor will attempt to reach this
angle.

VelocityMotor.DesiredAngle:[number](/docs/luau/numbers)

The desired angle to be reached. The motor will attempt to reach this
angle.

Provide feedback

---

Hole

Read Parallel

The [Hole](/docs/reference/engine/classes/Hole) linked to this VelocityMotor.

VelocityMotor.Hole:[Hole](/docs/reference/engine/classes/Hole)

The [Hole](/docs/reference/engine/classes/Hole) linked to this VelocityMotor.

Provide feedback

---

MaxVelocity

Read Parallel

The maximum amount of velocity able to be reached.

VelocityMotor.MaxVelocity:[number](/docs/luau/numbers)

The maximum amount of velocity able to be reached.

Provide feedback

---