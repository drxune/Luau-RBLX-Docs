# HingeConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HingeConstraint
Scraped: 2026-01-11T02:32:30.007058Z

## Tags
- Not Replicated

## Inherits
- Constraint
- HingeConstraint
- Instance
- Object
- Attachments
- ActuatorType
- AngularVelocity
- MotorMaxAcceleration
- MotorMaxTorque
- TargetAngle
- AngularSpeed
- ServoMaxTorque
- LimitsEnabled
- LowerAngle
- UpperAngle
- Restitution
- CurrentAngle
- Attachment
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [HingeConstraint](/docs/reference/engine/classes/HingeConstraint)

English

Feedback

Engine Class

![HingeConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/HingeConstraint-Dark.webp)HingeConstraint

Constrains its attachments to rotate about a single axis.

---

Summary

Properties

|  |
| --- |
| [ActuatorType](#ActuatorType):[Enum.ActuatorType](/docs/reference/engine/enums/ActuatorType) |
| [AngularResponsiveness](#AngularResponsiveness):[number](/docs/luau/numbers) |
| [AngularSpeed](#AngularSpeed):[number](/docs/luau/numbers) |
| [AngularVelocity](#AngularVelocity):[number](/docs/luau/numbers) |
| [CurrentAngle](#CurrentAngle):[number](/docs/luau/numbers) |
| [LimitsEnabled](#LimitsEnabled):[boolean](/docs/luau/booleans) |
| [LowerAngle](#LowerAngle):[number](/docs/luau/numbers) |
| [MotorMaxAcceleration](#MotorMaxAcceleration):[number](/docs/luau/numbers) |
| [MotorMaxTorque](#MotorMaxTorque):[number](/docs/luau/numbers) |
| [Radius](#Radius):[number](/docs/luau/numbers) |
| [Restitution](#Restitution):[number](/docs/luau/numbers) |
| [ServoMaxTorque](#ServoMaxTorque):[number](/docs/luau/numbers) |
| [SoftlockServoUponReachingTarget](#SoftlockServoUponReachingTarget):[boolean](/docs/luau/booleans)  Deprecated |
| [TargetAngle](#TargetAngle):[number](/docs/luau/numbers) |
| [UpperAngle](#UpperAngle):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A HingeConstraint allows two [Attachments](/docs/reference/engine/classes/Attachment) to rotate
about one axis, constraining the two [Attachments](/docs/reference/engine/classes/Attachment) so that
they both occupy the same position and that their X axes point in the same
direction.

Note that if this constraint attaches one part (A) to another part (B)
that is anchored or connected to an anchored part (Z), part A will not
be locally simulated when interacting with a player.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Angular Power

Hinges can be configured to actuate rotation. If a hinge's
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) is set to
[Motor](/docs/reference/engine/enums/ActuatorType), it attempts to rotate the attachments with the goal
of reaching its [AngularVelocity](/docs/reference/engine/classes/HingeConstraint#AngularVelocity). You
can further control this rotation through both
[MotorMaxAcceleration](/docs/reference/engine/classes/HingeConstraint#MotorMaxAcceleration) and
[MotorMaxTorque](/docs/reference/engine/classes/HingeConstraint#MotorMaxTorque). If a hinge's
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType), it attempts to rotate to an angle specified by
[TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle). This rotation is controlled
by both [AngularSpeed](/docs/reference/engine/classes/HingeConstraint#AngularSpeed) and
[ServoMaxTorque](/docs/reference/engine/classes/HingeConstraint#ServoMaxTorque).

#### Limits

You can set limits to restrict the rotation of a hinge, useful for mechanisms
like doors which should only swing open or closed within a set range. Enabling
the [LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) property exposes the
[LowerAngle](/docs/reference/engine/classes/HingeConstraint#LowerAngle) and
[UpperAngle](/docs/reference/engine/classes/HingeConstraint#UpperAngle) limits, as well as
[Restitution](/docs/reference/engine/classes/HingeConstraint#Restitution) which defines the elasticity
of the attachments when they reach either limit.

---

API Reference

Properties

ActuatorType

Read Parallel

Sets whether the rotation of the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) is actuated and,
if so, what kind of actuation it uses.

HingeConstraint.ActuatorType:[Enum.ActuatorType](/docs/reference/engine/enums/ActuatorType)

Sets whether the rotation of the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) is actuated and,
if so, what kind of actuation.

* If [ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) is set to
  [Motor](/docs/reference/engine/enums/ActuatorType), the hinge will attempt to rotate the
  attachments with the goal of reaching
  [AngularVelocity](/docs/reference/engine/classes/HingeConstraint#AngularVelocity). This rotation
  is limited by both
  [MotorMaxAcceleration](/docs/reference/engine/classes/HingeConstraint#MotorMaxAcceleration) and
  [MotorMaxTorque](/docs/reference/engine/classes/HingeConstraint#MotorMaxTorque).
* If [ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) is set to
  [Servo](/docs/reference/engine/enums/ActuatorType), the hinge will attempt to rotate to an angle
  specified by [TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle). This
  rotation is limited by both
  [AngularSpeed](/docs/reference/engine/classes/HingeConstraint#AngularSpeed) and
  [ServoMaxTorque](/docs/reference/engine/classes/HingeConstraint#ServoMaxTorque).

Note that both actuated and free spinning rotation can be limited by
setting [LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) to true.

Provide feedback

---

AngularResponsiveness

Read Parallel

Specifies the sharpness of the servo motor in reaching the
[TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle).

HingeConstraint.AngularResponsiveness:[number](/docs/luau/numbers)

This property specifies the sharpness of the servo motor in reaching the
[TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle), when
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType). Larger values correspond to a faster response
and smaller values results in more damping and a slower response.

Provide feedback

---

AngularSpeed

Read Parallel

The desired angular speed a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Servo](/docs/reference/engine/enums/ActuatorType) will attempt to maintain while rotating towards
its [TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle). Measured in
radians/second.

HingeConstraint.AngularSpeed:[number](/docs/luau/numbers)

The desired angular speed a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Servo](/docs/reference/engine/enums/ActuatorType) will attempt to maintain while rotating towards
its [TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle). Measured in
radians/second.

Provide feedback

---

AngularVelocity

Read Parallel

The angular velocity a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Motor](/docs/reference/engine/enums/ActuatorType) will attempt to achieve. Measured in
radians/second.

HingeConstraint.AngularVelocity:[number](/docs/luau/numbers)

The angular velocity a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Motor](/docs/reference/engine/enums/ActuatorType) will attempt to achieve. Measured in
radians/second.

Provide feedback

---

CurrentAngle

Read Only

Not Replicated

Read Parallel

The current angle of the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint).

HingeConstraint.CurrentAngle:[number](/docs/luau/numbers)

The current angle of the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint). This angle is calculated
by measuring the angle separation of the Y axes of the
[Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

LimitsEnabled

Read Parallel

Sets whether the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will limit the range of rotation.

HingeConstraint.LimitsEnabled:[boolean](/docs/luau/booleans)

Sets whether the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will limit the range of rotation.
If enabled, the constraint will only allow the
[CurrentAngle](/docs/reference/engine/classes/HingeConstraint#CurrentAngle) to be between
[LowerAngle](/docs/reference/engine/classes/HingeConstraint#LowerAngle) and
[UpperAngle](/docs/reference/engine/classes/HingeConstraint#UpperAngle). If the [Attachment](/docs/reference/engine/classes/Attachment)
reach the end of the limited range of rotation then they will stop
rotating. If [Restitution](/docs/reference/engine/classes/HingeConstraint#Restitution) is greater
than 0 then the attachments will bounce when they hit the ends of the
limited range.

Provide feedback

---

LowerAngle

Read Parallel

The minimum rotation angle the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will allow if
[LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) is true.

HingeConstraint.LowerAngle:[number](/docs/luau/numbers)

The minimum rotation angle the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will allow if
[LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) is true. Measured in
degrees.

Provide feedback

---

MotorMaxAcceleration

Read Parallel

The maximum angular acceleration a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Motor](/docs/reference/engine/enums/ActuatorType) can apply to achieve its
[AngularVelocity](/docs/reference/engine/classes/HingeConstraint#AngularVelocity). Measured in
radians/second².

HingeConstraint.MotorMaxAcceleration:[number](/docs/luau/numbers)

The maximum angular acceleration a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Motor](/docs/reference/engine/enums/ActuatorType) can apply to achieve its
[AngularVelocity](/docs/reference/engine/classes/HingeConstraint#AngularVelocity). Measured in
radians/second².

Provide feedback

---

MotorMaxTorque

Read Parallel

The maximum torque a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Motor](/docs/reference/engine/enums/ActuatorType) can apply when trying to reach its desired
[AngularVelocity](/docs/reference/engine/classes/HingeConstraint#AngularVelocity).

HingeConstraint.MotorMaxTorque:[number](/docs/luau/numbers)

The maximum torque a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Motor](/docs/reference/engine/enums/ActuatorType) can apply when trying to reach its desired
[AngularVelocity](/docs/reference/engine/classes/HingeConstraint#AngularVelocity).

Provide feedback

---

Radius

Read Parallel

The visualized radius of the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint).

HingeConstraint.Radius:[number](/docs/luau/numbers)

The visualized radius of the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint).

Provide feedback

---

Restitution

Read Parallel

How elastic [Attachment](/docs/reference/engine/classes/Attachment) connected by a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will
be when they reach the end of the range when
[LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) is true. Constrained
between 0 and 1.

HingeConstraint.Restitution:[number](/docs/luau/numbers)

How elastic [Attachment](/docs/reference/engine/classes/Attachment) connected by a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will
be when they reach the end of the range when
[LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) is true. Constrained
between 0 and 1.

Provide feedback

---

ServoMaxTorque

Read Parallel

The maximum torque a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Servo](/docs/reference/engine/enums/ActuatorType) can apply when trying to reach its desired
[TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle).

HingeConstraint.ServoMaxTorque:[number](/docs/luau/numbers)

The maximum torque a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) with
[ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) set to
[Servo](/docs/reference/engine/enums/ActuatorType) can apply when trying to reach its desired
[TargetAngle](/docs/reference/engine/classes/HingeConstraint#TargetAngle).

Provide feedback

---

SoftlockServoUponReachingTarget

Deprecated

Show details

---

TargetAngle

Read Parallel

The target angle a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will attempt to rotate to if
its [ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType). Measured in degrees.

HingeConstraint.TargetAngle:[number](/docs/luau/numbers)

The target angle a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will attempt to rotate to if
its [ActuatorType](/docs/reference/engine/classes/HingeConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType). Measured in degrees.

Provide feedback

---

UpperAngle

Read Parallel

The maximum rotation angle the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will allow if
[LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) is true.

HingeConstraint.UpperAngle:[number](/docs/luau/numbers)

The maximum rotation angle the [HingeConstraint](/docs/reference/engine/classes/HingeConstraint) will allow if
[LimitsEnabled](/docs/reference/engine/classes/HingeConstraint#LimitsEnabled) is true. Measured in
degrees.

Provide feedback

---