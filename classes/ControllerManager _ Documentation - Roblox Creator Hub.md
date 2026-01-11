# ControllerManager | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ControllerManager
Scraped: 2026-01-11T02:30:13.701992Z

## Inherits
- Instance
- ControllerManager
- ControllerManager.RootPart
- ControllerBase
- ControllerSensor
- BasePart
- Object
- WorldRoot
- Part
- GroundController
- ControllerBase.MoveSpeedFactor
- ClimbController
- ControllerPartSensor.HitPart
- ControllerPartSensor.HitFrame
- ControllerPartSensor.HitNormal
- ControllerPartSensor
- BaseMoveSpeed
- RootPart
- ActiveController
- Humanoid
- Humanoid.RootPart
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ControllerManager](/docs/reference/engine/classes/ControllerManager)

English

Feedback

Engine Class

ControllerManager

Manages simulated motion control for its assigned
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) .

---

Summary

Properties

|  |
| --- |
| [ActiveController](#ActiveController):[ControllerBase](/docs/reference/engine/classes/ControllerBase) |
| [BaseMoveSpeed](#BaseMoveSpeed):[number](/docs/luau/numbers) |
| [BaseTurnSpeed](#BaseTurnSpeed):[number](/docs/luau/numbers) |
| [ClimbSensor](#ClimbSensor):[ControllerSensor](/docs/reference/engine/classes/ControllerSensor) |
| [FacingDirection](#FacingDirection):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GroundSensor](#GroundSensor):[ControllerSensor](/docs/reference/engine/classes/ControllerSensor) |
| [MovingDirection](#MovingDirection):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [RootPart](#RootPart):[BasePart](/docs/reference/engine/classes/BasePart) |
| [UpDirection](#UpDirection):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [ControllerManager](/docs/reference/engine/classes/ControllerManager) instance manages simulated motion control for
its assigned [ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart). It can be used to build a
physics-based character controller.

---

API Reference

Properties

ActiveController

Read Parallel

The [ControllerBase](/docs/reference/engine/classes/ControllerBase) that is set to be activated on the character.

ControllerManager.ActiveController:[ControllerBase](/docs/reference/engine/classes/ControllerBase)

The [ControllerBase](/docs/reference/engine/classes/ControllerBase) that is set to be activated on the character.
It does not guarantee that the specified [ControllerBase](/docs/reference/engine/classes/ControllerBase) is, in
fact, active. If the [ControllerBase](/docs/reference/engine/classes/ControllerBase) cannot be activated for
whatever reason, such as being outside of the character's
[WorldRoot](/docs/reference/engine/classes/WorldRoot) or no [Part](/docs/reference/engine/classes/Part) being found to use as the floor for a
[GroundController](/docs/reference/engine/classes/GroundController), it will remain set and the
[ControllerManager](/docs/reference/engine/classes/ControllerManager) will attempt to activate it in the next frame.
This property can be set to nil to disable the physics controller.

Provide feedback

---

BaseMoveSpeed

Read Parallel

The base linear movement speed used by all controllers.

ControllerManager.BaseMoveSpeed:[number](/docs/luau/numbers)

The base linear movement speed used by all controllers. Controllers
individually customize speed by setting the
[ControllerBase.MoveSpeedFactor](/docs/reference/engine/classes/ControllerBase#MoveSpeedFactor) property.

Provide feedback

---

BaseTurnSpeed

Read Parallel

The base angular turning speed used by all controllers.

ControllerManager.BaseTurnSpeed:[number](/docs/luau/numbers)

The base angular turning speed used by all controllers to align the
character to face the desired direction.

Provide feedback

---

ClimbSensor

Read Parallel

A reference to the sensor data used while a [ClimbController](/docs/reference/engine/classes/ClimbController) is
active.

ControllerManager.ClimbSensor:[ControllerSensor](/docs/reference/engine/classes/ControllerSensor)

A reference to the sensor data used while a [ClimbController](/docs/reference/engine/classes/ClimbController) is
active. A [ClimbController](/docs/reference/engine/classes/ClimbController) will use the
[ControllerPartSensor.HitPart](/docs/reference/engine/classes/ControllerPartSensor#HitPart),
[ControllerPartSensor.HitFrame](/docs/reference/engine/classes/ControllerPartSensor#HitFrame), and
[ControllerPartSensor.HitNormal](/docs/reference/engine/classes/ControllerPartSensor#HitNormal) for climb movement computations.
Typically a [ControllerPartSensor](/docs/reference/engine/classes/ControllerPartSensor) set to [Enum.SensorMode.Ladder](/docs/reference/engine/enums/SensorMode#Ladder)
is used here. Otherwise, you can override the sensor's outputs to direct
what sensor data you want the [ClimbController](/docs/reference/engine/classes/ClimbController) to use.

Provide feedback

---

FacingDirection

Read Parallel

The unit vector describing the desired direction to face.

ControllerManager.FacingDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)

The unit vector describing the desired direction to face. Aligns the
[LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) of the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) to this. Any [Vector3](/docs/reference/engine/datatypes/Vector3)
assigned will be automatically unitized.

Provide feedback

---

GroundSensor

Read Parallel

A reference to the sensor data used while a [GroundController](/docs/reference/engine/classes/GroundController) is
active.

ControllerManager.GroundSensor:[ControllerSensor](/docs/reference/engine/classes/ControllerSensor)

A reference to the sensor data used while a [GroundController](/docs/reference/engine/classes/GroundController) is
active. A [GroundController](/docs/reference/engine/classes/GroundController) will use the
[ControllerPartSensor.HitPart](/docs/reference/engine/classes/ControllerPartSensor#HitPart),
[ControllerPartSensor.HitFrame](/docs/reference/engine/classes/ControllerPartSensor#HitFrame), and
[ControllerPartSensor.HitNormal](/docs/reference/engine/classes/ControllerPartSensor#HitNormal) for ground movement computations.
Typically a [ControllerPartSensor](/docs/reference/engine/classes/ControllerPartSensor) set to [Enum.SensorMode.Floor](/docs/reference/engine/enums/SensorMode#Floor) is
used here. Otherwise, you can override the sensor's outputs to direct what
sensor data you want the [GroundController](/docs/reference/engine/classes/GroundController) to use.

Provide feedback

---

MovingDirection

Read Parallel

The vector describing the desired direction to move in.

ControllerManager.MovingDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)

The vector describing the desired direction to move in, with a magnitude
between 0 and 1. This is multiplied by
[BaseMoveSpeed](/docs/reference/engine/classes/ControllerManager#BaseMoveSpeed) to determine a final
target move velocity. The [RootPart](/docs/reference/engine/classes/ControllerManager#RootPart) will
attempt to move in this direction based on the rules defined by the
[ActiveController](/docs/reference/engine/classes/ControllerManager#ActiveController).

Provide feedback

---

RootPart

Read Parallel

The [BasePart](/docs/reference/engine/classes/BasePart) where the controller's forces and torques are
applied.

ControllerManager.RootPart:[BasePart](/docs/reference/engine/classes/BasePart)

The [BasePart](/docs/reference/engine/classes/BasePart) where the controller's forces and torques are
applied. With a typical [Humanoid](/docs/reference/engine/classes/Humanoid)-based character, the
[Humanoid.RootPart](/docs/reference/engine/classes/Humanoid#RootPart) is assigned as the
[ControllerManager.RootPart](/docs/reference/engine/classes/ControllerManager#RootPart).

Provide feedback

---

UpDirection

Read Parallel

ControllerManager.UpDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---