# BodyMover | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyMover
Scraped: 2026-01-11T02:38:55.276801Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- BodyMover
- BodyAngularVelocity
- BodyForce
- BodyGyro
- BodyPosition
- BodyThrust
- BodyVelocity
- RocketPropulsion
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [BodyMover](/docs/reference/engine/classes/BodyMover)

English

Feedback

Engine Class

BodyMover

Deprecated

Base class for objects that continually exert forces to assemblies.

Not Creatable

This class has been deprecated. See the
[mover constraints](/docs/physics/mover-constraints) article for an
overview of [BodyMover](/docs/reference/engine/classes/BodyMover) replacements, as well as the
[legacy conversion notes](/docs/physics/mover-constraints#legacy-mover-conversion).

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[BodyAngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity), [BodyForce](/docs/reference/engine/classes/BodyForce), [BodyGyro](/docs/reference/engine/classes/BodyGyro), [BodyPosition](/docs/reference/engine/classes/BodyPosition), [BodyThrust](/docs/reference/engine/classes/BodyThrust), Show more...

BodyMover is the abstract base class for the set of legacy objects that
exert forces to assemblies in different ways. In general, the subclasses of
BodyMover are:

* [BodyForce](/docs/reference/engine/classes/BodyForce) exerts a force relative to world coordinates.
* [BodyPosition](/docs/reference/engine/classes/BodyPosition) exerts force to maintain a certain world position.
* [BodyVelocity](/docs/reference/engine/classes/BodyVelocity) exerts force to maintain a certain velocity.
* [BodyThrust](/docs/reference/engine/classes/BodyThrust) exerts a force relative to object coordinates which
  applies torque if positioned in a certain way.
* [BodyGyro](/docs/reference/engine/classes/BodyGyro) exerts torque to maintain a certain orientation.
* [BodyAngularVelocity](/docs/reference/engine/classes/BodyAngularVelocity) exerts torque to maintain a certain angular
  velocity.
* [RocketPropulsion](/docs/reference/engine/classes/RocketPropulsion) exerts both translational and rotational forces to
  cause an assembly to track down another.