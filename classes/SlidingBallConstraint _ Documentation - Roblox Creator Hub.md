# SlidingBallConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SlidingBallConstraint
Scraped: 2026-01-11T02:31:37.173805Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Constraint
- SlidingBallConstraint
- Instance
- Object
- CylindricalConstraint
- PrismaticConstraint
- ActuatorType
- Velocity
- MotorMaxAcceleration
- MotorMaxForce
- TargetPosition
- Speed
- LinearResponsiveness
- ServoMaxForce
- LimitsEnabled
- LowerLimit
- UpperLimit
- Restitution
- Attachments
- Attachment0
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint)

English

Feedback

Engine Class

SlidingBallConstraint

The base class for constraints that allow their attachments to slide along an
axis but not rotate.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [ActuatorType](#ActuatorType):[Enum.ActuatorType](/docs/reference/engine/enums/ActuatorType) |
| [CurrentPosition](#CurrentPosition):[number](/docs/luau/numbers) |
| [LimitsEnabled](#LimitsEnabled):[boolean](/docs/luau/booleans) |
| [LinearResponsiveness](#LinearResponsiveness):[number](/docs/luau/numbers) |
| [LowerLimit](#LowerLimit):[number](/docs/luau/numbers) |
| [MotorMaxAcceleration](#MotorMaxAcceleration):[number](/docs/luau/numbers) |
| [MotorMaxForce](#MotorMaxForce):[number](/docs/luau/numbers) |
| [Restitution](#Restitution):[number](/docs/luau/numbers) |
| [ServoMaxForce](#ServoMaxForce):[number](/docs/luau/numbers) |
| [Size](#Size):[number](/docs/luau/numbers) |
| [SoftlockServoUponReachingTarget](#SoftlockServoUponReachingTarget):[boolean](/docs/luau/booleans)  Deprecated |
| [Speed](#Speed):[number](/docs/luau/numbers) |
| [TargetPosition](#TargetPosition):[number](/docs/luau/numbers) |
| [UpperLimit](#UpperLimit):[number](/docs/luau/numbers) |
| [Velocity](#Velocity):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[CylindricalConstraint](/docs/reference/engine/classes/CylindricalConstraint), [PrismaticConstraint](/docs/reference/engine/classes/PrismaticConstraint)

SlidingBallConstraint is the base class for constraints that allow their
attachments to slide along an axis but not rotate, including
[PrismaticConstraint](/docs/reference/engine/classes/PrismaticConstraint) and [CylindricalConstraint](/docs/reference/engine/classes/CylindricalConstraint). This constrains
the attachments so that their X axes are collinear but pointing in
opposite directions. It also constrains the attachments so that their Y
axes are parallel.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Linear Power

If this constraint's [ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint) is set to
[Motor](/docs/reference/engine/enums/ActuatorType), it attempts to translate the attachments with the
goal of reaching [Velocity](/docs/reference/engine/classes/SlidingBallConstraint). You can further
control this translation through both
[MotorMaxAcceleration](/docs/reference/engine/classes/SlidingBallConstraint) and
[MotorMaxForce](/docs/reference/engine/classes/SlidingBallConstraint).

If this constraint's [ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint) is set to
[Servo](/docs/reference/engine/enums/ActuatorType), it attempts to translate the attachments to a set
separation specified by [TargetPosition](/docs/reference/engine/classes/SlidingBallConstraint). This
translation is controlled by [Speed](/docs/reference/engine/classes/SlidingBallConstraint),
[LinearResponsiveness](/docs/reference/engine/classes/SlidingBallConstraint), and
[ServoMaxForce](/docs/reference/engine/classes/SlidingBallConstraint).

#### Limits

You can set limits to restrict this constraint's sliding range. Enabling
the [LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint) property exposes the
[LowerLimit](/docs/reference/engine/classes/SlidingBallConstraint) and
[UpperLimit](/docs/reference/engine/classes/SlidingBallConstraint) values, as well as
[Restitution](/docs/reference/engine/classes/SlidingBallConstraint) which defines the elasticity of the
attachments when they reach either limit.

---

API Reference

Properties

ActuatorType

Read Parallel

Sets whether the translation of the [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint) is
actuated and, if so, what kind of actuation.

SlidingBallConstraint.ActuatorType:[Enum.ActuatorType](/docs/reference/engine/enums/ActuatorType)

Sets whether the translation of the [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint) is
actuated and, if so, what kind of actuation.

* If [ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint) is set to
  [None](/docs/reference/engine/enums/ActuatorType), the joint can slide freely.
* If [ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint) is set to
  [Motor](/docs/reference/engine/enums/ActuatorType), it attempts to translate the attachments with
  the goal of reaching [Velocity](/docs/reference/engine/classes/SlidingBallConstraint). You can
  further control this translation through both
  [MotorMaxAcceleration](/docs/reference/engine/classes/SlidingBallConstraint) and
  [MotorMaxForce](/docs/reference/engine/classes/SlidingBallConstraint).
* If this constraint's [ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint) is set
  to [Servo](/docs/reference/engine/enums/ActuatorType), it attempts to translate the attachments
  to a set separation specified by
  [TargetPosition](/docs/reference/engine/classes/SlidingBallConstraint). This translation is
  controlled by [Speed](/docs/reference/engine/classes/SlidingBallConstraint),
  [LinearResponsiveness](/docs/reference/engine/classes/SlidingBallConstraint), and
  [ServoMaxForce](/docs/reference/engine/classes/SlidingBallConstraint).

Provide feedback

---

CurrentPosition

Read Only

Not Replicated

Read Parallel

The current offset between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

SlidingBallConstraint.CurrentPosition:[number](/docs/luau/numbers)

The current offset between the constraint's
[Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

LimitsEnabled

Read Parallel

Sets whether the [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint) will limit the range of
translation.

SlidingBallConstraint.LimitsEnabled:[boolean](/docs/luau/booleans)

Sets whether the [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint) will limit the range of
translation. If true, this property exposes the
[LowerLimit](/docs/reference/engine/classes/SlidingBallConstraint) and
[UpperLimit](/docs/reference/engine/classes/SlidingBallConstraint) values, as well as
[Restitution](/docs/reference/engine/classes/SlidingBallConstraint) which defines the elasticity of
the attachments when they reach either limit.

Provide feedback

---

LinearResponsiveness

Read Parallel

Specifies the "sharpness" of the linear servo motor in reaching the
[TargetPosition](/docs/reference/engine/classes/SlidingBallConstraint#TargetPosition).

SlidingBallConstraint.LinearResponsiveness:[number](/docs/luau/numbers)

Specifies the "sharpness" of the linear servo motor in reaching the
[TargetPosition](/docs/reference/engine/classes/SlidingBallConstraint#TargetPosition) when the
derived classes' actuator type is set to [Servo](/docs/reference/engine/enums/ActuatorType). Larger
values correspond to faster a response and smaller values results in more
damping and a slower response.

Provide feedback

---

LowerLimit

Read Parallel

The lower positional limit along the X axis of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) if
[LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint#LimitsEnabled) is true.

SlidingBallConstraint.LowerLimit:[number](/docs/luau/numbers)

The lower positional limit along the X axis of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) if
[LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint#LimitsEnabled) is true.

Provide feedback

---

MotorMaxAcceleration

Read Parallel

The constraint's maximum acceleration when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Motor](/docs/reference/engine/enums/ActuatorType) as the constraint attempts to reach its desired
[Velocity](/docs/reference/engine/classes/SlidingBallConstraint#Velocity).

SlidingBallConstraint.MotorMaxAcceleration:[number](/docs/luau/numbers)

The constraint's maximum acceleration when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Motor](/docs/reference/engine/enums/ActuatorType), as the constraint attempts to reach its desired
[Velocity](/docs/reference/engine/classes/SlidingBallConstraint#Velocity).

Provide feedback

---

MotorMaxForce

Read Parallel

The constraint's maximum force when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Motor](/docs/reference/engine/enums/ActuatorType), as the constraint attempts to reach its desired
[Velocity](/docs/reference/engine/classes/SlidingBallConstraint#Velocity).

SlidingBallConstraint.MotorMaxForce:[number](/docs/luau/numbers)

The constraint's maximum force when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Motor](/docs/reference/engine/enums/ActuatorType), as the constraint attempts to reach its desired
[Velocity](/docs/reference/engine/classes/SlidingBallConstraint#Velocity).

Provide feedback

---

Restitution

Read Parallel

The elasticity of the constraint's [Attachments](/docs/reference/engine/classes/Attachment) when
they reach the end of the range specified by
[UpperLimit](/docs/reference/engine/classes/SlidingBallConstraint#UpperLimit) and
[LowerLimit](/docs/reference/engine/classes/SlidingBallConstraint#LowerLimit), assuming
[LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint#LimitsEnabled) is set to true.

SlidingBallConstraint.Restitution:[number](/docs/luau/numbers)

The elasticity of the constraint's [Attachments](/docs/reference/engine/classes/Attachment) when
they reach the end of the range specified by
[UpperLimit](/docs/reference/engine/classes/SlidingBallConstraint#UpperLimit) and
[LowerLimit](/docs/reference/engine/classes/SlidingBallConstraint#LowerLimit), assuming
[LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint#LimitsEnabled) is set to true.
The valid range is between 0–1.

Provide feedback

---

ServoMaxForce

Read Parallel

The constraint's maximum force when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType), as the constraint attempts to reach its desired
[Speed](/docs/reference/engine/classes/SlidingBallConstraint#Speed).

SlidingBallConstraint.ServoMaxForce:[number](/docs/luau/numbers)

The constraint's maximum force when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType), as the constraint attempts to reach its desired
[Speed](/docs/reference/engine/classes/SlidingBallConstraint#Speed).

Provide feedback

---

Size

Read Parallel

The constraint's visualized size.

SlidingBallConstraint.Size:[number](/docs/luau/numbers)

The constraint's visualized size.

Provide feedback

---

SoftlockServoUponReachingTarget

Deprecated

Show details

---

Speed

Read Parallel

The constraint's desired speed when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType), as the constraint translates towards its
[TargetPosition](/docs/reference/engine/classes/SlidingBallConstraint#TargetPosition). Measured in
studs per second.

SlidingBallConstraint.Speed:[number](/docs/luau/numbers)

The constraint's desired speed when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType), as the constraint translates towards its
[TargetPosition](/docs/reference/engine/classes/SlidingBallConstraint#TargetPosition). Measured in
studs per second.

Provide feedback

---

TargetPosition

Read Parallel

The constraint's attempted target position when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType). Measured in studs.

SlidingBallConstraint.TargetPosition:[number](/docs/luau/numbers)

The constraint's attempted target position when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Servo](/docs/reference/engine/enums/ActuatorType) Measured in studs.

Provide feedback

---

UpperLimit

Read Parallel

The upper positional limit along the X axis of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) if
[LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint#LimitsEnabled) is true.

SlidingBallConstraint.UpperLimit:[number](/docs/luau/numbers)

The upper positional limit along the X axis of
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) if
[LimitsEnabled](/docs/reference/engine/classes/SlidingBallConstraint#LimitsEnabled) is true.

Provide feedback

---

Velocity

Read Parallel

The constraint's attempted velocity when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Motor](/docs/reference/engine/enums/ActuatorType). Measured in studs per second.

SlidingBallConstraint.Velocity:[number](/docs/luau/numbers)

The constraint's attempted velocity when
[ActuatorType](/docs/reference/engine/classes/SlidingBallConstraint#ActuatorType) is set to
[Motor](/docs/reference/engine/enums/ActuatorType). Measured in studs per second.

Provide feedback

---