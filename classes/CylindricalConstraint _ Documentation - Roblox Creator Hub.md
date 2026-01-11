# CylindricalConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CylindricalConstraint
Scraped: 2026-01-11T02:40:57.760416Z

## Tags
- Not Replicated

## Inherits
- SlidingBallConstraint
- CylindricalConstraint
- Constraint
- Instance
- Object
- PrismaticConstraint
- HingeConstraint
- Attachment0
- Attachment1
- InclinationAngle
- SpringConstraint
- AngularActuatorType
- AngularVelocity
- MotorMaxAngularAcceleration
- MotorMaxTorque
- TargetAngle
- AngularSpeed
- AngularResponsiveness
- ServoMaxTorque
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
- AngularLimitsEnabled
- LowerAngle
- UpperAngle
- AngularRestitution
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint)
6. /
7. [CylindricalConstraint](/docs/reference/engine/classes/CylindricalConstraint)

English

Feedback

Engine Class

![CylindricalConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/CylindricalConstraint-Dark.webp)CylindricalConstraint

Constrains two attachments on two parts to have a relative linear and
rotational motion.

---

Summary

Properties

|  |
| --- |
| [AngularActuatorType](#AngularActuatorType):[Enum.ActuatorType](/docs/reference/engine/enums/ActuatorType) |
| [AngularLimitsEnabled](#AngularLimitsEnabled):[boolean](/docs/luau/booleans) |
| [AngularResponsiveness](#AngularResponsiveness):[number](/docs/luau/numbers) |
| [AngularRestitution](#AngularRestitution):[number](/docs/luau/numbers) |
| [AngularSpeed](#AngularSpeed):[number](/docs/luau/numbers) |
| [AngularVelocity](#AngularVelocity):[number](/docs/luau/numbers) |
| [CurrentAngle](#CurrentAngle):[number](/docs/luau/numbers) |
| [InclinationAngle](#InclinationAngle):[number](/docs/luau/numbers) |
| [LowerAngle](#LowerAngle):[number](/docs/luau/numbers) |
| [MotorMaxAngularAcceleration](#MotorMaxAngularAcceleration):[number](/docs/luau/numbers) |
| [MotorMaxTorque](#MotorMaxTorque):[number](/docs/luau/numbers) |
| [RotationAxisVisible](#RotationAxisVisible):[boolean](/docs/luau/booleans) |
| [ServoMaxTorque](#ServoMaxTorque):[number](/docs/luau/numbers) |
| [SoftlockAngularServoUponReachingTarget](#SoftlockAngularServoUponReachingTarget):[boolean](/docs/luau/booleans)  Deprecated |
| [TargetAngle](#TargetAngle):[number](/docs/luau/numbers) |
| [UpperAngle](#UpperAngle):[number](/docs/luau/numbers) |
| [WorldRotationAxis](#WorldRotationAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

15 inherited from [SlidingBallConstraint](/docs/reference/engine/classes/SlidingBallConstraint)

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A CylindricalConstraint allows its attachments to slide along one axis and
rotate about another axis. It can be thought of like a combination of a
[PrismaticConstraint](/docs/reference/engine/classes/PrismaticConstraint) and a [HingeConstraint](/docs/reference/engine/classes/HingeConstraint). The sliding axis is
determined by the X axis of the constraint's
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). The rotation axis is centered at
the constraint's [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) and is angled off
of the sliding constraint by the constraint's
[InclinationAngle](/docs/reference/engine/classes/CylindricalConstraint#InclinationAngle).

This constraint, along with a [SpringConstraint](/docs/reference/engine/classes/SpringConstraint), is ideal for building
vehicle suspension.

Note that if this constraint attaches one part (A) to another part (B)
that is anchored or connected to an anchored part (Z), part A will not
be locally simulated when interacting with a player.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Angular Power

If a cylindrical's
[AngularActuatorType](/docs/reference/engine/classes/CylindricalConstraint#AngularActuatorType) is set
to [Motor](/docs/reference/engine/enums/ActuatorType), it attempts to rotate the attachments with the
goal of reaching its
[AngularVelocity](/docs/reference/engine/classes/CylindricalConstraint#AngularVelocity). You can further
control this rotation through both
[MotorMaxAngularAcceleration](/docs/reference/engine/classes/CylindricalConstraint#MotorMaxAngularAcceleration)
and [MotorMaxTorque](/docs/reference/engine/classes/CylindricalConstraint#MotorMaxTorque). If a
cylindrical's
[AngularActuatorType](/docs/reference/engine/classes/CylindricalConstraint#AngularActuatorType) is set
to [Servo](/docs/reference/engine/enums/ActuatorType), it attempts to rotate to an angle specified by
[TargetAngle](/docs/reference/engine/classes/CylindricalConstraint#TargetAngle). This rotation is
controlled by [AngularSpeed](/docs/reference/engine/classes/CylindricalConstraint#AngularSpeed),
[AngularResponsiveness](/docs/reference/engine/classes/CylindricalConstraint#AngularResponsiveness), and
[ServoMaxTorque](/docs/reference/engine/classes/CylindricalConstraint#ServoMaxTorque).

#### Linear Power

If a cylindrical's [ActuatorType](/docs/reference/engine/classes/CylindricalConstraint) is set to
[Motor](/docs/reference/engine/enums/ActuatorType), it attempts to translate the attachments with the
goal of reaching [Velocity](/docs/reference/engine/classes/CylindricalConstraint). You can further
control this translation through both
[MotorMaxAcceleration](/docs/reference/engine/classes/CylindricalConstraint) and
[MotorMaxForce](/docs/reference/engine/classes/CylindricalConstraint). If a cylindrical's
[ActuatorType](/docs/reference/engine/classes/CylindricalConstraint) is set to
[Servo](/docs/reference/engine/enums/ActuatorType), it attempts to translate the attachments to a set
separation specified by [TargetPosition](/docs/reference/engine/classes/CylindricalConstraint). This
translation is controlled by [Speed](/docs/reference/engine/classes/CylindricalConstraint),
[LinearResponsiveness](/docs/reference/engine/classes/CylindricalConstraint), and
[ServoMaxForce](/docs/reference/engine/classes/CylindricalConstraint).

#### Limits

You can set limits to restrict both the sliding range and rotation of
a cylindrical constraint. Enabling the
[LimitsEnabled](/docs/reference/engine/classes/CylindricalConstraint) property exposes the
[LowerLimit](/docs/reference/engine/classes/CylindricalConstraint) and
[UpperLimit](/docs/reference/engine/classes/CylindricalConstraint) values, as well as
[Restitution](/docs/reference/engine/classes/CylindricalConstraint) which defines the elasticity of the
attachments when they reach either limit. Enabling the
[AngularLimitsEnabled](/docs/reference/engine/classes/CylindricalConstraint#AngularLimitsEnabled)
property exposes the [LowerAngle](/docs/reference/engine/classes/CylindricalConstraint#LowerAngle) and
[UpperAngle](/docs/reference/engine/classes/CylindricalConstraint#UpperAngle) limits, as well as
[AngularRestitution](/docs/reference/engine/classes/CylindricalConstraint#AngularRestitution) which
defines the elasticity of the attachments when they reach either limit.

#### Inclination Angle

[InclinationAngle](/docs/reference/engine/classes/CylindricalConstraint#InclinationAngle) defines the
direction of the rotation axis as an angle from the X axis in the XY
plane of [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0), from
-180 to 180. This lets you tilt the rotating element without
changing the sliding axis.

---

API Reference

Properties

AngularActuatorType

Read Parallel

Type of angular actuator.

CylindricalConstraint.AngularActuatorType:[Enum.ActuatorType](/docs/reference/engine/enums/ActuatorType)

If a cylindrical's
[AngularActuatorType](/docs/reference/engine/classes/CylindricalConstraint#AngularActuatorType) is
set to [Motor](/docs/reference/engine/enums/ActuatorType), it attempts to rotate the attachments
with the goal of reaching its
[AngularVelocity](/docs/reference/engine/classes/CylindricalConstraint#AngularVelocity). You can
further control this rotation through both
[MotorMaxAngularAcceleration](/docs/reference/engine/classes/CylindricalConstraint#MotorMaxAngularAcceleration)
and [MotorMaxTorque](/docs/reference/engine/classes/CylindricalConstraint#MotorMaxTorque).

If a cylindrical's
[AngularActuatorType](/docs/reference/engine/classes/CylindricalConstraint#AngularActuatorType) is
set to [Servo](/docs/reference/engine/enums/ActuatorType), it attempts to rotate to an angle
specified by [TargetAngle](/docs/reference/engine/classes/CylindricalConstraint#TargetAngle). This
rotation is controlled by
[AngularSpeed](/docs/reference/engine/classes/CylindricalConstraint#AngularSpeed),
[AngularResponsiveness](/docs/reference/engine/classes/CylindricalConstraint#AngularResponsiveness),
and [ServoMaxTorque](/docs/reference/engine/classes/CylindricalConstraint#ServoMaxTorque).

Provide feedback

---

AngularLimitsEnabled

Read Parallel

Enables the angular limits around the rotation axis.

CylindricalConstraint.AngularLimitsEnabled:[boolean](/docs/luau/booleans)

Enables the angular limits around the rotation axis.

Provide feedback

---

AngularResponsiveness

Read Parallel

Specifies the sharpness of the angular servo motor in reaching the
[TargetAngle](/docs/reference/engine/classes/CylindricalConstraint#TargetAngle).

CylindricalConstraint.AngularResponsiveness:[number](/docs/luau/numbers)

This property specifies the sharpness of the angular servo motor in
reaching the [TargetAngle](/docs/reference/engine/classes/CylindricalConstraint#TargetAngle), when
[AngularActuatorType](/docs/reference/engine/classes/CylindricalConstraint#AngularActuatorType) is
set to [Servo](/docs/reference/engine/enums/ActuatorType). Larger values correspond to a faster
response and smaller values results in more damping and a slower response.

Provide feedback

---

AngularRestitution

Read Parallel

Restitution of the two limits, or how elastic they are.

CylindricalConstraint.AngularRestitution:[number](/docs/luau/numbers)

Restitution of the two limits, or how elastic they are. Constrained
between 0 and 1.

Provide feedback

---

AngularSpeed

Read Parallel

Target angular speed. This value is unsigned as the servo will always move
toward its target. In radians per second.

CylindricalConstraint.AngularSpeed:[number](/docs/luau/numbers)

Target angular speed. This value is unsigned as the servo will always move
toward its target. In radians per second.

Provide feedback

---

AngularVelocity

Read Parallel

The target angular velocity of the motor in radians per second around the
rotation axis.

CylindricalConstraint.AngularVelocity:[number](/docs/luau/numbers)

The target angular velocity of the motor in radians per second around the
rotation axis.

Provide feedback

---

CurrentAngle

Read Only

Not Replicated

Read Parallel

Signed angle (in degrees) between the reference axis and the secondary
axis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the rotation
axis.

CylindricalConstraint.CurrentAngle:[number](/docs/luau/numbers)

Signed angle (in degrees) between the reference axis and the secondary
axis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the rotation
axis. Valid range between -180 and 180.

Provide feedback

---

InclinationAngle

Read Parallel

Direction of the rotation axis as an angle from the X axis in the
XY plane of [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0).

CylindricalConstraint.InclinationAngle:[number](/docs/luau/numbers)

Direction of the rotation axis as an angle from the X axis in the
XY plane of [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0). Valid range
between -180 and 180.

Provide feedback

---

LowerAngle

Read Parallel

Lower limit for the angle (in degrees) between the reference axis and the
SecondaryAxis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the
rotation axis.

CylindricalConstraint.LowerAngle:[number](/docs/luau/numbers)

Lower limit for the angle (in degrees) between the reference axis and the
SecondaryAxis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the
rotation axis. Valid range between -180 and 180.

Provide feedback

---

MotorMaxAngularAcceleration

Read Parallel

The maximum angular acceleration of the motor in radians per second
squared.

CylindricalConstraint.MotorMaxAngularAcceleration:[number](/docs/luau/numbers)

The maximum angular acceleration of the motor in radians per second
squared.

Provide feedback

---

MotorMaxTorque

Read Parallel

The maximum torque the motor can apply to achieve the target angular
velocity.

CylindricalConstraint.MotorMaxTorque:[number](/docs/luau/numbers)

The maximum torque the motor can apply to achieve the target angular
velocity. Units are mass × studs²/second².

Provide feedback

---

RotationAxisVisible

Read Parallel

Enable the visibility of the rotation axis.

CylindricalConstraint.RotationAxisVisible:[boolean](/docs/luau/booleans)

Enable the visibility of the rotation axis.

Provide feedback

---

ServoMaxTorque

Read Parallel

Maximum torque the servo motor can apply.

CylindricalConstraint.ServoMaxTorque:[number](/docs/luau/numbers)

Maximum torque the servo motor can apply. Units are
mass × studs²/second².

Provide feedback

---

SoftlockAngularServoUponReachingTarget

Deprecated

Show details

---

TargetAngle

Read Parallel

Target angle (in degrees) between the reference axis and the secondary
axis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the rotation
axis.

CylindricalConstraint.TargetAngle:[number](/docs/luau/numbers)

Target angle (in degrees) between the reference axis and the secondary
axis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the rotation
axis. Valid range between -180 and 180.

Provide feedback

---

UpperAngle

Read Parallel

Upper limit for the angle (in degrees) between the reference axis and the
secondary axis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the
rotation axis.

CylindricalConstraint.UpperAngle:[number](/docs/luau/numbers)

Upper limit for the angle (in degrees) between the reference axis and the
secondary axis of [Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) around the
rotation axis. Valid range between -180 and 180.

Provide feedback

---

WorldRotationAxis

Read Only

Not Replicated

Read Parallel

The unit vector direction of the rotation axis in world coordinates.

CylindricalConstraint.WorldRotationAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The unit vector direction of the rotation axis in world coordinates.

Provide feedback

---