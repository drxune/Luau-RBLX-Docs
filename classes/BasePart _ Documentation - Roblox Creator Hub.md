# BasePart | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BasePart
Scraped: 2026-01-11T02:37:18.105800Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- PVInstance
- BasePart
- Player
- Instance
- Object
- CornerWedgePart
- FormFactorPart
- Terrain
- TriangleMeshPart
- TrussPart
- Workspace
- Part
- MeshPart
- WedgePart
- SpawnLocation
- BaseParts
- Model
- PVInstance:PivotTo()
- Decal
- Texture
- SurfaceGui
- GuiObjects
- Attachments
- Constraint
- ParticleEmitter
- PointLight
- Tool
- Touched
- CFrame
- Position
- AssemblyLinearVelocity
- AssemblyAngularVelocity
- Weld
- Torque
- AngularVelocity
- ApplyAngularImpulse()
- Script
- LocalScript
- RunContext
- Mass
- AssemblyCenterOfMass
- GetVelocityAtPosition()
- VectorForce
- ApplyImpulse()
- Massless
- RootPriority
- CastShadow
- Material
- Color
- Transparency
- Reflectance
- Anchored
- Workspace.FallenPartsDestroyHeight
- CanTouch
- GetPartBoundsInBox
- Raycast
- CanCollide
- TouchEnded
- TouchTransmitter
- Workspace.TouchesUseCollisionGroups
- Raycasts
- Parts
- ExtentsCFrame
- BasePart.Position
- Attachment
- PhysicsService:CollisionGroupSetCollidable()
- BrickColor
- Workspace.FluidForces
- BasePart.Transparency
- GetMass()
- Size
- Shape
- CustomPhysicalProperties
- AssemblyRootPart
- MaterialVariant
- MaterialService
- Welds
- Motor6Ds
- C0
- C1
- WeldConstraints
- BasePart:GetPivot()
- BasePart.CFrame
- BasePart.PivotOffset
- Handles
- Handles.Faces
- Resize()
- ExtentsSize
- BlockMesh
- SpecialMesh
- MeshTypes
- SurfaceLight
- LocalTransparencyModifier
- mass
- center of mass
- BasePart:SetNetworkOwner()
- BasePart:SetNetworkOwnershipAuto()
- joint
- Snap
- ManualWeld
- Motor
- Motor6D
- WeldConstraint
- BasePart.CanCollide
- TouchInterest
- WorldRoot:GetPartsInPart()
- IntersectOperation
- PartOperation
- MeshParts
- Clone()
- Parent
- Density
- Elasticity
- ElasticityWeight
- Friction
- FrictionWeight
- IntersectAsync()
- Destroy()
- UsePartColor
- UnionOperation
- SubtractAsync()
- UnionAsync()
- PartA.Touched
- PartB.Touched
- BasePart.Touched
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PVInstance](/docs/reference/engine/classes/PVInstance)
6. /
7. [BasePart](/docs/reference/engine/classes/BasePart)

English

Feedback

Engine Class

BasePart

The abstract base class for in-world objects that physically interact.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [Anchored](#Anchored):[boolean](/docs/luau/booleans) |
| [AssemblyAngularVelocity](#AssemblyAngularVelocity):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [AssemblyCenterOfMass](#AssemblyCenterOfMass):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [AssemblyLinearVelocity](#AssemblyLinearVelocity):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [AssemblyMass](#AssemblyMass):[number](/docs/luau/numbers) |
| [AssemblyRootPart](#AssemblyRootPart):[BasePart](/docs/reference/engine/classes/BasePart) |
| [AudioCanCollide](#AudioCanCollide):[boolean](/docs/luau/booleans) |
| [BackParamA](#BackParamA):[number](/docs/luau/numbers)  Deprecated |
| [BackParamB](#BackParamB):[number](/docs/luau/numbers)  Deprecated |
| [BackSurface](#BackSurface):[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) |
| [BackSurfaceInput](#BackSurfaceInput):[Enum.InputType](/docs/reference/engine/enums/InputType)  Deprecated |
| [BottomParamA](#BottomParamA):[number](/docs/luau/numbers)  Deprecated |
| [BottomParamB](#BottomParamB):[number](/docs/luau/numbers)  Deprecated |
| [BottomSurface](#BottomSurface):[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) |
| [BottomSurfaceInput](#BottomSurfaceInput):[Enum.InputType](/docs/reference/engine/enums/InputType)  Deprecated |
| [BrickColor](#BrickColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor) |
| [brickColor](#brickColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |
| [CanCollide](#CanCollide):[boolean](/docs/luau/booleans) |
| [CanQuery](#CanQuery):[boolean](/docs/luau/booleans) |
| [CanTouch](#CanTouch):[boolean](/docs/luau/booleans) |
| [CastShadow](#CastShadow):[boolean](/docs/luau/booleans) |
| [CenterOfMass](#CenterOfMass):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [CollisionGroup](#CollisionGroup):[string](/docs/luau/strings) |
| [CollisionGroupId](#CollisionGroupId):[number](/docs/luau/numbers)  Deprecated |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [CurrentPhysicalProperties](#CurrentPhysicalProperties):[PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) |
| [CustomPhysicalProperties](#CustomPhysicalProperties):[PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) |
| [Elasticity](#Elasticity):[number](/docs/luau/numbers)  Deprecated |
| [EnableFluidForces](#EnableFluidForces):[boolean](/docs/luau/booleans) |
| [ExtentsCFrame](#ExtentsCFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [ExtentsSize](#ExtentsSize):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Friction](#Friction):[number](/docs/luau/numbers)  Deprecated |
| [FrontParamA](#FrontParamA):[number](/docs/luau/numbers)  Deprecated |
| [FrontParamB](#FrontParamB):[number](/docs/luau/numbers)  Deprecated |
| [FrontSurface](#FrontSurface):[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) |
| [FrontSurfaceInput](#FrontSurfaceInput):[Enum.InputType](/docs/reference/engine/enums/InputType)  Deprecated |
| [LeftParamA](#LeftParamA):[number](/docs/luau/numbers)  Deprecated |
| [LeftParamB](#LeftParamB):[number](/docs/luau/numbers)  Deprecated |
| [LeftSurface](#LeftSurface):[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) |
| [LeftSurfaceInput](#LeftSurfaceInput):[Enum.InputType](/docs/reference/engine/enums/InputType)  Deprecated |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [Locked](#Locked):[boolean](/docs/luau/booleans) |
| [Mass](#Mass):[number](/docs/luau/numbers) |
| [Massless](#Massless):[boolean](/docs/luau/booleans) |
| [Material](#Material):[Enum.Material](/docs/reference/engine/enums/Material) |
| [MaterialVariant](#MaterialVariant):[string](/docs/luau/strings) |
| [Orientation](#Orientation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [PivotOffset](#PivotOffset):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ReceiveAge](#ReceiveAge):[number](/docs/luau/numbers) |
| [Reflectance](#Reflectance):[number](/docs/luau/numbers) |
| [ResizeableFaces](#ResizeableFaces):[Faces](/docs/reference/engine/datatypes/Faces) |
| [ResizeIncrement](#ResizeIncrement):[number](/docs/luau/numbers) |
| [RightParamA](#RightParamA):[number](/docs/luau/numbers)  Deprecated |
| [RightParamB](#RightParamB):[number](/docs/luau/numbers)  Deprecated |
| [RightSurface](#RightSurface):[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) |
| [RightSurfaceInput](#RightSurfaceInput):[Enum.InputType](/docs/reference/engine/enums/InputType)  Deprecated |
| [RootPriority](#RootPriority):[number](/docs/luau/numbers) |
| [Rotation](#Rotation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [RotVelocity](#RotVelocity):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [Size](#Size):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [SpecificGravity](#SpecificGravity):[number](/docs/luau/numbers)  Deprecated |
| [TopParamA](#TopParamA):[number](/docs/luau/numbers)  Deprecated |
| [TopParamB](#TopParamB):[number](/docs/luau/numbers)  Deprecated |
| [TopSurface](#TopSurface):[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) |
| [TopSurfaceInput](#TopSurfaceInput):[Enum.InputType](/docs/reference/engine/enums/InputType)  Deprecated |
| [Transparency](#Transparency):[number](/docs/luau/numbers) |
| [Velocity](#Velocity):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |

Methods

|  |
| --- |
| [AngularAccelerationToTorque](#AngularAccelerationToTorque)(angAcceleration: [Vector3](/docs/reference/engine/datatypes/Vector3),angVelocity: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ApplyAngularImpulse](#ApplyAngularImpulse)(impulse: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [ApplyImpulse](#ApplyImpulse)(impulse: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [ApplyImpulseAtPosition](#ApplyImpulseAtPosition)(impulse: [Vector3](/docs/reference/engine/datatypes/Vector3),position: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [BreakJoints](#BreakJoints)():()  Deprecated |
| [breakJoints](#breakJoints)():()  Deprecated |
| [CanCollideWith](#CanCollideWith)(part: [BasePart](/docs/reference/engine/classes/BasePart)):[boolean](/docs/luau/booleans) |
| [CanSetNetworkOwnership](#CanSetNetworkOwnership)():[Tuple](/docs/luau/tuples) |
| [GetClosestPointOnSurface](#GetClosestPointOnSurface)(position: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GetConnectedParts](#GetConnectedParts)(recursive: [boolean](/docs/luau/booleans)):Instances |
| [GetJoints](#GetJoints)():Instances |
| [GetMass](#GetMass)():[number](/docs/luau/numbers) |
| [getMass](#getMass)():[number](/docs/luau/numbers)  Deprecated |
| [GetNetworkOwner](#GetNetworkOwner)():[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetNetworkOwnershipAuto](#GetNetworkOwnershipAuto)():[boolean](/docs/luau/booleans) |
| [GetNoCollisionConstraints](#GetNoCollisionConstraints)():Instances |
| [GetRenderCFrame](#GetRenderCFrame)():[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [GetRootPart](#GetRootPart)():[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [GetTouchingParts](#GetTouchingParts)():Instances |
| [GetVelocityAtPosition](#GetVelocityAtPosition)(position: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [IntersectAsync](#IntersectAsync)(parts: Instances,collisionfidelity: [Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity),renderFidelity: [Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [IsGrounded](#IsGrounded)():[boolean](/docs/luau/booleans) |
| [MakeJoints](#MakeJoints)():()  Deprecated |
| [makeJoints](#makeJoints)():()  Deprecated |
| [Resize](#Resize)(normalId: [Enum.NormalId](/docs/reference/engine/enums/NormalId),deltaAmount: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [resize](#resize)(normalId: [Enum.NormalId](/docs/reference/engine/enums/NormalId),deltaAmount: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [SetNetworkOwner](#SetNetworkOwner)(playerInstance: [Player](/docs/reference/engine/classes/Player)):() |
| [SetNetworkOwnershipAuto](#SetNetworkOwnershipAuto)():() |
| [SubtractAsync](#SubtractAsync)(parts: Instances,collisionfidelity: [Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity),renderFidelity: [Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [TorqueToAngularAcceleration](#TorqueToAngularAcceleration)(torque: [Vector3](/docs/reference/engine/datatypes/Vector3),angVelocity: [Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [UnionAsync](#UnionAsync)(parts: Instances,collisionfidelity: [Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity),renderFidelity: [Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)):[Instance](/docs/reference/engine/datatypes/Instance) |

Events

|  |
| --- |
| [LocalSimulationTouched](#LocalSimulationTouched)(part: [BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [OutfitChanged](#OutfitChanged)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [StoppedTouching](#StoppedTouching)(otherPart: [BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [Touched](#Touched)(otherPart: [BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchEnded](#TouchEnded)(otherPart: [BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[CornerWedgePart](/docs/reference/engine/classes/CornerWedgePart), [FormFactorPart](/docs/reference/engine/classes/FormFactorPart), [Terrain](/docs/reference/engine/classes/Terrain), [TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart), [TrussPart](/docs/reference/engine/classes/TrussPart), Show more...

[BasePart](/docs/reference/engine/classes/BasePart) is an abstract base class for in-world objects that render
and are physically simulated while in the [Workspace](/docs/reference/engine/classes/Workspace). There are several
implementations of [BasePart](/docs/reference/engine/classes/BasePart), the most common being [Part](/docs/reference/engine/classes/Part) and
[MeshPart](/docs/reference/engine/classes/MeshPart). Others include [WedgePart](/docs/reference/engine/classes/WedgePart), [SpawnLocation](/docs/reference/engine/classes/SpawnLocation), and
the singleton [Terrain](/docs/reference/engine/classes/Terrain) object. Generally, when documentation refers to
a "part," most [BasePart](/docs/reference/engine/classes/BasePart) implementations will work and not just
[Part](/docs/reference/engine/classes/Part).

For information on how [BaseParts](/docs/reference/engine/classes/BasePart) are grouped into simulated
rigid bodies, see [Assemblies](/docs/physics/assemblies).

There are many different objects that interact with [BasePart](/docs/reference/engine/classes/BasePart) (other
than [Terrain](/docs/reference/engine/classes/Terrain)), including:

* Several [BaseParts](/docs/reference/engine/classes/BasePart) may be grouped within a [Model](/docs/reference/engine/classes/Model) and
  moved at the same time using [PVInstance:PivotTo()](/docs/reference/engine/classes/PVInstance#PivotTo). See
  [Models](/docs/parts/models).
* A [Decal](/docs/reference/engine/classes/Decal) applies a stretched image texture to the faces of a
  [BasePart](/docs/reference/engine/classes/BasePart), while a [Texture](/docs/reference/engine/classes/Texture) applies a tiled image texture to
  the faces. See [Textures and Decals](/docs/parts/textures-decals).
* A [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) renders [GuiObjects](/docs/reference/engine/classes/GuiObject) on the face of a
  part. See
  [In-Experience UI Containers](/docs/ui/in-experience-containers).
* [Attachments](/docs/reference/engine/classes/Attachment) can be added to a [BasePart](/docs/reference/engine/classes/BasePart) to specify
  [CFrames](/docs/reference/engine/datatypes/CFrame) relative to the part. These are often used by
  physical [Constraint](/docs/reference/engine/classes/Constraint) objects as outlined in
  [Mechanical Constraints](/docs/physics/mechanical-constraints) and
  [Mover Constraints](/docs/physics/mover-constraints).
* [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) objects emit particles uniformly in the volume of
  the [BasePart](/docs/reference/engine/classes/BasePart) to which they are parented. See
  [Particle Emitters](/docs/effects/particle-emitters).
* Light objects like [PointLight](/docs/reference/engine/classes/PointLight) emit light from the center of a
  [BasePart](/docs/reference/engine/classes/BasePart) as illustrated in
  [Light Sources](/docs/effects/light-sources).
* If parented to a [Tool](/docs/reference/engine/classes/Tool) and given the name Handle, a
  [BasePart](/docs/reference/engine/classes/BasePart) can be held by characters. See
  [In-Experience Tools](/docs/players/tools).

---

API Reference

Properties

Anchored

Read Parallel

Determines whether a part is immovable by physics.

BasePart.Anchored:[boolean](/docs/luau/booleans)

The Anchored property determines whether the part will be immovable by
physics. When enabled, a part will never change position due to gravity,
other part collisions, overlapping other parts, or any other
physics-related causes. As a result, two anchored parts will never fire
the [Touched](/docs/reference/engine/classes/BasePart#Touched) event on each other.

An anchored part may still be moved by changing its
[CFrame](/docs/reference/engine/classes/BasePart#CFrame) or [Position](/docs/reference/engine/classes/BasePart#Position), and
it still may have a nonzero
[AssemblyLinearVelocity](/docs/reference/engine/classes/BasePart#AssemblyLinearVelocity) and
[AssemblyAngularVelocity](/docs/reference/engine/classes/BasePart#AssemblyAngularVelocity).

Finally, if an unanchored part is joined with an anchored part through an
object like a [Weld](/docs/reference/engine/classes/Weld), it too will act anchored. If such a joint
breaks, the part may be affected by physics again. See
[Assemblies](/docs/physics/assemblies) for more details.

Network ownership cannot be set on anchored parts. If a part's anchored
status changes on the server, the network ownership of that part will be
affected.

Code Samples

Part Anchored Toggle

This code sample will allow a part to be clicked to toggle its anchored property. When toggled, the visual appearance of the part is updated (red means anchored, yellow means free).

```
local part = script.Parent



-- Create a ClickDetector so we can tell when the part is clicked



local cd = Instance.new("ClickDetector", part)



-- This function updates how the part looks based on its Anchored state



local function updateVisuals()



if part.Anchored then



-- When the part is anchored...



part.BrickColor = BrickColor.new("Bright red")



part.Material = Enum.Material.DiamondPlate



else



-- When the part is unanchored...



part.BrickColor = BrickColor.new("Bright yellow")



part.Material = Enum.Material.Wood



end



end



local function onToggle()



-- Toggle the anchored property



part.Anchored = not part.Anchored



-- Update visual state of the brick



updateVisuals()



end



-- Update, then start listening for clicks



updateVisuals()



cd.MouseClick:Connect(onToggle)
```

Provide feedback

---

AssemblyAngularVelocity

Not Replicated

Read Parallel

The angular velocity of the part's assembly.

BasePart.AssemblyAngularVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

The angular velocity vector of this part's assembly. It's the rate of
change of orientation in radians per second.

Angular velocity is the same at every point of the assembly.

Setting the velocity directly may lead to unrealistic motion. Using
[Torque](/docs/reference/engine/classes/Torque) or [AngularVelocity](/docs/reference/engine/classes/AngularVelocity) constraint is preferred, or use
[ApplyAngularImpulse()](/docs/reference/engine/classes/BasePart#ApplyAngularImpulse) if you want
instantaneous change in velocity.

If the part is [owned](/docs/physics/network-ownership) by the
server, this property must be changed from a server [Script](/docs/reference/engine/classes/Script) (not
from a [LocalScript](/docs/reference/engine/classes/LocalScript) or a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client)).
If the part is owned by a client through automatic ownership, this
property can be changed from either a client script or a server
script; changing it from a client script for a server-owned part will have
no effect.

Provide feedback

---

AssemblyCenterOfMass

Read Only

Not Replicated

Read Parallel

The center of mass of the part's assembly in world space.

BasePart.AssemblyCenterOfMass:[Vector3](/docs/reference/engine/datatypes/Vector3)

A position calculated via the [Mass](/docs/reference/engine/classes/BasePart#Mass) and
[Position](/docs/reference/engine/classes/BasePart#Position) of all the parts in the assembly.

If the assembly has an anchored part, that part's center of mass will be
the assembly's center of mass, and the assembly will have infinite mass.

Knowing the center of mass can help the assembly maintain stability. A
force applied to the center of mass will not cause angular acceleration,
only linear. An assembly with a low center of mass will have a better time
staying upright under the effect of gravity.

Provide feedback

---

AssemblyLinearVelocity

Not Replicated

Read Parallel

The linear velocity of the part's assembly.

BasePart.AssemblyLinearVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

The linear velocity vector of this part's assembly. It's the rate of
change in position of
[AssemblyCenterOfMass](/docs/reference/engine/classes/BasePart#AssemblyCenterOfMass) in studs per
second.

If you want to know the velocity at a point other than the assembly's
center of mass, use
[GetVelocityAtPosition()](/docs/reference/engine/classes/BasePart#GetVelocityAtPosition).

Setting the velocity directly may lead to unrealistic motion. Using a
[VectorForce](/docs/reference/engine/classes/VectorForce) constraint is preferred, or use
[ApplyImpulse()](/docs/reference/engine/classes/BasePart#ApplyImpulse) if you want instantaneous
change in velocity.

If the part is [owned](/docs/physics/network-ownership) by the
server, this property must be changed from a server [Script](/docs/reference/engine/classes/Script) (not
from a [LocalScript](/docs/reference/engine/classes/LocalScript) or a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client)).
If the part is owned by a client through automatic ownership, this
property can be changed from either a client script or a server
script; changing it from a client script for a server-owned part will have
no effect.

Provide feedback

---

AssemblyMass

Read Only

Not Replicated

Read Parallel

The total mass of the part's assembly.

BasePart.AssemblyMass:[number](/docs/luau/numbers)

The sum of the mass of all the [BaseParts](/docs/reference/engine/classes/BasePart) in this part's
assembly. Parts that are [Massless](/docs/reference/engine/classes/BasePart#Massless) and are not
the assembly's root part will not contribute to the AssemblyMass.

If the assembly has an anchored part, the assembly's mass is considered
infinite. Constraints and other physical interactions between unanchored
assemblies with a large difference in mass may cause instabilities.

Provide feedback

---

AssemblyRootPart

Read Only

Not Replicated

Read Parallel

A reference to the root part of the assembly.

BasePart.AssemblyRootPart:[BasePart](/docs/reference/engine/classes/BasePart)

This property indicates the [BasePart](/docs/reference/engine/classes/BasePart) automatically chosen to
represent the assembly's root part. If the part is not parented to the
[Workspace](/docs/reference/engine/classes/Workspace), this property will be nil.

The root part can be changed by changing the
[RootPriority](/docs/reference/engine/classes/BasePart#RootPriority) of the parts in the assembly.

Parts that all share the same AssemblyRootPart are in the same assembly.

For more information on root parts, see
[Assemblies](/docs/physics/assemblies).

Provide feedback

---

AudioCanCollide

Read Parallel

Determines whether the part will physically interact with audio
simulation, similar to [CastShadow](/docs/reference/engine/classes/BasePart#CastShadow) for
lighting.

BasePart.AudioCanCollide:[boolean](/docs/luau/booleans)

AudioCanCollide determines whether the part will physically interact
with audio simulation, similar to [CastShadow](/docs/reference/engine/classes/BasePart#CastShadow)
for lighting.

When disabled, audio passes through the part; it is not occluded or
reflected.

Provide feedback

---

BackParamA

Deprecated

Show details

---

BackParamB

Deprecated

Show details

---

BackSurface

Read Parallel

Determines the type of surface for the back face of a part.

BasePart.BackSurface:[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType)

The BackSurface property determines the type of surface used for the
positive Z direction of a part. When two parts' faces are placed next
to each other, they may create a joint between them.

Provide feedback

---

BackSurfaceInput

Deprecated

Show details

---

BottomParamA

Deprecated

Show details

---

BottomParamB

Deprecated

Show details

---

BottomSurface

Read Parallel

Determines the type of surface for the bottom face of a part.

BasePart.BottomSurface:[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType)

The BottomSurface property determines the type of surface used for the
negative Y direction of a part. When two parts' faces are placed next
to each other, they may create a joint between them.

Provide feedback

---

BottomSurfaceInput

Deprecated

Show details

---

BrickColor

Not Replicated

Read Parallel

Determines the color of a part.

BasePart.BrickColor:[BrickColor](/docs/reference/engine/datatypes/BrickColor)

This property determines the color of a part. If the part has a
[Material](/docs/reference/engine/classes/BasePart#Material), this also determines the color used
when rendering the material texture. For more control over the color, the
[Color](/docs/reference/engine/classes/BasePart#Color) property can be used and this property will
use the closest BrickColor.

Other visual properties of a part are determined by
[Transparency](/docs/reference/engine/classes/BasePart#Transparency) and
[Reflectance](/docs/reference/engine/classes/BasePart#Reflectance).

Provide feedback

---

brickColor

Deprecated

Show details

---

CanCollide

Read Parallel

Determines whether a part may collide with other parts.

BasePart.CanCollide:[boolean](/docs/luau/booleans)

CanCollide determines whether a part will physically interact with other
parts. When disabled, other parts can pass through the part uninterrupted.
Parts used for decoration usually have CanCollide disabled, as they
need not be considered by the physics engine.

If a part is not [Anchored](/docs/reference/engine/classes/BasePart#Anchored) and has CanCollide
disabled, it may fall out of the world to be eventually destroyed by
[Workspace.FallenPartsDestroyHeight](/docs/reference/engine/classes/Workspace#FallenPartsDestroyHeight).

When CanCollide is disabled, parts may still fire the
[Touched](/docs/reference/engine/classes/BasePart#Touched) event (as well the other parts touching
them). You can disable this with [CanTouch](/docs/reference/engine/classes/BasePart#CanTouch).

For more information on collisions, see
[Collisions](/docs/workspace/collisions).

Code Samples

Fade Door

This code sample shows how a part can fade away when touched by a Humanoid
then reappear a moment after to create a passable door.

```
-- Paste into a Script inside a tall part



local part = script.Parent



local OPEN_TIME = 1



-- Can the door be opened at the moment?



local debounce = false



local function open()



part.CanCollide = false



part.Transparency = 0.7



part.BrickColor = BrickColor.new("Black")



end



local function close()



part.CanCollide = true



part.Transparency = 0



part.BrickColor = BrickColor.new("Bright blue")



end



local function onTouch(otherPart)



-- If the door was already open, do nothing



if debounce then



print("D")



return



end



-- Check if touched by a Humanoid



local human = otherPart.Parent:FindFirstChildOfClass("Humanoid")



if not human then



print("not human")



return



end



-- Perform the door opening sequence



debounce = true



open()



task.wait(OPEN_TIME)



close()



debounce = false



end



part.Touched:Connect(onTouch)



close()
```

Provide feedback

---

CanQuery

Read Parallel

Determines whether the part is considered during spatial query operations.

BasePart.CanQuery:[boolean](/docs/luau/booleans)

This property determines whether the part is considered during spatial
query operations, such as
[GetPartBoundsInBox](/docs/reference/engine/classes/WorldRoot#GetPartBoundsInBox) or
[Raycast](/docs/reference/engine/classes/WorldRoot#Raycast). Note that
[CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) must be disabled for CanQuery to
take effect, and spatial query functions will never include parts with
CanQuery of false.

Beyond this property, it is also possible to exclude parts which are
descendants of a given list of parts using an [OverlapParams](/docs/reference/engine/datatypes/OverlapParams) or
[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) object when calling the spatial query functions.

Provide feedback

---

CanTouch

Read Parallel

Determines if [Touched](/docs/reference/engine/classes/BasePart#Touched) and
[TouchEnded](/docs/reference/engine/classes/BasePart#TouchEnded) events fire on the part.

BasePart.CanTouch:[boolean](/docs/luau/booleans)

This property determines if [Touched](/docs/reference/engine/classes/BasePart#Touched) and
[TouchEnded](/docs/reference/engine/classes/BasePart#TouchEnded) events fire on the part. If true,
other touching parts must also have CanTouch set to true for touch
events to fire. If false, touch events cannot be set up for the part and
attempting to do so will throw an error. Similarly, if the property is set
to false after a touch event is connected, the event will be
disconnected and the [TouchTransmitter](/docs/reference/engine/classes/TouchTransmitter) removed.

Note that this collision logic can be set to respect
[collision groups](/docs/workspace/collisions#collision-filtering)
through the [Workspace.TouchesUseCollisionGroups](/docs/reference/engine/classes/Workspace#TouchesUseCollisionGroups) property. If
true, parts in non-colliding groups will ignore both collisions and
touch events, thereby making this property irrelevant.

#### Performance

There is a small performance gain on parts that have both CanTouch and
[CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) set to false, as these parts will
never need to compute any kind of part to part collisions. However, they
can still be hit by [Raycasts](/docs/reference/engine/classes/WorldRoot#Raycast) and
[OverlapParams](/docs/reference/engine/datatypes/OverlapParams) queries.

Provide feedback

---

CastShadow

Read Parallel

Determines whether or not a part casts a shadow.

BasePart.CastShadow:[boolean](/docs/luau/booleans)

Determines whether or not a part casts a shadow. Disabling this property
for a given part can cause visual artifacts on the shadows cast upon that
part.

This property is not designed for performance enhancement, but in complex
scenes, strategically disabling it on certain parts can improve
performance. Due to the possibility of visual artifacts, we recommend
leaving it enabled on all parts in most situations.

Provide feedback

---

CenterOfMass

Read Only

Not Replicated

Read Parallel

Describes the world position in which a part's center of mass is located.

BasePart.CenterOfMass:[Vector3](/docs/reference/engine/datatypes/Vector3)

The CenterOfMass property describes the local position of a part's
center of mass. If this is a single part assembly, this is the
[AssemblyCenterOfMass](/docs/reference/engine/classes/BasePart#AssemblyCenterOfMass) converted from
world space to local. On simple [Parts](/docs/reference/engine/classes/Part), the center of mass is
always (0, 0, 0), but it can vary for [WedgePart](/docs/reference/engine/classes/WedgePart) or
[MeshPart](/docs/reference/engine/classes/MeshPart).

Provide feedback

---

CFrame

Read Parallel

Determines the position and orientation of the [BasePart](/docs/reference/engine/classes/BasePart) in the
world.

BasePart.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

The CFrame property determines both the position and orientation of the
[BasePart](/docs/reference/engine/classes/BasePart) in the world. It acts as an arbitrary reference location
on the geometry, but [ExtentsCFrame](/docs/reference/engine/classes/BasePart#ExtentsCFrame)
represents the actual [CFrame](/docs/reference/engine/datatypes/CFrame) of its physical center.

When setting CFrame on a part, other joined parts are also moved
relative to the part, but it is recommended that you use
[PVInstance:PivotTo()](/docs/reference/engine/classes/PVInstance#PivotTo) to move an entire model, such as when
teleporting a player's character.

Unlike setting [BasePart.Position](/docs/reference/engine/classes/BasePart#Position), setting CFrame will always
move the part to the exact given [CFrame](/docs/reference/engine/datatypes/CFrame); in other words: no
overlap checking is done and the physics solver will attempt to resolve
any overlap unless both parts are [Anchored](/docs/reference/engine/classes/BasePart#Anchored).

For keeping track of positions relative to a part's [CFrame](/docs/reference/engine/datatypes/CFrame), an
[Attachment](/docs/reference/engine/classes/Attachment) may be useful.

Code Samples

Setting Part CFrame

This code sample demonstrates setting a part's CFrame in many different ways.
It showcases how to create and compose CFrame values. It references a sibling
part called "OtherPart" for demonstrating relative positioning.

```
local part = script.Parent:WaitForChild("Part")



local otherPart = script.Parent:WaitForChild("OtherPart")



-- Reset the part's CFrame to (0, 0, 0) with no rotation.



-- This is sometimes called the "identity" CFrame



part.CFrame = CFrame.new()



-- Set to a specific position (X, Y, Z)



part.CFrame = CFrame.new(0, 25, 10)



-- Same as above, but use a Vector3 instead



local point = Vector3.new(0, 25, 10)



part.CFrame = CFrame.new(point)



-- Set the part's CFrame to be at one point, looking at another



local lookAtPoint = Vector3.new(0, 20, 15)



part.CFrame = CFrame.lookAt(point, lookAtPoint)



-- Rotate the part's CFrame by pi/2 radians on local X axis



part.CFrame = part.CFrame * CFrame.Angles(math.pi / 2, 0, 0)



-- Rotate the part's CFrame by 45 degrees on local Y axis



part.CFrame = part.CFrame * CFrame.Angles(0, math.rad(45), 0)



-- Rotate the part's CFrame by 180 degrees on global Z axis (note the order!)



part.CFrame = CFrame.Angles(0, 0, math.pi) * part.CFrame -- Pi radians is equal to 180 degrees



-- Composing two CFrames is done using * (the multiplication operator)



part.CFrame = CFrame.new(2, 3, 4) * CFrame.new(4, 5, 6) --> equal to CFrame.new(6, 8, 10)



-- Unlike algebraic multiplication, CFrame composition is NOT communitative: a * b is not necessarily b * a!



-- Imagine * as an ORDERED series of actions. For example, the following lines produce different CFrames:



-- 1) Slide the part 5 units on X.



-- 2) Rotate the part 45 degrees around its Y axis.



part.CFrame = CFrame.new(5, 0, 0) * CFrame.Angles(0, math.rad(45), 0)



-- 1) Rotate the part 45 degrees around its Y axis.



-- 2) Slide the part 5 units on X.



part.CFrame = CFrame.Angles(0, math.rad(45), 0) * CFrame.new(5, 0, 0)



-- There is no "CFrame division", but instead simply "doing the inverse operation".



part.CFrame = CFrame.new(4, 5, 6) * CFrame.new(4, 5, 6):Inverse() --> is equal to CFrame.new(0, 0, 0)



part.CFrame = CFrame.Angles(0, 0, math.pi) * CFrame.Angles(0, 0, math.pi):Inverse() --> equal to CFrame.Angles(0, 0, 0)



-- Position a part relative to another (in this case, put our part on top of otherPart)



part.CFrame = otherPart.CFrame * CFrame.new(0, part.Size.Y / 2 + otherPart.Size.Y / 2, 0)
```

Provide feedback

---

CollisionGroup

Not Replicated

Read Parallel

Describes the name of a part's collision group.

BasePart.CollisionGroup:[string](/docs/luau/strings)

The CollisionGroup property describes the name of the part's collision
group (maximum of 100 characters). Parts start off in the default group
whose name is "Default". This value cannot be empty.

Although this property itself is non-replicated, the engine internally
replicates the value through another private property to solve backward
compatibility issues.

Code Samples

PhysicsService:RegisterCollisionGroup

This example demonstrates one basic use of collision groups. It assigns
BallPart to "CollisionGroupBall" and DoorPart to
"CollisionGroupDoor", then makes the two groups non-collidable using
[PhysicsService:CollisionGroupSetCollidable()](/docs/reference/engine/classes/PhysicsService#CollisionGroupSetCollidable).

```
local PhysicsService = game:GetService("PhysicsService")



local collisionGroupBall = "CollisionGroupBall"



local collisionGroupDoor = "CollisionGroupDoor"



-- Register collision groups



PhysicsService:RegisterCollisionGroup(collisionGroupBall)



PhysicsService:RegisterCollisionGroup(collisionGroupDoor)



-- Assign parts to collision groups



script.Parent.BallPart.CollisionGroup = collisionGroupBall



script.Parent.DoorPart.CollisionGroup = collisionGroupDoor



-- Set groups as non-collidable with each other and check the result



PhysicsService:CollisionGroupSetCollidable(collisionGroupBall, collisionGroupDoor, false)



print(PhysicsService:CollisionGroupsAreCollidable(collisionGroupBall, collisionGroupDoor)) --> false
```

Provide feedback

---

CollisionGroupId

Deprecated

Show details

---

Color

Not Replicated

Read Parallel

Determines the color of a part.

BasePart.Color:[Color3](/docs/reference/engine/datatypes/Color3)

The Color property determines the color of a part. If the part has a
[Material](/docs/reference/engine/classes/BasePart#Material), this also determines the color used
when rendering the material texture.

If this property is set, [BrickColor](/docs/reference/engine/classes/BasePart#BrickColor) will use
the closest match to this Color value.

Other visual properties of a part are determined by
[Transparency](/docs/reference/engine/classes/BasePart#Transparency) and
[Reflectance](/docs/reference/engine/classes/BasePart#Reflectance).

Code Samples

Character Health Body Color

This code sample colors a player's entire character based on how much health
they have. It generates a color based on their max health, then sets the color
properties of objects within their character, removing any extra objects.

```
-- Paste into a Script within StarterCharacterScripts



-- Then play the game, and fiddle with your character's health



local char = script.Parent



local human = char.Humanoid



local colorHealthy = Color3.new(0.4, 1, 0.2)



local colorUnhealthy = Color3.new(1, 0.4, 0.2)



local function setColor(color)



for _, child in pairs(char:GetChildren()) do



if child:IsA("BasePart") then



child.Color = color



while child:FindFirstChildOfClass("Decal") do



child:FindFirstChildOfClass("Decal"):Destroy()



end



elseif child:IsA("Accessory") then



child.Handle.Color = color



local mesh = child.Handle:FindFirstChildOfClass("SpecialMesh")



if mesh then



mesh.TextureId = ""



end



elseif child:IsA("Shirt") or child:IsA("Pants") then



child:Destroy()



end



end



end



local function update()



local percentage = human.Health / human.MaxHealth



-- Create a color by tweening based on the percentage of your health



-- The color goes from colorHealthy (100%) ----- > colorUnhealthy (0%)



local color = Color3.new(



colorHealthy.R * percentage + colorUnhealthy.r * (1 - percentage),



colorHealthy.G * percentage + colorUnhealthy.g * (1 - percentage),



colorHealthy.B * percentage + colorUnhealthy.b * (1 - percentage)



)



setColor(color)



end



update()



human.HealthChanged:Connect(update)
```

Provide feedback

---

CurrentPhysicalProperties

Read Only

Not Replicated

Read Parallel

Indicates the current physical properties of the part.

BasePart.CurrentPhysicalProperties:[PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties)

CurrentPhysicalProperties indicates the current physical properties of
the part. You can set custom values for the physical properties per part,
[custom material](/docs/parts/materials), and material override. The
Roblox engine prioritizes more granular definitions when determining the
effective physical properties of a part. The values in the following list
are in order from highest to lowest priority:

* Custom physical properties of the part
* Custom physical properties of the part's custom material
* Custom physical properties of the material override of the part's
  material
* Default physical properties of the part's material

Provide feedback

---

CustomPhysicalProperties

Read Parallel

Determines several physical properties of a part.

BasePart.CustomPhysicalProperties:[PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties)

CustomPhysicalProperties lets you customize various physical aspects of
a part, such as its density, friction, and elasticity.

If enabled, this property let's you configure these physical properties.
If disabled, these physical properties are determined by the
[Material](/docs/reference/engine/classes/BasePart#Material) of the part.

Code Samples

Set CustomPhysicalProperties

This code sample demonstrates how to set the CustomPhysicalProperties property
of a part.

```
local part = script.Parent



-- This will make the part light and bouncy!



local DENSITY = 0.3



local FRICTION = 0.1



local ELASTICITY = 1



local FRICTION_WEIGHT = 1



local ELASTICITY_WEIGHT = 1



local physProperties = PhysicalProperties.new(DENSITY, FRICTION, ELASTICITY, FRICTION_WEIGHT, ELASTICITY_WEIGHT)



part.CustomPhysicalProperties = physProperties
```

Provide feedback

---

Elasticity

Deprecated

Show details

---

EnableFluidForces

Read Parallel

Used to enable or disable aerodynamic forces on parts and assemblies.

BasePart.EnableFluidForces:[boolean](/docs/luau/booleans)

When true, and when [Workspace.FluidForces](/docs/reference/engine/classes/Workspace#FluidForces) is enabled, causes the
physics engine to compute aerodynamic forces on this [BasePart](/docs/reference/engine/classes/BasePart).

Provide feedback

---

ExtentsCFrame

Read Only

Not Replicated

Read Parallel

The [CFrame](/docs/reference/engine/datatypes/CFrame) of the physical extents of the [BasePart](/docs/reference/engine/classes/BasePart).

BasePart.ExtentsCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

The [CFrame](/docs/reference/engine/datatypes/CFrame) of the physical extents of the [BasePart](/docs/reference/engine/classes/BasePart),
representing its physical center.

Provide feedback

---

ExtentsSize

Read Only

Not Replicated

Read Parallel

The actual physical size of the [BasePart](/docs/reference/engine/classes/BasePart) as regarded by the
physics engine.

BasePart.ExtentsSize:[Vector3](/docs/reference/engine/datatypes/Vector3)

The actual physical size of the [BasePart](/docs/reference/engine/classes/BasePart) as regarded by the
physics engine, for example in
[collision detection](/docs/workspace/collisions).

Provide feedback

---

Friction

Deprecated

Show details

---

FrontParamA

Deprecated

Show details

---

FrontParamB

Deprecated

Show details

---

FrontSurface

Read Parallel

Determines the type of surface for the front face of a part.

BasePart.FrontSurface:[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType)

The FrontSurface property determines the type of surface used for the
negative Z direction of a part. When two parts' faces are placed next
to each other, they may create a joint between them.

Provide feedback

---

FrontSurfaceInput

Deprecated

Show details

---

LeftParamA

Deprecated

Show details

---

LeftParamB

Deprecated

Show details

---

LeftSurface

Read Parallel

Determines the type of surface for the left face of a part.

BasePart.LeftSurface:[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType)

The LeftSurface property determines the type of surface used for the
negative X direction of a part. When two parts' faces are placed next
to each other, they may create a joint between them.

Provide feedback

---

LeftSurfaceInput

Deprecated

Show details

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

Determines a multiplier for [BasePart.Transparency](/docs/reference/engine/classes/BasePart#Transparency) that is only
visible to the local client.

BasePart.LocalTransparencyModifier:[number](/docs/luau/numbers)

The LocalTransparencyModifier property is a multiplier to
[Transparency](/docs/reference/engine/classes/BasePart#Transparency) that is only visible to the
local client. It does not replicate from client to server and is useful
for when a part should not render for a specific client, such as how the
player does not see their character's body parts when they zoom into first
person mode.

This property modifies the local part's transparency through the following
formula, with resulting values clamped between 0 and 1.

1 - ((1 - [Transparency](/docs/reference/engine/classes/BasePart#Transparency)) × (1 -
LocalTransparencyModifier))

| [Transparency](/docs/reference/engine/classes/BasePart#Transparency) | LocalTransparencyModifier | Server-Side | Client-Side |
| --- | --- | --- | --- |
| 0.5 | 0 | 0.5 | 0.5 |
| 0.5 | 0.25 | 0.5 | 0.625 |
| 0.5 | 0.5 | 0.5 | 0.75 |
| 0.5 | 0.75 | 0.5 | 0.875 |
| 0.5 | 1 | 0.5 | 1 |

Provide feedback

---

Locked

Read Parallel

Determines whether a part is selectable in Studio.

BasePart.Locked:[boolean](/docs/luau/booleans)

The Locked property determines whether a part (or a [Model](/docs/reference/engine/classes/Model) it is
contained within) may be selected in Studio by clicking on it. This
property is most often enabled on parts within environment models that
aren't being edited at the moment.

Code Samples

Recursive Unlock

This code sample uses the concept of recursion to unlock all parts that are a
descendant of a model.

```
-- Paste into a Script within a Model you want to unlock



local model = script.Parent



-- This function recurses through a model's heirarchy and unlocks



-- every part that it encounters.



local function recursiveUnlock(object)



if object:IsA("BasePart") then



object.Locked = false



end



-- Call the same function on the children of the object



-- The recursive process stops if an object has no children



for _, child in pairs(object:GetChildren()) do



recursiveUnlock(child)



end



end



recursiveUnlock(model)
```

Provide feedback

---

Mass

Read Only

Not Replicated

Read Parallel

Describes the mass of the part, the product of its density and volume.

BasePart.Mass:[number](/docs/luau/numbers)

Mass is a read-only property that describes the product of a part's
volume and density. It is returned by the
[GetMass()](/docs/reference/engine/classes/BasePart#GetMass) function.

* The volume of a part is determined by its [Size](/docs/reference/engine/classes/BasePart#Size) and
  its [Shape](/docs/reference/engine/classes/Part#Shape), which varies depending on the kind of
  [BasePart](/docs/reference/engine/classes/BasePart) used, such as [WedgePart](/docs/reference/engine/classes/WedgePart).
* The density of a part is determined by its
  [Material](/docs/reference/engine/classes/BasePart#Material) or
  [CustomPhysicalProperties](/docs/reference/engine/classes/BasePart#CustomPhysicalProperties), if
  specified.

Provide feedback

---

Massless

Read Parallel

Determines whether the part contributes to the total mass or inertia of
its rigid body.

BasePart.Massless:[boolean](/docs/luau/booleans)

If this property is enabled, the part will not contribute to the total
mass or inertia of its assembly as long as it is welded to another part
that has mass.

If the part is its own root part according to
[AssemblyRootPart](/docs/reference/engine/classes/BasePart#AssemblyRootPart), this will be ignored
for that part, and it will still contribute mass and inertia to its
assembly like a normal part. Parts that are massless should never become
an assembly root part unless all other parts in the assembly are also
massless.

This might be useful for things like optional accessories on vehicles that
you don't want to affect the handling of the car or a massless render mesh
welded to a simpler collision mesh.

See also [Assemblies](/docs/physics/assemblies), an article
documenting what root parts are and how to use them.

Provide feedback

---

Material

Read Parallel

Determines the texture and default physical properties of a part.

BasePart.Material:[Enum.Material](/docs/reference/engine/enums/Material)

The Material property allows you to set a part's texture and default
physical properties (in the case that
[CustomPhysicalProperties](/docs/reference/engine/classes/BasePart#CustomPhysicalProperties) is
unset). The default [Plastic](/docs/reference/engine/enums/Material) material has a very light
texture, while the [SmoothPlastic](/docs/reference/engine/enums/Material) material has no texture
at all. Some material textures like [DiamondPlate](/docs/reference/engine/enums/Material) and
[Granite](/docs/reference/engine/enums/Material) have very visible textures. Each material's
texture reflects sunlight differently, especially [Foil](/docs/reference/engine/enums/Material).

Setting this property then enabling
[CustomPhysicalProperties](/docs/reference/engine/classes/BasePart#CustomPhysicalProperties) will
use the default physical properties of a material. For instance,
[DiamondPlate](/docs/reference/engine/enums/Material) is a very dense material while
[Wood](/docs/reference/engine/enums/Material) is very light. A part's density determines whether it
will float in terrain water.

The [Glass](/docs/reference/engine/enums/Material) material changes rendering behavior on moderate
graphics settings by applying a bit of reflectiveness (similar to
[Reflectance](/docs/reference/engine/classes/BasePart#Reflectance)) and perspective distortion. The
effect is especially pronounced on sphere-shaped parts. Semi‑transparent
parts behind [Glass](/docs/reference/engine/enums/Material) parts are not visible.

Provide feedback

---

MaterialVariant

Not Replicated

Read Parallel

The name of [MaterialVariant](/docs/reference/engine/classes/MaterialVariant).

BasePart.MaterialVariant:[string](/docs/luau/strings)

The system searches the [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) instance with the
specified MaterialVariant name and [Material](/docs/reference/engine/classes/BasePart#Material)
type. If it successfully finds a matching [MaterialVariant](/docs/reference/engine/classes/MaterialVariant)
instance, it uses that instance to replace the default material. The
default material can be the built-in material or an override
[MaterialVariant](/docs/reference/engine/classes/MaterialVariant) specified in [MaterialService](/docs/reference/engine/classes/MaterialService).

Provide feedback

---

Orientation

Hidden

Not Replicated

Read Parallel

Describes the rotation of the part in the world.

BasePart.Orientation:[Vector3](/docs/reference/engine/datatypes/Vector3)

The Orientation property describes the part's rotation in degrees around
the X, Y, and Z axes using a [Vector3](/docs/reference/engine/datatypes/Vector3). The rotations
are applied in Y ⟩ X ⟩ Z order. This
differs from proper [Euler](https://en.wikipedia.org/wiki/Euler_angles) angles and is instead [Tait-Bryan](https://en.wikipedia.org/wiki/Euler_angles#Tait-Bryan_angles)
angles which describe yaw, pitch, and roll.

It is also worth noting how this property differs from the
[CFrame.Angles()](/docs/reference/engine/datatypes/CFrame#Angles) constructor which applies rotations in a
different order (Z ⟩ Y ⟩ X). For better
control over the rotation of a part, it's recommended that
[CFrame](/docs/reference/engine/classes/BasePart#CFrame) is set instead.

When setting this property, any [Welds](/docs/reference/engine/classes/Weld) or
[Motor6Ds](/docs/reference/engine/classes/Motor6D) connected to this part will have the matching
[C0](/docs/reference/engine/classes/JointInstance#C0) or [C1](/docs/reference/engine/classes/JointInstance#C1) property
updated to allow the part to move relative to any other parts it is joined
to. [WeldConstraints](/docs/reference/engine/classes/WeldConstraint) will also be temporarily
disabled and re-enabled during the move.

Code Samples

Part Spinner

This code sample rotates a part continually on the Y axis.

```
local part = script.Parent



local INCREMENT = 360 / 20



-- Rotate the part continually



while true do



for degrees = 0, 360, INCREMENT do



-- Set only the Y axis rotation



part.Rotation = Vector3.new(0, degrees, 0)



-- A better way to do this would be setting CFrame



--part.CFrame = CFrame.new(part.Position) * CFrame.Angles(0, math.rad(degrees), 0)



task.wait()



end



end
```

Provide feedback

---

PivotOffset

Read Parallel

Specifies the offset of the part's pivot from its [CFrame](/docs/reference/engine/datatypes/CFrame).

BasePart.PivotOffset:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property specifies the offset of the part's pivot from its
[CFrame](/docs/reference/engine/datatypes/CFrame), that is [BasePart:GetPivot()](/docs/reference/engine/classes/BasePart#GetPivot) is the same as
[BasePart.CFrame](/docs/reference/engine/classes/BasePart#CFrame) multiplied by [BasePart.PivotOffset](/docs/reference/engine/classes/BasePart#PivotOffset).

This is convenient for setting the pivot to a location in local space,
but setting a part's pivot to a location in world space can be done as
follows:

```
local Workspace = game:GetService("Workspace")



local part = Workspace.BluePart



local desiredPivotCFrameInWorldSpace = CFrame.new(0, 10, 0)



part.PivotOffset = part.CFrame:ToObjectSpace(desiredPivotCFrameInWorldSpace)
```

Code Samples

Reset Pivot

This code sample shows a custom function for resetting the pivot of a model
back to the center of that model's bounding box.

```
local function resetPivot(model)



local boundsCFrame = model:GetBoundingBox()



if model.PrimaryPart then



model.PrimaryPart.PivotOffset = model.PrimaryPart.CFrame:ToObjectSpace(boundsCFrame)



else



model.WorldPivot = boundsCFrame



end



end



resetPivot(script.Parent)
```

Clock Hands

This code sample creates a clock at the origin with a minute, second, and hour
hand, and makes it tick, displaying the local time.

```
local function createHand(length, width, yOffset)



local part = Instance.new("Part")



part.Size = Vector3.new(width, 0.1, length)



part.Material = Enum.Material.Neon



part.PivotOffset = CFrame.new(0, -(yOffset + 0.1), length / 2)



part.Anchored = true



part.Parent = workspace



return part



end



local function positionHand(hand, fraction)



hand:PivotTo(CFrame.fromEulerAnglesXYZ(0, -fraction * 2 * math.pi, 0))



end



-- Create dial



for i = 0, 11 do



local dialPart = Instance.new("Part")



dialPart.Size = Vector3.new(0.2, 0.2, 1)



dialPart.TopSurface = Enum.SurfaceType.Smooth



if i == 0 then



dialPart.Size = Vector3.new(0.2, 0.2, 2)



dialPart.Color = Color3.new(1, 0, 0)



end



dialPart.PivotOffset = CFrame.new(0, -0.1, 10.5)



dialPart.Anchored = true



dialPart:PivotTo(CFrame.fromEulerAnglesXYZ(0, (i / 12) * 2 * math.pi, 0))



dialPart.Parent = workspace



end



-- Create hands



local hourHand = createHand(7, 1, 0)



local minuteHand = createHand(10, 0.6, 0.1)



local secondHand = createHand(11, 0.2, 0.2)



-- Run clock



while true do



local components = os.date("*t")



positionHand(hourHand, (components.hour + components.min / 60) / 12)



positionHand(minuteHand, (components.min + components.sec / 60) / 60)



positionHand(secondHand, components.sec / 60)



task.wait()



end
```

Provide feedback

---

Position

Hidden

Not Replicated

Read Parallel

Describes the position of the part in the world.

BasePart.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

The Position property describes the coordinates of a part using a
[Vector3](/docs/reference/engine/datatypes/Vector3). It reflects the position of the part's
[CFrame](/docs/reference/engine/classes/BasePart#CFrame), however it can also be set.

When setting this property, any [Welds](/docs/reference/engine/classes/Weld) or
[Motor6Ds](/docs/reference/engine/classes/Motor6D) connected to this part will have the matching
[C0](/docs/reference/engine/classes/JointInstance#C0) or [C1](/docs/reference/engine/classes/JointInstance#C1) property
updated to allow the part to move relative to any other parts it is joined
to. [WeldConstraints](/docs/reference/engine/classes/WeldConstraint) will also be temporarily
disabled and re-enabled during the move.

Provide feedback

---

ReceiveAge

Hidden

Read Only

Not Replicated

Read Parallel

Time since last recorded physics update.

BasePart.ReceiveAge:[number](/docs/luau/numbers)

Indicates the time in seconds since the part's physics were last updated
on the local client or the server. This value will be 0 when the part
has no physics ([Anchored](/docs/reference/engine/classes/BasePart#Anchored) is true).

Provide feedback

---

Reflectance

Read Parallel

Determines how much a part reflects the skybox.

BasePart.Reflectance:[number](/docs/luau/numbers)

The Reflectance property determines how much a part reflects the sky. A
value of 0 indicates the part is not reflective at all, and a value of
1 indicates the part should fully reflect.

Reflectance is not affected by [Transparency](/docs/reference/engine/classes/BasePart#Transparency)
unless the part is fully transparent, in which case reflectance will not
render at all. Reflectance may or may not be ignored depending on the
[Material](/docs/reference/engine/classes/BasePart#Material) of the part.

Provide feedback

---

ResizeableFaces

Read Only

Not Replicated

Read Parallel

Describes the faces on which a part may be resized.

BasePart.ResizeableFaces:[Faces](/docs/reference/engine/datatypes/Faces)

The ResizeableFaces property uses a [Faces](/docs/reference/engine/datatypes/Faces) object to describe
the different faces on which a part may be resized. For most
implementations of [BasePart](/docs/reference/engine/classes/BasePart), such as [Part](/docs/reference/engine/classes/Part) and
[WedgePart](/docs/reference/engine/classes/WedgePart), this property includes all faces. However,
[TrussPart](/docs/reference/engine/classes/TrussPart) will set its ResizeableFaces set to only two faces
since those kinds of parts must have two [Size](/docs/reference/engine/classes/BasePart#Size)
dimensions of length 2.

This property is most commonly used with tools for building and
manipulating parts and has little use outside of that context. The
[Handles](/docs/reference/engine/classes/Handles) class, which has the [Handles.Faces](/docs/reference/engine/classes/Handles#Faces) property, can
be used in conjunction with this property to display only the handles on
faces that can be resized on a part.

Code Samples

Resize Handles

This code sample creates a Handles object and shows how to set the Faces
property of the object. It also references ResizeableFaces of a part. Try
placing this script in multiple kinds of parts to see how ResizeableFaces
varies.

```
-- Put this Script in several kinds of BasePart, like



-- Part, TrussPart, WedgePart, CornerWedgePart, etc.



local part = script.Parent



-- Create a handles object for this part



local handles = Instance.new("Handles")



handles.Adornee = part



handles.Parent = part



-- Manually specify the faces applicable for this handle



handles.Faces = Faces.new(Enum.NormalId.Top, Enum.NormalId.Front, Enum.NormalId.Left)



-- Alternatively, use the faces on which the part can be resized.



-- If part is a TrussPart with only two Size dimensions



-- of length 2, then ResizeableFaces will only have two



-- enabled faces. For other parts, all faces will be enabled.



handles.Faces = part.ResizeableFaces
```

Provide feedback

---

ResizeIncrement

Read Only

Not Replicated

Read Parallel

Describes the smallest change in size allowable by the
[Resize()](/docs/reference/engine/classes/BasePart#Resize) method.

BasePart.ResizeIncrement:[number](/docs/luau/numbers)

The ResizeIncrement property is a read-only property that describes the
smallest change in size allowable by the
[Resize()](/docs/reference/engine/classes/BasePart#Resize) method. It differs between
implementations of the [BasePart](/docs/reference/engine/classes/BasePart) abstract class; for instance,
[Part](/docs/reference/engine/classes/Part) has this set to 1 while [TrussPart](/docs/reference/engine/classes/TrussPart) has this set to
2 since individual truss sections are 2×2×2 in size.

Provide feedback

---

RightParamA

Deprecated

Show details

---

RightParamB

Deprecated

Show details

---

RightSurface

Read Parallel

Determines the type of surface for the right face of a part.

BasePart.RightSurface:[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType)

The RightSurface property determines the type of surface used for the
positive X direction of a part. When two parts' faces are placed next
to each other, they may create a joint between them.

Provide feedback

---

RightSurfaceInput

Deprecated

Show details

---

RootPriority

Read Parallel

The main rule in determining the root part of an assembly.

BasePart.RootPriority:[number](/docs/luau/numbers)

This property is an integer between -127 and 127 that takes precedence
over all other rules for root part sort. When considering multiple parts
that are not [Anchored](/docs/reference/engine/classes/BasePart#Anchored) and which share the same
[Massless](/docs/reference/engine/classes/BasePart#Massless) value, a part with a higher
RootPriority will take priority over those with lower RootPriority.

You can use this property to control which part of an assembly is the root
part and keep the root part stable if size changes.

See also [Assemblies](/docs/physics/assemblies), an article
documenting what root parts are and how to use them.

Provide feedback

---

Rotation

Not Replicated

Read Parallel

The rotation of the part in degrees for the three axes.

BasePart.Rotation:[Vector3](/docs/reference/engine/datatypes/Vector3)

The rotation of the part in degrees for the three axes.

When setting this property, any [Welds](/docs/reference/engine/classes/Weld) or
[Motor6Ds](/docs/reference/engine/classes/Motor6D) connected to this part will have the matching
[C0](/docs/reference/engine/classes/JointInstance#C0) or [C1](/docs/reference/engine/classes/JointInstance#C1) property
updated to allow the part to move relative to any other parts it is joined
to. [WeldConstraints](/docs/reference/engine/classes/WeldConstraint) will also be temporarily
disabled and re-enabled during the move.

Provide feedback

---

RotVelocity

Deprecated

Show details

---

Size

Not Replicated

Read Parallel

Determines the dimensions of a part (length, width, height).

BasePart.Size:[Vector3](/docs/reference/engine/datatypes/Vector3)

A part's Size property determines its visual dimensions, while
[ExtentsSize](/docs/reference/engine/classes/BasePart#ExtentsSize) represents the actual size used
by the physics engine, such as in
[collision detection](/docs/workspace/collisions). The individual
dimensions (length, width, height) can be as low as 0.001 and as high as
2048. Size dimensions below 0.05 will be visually represented as
if the part's dimensions are 0.05.

A part's Size is used in a variety of additional ways:

* To influence its mass as given by [GetMass()](/docs/reference/engine/classes/BasePart#GetMass).
* By [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) to determine the area from which particles
  are spawned.
* By [BlockMesh](/docs/reference/engine/classes/BlockMesh) to partially determine the rendered rectangular
  prism.
* By [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) for certain
  [MeshTypes](/docs/reference/engine/classes/SpecialMesh#MeshType) to determine the size of the
  rendered mesh.
* By [SurfaceLight](/docs/reference/engine/classes/SurfaceLight) to determine the space to illuminate.

Code Samples

Pyramid Builder

This code sample constructs a pyramid by stacking parts that get progressively
smaller. It also colors the parts so they blend between a start color and end
color.

```
local TOWER_BASE_SIZE = 30



local position = Vector3.new(50, 50, 50)



local hue = math.random()



local color0 = Color3.fromHSV(hue, 1, 1)



local color1 = Color3.fromHSV((hue + 0.35) % 1, 1, 1)



local model = Instance.new("Model")



model.Name = "Tower"



for i = TOWER_BASE_SIZE, 1, -2 do



local part = Instance.new("Part")



part.Size = Vector3.new(i, 2, i)



part.Position = position



part.Anchored = true



part.Parent = model



-- Tween from color0 and color1



local perc = i / TOWER_BASE_SIZE



part.Color = Color3.new(



color0.R * perc + color1.R * (1 - perc),



color0.G * perc + color1.G * (1 - perc),



color0.B * perc + color1.B * (1 - perc)



)



position = position + Vector3.new(0, part.Size.Y, 0)



end



model.Parent = workspace
```

Provide feedback

---

SpecificGravity

Deprecated

Show details

---

TopParamA

Deprecated

Show details

---

TopParamB

Deprecated

Show details

---

TopSurface

Read Parallel

Determines the type of surface for the top face of a part.

BasePart.TopSurface:[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType)

The TopSurface property determines the type of surface used for the
positive Y direction of a part. When two parts' faces are placed next
to each other, they may create a joint between them.

Provide feedback

---

TopSurfaceInput

Deprecated

Show details

---

Transparency

Read Parallel

Determines how much a part can be seen through (the inverse of part
opacity).

BasePart.Transparency:[number](/docs/luau/numbers)

The Transparency property controls the visibility of a part on a scale
of 0 to 1 where 0 is completely visible (opaque) and 1 is
completely invisible (not rendered at all).

While fully transparent parts are not rendered at all, partially
transparent objects have some significant rendering costs. Having many
translucent parts may impact performance.

When transparent parts overlap, render order may act unpredictably, so you
should avoid semi-transparent parts from overlapping.

See also
[LocalTransparencyModifier](/docs/reference/engine/classes/BasePart#LocalTransparencyModifier) as a
multiplier to Transparency that's only visible to the local client.

Code Samples

Fade Door

This code sample shows how a part can fade away when touched by a Humanoid
then reappear a moment after to create a passable door.

```
-- Paste into a Script inside a tall part



local part = script.Parent



local OPEN_TIME = 1



-- Can the door be opened at the moment?



local debounce = false



local function open()



part.CanCollide = false



part.Transparency = 0.7



part.BrickColor = BrickColor.new("Black")



end



local function close()



part.CanCollide = true



part.Transparency = 0



part.BrickColor = BrickColor.new("Bright blue")



end



local function onTouch(otherPart)



-- If the door was already open, do nothing



if debounce then



print("D")



return



end



-- Check if touched by a Humanoid



local human = otherPart.Parent:FindFirstChildOfClass("Humanoid")



if not human then



print("not human")



return



end



-- Perform the door opening sequence



debounce = true



open()



task.wait(OPEN_TIME)



close()



debounce = false



end



part.Touched:Connect(onTouch)



close()
```

Provide feedback

---

Velocity

Deprecated

Show details

---

Methods

AngularAccelerationToTorque

BasePart:AngularAccelerationToTorque(

angAcceleration:[Vector3](/docs/reference/engine/datatypes/Vector3), angVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| angAcceleration:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| angVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3) Default Value: "0, 0, 0" |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---

ApplyAngularImpulse

Apply an angular impulse to the assembly.

BasePart:ApplyAngularImpulse(impulse:[Vector3](/docs/reference/engine/datatypes/Vector3)):()

Parameters

|  |
| --- |
| impulse:[Vector3](/docs/reference/engine/datatypes/Vector3)  An angular impulse vector to be applied to the assembly. |

Returns

()

Applies an instant angular force impulse to this part's assembly, causing
the assembly to spin.

The resulting angular velocity from the impulse relies on the assembly's
[mass](/docs/reference/engine/classes/BasePart#AssemblyMass). So a higher impulse is required to
move more massive assemblies. Impulses are useful for cases where you want
a force applied instantly, such as an explosion or collision.

If the part is [owned](/docs/physics/network-ownership) by the
server, this function must be called from a server [Script](/docs/reference/engine/classes/Script) (not
from a [LocalScript](/docs/reference/engine/classes/LocalScript) or a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client)).
If the part is owned by a client through automatic ownership, this
function can be called from either a client script or a server script;
calling it from a client script for a server-owned part will have no
effect.

Provide feedback

---

ApplyImpulse

Apply an impulse to the assembly at the assembly's
[center of mass](/docs/reference/engine/classes/BasePart#AssemblyCenterOfMass).

BasePart:ApplyImpulse(impulse:[Vector3](/docs/reference/engine/datatypes/Vector3)):()

Parameters

|  |
| --- |
| impulse:[Vector3](/docs/reference/engine/datatypes/Vector3)  A linear impulse vector to be applied to the assembly. |

Returns

()

This function applies an instant force impulse to this part's assembly.

The force is applied at the assembly's
[center of mass](/docs/reference/engine/classes/BasePart#AssemblyCenterOfMass), so the resulting
movement will only be linear.

The resulting velocity from the impulse relies on the assembly's
[mass](/docs/reference/engine/classes/BasePart#AssemblyMass). So a higher impulse is required to
move more massive assemblies. Impulses are useful for cases where you want
a force applied instantly, such as an explosion or collision.

If the part is [owned](/docs/physics/network-ownership) by the
server, this function must be called from a server [Script](/docs/reference/engine/classes/Script) (not
from a [LocalScript](/docs/reference/engine/classes/LocalScript) or a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client)).
If the part is owned by a client through automatic ownership, this
function can be called from either a client script or a server script;
calling it from a client script for a server-owned part will have no
effect.

Provide feedback

---

ApplyImpulseAtPosition

Apply an impulse to the assembly at specified position.

BasePart:ApplyImpulseAtPosition(

impulse:[Vector3](/docs/reference/engine/datatypes/Vector3), position:[Vector3](/docs/reference/engine/datatypes/Vector3)

):()

Parameters

|  |
| --- |
| impulse:[Vector3](/docs/reference/engine/datatypes/Vector3)  An impulse vector to be applied to the assembly. |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3)  The position, in world space, to apply the impulse. |

Returns

()

This function applies an instant force impulse to this part's assembly, at
the specified position in world space.

If the position is not at the assembly's
[center of mass](/docs/reference/engine/classes/BasePart#AssemblyCenterOfMass), the impulse will
cause a positional and rotational movement.

The resulting velocity from the impulse relies on the assembly's
[mass](/docs/reference/engine/classes/BasePart#AssemblyMass). So a higher impulse is required to
move more massive assemblies. Impulses are useful for cases where
developers want a force applied instantly, such as an explosion or
collision.

If the part is [owned](/docs/physics/network-ownership) by the
server, this function must be called from a server [Script](/docs/reference/engine/classes/Script) (not
from a [LocalScript](/docs/reference/engine/classes/LocalScript) or a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client)).
If the part is owned by a client through automatic ownership, this
function can be called from either a client script or a server script;
calling it from a client script for a server-owned part will have no
effect.

Provide feedback

---

BreakJoints

Deprecated

Show details

---

breakJoints

Deprecated

Show details

---

CanCollideWith

Write Parallel

Returns whether the parts can collide with each other.

BasePart:CanCollideWith(part:[BasePart](/docs/reference/engine/classes/BasePart)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| part:[BasePart](/docs/reference/engine/classes/BasePart)  The specified part being checked for collidability. |

Returns

[boolean](/docs/luau/booleans)

Whether the parts can collide with each other.

Returns whether the parts can collide with each other or not. This
function takes into account the collision groups of the two parts. This
function will error if the specified part is not a BasePart.

Provide feedback

---

CanSetNetworkOwnership

Checks whether you can set a part's network ownership.

BasePart:CanSetNetworkOwnership():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Whether you can modify or read the network ownership and the reason.

The CanSetNetworkOwnership function checks whether you can set a part's
network ownership.

The function's return value verifies whether or not you can call
[BasePart:SetNetworkOwner()](/docs/reference/engine/classes/BasePart#SetNetworkOwner) or
[BasePart:SetNetworkOwnershipAuto()](/docs/reference/engine/classes/BasePart#SetNetworkOwnershipAuto) without encountering an error.
It returns true if you can modify/read the network ownership, or returns
false and the reason you can't, as a string.

Code Samples

Check if a Part's Network Ownership Can Be Set

This example checks whether or not the network ownership of the first
BasePart named *Part* in the Workspace can be set.

```
local part = workspace:FindFirstChild("Part")



if part and part:IsA("BasePart") then



local canSet, errorReason = part:CanSetNetworkOwnership()



if canSet then



print(part:GetFullName() .. "'s Network Ownership can be changed!")



else



warn("Cannot change the Network Ownership of " .. part:GetFullName() .. " because: " .. errorReason)



end



end
```

Provide feedback

---

GetClosestPointOnSurface

BasePart:GetClosestPointOnSurface(position:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---

GetConnectedParts

Write Parallel

Returns a table of parts connected to the object by any kind of rigid
joint.

BasePart:GetConnectedParts(recursive:[boolean](/docs/luau/booleans)):Instances

Parameters

|  |
| --- |
| recursive:[boolean](/docs/luau/booleans) Default Value: false A table of parts connected to the object by any kind of [joint](/docs/reference/engine/classes/JointInstance). |

Returns

Instances

Returns a table of parts connected to the object by any kind of rigid
joint.

If recursive is true this function will return all of the parts in the
assembly rigidly connected to the BasePart.

#### Rigid Joints

When a joint connects two parts together (Part0 → Part1), a joint is
rigid if the physics of Part1 are completely locked down by Part0.
This only applies to the following joint types:

* [Weld](/docs/reference/engine/classes/Weld)
* [Snap](/docs/reference/engine/classes/Snap)
* [ManualWeld](/docs/reference/engine/classes/ManualWeld)
* [Motor](/docs/reference/engine/classes/Motor)
* [Motor6D](/docs/reference/engine/classes/Motor6D)
* [WeldConstraint](/docs/reference/engine/classes/WeldConstraint)

Provide feedback

---

GetJoints

Write Parallel

Return all Joints or Constraints that is connected to this Part.

BasePart:GetJoints():Instances

Returns

Instances

An array of all Joints or Constraints connected to the Part.

Return all Joints or Constraints that is connected to this Part.

Provide feedback

---

GetMass

Write Parallel

Returns the value of the [Mass](/docs/reference/engine/classes/BasePart#Mass) property.

BasePart:GetMass():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

The part's mass.

GetMass returns the value of the read-only [Mass](/docs/reference/engine/classes/BasePart#Mass)
property.

This function predates the Mass property. It remains supported for
backward-compatibility; you should use the Mass property directly.

Code Samples

Finding a Part's Mass

This example creates a new part, myPart, in the game's Workspace, with
dimensions 4x6x4 studs. The part is also anchored.

Then, myMass is set to equal the mass of the new part. The mass of the part is
printed at the end of the print statement:

My part's mass is ...

```
local myPart = Instance.new("Part")



myPart.Size = Vector3.new(4, 6, 4)



myPart.Anchored = true



myPart.Parent = workspace



local myMass = myPart:GetMass()



print("My part's mass is " .. myMass)
```

Provide feedback

---

getMass

Deprecated

Show details

---

GetNetworkOwner

Write Parallel

Returns the current player who is the network owner of this part, or nil
in case of the server.

BasePart:GetNetworkOwner():[Instance](/docs/reference/engine/datatypes/Instance)

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The current player who is the network owner of this part, or nil in
case of the server.

Returns the current player who is the network owner of this part, or nil
in case of the server.

Provide feedback

---

GetNetworkOwnershipAuto

Write Parallel

Returns true if the game engine automatically decides the network owner
for this part.

BasePart:GetNetworkOwnershipAuto():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the game engine automatically decides the network owner for
this part.

Returns true if the game engine automatically decides the network owner
for this part.

Provide feedback

---

GetNoCollisionConstraints

BasePart:GetNoCollisionConstraints():Instances

Returns

Instances

Provide feedback

---

GetRenderCFrame

Deprecated

Show details

---

GetRootPart

Deprecated

Show details

---

GetTouchingParts

Returns a table of all [BasePart.CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) true parts that
intersect with this part.

BasePart:GetTouchingParts():Instances

Returns

Instances

A table of all parts that intersect and can collide with this part.

Returns a table of all parts that are physically interacting with this
part. If the part itself has CanCollide set to false, then this function
returns an empty table unless the part has a
[TouchInterest](/docs/reference/engine/classes/TouchTransmitter) object parented to it (meaning
something is connected to its Touched event). Parts that are adjacent but
not intersecting are not considered touching. This function predates the
[WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart) function, which provides more
flexibility and avoids the special [TouchInterest](/docs/reference/engine/classes/TouchTransmitter)
rules described above. Use [WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart) instead.

Provide feedback

---

GetVelocityAtPosition

Write Parallel

Returns the linear velocity of the part's assembly at the given position
relative to this part.

BasePart:GetVelocityAtPosition(position:[Vector3](/docs/reference/engine/datatypes/Vector3)):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns the linear velocity of the part's assembly at the given position
relative to this part. It can be used to identify the linear velocity of
parts in an assembly other than the root part. If the assembly has no
angular velocity, than the linear velocity will always be the same for
every position.

Provide feedback

---

IntersectAsync

Yields

Creates a new [IntersectOperation](/docs/reference/engine/classes/IntersectOperation) from the overlapping geometry of
the part and the other parts in the given array.

BasePart:IntersectAsync(

parts:Instances, collisionfidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity), renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| parts:Instances  The objects taking part in the intersection. |
| collisionfidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity) Default Value: "Default" The [Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity) value for the resulting [IntersectOperation](/docs/reference/engine/classes/IntersectOperation). |
| renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) Default Value: "Automatic" The [Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) value of the resulting [PartOperation](/docs/reference/engine/classes/PartOperation). |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Resulting [IntersectOperation](/docs/reference/engine/classes/IntersectOperation) with default name Intersect.

Creates a new [IntersectOperation](/docs/reference/engine/classes/IntersectOperation) from the intersecting geometry of
the part and the other parts in the given array. Only [Parts](/docs/reference/engine/classes/Part)
are supported, not [Terrain](/docs/reference/engine/classes/Terrain) or [MeshParts](/docs/reference/engine/classes/MeshPart). Similar
to [Clone()](/docs/reference/engine/classes/Instance#Clone), the returned object has no set
[Parent](/docs/reference/engine/classes/Instance#Parent).

The following properties from the calling part are applied to the
resulting [IntersectOperation](/docs/reference/engine/classes/IntersectOperation):

* [Color](/docs/reference/engine/classes/BasePart#Color), [Material](/docs/reference/engine/classes/BasePart#Material),
  [MaterialVariant](/docs/reference/engine/classes/BasePart#MaterialVariant),
  [Reflectance](/docs/reference/engine/classes/BasePart#Reflectance),
  [Transparency](/docs/reference/engine/classes/BasePart#Transparency)
* [CanCollide](/docs/reference/engine/classes/BasePart#CanCollide)
* [Anchored](/docs/reference/engine/classes/BasePart#Anchored), [Density](/docs/reference/engine/classes/BasePart#Density),
  [Elasticity](/docs/reference/engine/classes/BasePart#Elasticity),
  [ElasticityWeight](/docs/reference/engine/classes/BasePart#ElasticityWeight),
  [Friction](/docs/reference/engine/classes/BasePart#Friction),
  [FrictionWeight](/docs/reference/engine/classes/BasePart#FrictionWeight)

In the following image comparison,
[IntersectAsync()](/docs/reference/engine/classes/BasePart#IntersectAsync) is called on the purple
block using a table containing the blue block. The resulting
[IntersectOperation](/docs/reference/engine/classes/IntersectOperation) resolves into a shape of the intersecting
geometry of both parts.

![Two block parts overlapping](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Separate-Parts-To-Intersect.jpg)


Separate parts


![Parts intersected into a new solid model](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Intersect-Result.jpg)


Resulting [IntersectOperation](/docs/reference/engine/classes/IntersectOperation)

#### Notes

* The original parts remain intact following a successful intersect
  operation. In most cases, you should [Destroy()](/docs/reference/engine/classes/Instance#Destroy)
  all of the original parts and parent the returned
  [IntersectOperation](/docs/reference/engine/classes/IntersectOperation) to the same place as the calling
  [BasePart](/docs/reference/engine/classes/BasePart).
* By default, the face colors of the resulting intersection are borrowed
  from the [Color](/docs/reference/engine/classes/BasePart#Color) property of the original parts. To
  change the entire intersection to a specific color, set its
  [UsePartColor](/docs/reference/engine/classes/PartOperation#UsePartColor) property to true.
* If an intersect operation would result in a part with more than 20,000
  triangles, it will be simplified to 20,000 triangles.

Provide feedback

---

IsGrounded

Write Parallel

Returns true if the object is connected to a part that will hold it in
place (eg an [Anchored](/docs/reference/engine/classes/BasePart#Anchored) part), otherwise returns
false.

BasePart:IsGrounded():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the object is connected to a part that will hold it in place.

Returns true if the object is connected to a part that will hold it in
place (eg an [Anchored](/docs/reference/engine/classes/BasePart#Anchored) part), otherwise returns
false. In an assembly that has an [Anchored](/docs/reference/engine/classes/BasePart#Anchored) part,
every other part is grounded.

Provide feedback

---

MakeJoints

Deprecated

Show details

---

makeJoints

Deprecated

Show details

---

Resize

Changes the size of an object just like using the Studio resize tool.

BasePart:Resize(

normalId:[Enum.NormalId](/docs/reference/engine/enums/NormalId), deltaAmount:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| normalId:[Enum.NormalId](/docs/reference/engine/enums/NormalId)  The side to resize. |
| deltaAmount:[number](/docs/luau/numbers)  How much to grow/shrink on the specified side. |

Returns

[boolean](/docs/luau/booleans)

Whether the part is resized.

Changes the size of an object just like using the Studio resize tool.

Provide feedback

---

resize

Deprecated

Show details

---

SetNetworkOwner

Sets the given player as network owner for this and all connected parts.

BasePart:SetNetworkOwner(playerInstance:[Player](/docs/reference/engine/classes/Player)):()

Parameters

|  |
| --- |
| playerInstance:[Player](/docs/reference/engine/classes/Player) Default Value: "nil" The player being given network ownership of the part. |

Returns

()

Sets the given player as network owner for this and all connected parts.
When playerInstance is nil, the server will be the owner instead of a
player.

Provide feedback

---

SetNetworkOwnershipAuto

Lets the game engine dynamically decide who will handle the part's physics
(one of the clients or the server).

BasePart:SetNetworkOwnershipAuto():()

Returns

()

Lets the game engine dynamically decide who will handle the part's physics
(one of the clients or the server).

Provide feedback

---

SubtractAsync

Yields

Creates a new [UnionOperation](/docs/reference/engine/classes/UnionOperation) from the part, minus the geometry
occupied by the parts in the given array.

BasePart:SubtractAsync(

parts:Instances, collisionfidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity), renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| parts:Instances  The objects taking part in the subtraction. |
| collisionfidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity) Default Value: "Default" The [Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity) value for the resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation). |
| renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) Default Value: "Automatic" The [Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) value of the resulting [PartOperation](/docs/reference/engine/classes/PartOperation). |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation) with default name Union.

Creates a new [UnionOperation](/docs/reference/engine/classes/UnionOperation) from the part, minus the geometry
occupied by the parts in the given array. Only [Parts](/docs/reference/engine/classes/Part) are
supported, not [Terrain](/docs/reference/engine/classes/Terrain) or [MeshParts](/docs/reference/engine/classes/MeshPart). Similar to
[Clone()](/docs/reference/engine/classes/Instance#Clone), the returned object has no set
[Parent](/docs/reference/engine/classes/Instance#Parent).

Note that the resulting union cannot be empty due to subtractions. If the
operation would result in completely empty geometry, it will fail.

In the following image comparison,
[SubtractAsync()](/docs/reference/engine/classes/BasePart#SubtractAsync) is called on the blue
cylinder using a table containing the purple block. The resulting
[UnionOperation](/docs/reference/engine/classes/UnionOperation) resolves into a shape that omits the block's
geometry from that of the cylinder.

![Longer block overlapping a cylinder](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Separate-Parts-To-Subtract.jpg)


Separate parts


![Block part subtracted from cylinder](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Negate-Result.jpg)


Resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation)

Code Samples

BasePart:SubtractAsync()

This example demonstrates how to subtract part(s) from another
[BasePart](/docs/reference/engine/classes/BasePart) to form a negated [UnionOperation](/docs/reference/engine/classes/UnionOperation).

```
local Workspace = game:GetService("Workspace")



local mainPart = script.Parent.PartA



local otherParts = { script.Parent.PartB, script.Parent.PartC }



-- Perform subtract operation



local success, newSubtract = pcall(function()



return mainPart:SubtractAsync(otherParts)



end)



-- If operation succeeds, position it at the same location and parent it to the workspace



if success and newSubtract then



newSubtract.Position = mainPart.Position



newSubtract.Parent = Workspace



end



-- Destroy original parts which remain intact after operation



mainPart:Destroy()



for _, part in otherParts do



part:Destroy()



end
```

Provide feedback

---

TorqueToAngularAcceleration

BasePart:TorqueToAngularAcceleration(

torque:[Vector3](/docs/reference/engine/datatypes/Vector3), angVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3)

):[Vector3](/docs/reference/engine/datatypes/Vector3)

Parameters

|  |
| --- |
| torque:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| angVelocity:[Vector3](/docs/reference/engine/datatypes/Vector3) Default Value: "0, 0, 0" |

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---

UnionAsync

Yields

Creates a new [UnionOperation](/docs/reference/engine/classes/UnionOperation) from the part, plus the geometry
occupied by the parts in the given array.

BasePart:UnionAsync(

parts:Instances, collisionfidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity), renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| parts:Instances  The objects taking part in the union with the calling part. |
| collisionfidelity:[Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity) Default Value: "Default" The [Enum.CollisionFidelity](/docs/reference/engine/enums/CollisionFidelity) value for the resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation). |
| renderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) Default Value: "Automatic" The [Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) value of the resulting [PartOperation](/docs/reference/engine/classes/PartOperation). |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation) with default name Union.

Creates a new [UnionOperation](/docs/reference/engine/classes/UnionOperation) from the part, plus the geometry
occupied by the parts in the given array. Only [Parts](/docs/reference/engine/classes/Part) are
supported, not [Terrain](/docs/reference/engine/classes/Terrain) or [MeshParts](/docs/reference/engine/classes/MeshPart). Similar to
[Clone()](/docs/reference/engine/classes/Instance#Clone), the returned object has no set
[Parent](/docs/reference/engine/classes/Instance#Parent).

The following properties from the calling part are applied to the
resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation):

* [Color](/docs/reference/engine/classes/BasePart#Color), [Material](/docs/reference/engine/classes/BasePart#Material),
  [MaterialVariant](/docs/reference/engine/classes/BasePart#MaterialVariant),
  [Reflectance](/docs/reference/engine/classes/BasePart#Reflectance),
  [Transparency](/docs/reference/engine/classes/BasePart#Transparency)
* [CanCollide](/docs/reference/engine/classes/BasePart#CanCollide)
* [Anchored](/docs/reference/engine/classes/BasePart#Anchored), [Density](/docs/reference/engine/classes/BasePart#Density),
  [Elasticity](/docs/reference/engine/classes/BasePart#Elasticity),
  [ElasticityWeight](/docs/reference/engine/classes/BasePart#ElasticityWeight),
  [Friction](/docs/reference/engine/classes/BasePart#Friction),
  [FrictionWeight](/docs/reference/engine/classes/BasePart#FrictionWeight)

In the following image comparison,
[UnionAsync()](/docs/reference/engine/classes/BasePart#UnionAsync) is called on the blue block
using a table containing the purple cylinder. The resulting
[UnionOperation](/docs/reference/engine/classes/UnionOperation) resolves into a shape of the combined geometry of
both parts.

![Block and cylinder parts overlapping](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Separate-Parts-To-Union.jpg)


Separate parts


![Parts joined together into a single solid union](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Union-Result.jpg)


Resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation)

#### Notes

* The original parts remain intact following a successful union operation.
  In most cases, you should [Destroy()](/docs/reference/engine/classes/Instance#Destroy) all of the
  original parts and parent the returned [UnionOperation](/docs/reference/engine/classes/UnionOperation) to the
  same place as the calling [BasePart](/docs/reference/engine/classes/BasePart).
* By default, the resulting union respects the
  [Color](/docs/reference/engine/classes/BasePart#Color) property of each of its parts. To change
  the entire union to a specific color, set its
  [UsePartColor](/docs/reference/engine/classes/PartOperation#UsePartColor) property to true.
* If a union operation would result in a part with more than 20,000
  triangles, it will be simplified to 20,000 triangles.

Code Samples

BasePart:UnionAsync()

This example demonstrates how to combine the geometry of one [BasePart](/docs/reference/engine/classes/BasePart)
with the geometry of other part(s) to form a [UnionOperation](/docs/reference/engine/classes/UnionOperation).

```
local Workspace = game:GetService("Workspace")



local mainPart = script.Parent.PartA



local otherParts = { script.Parent.PartB, script.Parent.PartC }



-- Perform union operation



local success, newUnion = pcall(function()



return mainPart:UnionAsync(otherParts)



end)



-- If operation succeeds, position it at the same location and parent it to the workspace



if success and newUnion then



newUnion.Position = mainPart.Position



newUnion.Parent = Workspace



end



-- Destroy original parts which remain intact after operation



mainPart:Destroy()



for _, part in otherParts do



part:Destroy()



end
```

Provide feedback

---

Events

LocalSimulationTouched

Deprecated

Show details

---

OutfitChanged

Deprecated

Show details

---

StoppedTouching

Deprecated

Show details

---

Touched

Fires when a part touches another part as a result of physical movement.

BasePart.Touched(otherPart:[BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| otherPart:[BasePart](/docs/reference/engine/classes/BasePart)  The other part that came in contact with the given part. |

The Touched event fires when a part comes in contact with another
part. For instance, if PartA bumps into PartB, then
[PartA.Touched](/docs/reference/engine/classes/BasePart#Touched) fires with PartB, and
[PartB.Touched](/docs/reference/engine/classes/BasePart#Touched) fires with PartA.

This event only fires as a result of physical movement, so it will not
fire if the [CFrame](/docs/reference/engine/classes/BasePart#CFrame) property was changed such that
the part overlaps another part. This also means that at least one of the
parts involved must not be [Anchored](/docs/reference/engine/classes/BasePart#Anchored) at the
time of the collision.

This event works in conjunction with
[Workspace.TouchesUseCollisionGroups](/docs/reference/engine/classes/Workspace#TouchesUseCollisionGroups) to specify whether
[collision groups](/docs/workspace/collisions#collision-filtering)
are acknowledged for detection.

Code Samples

Touching Parts Count

This code sample creates a BillboardGui on a part that displays the number of
parts presently touching it.

```
local part = script.Parent



local billboardGui = Instance.new("BillboardGui")



billboardGui.Size = UDim2.new(0, 200, 0, 50)



billboardGui.Adornee = part



billboardGui.AlwaysOnTop = true



billboardGui.Parent = part



local tl = Instance.new("TextLabel")



tl.Size = UDim2.new(1, 0, 1, 0)



tl.BackgroundTransparency = 1



tl.Parent = billboardGui



local numTouchingParts = 0



local function onTouch(otherPart)



print("Touch started: " .. otherPart.Name)



numTouchingParts = numTouchingParts + 1



tl.Text = numTouchingParts



end



local function onTouchEnded(otherPart)



print("Touch ended: " .. otherPart.Name)



numTouchingParts = numTouchingParts - 1



tl.Text = numTouchingParts



end



part.Touched:Connect(onTouch)



part.TouchEnded:Connect(onTouchEnded)
```

Model Touched

This code sample demonstrates how to connect the [BasePart.Touched](/docs/reference/engine/classes/BasePart#Touched) event of multiple parts in a [Model](/docs/reference/engine/classes/Model) to one function.

```
local model = script.Parent



local function onTouched(otherPart)



-- Ignore instances of the model coming in contact with itself



if otherPart:IsDescendantOf(model) then



return



end



print(model.Name .. " collided with " .. otherPart.Name)



end



for _, child in pairs(model:GetChildren()) do



if child:IsA("BasePart") then



child.Touched:Connect(onTouched)



end



end
```

Provide feedback

---

TouchEnded

Fires when a part stops touching another part as a result of physical
movement.

BasePart.TouchEnded(otherPart:[BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| otherPart:[BasePart](/docs/reference/engine/classes/BasePart) |

Fires when a part stops touching another part under similar conditions to
those of [BasePart.Touched](/docs/reference/engine/classes/BasePart#Touched).

This event works in conjunction with
[Workspace.TouchesUseCollisionGroups](/docs/reference/engine/classes/Workspace#TouchesUseCollisionGroups) to specify whether
[collision groups](/docs/workspace/collisions#collision-filtering)
are acknowledged for detection.

Code Samples

Touching Parts Count

This code sample creates a BillboardGui on a part that displays the number of
parts presently touching it.

```
local part = script.Parent



local billboardGui = Instance.new("BillboardGui")



billboardGui.Size = UDim2.new(0, 200, 0, 50)



billboardGui.Adornee = part



billboardGui.AlwaysOnTop = true



billboardGui.Parent = part



local tl = Instance.new("TextLabel")



tl.Size = UDim2.new(1, 0, 1, 0)



tl.BackgroundTransparency = 1



tl.Parent = billboardGui



local numTouchingParts = 0



local function onTouch(otherPart)



print("Touch started: " .. otherPart.Name)



numTouchingParts = numTouchingParts + 1



tl.Text = numTouchingParts



end



local function onTouchEnded(otherPart)



print("Touch ended: " .. otherPart.Name)



numTouchingParts = numTouchingParts - 1



tl.Text = numTouchingParts



end



part.Touched:Connect(onTouch)



part.TouchEnded:Connect(onTouchEnded)
```

Provide feedback

---