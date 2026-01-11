# TorsionSpringConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TorsionSpringConstraint
Scraped: 2026-01-11T02:35:46.201127Z

## Tags
- Not Replicated

## Inherits
- Constraint
- TorsionSpringConstraint
- Instance
- Object
- SecondaryAxis
- Damping
- Stiffness
- LimitsEnabled
- MaxAngle
- Restitution
- Attachment0
- Attachments
- LimitEnabled
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [TorsionSpringConstraint](/docs/reference/engine/classes/TorsionSpringConstraint)

English

Feedback

Engine Class

![TorsionSpringConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TorsionSpringConstraint-Dark.webp)TorsionSpringConstraint

A rotational spring that opposes the angular motion between two axes.

---

Summary

Properties

|  |
| --- |
| [Coils](#Coils):[number](/docs/luau/numbers) |
| [CurrentAngle](#CurrentAngle):[number](/docs/luau/numbers) |
| [Damping](#Damping):[number](/docs/luau/numbers) |
| [LimitEnabled](#LimitEnabled):[boolean](/docs/luau/booleans)  Deprecated |
| [LimitsEnabled](#LimitsEnabled):[boolean](/docs/luau/booleans) |
| [MaxAngle](#MaxAngle):[number](/docs/luau/numbers) |
| [MaxTorque](#MaxTorque):[number](/docs/luau/numbers) |
| [Radius](#Radius):[number](/docs/luau/numbers) |
| [Restitution](#Restitution):[number](/docs/luau/numbers) |
| [Stiffness](#Stiffness):[number](/docs/luau/numbers) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A TorsionSpringConstraint applies a torque based on a relative angle and a
relative angular velocity. Specifically, torsion springs try to bring two axes
from two parts together in a compliant way.

Correct orientation of a torsion spring's attachments is important. The
constraint will attempt to bring the
[SecondaryAxis](/docs/reference/engine/classes/Attachment#SecondaryAxis) of each attachment into
alignment. When building mechanisms like swinging doors, ensure that the
secondary axes are perpendicular to the intended axis of rotation.

When configuring this constraint, it may be helpful to study
[Roblox Units](/docs/physics/units) to understand how Roblox units
compare to metric units.

#### Damping

The [Damping](/docs/reference/engine/classes/TorsionSpringConstraint#Damping) value controls how fast
the spring's oscillation dies down. A value of 0 allows the spring to
oscillate endlessly, while higher values bring the spring to a rest more
quickly.

#### Stiffness

[Stiffness](/docs/reference/engine/classes/TorsionSpringConstraint#Stiffness) sets the torsional
strength of the spring. Higher values create a spring that responds with more
force.

#### Limits

Enabling the [LimitsEnabled](/docs/reference/engine/classes/TorsionSpringConstraint#LimitsEnabled)
property exposes the [MaxAngle](/docs/reference/engine/classes/TorsionSpringConstraint#MaxAngle) value
to restrict the spring's range within a cone; it also exposes the
[Restitution](/docs/reference/engine/classes/TorsionSpringConstraint#Restitution) value which defines
the elasticity of the attachments when they reach their limit.

---

API Reference

Properties

Coils

Read Parallel

The number of coils visualized for the constraint.

TorsionSpringConstraint.Coils:[number](/docs/luau/numbers)

This property indicates the number of spring coils for visualization.
Default value is 8.

Provide feedback

---

CurrentAngle

Read Only

Not Replicated

Read Parallel

The current angle, in degrees, of the limiting cone.

TorsionSpringConstraint.CurrentAngle:[number](/docs/luau/numbers)

The current angle, in degrees, of the torsion spring's limiting cone. The
limiting cone is formed at the position of the constraint's
[Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) around its secondary axis with
an angle equal to [MaxAngle](/docs/reference/engine/classes/TorsionSpringConstraint#MaxAngle).

Provide feedback

---

Damping

Read Parallel

Damping constant for the [TorsionSpringConstraint](/docs/reference/engine/classes/TorsionSpringConstraint). Multiplied to
the velocity of the constraint's [Attachments](/docs/reference/engine/classes/Attachment) to reduce
the spring force applied.

TorsionSpringConstraint.Damping:[number](/docs/luau/numbers)

Damping constant for the [TorsionSpringConstraint](/docs/reference/engine/classes/TorsionSpringConstraint). Multiplied to
the velocity of the constraint's [Attachments](/docs/reference/engine/classes/Attachment) to reduce
the spring force applied.

Provide feedback

---

LimitEnabled

Deprecated

Show details

---

LimitsEnabled

Read Parallel

Limits the relative angular motion of the secondary axes of attachments
through a cone constraint.

TorsionSpringConstraint.LimitsEnabled:[boolean](/docs/luau/booleans)

This property, when enabled, limits the relative angular motion of the
secondary axes of attachments through a cone constraint. The default value
is false.

Provide feedback

---

MaxAngle

Read Parallel

The maximum angle of the constraint's limiting cone.

TorsionSpringConstraint.MaxAngle:[number](/docs/luau/numbers)

This property determines the maximum angle (in degrees) of the torsion
spring's limiting cone. The limiting cone is formed at the position of the
constraint's [Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) around its
secondary axis with an angle equal to
[MaxAngle](/docs/reference/engine/classes/TorsionSpringConstraint#MaxAngle). Default value is 45
degrees.

Provide feedback

---

MaxTorque

Read Parallel

The maximum allowable torque provided by the torsion spring.

TorsionSpringConstraint.MaxTorque:[number](/docs/luau/numbers)

This property determines the maximum torque supported by the torsion
spring. Defaults to 1000.

Provide feedback

---

Radius

Read Parallel

The visualization radius of the spring.

TorsionSpringConstraint.Radius:[number](/docs/luau/numbers)

This property indicates the visualization radius of the spring, in studs.
Default value is 0.4.

Provide feedback

---

Restitution

Read Parallel

The restitution coefficient of the cone constraint.

TorsionSpringConstraint.Restitution:[number](/docs/luau/numbers)

This property defines how elastic [Attachments](/docs/reference/engine/classes/Attachment) connected
by a [TorsionSpringConstraint](/docs/reference/engine/classes/TorsionSpringConstraint) are when they reach the end of the
range specified by [MaxAngle](/docs/reference/engine/classes/TorsionSpringConstraint#MaxAngle), when
[LimitEnabled](/docs/reference/engine/classes/TorsionSpringConstraint#LimitEnabled) is true. The
value defaults to 0 and can be any floating number within the range of 0
and 1.

Provide feedback

---

Stiffness

Read Parallel

The torsional stiffness of the spring.

TorsionSpringConstraint.Stiffness:[number](/docs/luau/numbers)

In the absence of damping, this property is proportional to the opposing
torque of the spring. For instance, higher stiffness results in a larger
opposing torque, and smaller stiffness results in a smaller opposing
torque. The larger the torque value, the faster the axes are pushed
together when the relative angle is positive (or away from each other if
the relative angle is negative). The value defaults to 100.

Provide feedback

---