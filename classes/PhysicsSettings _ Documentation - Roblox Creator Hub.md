# PhysicsSettings | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PhysicsSettings
Scraped: 2026-01-11T02:32:47.890382Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- PhysicsSettings
- BasePart.Anchored
- Part
- JointInstance
- SelectionBox
- Workspace.PGSPhysicsSolverEnabled
- Humanoid
- BasePart.CFrame
- Model
- BasePart
- Player.SimulationRadius
- BasePart.ReceiveAge
- BasePart:IsGrounded()
- PartOperation
- MeshPart
- PhysicsSettings.PhysicsEnvironmentalThrottle
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PhysicsSettings](/docs/reference/engine/classes/PhysicsSettings)

English

Feedback

Engine Class

PhysicsSettings

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [AllowSleep](#AllowSleep):[boolean](/docs/luau/booleans) |
| [AreAnchorsShown](#AreAnchorsShown):[boolean](/docs/luau/booleans) |
| [AreAssembliesShown](#AreAssembliesShown):[boolean](/docs/luau/booleans) |
| [AreAssemblyCentersOfMassShown](#AreAssemblyCentersOfMassShown):[boolean](/docs/luau/booleans) |
| [AreAwakePartsHighlighted](#AreAwakePartsHighlighted):[boolean](/docs/luau/booleans) |
| [AreBodyTypesShown](#AreBodyTypesShown):[boolean](/docs/luau/booleans) |
| [AreCollisionCostsShown](#AreCollisionCostsShown):[boolean](/docs/luau/booleans) |
| [AreConstraintForcesShownForSelectedOrHoveredInstances](#AreConstraintForcesShownForSelectedOrHoveredInstances):[boolean](/docs/luau/booleans) |
| [AreConstraintTorquesShownForSelectedOrHoveredInstances](#AreConstraintTorquesShownForSelectedOrHoveredInstances):[boolean](/docs/luau/booleans) |
| [AreContactForcesShownForSelectedOrHoveredAssemblies](#AreContactForcesShownForSelectedOrHoveredAssemblies):[boolean](/docs/luau/booleans) |
| [AreContactIslandsShown](#AreContactIslandsShown):[boolean](/docs/luau/booleans) |
| [AreContactPointsShown](#AreContactPointsShown):[boolean](/docs/luau/booleans) |
| [AreGravityForcesShownForSelectedOrHoveredAssemblies](#AreGravityForcesShownForSelectedOrHoveredAssemblies):[boolean](/docs/luau/booleans) |
| [AreJointCoordinatesShown](#AreJointCoordinatesShown):[boolean](/docs/luau/booleans) |
| [AreMagnitudesShownForDrawnForcesAndTorques](#AreMagnitudesShownForDrawnForcesAndTorques):[boolean](/docs/luau/booleans) |
| [AreMechanismsShown](#AreMechanismsShown):[boolean](/docs/luau/booleans) |
| [AreModelCoordsShown](#AreModelCoordsShown):[boolean](/docs/luau/booleans) |
| [AreNonAnchorsShown](#AreNonAnchorsShown):[boolean](/docs/luau/booleans) |
| [AreOwnersShown](#AreOwnersShown):[boolean](/docs/luau/booleans) |
| [ArePartCoordsShown](#ArePartCoordsShown):[boolean](/docs/luau/booleans) |
| [AreRegionsShown](#AreRegionsShown):[boolean](/docs/luau/booleans) |
| [AreSolverIslandsShown](#AreSolverIslandsShown):[boolean](/docs/luau/booleans) |
| [AreTerrainReplicationRegionsShown](#AreTerrainReplicationRegionsShown):[boolean](/docs/luau/booleans) |
| [AreTimestepsShown](#AreTimestepsShown):[boolean](/docs/luau/booleans) |
| [AreUnalignedPartsShown](#AreUnalignedPartsShown):[boolean](/docs/luau/booleans) |
| [AreWorldCoordsShown](#AreWorldCoordsShown):[boolean](/docs/luau/booleans) |
| [DisableCSGv2](#DisableCSGv2):[boolean](/docs/luau/booleans) |
| [DisableCSGv3ForPlugins](#DisableCSGv3ForPlugins):[boolean](/docs/luau/booleans) |
| [DrawConstraintsNetForce](#DrawConstraintsNetForce):[boolean](/docs/luau/booleans) |
| [DrawContactsNetForce](#DrawContactsNetForce):[boolean](/docs/luau/booleans) |
| [DrawTotalNetForce](#DrawTotalNetForce):[boolean](/docs/luau/booleans) |
| [EnableForceVisualizationSmoothing](#EnableForceVisualizationSmoothing):[boolean](/docs/luau/booleans) |
| [FluidForceDrawScale](#FluidForceDrawScale):[number](/docs/luau/numbers) |
| [ForceCSGv2](#ForceCSGv2):[boolean](/docs/luau/booleans) |
| [ForceDrawScale](#ForceDrawScale):[number](/docs/luau/numbers) |
| [ForceVisualizationSmoothingSteps](#ForceVisualizationSmoothingSteps):[number](/docs/luau/numbers) |
| [IsInterpolationThrottleShown](#IsInterpolationThrottleShown):[boolean](/docs/luau/booleans) |
| [IsReceiveAgeShown](#IsReceiveAgeShown):[boolean](/docs/luau/booleans) |
| [IsTreeShown](#IsTreeShown):[boolean](/docs/luau/booleans) |
| [PhysicsEnvironmentalThrottle](#PhysicsEnvironmentalThrottle):[Enum.EnviromentalPhysicsThrottle](/docs/reference/engine/enums/EnviromentalPhysicsThrottle) |
| [ShowDecompositionGeometry](#ShowDecompositionGeometry):[boolean](/docs/luau/booleans) |
| [ShowFluidForcesForSelectedOrHoveredMechanisms](#ShowFluidForcesForSelectedOrHoveredMechanisms):[boolean](/docs/luau/booleans) |
| [ShowInstanceNamesForDrawnForcesAndTorques](#ShowInstanceNamesForDrawnForcesAndTorques):[boolean](/docs/luau/booleans) |
| [SolverConvergenceMetricType](#SolverConvergenceMetricType):[Enum.SolverConvergenceMetricType](/docs/reference/engine/enums/SolverConvergenceMetricType) |
| [SolverConvergenceVisualizationMode](#SolverConvergenceVisualizationMode):[Enum.SolverConvergenceVisualizationMode](/docs/reference/engine/enums/SolverConvergenceVisualizationMode) |
| [ThrottleAdjustTime](#ThrottleAdjustTime):[number](/docs/luau/numbers) |
| [TorqueDrawScale](#TorqueDrawScale):[number](/docs/luau/numbers) |
| [UseCSGv2](#UseCSGv2):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The PhysicsSettings is a singleton class, which lets you view debugging
features in Roblox's physics engine. You can find it under the Physics tab in
Studio's settings menu.

---

API Reference

Properties

AllowSleep

Read Parallel

When set to true, physically simulated objects will stop being simulated
if they have little to no motion for a set period of time.

PhysicsSettings.AllowSleep:[boolean](/docs/luau/booleans)

When set to true, physically simulated objects will stop being simulated
if they have little to no motion for a set period of time.

Provide feedback

---

AreAnchorsShown

Read Parallel

When set to true, parts that are [BasePart.Anchored](/docs/reference/engine/classes/BasePart#Anchored) will show a
gray surface outline on the surface of the part's bounding box that is
currently facing the ground.

PhysicsSettings.AreAnchorsShown:[boolean](/docs/luau/booleans)

When set to true, parts that are [BasePart.Anchored](/docs/reference/engine/classes/BasePart#Anchored) will show a
gray surface outline on the surface of the part's bounding box that is
currently facing the ground.

Provide feedback

---

AreAssembliesShown

Read Parallel

When set to true, each physics assembly is assigned a unique color and the
[Part](/docs/reference/engine/classes/Part) associated with the assembly are outlined with the color.
Parts that are attached together by [JointInstance](/docs/reference/engine/classes/JointInstance) will share the
same color.

PhysicsSettings.AreAssembliesShown:[boolean](/docs/luau/booleans)

When set to true, each physics assembly is assigned a unique color and the
[Part](/docs/reference/engine/classes/Part) associated with the assembly are outlined with the color.
Parts that are attached together by [JointInstance](/docs/reference/engine/classes/JointInstance) will share the
same color.

Provide feedback

---

AreAssemblyCentersOfMassShown

Roblox Script Security

Read Parallel

PhysicsSettings.AreAssemblyCentersOfMassShown:[boolean](/docs/luau/booleans)

Provide feedback

---

AreAwakePartsHighlighted

Read Parallel

When set to true, parts that are actively being physically simulated will
have a red outline.

PhysicsSettings.AreAwakePartsHighlighted:[boolean](/docs/luau/booleans)

When set to true, parts that are actively being physically simulated will
have a red outline.

Provide feedback

---

AreBodyTypesShown

Read Parallel

When set to true, [Part](/docs/reference/engine/classes/Part) will be outlined with a specific color,
depending on the state of its root simulation body.

PhysicsSettings.AreBodyTypesShown:[boolean](/docs/luau/booleans)

When set to true, [Part](/docs/reference/engine/classes/Part) will be outlined with a specific color,
depending on the state of its root simulation body.

#### Body Types

|  |  |  |
| --- | --- | --- |
| Color | Body Type | Description |
|  | Real-Time Body | Physics Body that is always simulated in real time, and is never throttled. Used for Humanoids. |
|  | Free-Fall Body | Physics Body that is freely moving with no physical contact. |
|  | Joint Body | Physics Body that is being influenced by a physically simulated joint, such as a Motor or a Hinge. |
|  | Contact Body | Physics Body that is in contact with another physics body. |
|  | Symmetric Contact Body | Physics Body that is experiencing a torquing force, while in contact with another body. |
|  | Vertical Contact Body | Physics Body that is moving very little along the Y plane, while in contact with another body. |

Provide feedback

---

AreCollisionCostsShown

Roblox Script Security

Read Parallel

PhysicsSettings.AreCollisionCostsShown:[boolean](/docs/luau/booleans)

Provide feedback

---

AreConstraintForcesShownForSelectedOrHoveredInstances

Roblox Script Security

Read Parallel

PhysicsSettings.AreConstraintForcesShownForSelectedOrHoveredInstances:[boolean](/docs/luau/booleans)

Provide feedback

---

AreConstraintTorquesShownForSelectedOrHoveredInstances

Roblox Script Security

Read Parallel

PhysicsSettings.AreConstraintTorquesShownForSelectedOrHoveredInstances:[boolean](/docs/luau/booleans)

Provide feedback

---

AreContactForcesShownForSelectedOrHoveredAssemblies

Roblox Script Security

Read Parallel

PhysicsSettings.AreContactForcesShownForSelectedOrHoveredAssemblies:[boolean](/docs/luau/booleans)

Provide feedback

---

AreContactIslandsShown

Read Parallel

When set to true, each contact island will render [SelectionBox](/docs/reference/engine/classes/SelectionBox)
adorns on the parts in contact islands, where each contact island is
assigned a random color.

PhysicsSettings.AreContactIslandsShown:[boolean](/docs/luau/booleans)

When set to true, each contact island will render [SelectionBox](/docs/reference/engine/classes/SelectionBox)
adorns on the parts in contact islands, where each contact island is
assigned a random color.

Provide feedback

---

AreContactPointsShown

Read Parallel

When set to true, sphere adorns will be drawn at the contact points of
each part where physics interactions are occurring.

PhysicsSettings.AreContactPointsShown:[boolean](/docs/luau/booleans)

When set to true, sphere adorns will be drawn at the contact points of
each part where physics interactions are occurring. Each sphere also has
an arrow drawn in 3D, facing the surface that the contact point is
detecting.

#### Solver Variations

The behavior of this property varies depending on whether Roblox's physics
engine is using the PGS Physics Solver, or the Spring Physics Solver.

This is controlled by the [Workspace.PGSPhysicsSolverEnabled](/docs/reference/engine/classes/Workspace#PGSPhysicsSolverEnabled)
property.

##### Spring Physics Solver

When [Workspace.PGSPhysicsSolverEnabled](/docs/reference/engine/classes/Workspace#PGSPhysicsSolverEnabled) is set to false, the
contact points are color coded as listed below. The length of the arrow
extruding from the sphere depends on how much force the contact point is
exerting, and what the contact type is.

|  |  |  |
| --- | --- | --- |
| Color | Contact Type | Description |
|  | Normal Contact | Contact point with no special conditions. |
|  | Resting Contact | Contact point that has been active for at least 4 frames. |
|  | Second Pass Contact | Contact point that was made by a kernel joint going through a second pass. Rarely seen. |
|  | Real-Time Contact | Contact point that was made with a real-time physics body. This applies to tripped [Humanoid](/docs/reference/engine/classes/Humanoid). |
|  | Joint Contact | Contact point that was made under the context of a physically simulated joint. This applies to Motors and Hinges. |

**PGS Physics Solver**

When [Workspace.PGSPhysicsSolverEnabled](/docs/reference/engine/classes/Workspace#PGSPhysicsSolverEnabled) is set to true, the contact
points are always colored RED, and the length of the arrow will always
be 1 stud. There are no special conditions tracked, because the PGS solver
does not keep specific lookup tables for the states listed in the Spring
Solver.

|  |  |  |
| --- | --- | --- |
| Color | Contact Type | Description |
|  | Normal Contact | Contact point with no special conditions. |

Provide feedback

---

AreGravityForcesShownForSelectedOrHoveredAssemblies

Roblox Script Security

Read Parallel

PhysicsSettings.AreGravityForcesShownForSelectedOrHoveredAssemblies:[boolean](/docs/luau/booleans)

Provide feedback

---

AreJointCoordinatesShown

Read Parallel

When set to true, XYZ axes are rendered at the [BasePart.CFrame](/docs/reference/engine/classes/BasePart#CFrame) of
every part.

PhysicsSettings.AreJointCoordinatesShown:[boolean](/docs/luau/booleans)

When set to true, XYZ axes are rendered at the [BasePart.CFrame](/docs/reference/engine/classes/BasePart#CFrame) of
every part.

Provide feedback

---

AreMagnitudesShownForDrawnForcesAndTorques

Roblox Script Security

Read Parallel

PhysicsSettings.AreMagnitudesShownForDrawnForcesAndTorques:[boolean](/docs/luau/booleans)

Provide feedback

---

AreMechanismsShown

Read Parallel

When set to true, every individual mechanism of parts is given a unique
color.

PhysicsSettings.AreMechanismsShown:[boolean](/docs/luau/booleans)

When set to true, every individual mechanism of parts is given a unique
color.

Provide feedback

---

AreModelCoordsShown

Read Parallel

An ancient property that hasn't work correctly since late 2007. It's
supposed to render an XYZ axis on the root part of a [Model](/docs/reference/engine/classes/Model), but
the axis rendering component doesn't work correctly.

PhysicsSettings.AreModelCoordsShown:[boolean](/docs/luau/booleans)

An ancient property that hasn't work correctly since late 2007. It's
supposed to render an XYZ axis on the root part of a [Model](/docs/reference/engine/classes/Model), but
the axis rendering component doesn't work correctly.

Provide feedback

---

AreNonAnchorsShown

Read Parallel

PhysicsSettings.AreNonAnchorsShown:[boolean](/docs/luau/booleans)

Provide feedback

---

AreOwnersShown

Read Parallel

When set to true, each player's character is outlined with a unique color,
and each part that the player has network ownership over is outlined with
the same color.

PhysicsSettings.AreOwnersShown:[boolean](/docs/luau/booleans)

When set to true, each player's character is outlined with a unique color,
and each part that the player has network ownership over is outlined with
the same color.

Provide feedback

---

ArePartCoordsShown

Read Parallel

An ancient property that hasn't worked correctly since late 2007. It's
supposed to render a large XYZ axis in the center of each
[BasePart](/docs/reference/engine/classes/BasePart), but the axis rendering component doesn't work correctly.

PhysicsSettings.ArePartCoordsShown:[boolean](/docs/luau/booleans)

An ancient property that hasn't worked correctly since late 2007. It's
supposed to render a large XYZ axis in the center of each
[BasePart](/docs/reference/engine/classes/BasePart), but the axis rendering component doesn't work correctly.

Provide feedback

---

AreRegionsShown

Read Parallel

When set to true, a cylinder is drawn around each player's character,
representing their [Player.SimulationRadius](/docs/reference/engine/classes/Player#SimulationRadius).

PhysicsSettings.AreRegionsShown:[boolean](/docs/luau/booleans)

When set to true, a cylinder is drawn around each player's character,
representing their [Player.SimulationRadius](/docs/reference/engine/classes/Player#SimulationRadius). Each physically
simulated object will check to see which player is closest to that object,
and if they are within the player's simulation radius. If both conditions
are met, that player will becomes the network owner of that object.

Provide feedback

---

AreSolverIslandsShown

Roblox Script Security

Read Parallel

PhysicsSettings.AreSolverIslandsShown:[boolean](/docs/luau/booleans)

Provide feedback

---

AreTerrainReplicationRegionsShown

Read Parallel

PhysicsSettings.AreTerrainReplicationRegionsShown:[boolean](/docs/luau/booleans)

Provide feedback

---

AreTimestepsShown

Roblox Script Security

Read Parallel

PhysicsSettings.AreTimestepsShown:[boolean](/docs/luau/booleans)

Provide feedback

---

AreUnalignedPartsShown

Read Parallel

When set to true, parts that aren't aligned on the 1x1x1 grid will be
outlined yellow.

PhysicsSettings.AreUnalignedPartsShown:[boolean](/docs/luau/booleans)

When set to true, parts that aren't aligned on the 1x1x1 grid will be
outlined yellow.

Provide feedback

---

AreWorldCoordsShown

Read Parallel

An ancient property that hasn't worked correctly since late 2007. It's
supposed to render a large XYZ axis in the center of the world, but the
axis rendering component doesn't work correctly.

PhysicsSettings.AreWorldCoordsShown:[boolean](/docs/luau/booleans)

An ancient property that hasn't worked correctly since late 2007. It's
supposed to render a large XYZ axis in the center of the world, but the
axis rendering component doesn't work correctly.

Provide feedback

---

DisableCSGv2

Read Parallel

When set to true, Roblox will fall back to using its legacy CSG solver
when performing solid model operations.

PhysicsSettings.DisableCSGv2:[boolean](/docs/luau/booleans)

When set to true, Roblox will fall back to using its legacy CSG solver
when performing solid model operations.

Provide feedback

---

DisableCSGv3ForPlugins

Read Parallel

PhysicsSettings.DisableCSGv3ForPlugins:[boolean](/docs/luau/booleans)

Provide feedback

---

DrawConstraintsNetForce

Roblox Script Security

Read Parallel

PhysicsSettings.DrawConstraintsNetForce:[boolean](/docs/luau/booleans)

Provide feedback

---

DrawContactsNetForce

Roblox Script Security

Read Parallel

PhysicsSettings.DrawContactsNetForce:[boolean](/docs/luau/booleans)

Provide feedback

---

DrawTotalNetForce

Roblox Script Security

Read Parallel

PhysicsSettings.DrawTotalNetForce:[boolean](/docs/luau/booleans)

Provide feedback

---

EnableForceVisualizationSmoothing

Roblox Script Security

Read Parallel

PhysicsSettings.EnableForceVisualizationSmoothing:[boolean](/docs/luau/booleans)

Provide feedback

---

FluidForceDrawScale

Roblox Script Security

Read Parallel

Sets the scale of arrows drawn for aerodynamic force visualization.

PhysicsSettings.FluidForceDrawScale:[number](/docs/luau/numbers)

Sets the scale of arrows drawn for aerodynamic force visualization. The
default value is 1.0; smaller values draw smaller arrows and vice versa.
The default value is a good starting point for a wide range of aerodynamic
mechanisms.

Provide feedback

---

ForceCSGv2

Hidden

Not Replicated

Read Parallel

PhysicsSettings.ForceCSGv2:[boolean](/docs/luau/booleans)

Provide feedback

---

ForceDrawScale

Roblox Script Security

Read Parallel

PhysicsSettings.ForceDrawScale:[number](/docs/luau/numbers)

Provide feedback

---

ForceVisualizationSmoothingSteps

Roblox Script Security

Read Parallel

PhysicsSettings.ForceVisualizationSmoothingSteps:[number](/docs/luau/numbers)

Provide feedback

---

IsInterpolationThrottleShown

Read Parallel

PhysicsSettings.IsInterpolationThrottleShown:[boolean](/docs/luau/booleans)

Provide feedback

---

IsReceiveAgeShown

Read Parallel

This property is supposed to show the [BasePart.ReceiveAge](/docs/reference/engine/classes/BasePart#ReceiveAge) of a
part, but it does not work correctly.

PhysicsSettings.IsReceiveAgeShown:[boolean](/docs/luau/booleans)

This property is supposed to show the [BasePart.ReceiveAge](/docs/reference/engine/classes/BasePart#ReceiveAge) of a
part, but it does not work correctly.

Provide feedback

---

IsTreeShown

Read Parallel

When set to true, the joint connections of each part, and the states of
their underlying primitive components are visualized as a spanning tree.

PhysicsSettings.IsTreeShown:[boolean](/docs/luau/booleans)

When set to true, the joint connections of each part, and the states of
their underlying primitive components are visualized as a spanning tree.

##### Spanning Tree Table

There are several visualizations made available when this property is set
to true:

|  |  |  |
| --- | --- | --- |
| Color | Adorn Type | Description |
|  | Box | Root Primitive of a Mechanism that is currently anchored, or connected to an anchored primitive. See [BasePart:IsGrounded()](/docs/reference/engine/classes/BasePart#IsGrounded). |
|  | Box | Root Primitive of a Mechanism that is free to be physically simulated. |
|  | Box | Root Primitive of a Mechanism that has moving components. |
|  | Sphere | Root Primitive of an Assembly. |
|  | Cylinder | Root Primitive of a Clump. |
|  | Line | Connection between two Primitives that share the same Assembly and Clump. |
|  | Line | Connection between two Primitives that share the same Assembly. |
|  | Line | Connection between two Primitives. |

Provide feedback

---

PhysicsEnvironmentalThrottle

Read Parallel

Controls the throttle rate of Roblox's physics engine.

PhysicsSettings.PhysicsEnvironmentalThrottle:[Enum.EnviromentalPhysicsThrottle](/docs/reference/engine/enums/EnviromentalPhysicsThrottle)

Controls the throttle rate of Roblox's physics engine. By default, the
physics engine will adjust the physics environment throttle depending on
how much work the physics engine is doing, and the current framerate. See
the enum page for [Enum.EnviromentalPhysicsThrottle](/docs/reference/engine/enums/EnviromentalPhysicsThrottle) for more information.

Provide feedback

---

ShowDecompositionGeometry

Read Parallel

When set to true, the underlying collision geometry for
[PartOperation](/docs/reference/engine/classes/PartOperation) and [MeshPart](/docs/reference/engine/classes/MeshPart) is rendered.

PhysicsSettings.ShowDecompositionGeometry:[boolean](/docs/luau/booleans)

When set to true, the underlying collision geometry for
[PartOperation](/docs/reference/engine/classes/PartOperation) and [MeshPart](/docs/reference/engine/classes/MeshPart) is rendered.

Provide feedback

---

ShowFluidForcesForSelectedOrHoveredMechanisms

Roblox Script Security

Read Parallel

When set to true, enables aerodynamic visualization for selected or
hovered mechanisms in Studio's play and run modes.

PhysicsSettings.ShowFluidForcesForSelectedOrHoveredMechanisms:[boolean](/docs/luau/booleans)

When set to true, enables aerodynamic visualization for selected or
hovered mechanisms in Studio's play and run modes. This visualization
shows aerodynamic force, torque, and center of pressure for the hovered or
selected mechanisms.

Provide feedback

---

ShowInstanceNamesForDrawnForcesAndTorques

Roblox Script Security

Read Parallel

PhysicsSettings.ShowInstanceNamesForDrawnForcesAndTorques:[boolean](/docs/luau/booleans)

Provide feedback

---

SolverConvergenceMetricType

Roblox Script Security

Read Parallel

PhysicsSettings.SolverConvergenceMetricType:[Enum.SolverConvergenceMetricType](/docs/reference/engine/enums/SolverConvergenceMetricType)

Provide feedback

---

SolverConvergenceVisualizationMode

Roblox Script Security

Read Parallel

PhysicsSettings.SolverConvergenceVisualizationMode:[Enum.SolverConvergenceVisualizationMode](/docs/reference/engine/enums/SolverConvergenceVisualizationMode)

Provide feedback

---

ThrottleAdjustTime

Read Parallel

If the [PhysicsSettings.PhysicsEnvironmentalThrottle](/docs/reference/engine/classes/PhysicsSettings#PhysicsEnvironmentalThrottle) is set to
DefaultAuto, this specifies the maximum time that the physics
environmental throttle has to wait before it is allowed to automatically
change.

PhysicsSettings.ThrottleAdjustTime:[number](/docs/luau/numbers)

If the [PhysicsSettings.PhysicsEnvironmentalThrottle](/docs/reference/engine/classes/PhysicsSettings#PhysicsEnvironmentalThrottle) is set to
DefaultAuto, this specifies the maximum time that the physics
environmental throttle has to wait before it is allowed to automatically
change.

Provide feedback

---

TorqueDrawScale

Roblox Script Security

Read Parallel

PhysicsSettings.TorqueDrawScale:[number](/docs/luau/numbers)

Provide feedback

---

UseCSGv2

Read Parallel

If set to true, version 2 of Roblox's CSG solver will be used instead of
version 1.

PhysicsSettings.UseCSGv2:[boolean](/docs/luau/booleans)

If set to true, version 2 of Roblox's CSG solver will be used instead of
version 1.

Provide feedback

---