# Workspace | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Workspace
Scraped: 2026-01-11T02:37:52.482369Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- WorldRoot
- Workspace
- Camera
- Terrain
- Player
- Model
- PVInstance
- Instance
- Object
- BaseParts
- Attachments
- ParticleEmitters
- Beams
- BillboardGuis
- Models
- ReplicatedStorage
- ServerStorage
- Model:MakeJoints()
- Model:BreakJoints()
- Workspace:MakeJoints()
- Workspace:BreakJoints()
- FallenPartsDestroyHeight
- Workspace.CurrentCamera
- Workspace.Terrain
- Workspace.FluidForces
- MarketplaceService
- EnableFluidForces
- IKControl
- MeshParts
- AlignOrientation
- AlignPosition
- AngularVelocity
- LinearVelocity
- AngularVelocity.ReactionTorqueEnabled
- AlignPosition.ReactionForceEnabled
- AlignOrientation.Mode
- Constraints
- StarterPlayer
- UserInputService
- RunService.PreRender
- RunService.PreAnimation
- RunService.PreSimulation
- RunService.PostSimulation
- RunService.Heartbeat
- DataModel.BindToClose
- Workspace.StreamingMinRadius
- Workspace.StreamingTargetRadius
- Workspace.StreamingIntegrityMode
- ReplicationFocus
- Workspace.StreamingEnabled
- parts
- CanTouch
- BasePart.CanCollide
- RunService:BindToSimulation()
- BasePart.Anchored
- BasePart
- Humanoids
- Workspace:SetPhysicsThrottleEnabled()
- Parts
- Player:Kick()
- DistributedGameTime
- Rotate
- RotateP
- Plugin:GetJoinMode()
- Workspace:UnjoinFromOutsiders()
- Workspace.PGSPhysicsSolverEnabled
- Workspace:JoinToOutsiders()
- DataModel.Loaded
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [WorldRoot](/docs/reference/engine/classes/WorldRoot)
6. /
7. [Workspace](/docs/reference/engine/classes/Workspace)

English

Feedback

Engine Class

![Workspace](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Workspace-Dark.webp)Workspace

Workspace houses 3D objects which are rendered to the 3D world. Objects
not descending from it will not be rendered or physically interact with the
world.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [AirDensity](#AirDensity):[number](/docs/luau/numbers) |
| [AirTurbulenceIntensity](#AirTurbulenceIntensity):[number](/docs/luau/numbers) |
| [AllowThirdPartySales](#AllowThirdPartySales):[boolean](/docs/luau/booleans) |
| [AuthorityMode](#AuthorityMode):[Enum.AuthorityMode](/docs/reference/engine/enums/AuthorityMode) |
| [AvatarUnificationMode](#AvatarUnificationMode):[Enum.AvatarUnificationMode](/docs/reference/engine/enums/AvatarUnificationMode) |
| [ClientAnimatorThrottling](#ClientAnimatorThrottling):[Enum.ClientAnimatorThrottlingMode](/docs/reference/engine/enums/ClientAnimatorThrottlingMode) |
| [CurrentCamera](#CurrentCamera):[Camera](/docs/reference/engine/classes/Camera) |
| [DistributedGameTime](#DistributedGameTime):[number](/docs/luau/numbers) |
| [FallenPartsDestroyHeight](#FallenPartsDestroyHeight):[number](/docs/luau/numbers) |
| [FallHeightEnabled](#FallHeightEnabled):[boolean](/docs/luau/booleans) |
| [FilteringEnabled](#FilteringEnabled):[boolean](/docs/luau/booleans)  Deprecated |
| [FluidForces](#FluidForces):[Enum.FluidForces](/docs/reference/engine/enums/FluidForces) |
| [GlobalWind](#GlobalWind):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Gravity](#Gravity):[number](/docs/luau/numbers) |
| [IKControlConstraintSupport](#IKControlConstraintSupport):[Enum.IKControlConstraintSupport](/docs/reference/engine/enums/IKControlConstraintSupport) |
| [InsertPoint](#InsertPoint):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [InterpolationThrottling](#InterpolationThrottling):[Enum.InterpolationThrottlingMode](/docs/reference/engine/enums/InterpolationThrottlingMode)  Deprecated |
| [LuauTypeCheckMode](#LuauTypeCheckMode):[Enum.LuauTypeCheckMode](/docs/reference/engine/enums/LuauTypeCheckMode) |
| [MeshPartHeadsAndAccessories](#MeshPartHeadsAndAccessories):[Enum.MeshPartHeadsAndAccessories](/docs/reference/engine/enums/MeshPartHeadsAndAccessories) |
| [ModelStreamingBehavior](#ModelStreamingBehavior):[Enum.ModelStreamingBehavior](/docs/reference/engine/enums/ModelStreamingBehavior) |
| [MoverConstraintRootBehavior](#MoverConstraintRootBehavior):[Enum.MoverConstraintRootBehaviorMode](/docs/reference/engine/enums/MoverConstraintRootBehaviorMode) |
| [NextGenerationReplication](#NextGenerationReplication):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [PathfindingUseImprovedSearch](#PathfindingUseImprovedSearch):[Enum.PathfindingUseImprovedSearch](/docs/reference/engine/enums/PathfindingUseImprovedSearch) |
| [PhysicsImprovedSleep](#PhysicsImprovedSleep):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [PhysicsSteppingMethod](#PhysicsSteppingMethod):[Enum.PhysicsSteppingMethod](/docs/reference/engine/enums/PhysicsSteppingMethod) |
| [PlayerCharacterDestroyBehavior](#PlayerCharacterDestroyBehavior):[Enum.PlayerCharacterDestroyBehavior](/docs/reference/engine/enums/PlayerCharacterDestroyBehavior) |
| [PlayerScriptsUseInputActionSystem](#PlayerScriptsUseInputActionSystem):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [PrimalPhysicsSolver](#PrimalPhysicsSolver):[Enum.PrimalPhysicsSolver](/docs/reference/engine/enums/PrimalPhysicsSolver) |
| [RejectCharacterDeletions](#RejectCharacterDeletions):[Enum.RejectCharacterDeletions](/docs/reference/engine/enums/RejectCharacterDeletions) |
| [RenderingCacheOptimizations](#RenderingCacheOptimizations):[Enum.RenderingCacheOptimizationMode](/docs/reference/engine/enums/RenderingCacheOptimizationMode) |
| [ReplicateInstanceDestroySetting](#ReplicateInstanceDestroySetting):[Enum.ReplicateInstanceDestroySetting](/docs/reference/engine/enums/ReplicateInstanceDestroySetting) |
| [Retargeting](#Retargeting):[Enum.AnimatorRetargetingMode](/docs/reference/engine/enums/AnimatorRetargetingMode) |
| [SandboxedInstanceMode](#SandboxedInstanceMode):[Enum.SandboxedInstanceMode](/docs/reference/engine/enums/SandboxedInstanceMode) |
| [SignalBehavior](#SignalBehavior):[Enum.SignalBehavior](/docs/reference/engine/enums/SignalBehavior) |
| [StreamingEnabled](#StreamingEnabled):[boolean](/docs/luau/booleans) |
| [StreamingIntegrityMode](#StreamingIntegrityMode):[Enum.StreamingIntegrityMode](/docs/reference/engine/enums/StreamingIntegrityMode) |
| [StreamingMinRadius](#StreamingMinRadius):[number](/docs/luau/numbers) |
| [StreamingTargetRadius](#StreamingTargetRadius):[number](/docs/luau/numbers) |
| [StreamOutBehavior](#StreamOutBehavior):[Enum.StreamOutBehavior](/docs/reference/engine/enums/StreamOutBehavior) |
| [Terrain](#Terrain):[Terrain](/docs/reference/engine/classes/Terrain) |
| [TouchesUseCollisionGroups](#TouchesUseCollisionGroups):[boolean](/docs/luau/booleans) |
| [TouchEventsUseCollisionGroups](#TouchEventsUseCollisionGroups):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [UseFixedSimulation](#UseFixedSimulation):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [UseNewLuauTypeSolver](#UseNewLuauTypeSolver):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |

Methods

|  |
| --- |
| [BreakJoints](#BreakJoints)(objects: Instances):()  Deprecated |
| [GetNumAwakeParts](#GetNumAwakeParts)():[number](/docs/luau/numbers) |
| [GetPhysicsThrottling](#GetPhysicsThrottling)():[number](/docs/luau/numbers) |
| [GetRealPhysicsFPS](#GetRealPhysicsFPS)():[number](/docs/luau/numbers) |
| [GetServerTimeNow](#GetServerTimeNow)():[number](/docs/luau/numbers) |
| [JoinToOutsiders](#JoinToOutsiders)(objects: Instances,jointType: [Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode)):() |
| [MakeJoints](#MakeJoints)(objects: Instances):()  Deprecated |
| [PGSIsEnabled](#PGSIsEnabled)():[boolean](/docs/luau/booleans) |
| [UnjoinFromOutsiders](#UnjoinFromOutsiders)(objects: Instances):() |
| [ZoomToExtents](#ZoomToExtents)():() |

Events

|  |
| --- |
| [PersistentLoaded](#PersistentLoaded)(player: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

21 inherited from [WorldRoot](/docs/reference/engine/classes/WorldRoot)

26 inherited from [Model](/docs/reference/engine/classes/Model)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The core job of [Workspace](/docs/reference/engine/classes/Workspace) is to hold objects that exist in the 3D
world, effectively [BaseParts](/docs/reference/engine/classes/BasePart) and
[Attachments](/docs/reference/engine/classes/Attachment). While such objects are descendant of
[Workspace](/docs/reference/engine/classes/Workspace), they will be active. For [BaseParts](/docs/reference/engine/classes/BasePart), this
means they will be rendered, and physically interact with other parts and the
world. For [Attachments](/docs/reference/engine/classes/Attachment), this means that objects adorned to
them, such as [ParticleEmitters](/docs/reference/engine/classes/ParticleEmitter), [Beams](/docs/reference/engine/classes/Beam),
and [BillboardGuis](/docs/reference/engine/classes/BillboardGui), will render.

Understanding this behavior is important, as it means objects can be removed
from [Workspace](/docs/reference/engine/classes/Workspace) when they are not needed. For example, map
[Models](/docs/reference/engine/classes/Model) can be removed when a different map is being played on.
Objects that are not immediately needed in the 3D world are generally stored
in [ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage) or [ServerStorage](/docs/reference/engine/classes/ServerStorage).

In its role as the holder of active 3D objects, [Workspace](/docs/reference/engine/classes/Workspace) includes a
number of useful functions related to parts, their positions, and joints
between them.

##### Accessing the Workspace

[Workspace](/docs/reference/engine/classes/Workspace) can be accessed several ways, all of which are valid.

* workspace
* game:GetService("Workspace")
* game.Workspace

##### Notes

* Objects that require adornment, such as
  [ParticleEmitters](/docs/reference/engine/classes/ParticleEmitter) and
  [BillboardGuis](/docs/reference/engine/classes/BillboardGui), will be at the
  (0, 0, 0) position when parented to
  [Workspace](/docs/reference/engine/classes/Workspace) without an adornee otherwise being set.
* The [Model:MakeJoints()](/docs/reference/engine/classes/Model#MakeJoints) and [Model:BreakJoints()](/docs/reference/engine/classes/Model#BreakJoints) methods
  inherited from the [Model](/docs/reference/engine/classes/Model) class are overridden by
  [Workspace:MakeJoints()](/docs/reference/engine/classes/Workspace#MakeJoints) and [Workspace:BreakJoints()](/docs/reference/engine/classes/Workspace#BreakJoints) which can
  only be used in plugins.
* It is impossible to delete [Workspace](/docs/reference/engine/classes/Workspace).
* [Workspace](/docs/reference/engine/classes/Workspace) automatically cleans up [BaseParts](/docs/reference/engine/classes/BasePart) that
  fall beneath
  [FallenPartsDestroyHeight](/docs/reference/engine/classes/Workspace#FallenPartsDestroyHeight).
* A client's current [Camera](/docs/reference/engine/classes/Camera) object can be accessed using the
  [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) property.
* The [Terrain](/docs/reference/engine/classes/Terrain) object can be accessed using the
  [Workspace.Terrain](/docs/reference/engine/classes/Workspace#Terrain) property.

---

API Reference

Properties

AirDensity

Read Parallel

The air density at ground level, used in the aerodynamic force model.

Workspace.AirDensity:[number](/docs/luau/numbers)

The ground level (Y of 0) air density in RMU/stud³ units (see
[Roblox Units](/docs/physics/units)), used to calculate the
aerodynamic force if [Workspace.FluidForces](/docs/reference/engine/classes/Workspace#FluidForces) is
[Experimental](/docs/reference/engine/enums/FluidForces). The default corresponds to realistic sea
level air density at standard temperature and pressure. Air density decays
as the Y altitude increases, reaching 5% of its ground level value at
100,000 studs. Below Y of 0, the air density is fixed at the input
value.

Provide feedback

---

AirTurbulenceIntensity

Read Parallel

Controls the strength of turbulence present in the wind velocity field,
affecting the aerodynamic force model.

Workspace.AirTurbulenceIntensity:[number](/docs/luau/numbers)

Controls the intensity of turbulence by determining the magnitude of
fluctuations in wind velocities. Ranges from 0 to 1, with a value of
0 disabling turbulence and a value of 1 providing the most intense
turbulence. The values of AirTurbulenceIntensity roughly correspond to
the following levels:

* (0, 0.4]: Low intensity turbulence
* (0.4, 0.7]: Moderate intensity turbulence
* (0.7, 1]: High intensity turbulence

The magnitude of the fluctuations at a fixed intensity scale linearly with
the magnitude of the global wind, except in the case that the global wind
is zero. When the global wind is zero, the magnitude of the fluctuations
scale exponentially with AirTurbulenceIntensity, allowing low and high
intensity turbulence to exist with wind velocities that still average out
to zero.

Provide feedback

---

AllowThirdPartySales

Not Replicated

Read Parallel

Determines whether assets created by other users can be sold in the game.

Workspace.AllowThirdPartySales:[boolean](/docs/luau/booleans)

This [Workspace](/docs/reference/engine/classes/Workspace) property determines whether assets created by other
uses can be sold in the game.

#### What are third party sales?

When this value is false, as it is by default, only assets created by the
place creator (be it a player or a group) and Roblox can be sold using
[MarketplaceService](/docs/reference/engine/classes/MarketplaceService).

In most cases, games do not need to sell third party assets. However, some
games such as trade hangouts require this feature and therefore it exists
as an opt-in option.

#### What third party products can I sell?

Note,
[developer products](/docs/production/monetization/developer-products)
can only be sold in the game they are associated with, regardless of what
AllowThirdPartySales is set to. This property affects
[Game Passes](/docs/production/monetization/game-passes) and
[clothing](/docs/art/classic-clothing).

Provide feedback

---

AuthorityMode

Roblox Script Security

Read Parallel

Sets the server authority mode.

Workspace.AuthorityMode:[Enum.AuthorityMode](/docs/reference/engine/enums/AuthorityMode)

Sets the server authority mode. See [Enum.AuthorityMode](/docs/reference/engine/enums/AuthorityMode) for options.

Provide feedback

---

AvatarUnificationMode

Not Scriptable

Read Parallel

Workspace.AvatarUnificationMode:[Enum.AvatarUnificationMode](/docs/reference/engine/enums/AvatarUnificationMode)

Provide feedback

---

ClientAnimatorThrottling

Read Parallel

Specifies the animation throttling mode for the local client.

Workspace.ClientAnimatorThrottling:[Enum.ClientAnimatorThrottlingMode](/docs/reference/engine/enums/ClientAnimatorThrottlingMode)

Specifies the [Enum.ClientAnimatorThrottlingMode](/docs/reference/engine/enums/ClientAnimatorThrottlingMode) to use for the local
client.

When enabled, animations on remotely-simulated [Model](/docs/reference/engine/classes/Model) instances
will begin to throttle. The throttler calculates throttling intensity
using:

* Visibility of a [Model](/docs/reference/engine/classes/Model) in relation to the [Camera](/docs/reference/engine/classes/Camera)
* In-game FPS
* Number of active animations

Provide feedback

---

CurrentCamera

Not Replicated

Read Parallel

The [Camera](/docs/reference/engine/classes/Camera) object being used by the local player.

Workspace.CurrentCamera:[Camera](/docs/reference/engine/classes/Camera)

The [Camera](/docs/reference/engine/classes/Camera) object being used by the local player.

#### How to use CurrentCamera

When looking for a client's [Camera](/docs/reference/engine/classes/Camera) object, use this property
rather than looking for a child of [Workspace](/docs/reference/engine/classes/Workspace) named "Camera".

When you set this property, all other Camera objects in the Workspace
are destroyed, including the previous CurrentCamera. If you set this
property to nil or to a camera that is not a descendant of the Workspace
(or the CurrentCamera is otherwise destroyed), a new Camera will be
created and assigned. Avoid these scenarios, as destroying the camera can
have unintended consequences.

For more information, see
[Scripting the Camera](/docs/workspace/camera#scripting-the-camera).

Provide feedback

---

DistributedGameTime

Not Replicated

Read Parallel

The amount of time, in seconds, that the game has been running.

Workspace.DistributedGameTime:[number](/docs/luau/numbers)

The amount of time, in seconds, that the game has been running.

Despite the title, this value is currently not 'Distributed' across the
client and the server. Instead, on the server it represents how long the
server has been running. On the client, it represents how long the client
has been connected to the server.

Developers should not rely on the above behavior, and it is possible this
property will be synchronized across clients and the server in the future.

Those looking for the time since the program started running should use
the 'time' function instead. See below for a comparison between
DistributedGameTime and its alternatives.

```
local Workspace = game:GetService("Workspace")



print(Workspace.DistributedGameTime) -- Time the game started running



print(os.time()) -- Time since epoch (1 January 1970, 00:00:00) UTC



print(tick()) -- Time since epoch (1 January 1970, 00:00:00) system time



print(time()) -- Time the game started running



print(elapsedTime()) -- Time since Roblox started running
```

Provide feedback

---

FallenPartsDestroyHeight

Plugin Security

Read Parallel

Determines the height at which falling [BaseParts](/docs/reference/engine/classes/BasePart) and
their ancestor [Models](/docs/reference/engine/classes/Model) are removed from [Workspace](/docs/reference/engine/classes/Workspace).

Workspace.FallenPartsDestroyHeight:[number](/docs/luau/numbers)

This property determines the height at which the engine automatically
removes falling [BaseParts](/docs/reference/engine/classes/BasePart) and their ancestor
[Models](/docs/reference/engine/classes/Model) from [Workspace](/docs/reference/engine/classes/Workspace) by parenting them to nil.
This is to prevent parts that have fallen off the map from continuing to
fall forever.

If a part removed due to this behavior is the last part in a
[Model](/docs/reference/engine/classes/Model), that model will also be removed. This applies to all model
ancestors of the part.

This property is clamped between -50,000 and 50,000 because
[BaseParts](/docs/reference/engine/classes/BasePart) do not simulate or render properly at a great
distance from the origin due to floating point inaccuracies.

This property can be read by scripts, but can only be set by plugins, the
command bar, or the properties window in Studio.

Provide feedback

---

FallHeightEnabled

Plugin Security

Read Parallel

Workspace.FallHeightEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

FilteringEnabled

Deprecated

Show details

---

FluidForces

Not Scriptable

Read Parallel

Determines whether the physics engine computes aerodynamic forces on
[BaseParts](/docs/reference/engine/classes/BasePart) whose
[EnableFluidForces](/docs/reference/engine/classes/BasePart#EnableFluidForces) property is true.

Workspace.FluidForces:[Enum.FluidForces](/docs/reference/engine/enums/FluidForces)

With this property enabled, the physics engine computes aerodynamic forces
on [BaseParts](/docs/reference/engine/classes/BasePart) whose
[EnableFluidForces](/docs/reference/engine/classes/BasePart#EnableFluidForces) property is true. The
default, [Default](/docs/reference/engine/enums/FluidForces), disables aerodynamic forces. Note
that this property cannot be set through scripting and instead must be
toggled in Studio.

Provide feedback

---

GlobalWind

Read Parallel

Specifies the global wind vector for animated terrain grass, dynamic
clouds, and particles.

Workspace.GlobalWind:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property specifies the direction and strength that wind blows through
the experience, affecting terrain grass, dynamic clouds, and particles.
See the [Global Wind](/docs/environment/global-wind) article for
details.

Provide feedback

---

Gravity

Read Parallel

Determines the acceleration due to gravity applied to falling
[BaseParts](/docs/reference/engine/classes/BasePart).

Workspace.Gravity:[number](/docs/luau/numbers)

Determines the acceleration due to gravity applied to falling
[BaseParts](/docs/reference/engine/classes/BasePart). This value is measured in studs per second
squared and by default is set to 196.2 studs/second2. By
changing this value, developers can simulate the effects of lower or
higher gravity in game.

Code Samples

Low Gravity Button

This script creates a touch pad in the workspace that, when touched, will
reduce the game's gravity. Activating the pad again will switch back to normal
gravity.

```
local MOON_GRAVITY_RATIO = 1.62 / 9.81



local DEFAULT_GRAVITY = 196.2



local MOON_GRAVITY = DEFAULT_GRAVITY * MOON_GRAVITY_RATIO



-- Create a touch pad



local pad = Instance.new("Part")



pad.Size = Vector3.new(5, 1, 5)



pad.Position = Vector3.new(0, 0.5, 0)



pad.Anchored = true



pad.BrickColor = BrickColor.new("Bright green")



pad.Parent = workspace



-- Listen for pad touch



local enabled = false



local debounce = false



local function onPadTouched(_hit)



if not debounce then



debounce = true



enabled = not enabled



workspace.Gravity = enabled and MOON_GRAVITY or DEFAULT_GRAVITY



pad.BrickColor = enabled and BrickColor.new("Bright red") or BrickColor.new("Bright green")



task.wait(1)



debounce = false



end



end



pad.Touched:Connect(onPadTouched)
```

Provide feedback

---

IKControlConstraintSupport

Not Scriptable

Read Parallel

Enables support for constraints for IKControls. If disabled, IKControls
ignore physics constraints.

Workspace.IKControlConstraintSupport:[Enum.IKControlConstraintSupport](/docs/reference/engine/enums/IKControlConstraintSupport)

Enables support for constraints for IKControls. The Default value is the
same as Enabled. If disabled, IKControls ignore physics constraints. See
[IKControl](/docs/reference/engine/classes/IKControl) for additional details.

Provide feedback

---

InsertPoint

Not Replicated

Read Parallel

Workspace.InsertPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---

InterpolationThrottling

Deprecated

Show details

---

LuauTypeCheckMode

Plugin Security

Read Parallel

Workspace.LuauTypeCheckMode:[Enum.LuauTypeCheckMode](/docs/reference/engine/enums/LuauTypeCheckMode)

Provide feedback

---

MeshPartHeadsAndAccessories

Not Scriptable

Read Parallel

Sets whether character Heads and Accessories should be downloaded as
MeshParts.

Workspace.MeshPartHeadsAndAccessories:[Enum.MeshPartHeadsAndAccessories](/docs/reference/engine/enums/MeshPartHeadsAndAccessories)

Sets whether character Heads and Accessories should be downloaded as
[MeshParts](/docs/reference/engine/classes/MeshPart). The Default value is the same as Enabled.
If this feature is enabled, built-in avatars will use
[MeshParts](/docs/reference/engine/classes/MeshPart) for the character's Head and Accessories.

Provide feedback

---

ModelStreamingBehavior

Not Scriptable

Read Parallel

Workspace.ModelStreamingBehavior:[Enum.ModelStreamingBehavior](/docs/reference/engine/enums/ModelStreamingBehavior)

Provide feedback

---

MoverConstraintRootBehavior

Not Scriptable

Read Parallel

Controls the logic used to select the assembly root part when using any of
the mover constraints.

Workspace.MoverConstraintRootBehavior:[Enum.MoverConstraintRootBehaviorMode](/docs/reference/engine/enums/MoverConstraintRootBehaviorMode)

Controls the logic used to select the assembly root part for mechanisms
that use any of the following constraints:

* [AlignOrientation](/docs/reference/engine/classes/AlignOrientation)
* [AlignPosition](/docs/reference/engine/classes/AlignPosition)
* [AngularVelocity](/docs/reference/engine/classes/AngularVelocity)
* [LinearVelocity](/docs/reference/engine/classes/LinearVelocity)

When this property is set to
[Enum.MoverConstraintRootBehaviorMode.Enabled](/docs/reference/engine/enums/MoverConstraintRootBehaviorMode#Enabled), these constraints will be
ignored when selecting the assembly root part if the constraint does not
transmit forces between two parts (some examples being
[AngularVelocity.ReactionTorqueEnabled](/docs/reference/engine/classes/AngularVelocity#ReactionTorqueEnabled) set to false,
[AlignPosition.ReactionForceEnabled](/docs/reference/engine/classes/AlignPosition#ReactionForceEnabled) set to false, or
[AlignOrientation.Mode](/docs/reference/engine/classes/AlignOrientation#Mode) set to
[Enum.OrientationAlignmentMode.OneAttachment](/docs/reference/engine/enums/OrientationAlignmentMode#OneAttachment)).

When this property is set to
[Enum.MoverConstraintRootBehaviorMode.Disabled](/docs/reference/engine/enums/MoverConstraintRootBehaviorMode#Disabled), these constraints may be
erroneously considered when selecting the assembly root part, leading to
inconsistent network ownership and delays when adding these constraints to
a mechanism.

Provide feedback

---

NextGenerationReplication

Not Scriptable

Read Parallel

When true, enables an alternate replication system that alters and
improves how properties are replicated under the hood.

Workspace.NextGenerationReplication:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

When true, enables an alternate replication system that alters and
improves how properties are replicated under the hood; note that when
true, you should not rely on the ordering of property replication and
remote events.

Provide feedback

---

PathfindingUseImprovedSearch

Not Scriptable

Read Parallel

Workspace.PathfindingUseImprovedSearch:[Enum.PathfindingUseImprovedSearch](/docs/reference/engine/enums/PathfindingUseImprovedSearch)

Provide feedback

---

PhysicsImprovedSleep

Not Scriptable

Read Parallel

Workspace.PhysicsImprovedSleep:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

Provide feedback

---

PhysicsSteppingMethod

Not Scriptable

Read Parallel

Sets how the solver will advance the physics simulation forward in time.

Workspace.PhysicsSteppingMethod:[Enum.PhysicsSteppingMethod](/docs/reference/engine/enums/PhysicsSteppingMethod)

Sets how the solver will advance the physics simulation forward in time.
This option is not scriptable and must be set from the
PhysicsSteppingMethod property of Workspace within Studio. See
[Adaptive Timestepping](/docs/physics/adaptive-timestepping) for
details.

Note that when assemblies of different simulation rates become connected
via [Constraints](/docs/reference/engine/classes/Constraint) or collisions, the combined mechanism
will default to the highest simulation rate for stability.

Provide feedback

---

PlayerCharacterDestroyBehavior

Not Scriptable

Read Parallel

Workspace.PlayerCharacterDestroyBehavior:[Enum.PlayerCharacterDestroyBehavior](/docs/reference/engine/enums/PlayerCharacterDestroyBehavior)

Provide feedback

---

PlayerScriptsUseInputActionSystem

Not Scriptable

Read Parallel

Controls internal behavior of the built-in [Player](/docs/reference/engine/classes/Player) scripts.

Workspace.PlayerScriptsUseInputActionSystem:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

When true, updates the built-in [Player](/docs/reference/engine/classes/Player) scripts to a new system
where they live under [StarterPlayer](/docs/reference/engine/classes/StarterPlayer), use the
[Input Action System](/docs/input/input-action-system), and allow
the server to process player inputs.

Provide feedback

---

PrimalPhysicsSolver

Not Scriptable

Read Parallel

Workspace.PrimalPhysicsSolver:[Enum.PrimalPhysicsSolver](/docs/reference/engine/enums/PrimalPhysicsSolver)

Provide feedback

---

RejectCharacterDeletions

Not Scriptable

Read Parallel

Workspace.RejectCharacterDeletions:[Enum.RejectCharacterDeletions](/docs/reference/engine/enums/RejectCharacterDeletions)

Provide feedback

---

RenderingCacheOptimizations

Not Scriptable

Read Parallel

Workspace.RenderingCacheOptimizations:[Enum.RenderingCacheOptimizationMode](/docs/reference/engine/enums/RenderingCacheOptimizationMode)

Provide feedback

---

ReplicateInstanceDestroySetting

Not Scriptable

Read Parallel

Workspace.ReplicateInstanceDestroySetting:[Enum.ReplicateInstanceDestroySetting](/docs/reference/engine/enums/ReplicateInstanceDestroySetting)

Provide feedback

---

Retargeting

Read Parallel

Workspace.Retargeting:[Enum.AnimatorRetargetingMode](/docs/reference/engine/enums/AnimatorRetargetingMode)

Provide feedback

---

SandboxedInstanceMode

Not Scriptable

Read Parallel

Workspace.SandboxedInstanceMode:[Enum.SandboxedInstanceMode](/docs/reference/engine/enums/SandboxedInstanceMode)

Provide feedback

---

SignalBehavior

Not Scriptable

Read Parallel

Configures when the engine resumes event handlers.

Workspace.SignalBehavior:[Enum.SignalBehavior](/docs/reference/engine/enums/SignalBehavior)

This property determines whether event handlers will be resumed
immediately when the event fires, or deferred and then resumed at a later
resumption point. Resumption points currently include:

* Input processing (resumes once per input to be processed, see
  [UserInputService](/docs/reference/engine/classes/UserInputService))
* [RunService.PreRender](/docs/reference/engine/classes/RunService#PreRender)
* Legacy waiting script resumption such as wait(), spawn(), and
  delay()
* [RunService.PreAnimation](/docs/reference/engine/classes/RunService#PreAnimation)
* [RunService.PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation)
* [RunService.PostSimulation](/docs/reference/engine/classes/RunService#PostSimulation)
* Waiting script resumption such as [task.wait()](/docs/reference/engine/libraries/task#wait),
  [task.spawn()](/docs/reference/engine/libraries/task#spawn), and [task.delay()](/docs/reference/engine/libraries/task#delay)
* [RunService.Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat)
* [DataModel.BindToClose](/docs/reference/engine/classes/DataModel#BindToClose)

For more information, see
[Deferred Events](/docs/scripting/events/deferred).

Provide feedback

---

StreamingEnabled

Plugin Security

Read Parallel

Whether content streaming is enabled for the place.

Workspace.StreamingEnabled:[boolean](/docs/luau/booleans)

The StreamingEnabled property determines whether game content
streaming is enabled for the place. This property is not scriptable and
therefore must be set on the Workspace object in Studio.

See also:

* [Workspace.StreamingMinRadius](/docs/reference/engine/classes/Workspace#StreamingMinRadius)
* [Workspace.StreamingTargetRadius](/docs/reference/engine/classes/Workspace#StreamingTargetRadius)
* [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode)

Provide feedback

---

StreamingIntegrityMode

Not Scriptable

Read Parallel

Determines whether StreamingIntegrityMode is active.

Workspace.StreamingIntegrityMode:[Enum.StreamingIntegrityMode](/docs/reference/engine/enums/StreamingIntegrityMode)

If instance [streaming](/docs/workspace/streaming) is enabled, an
experience may behave in unintended ways if a player's character moves
into a region of the world that has not been streamed to their client. The
streaming integrity feature offers a way to avoid those potentially
problematic situations.

Provide feedback

---

StreamingMinRadius

Not Scriptable

Read Parallel

Minimum distance that content will be streamed to players with high
priority.

Workspace.StreamingMinRadius:[number](/docs/luau/numbers)

The StreamingMinRadius property indicates the radius around the
player's character or the current
[ReplicationFocus](/docs/reference/engine/classes/Player#ReplicationFocus) in which content will be
streamed in at the highest priority. Defaults to 64 studs.

Care should be taken when increasing the default minimum radius since
doing so will require more memory and more server bandwidth at the expense
of other components.

See also:

* [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) which controls whether content
  streaming is enabled
* [Workspace.StreamingTargetRadius](/docs/reference/engine/classes/Workspace#StreamingTargetRadius)
* [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode)

Provide feedback

---

StreamingTargetRadius

Not Scriptable

Read Parallel

Maximum distance that content will be streamed to players.

Workspace.StreamingTargetRadius:[number](/docs/luau/numbers)

The StreamingTargetRadius property controls the maximum distance away
from the player's character or the current
[ReplicationFocus](/docs/reference/engine/classes/Player#ReplicationFocus) in which content will be
streamed in. Defaults to 1024 studs.

Note that the engine is allowed to retain previously loaded content beyond
the target radius, memory permitting.

See also:

* [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) which controls whether content
  streaming is enabled
* [Workspace.StreamingMinRadius](/docs/reference/engine/classes/Workspace#StreamingMinRadius)
* [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode)

Provide feedback

---

StreamOutBehavior

Not Scriptable

Read Parallel

Configures how the engine decides when to Stream content away from
players.

Workspace.StreamOutBehavior:[Enum.StreamOutBehavior](/docs/reference/engine/enums/StreamOutBehavior)

The StreamOutBehavior controls where content will be unloaded from the
[ReplicationFocus](/docs/reference/engine/classes/Player#ReplicationFocus) based on device Memory
Conditions, or based on Streaming Radius.

See also:

* [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) which controls whether content
  streaming is enabled
* [Workspace.StreamingMinRadius](/docs/reference/engine/classes/Workspace#StreamingMinRadius)
* [Workspace.StreamingTargetRadius](/docs/reference/engine/classes/Workspace#StreamingTargetRadius)
* [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode)

Provide feedback

---

Terrain

Read Only

Not Replicated

Read Parallel

A reference to the [Terrain](/docs/reference/engine/classes/Terrain) object parented to the
[Workspace](/docs/reference/engine/classes/Workspace).

Workspace.Terrain:[Terrain](/docs/reference/engine/classes/Terrain)

This property is a reference to the [Terrain](/docs/reference/engine/classes/Terrain) object parented to the
[Workspace](/docs/reference/engine/classes/Workspace).

![Terrain object within the Workspace hierarchy](https://prod.docsiteassets.roblox.com/assets/studio/explorer/Workspace-Terrain.png)

See [Environmental Terrain](/docs/parts/terrain) for more
information.

Provide feedback

---

TouchesUseCollisionGroups

Not Scriptable

Read Parallel

Determines whether [parts](/docs/reference/engine/classes/BasePart) in different groups set to not
collide will ignore collisions and touch events.

Workspace.TouchesUseCollisionGroups:[boolean](/docs/luau/booleans)

This property determines whether [parts](/docs/reference/engine/classes/BasePart) in different
groups set to not collide will ignore collisions and touch events. By
default, the value of this property is set to false.

When this property is enabled, parts in different groups set to not
collide will also ignore the [CanTouch](/docs/reference/engine/classes/BasePart#CanTouch) property,
similar to how [BasePart.CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) is ignored. For more
information on the behavior of CanTouch, please visit its property page.

Provide feedback

---

TouchEventsUseCollisionGroups

Not Scriptable

Read Parallel

Workspace.TouchEventsUseCollisionGroups:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

Provide feedback

---

UseFixedSimulation

Not Scriptable

Read Parallel

When true, enables [RunService:BindToSimulation()](/docs/reference/engine/classes/RunService#BindToSimulation) which calls a
function at a fixed frequency, updates physics stepping logic, and makes
the [time()](/docs/reference/engine/globals/RobloxGlobals#time) function return the fixed stepped frame
time.

Workspace.UseFixedSimulation:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

When true, enables [RunService:BindToSimulation()](/docs/reference/engine/classes/RunService#BindToSimulation) which calls a
function at a fixed frequency. Also updates physics stepping logic such
that character controller updates and joint transforms are performed at a
fixed frequency rather than once per frame, as well as makes the
[time()](/docs/reference/engine/globals/RobloxGlobals#time) function return the fixed stepped frame
time.

Provide feedback

---

UseNewLuauTypeSolver

Not Scriptable

Read Parallel

Workspace.UseNewLuauTypeSolver:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

Provide feedback

---

Methods

BreakJoints

Deprecated

Show details

---

GetNumAwakeParts

Write Parallel

Returns the number of [BaseParts](/docs/reference/engine/classes/BasePart) that are deemed
physically active, due to being recently under the influence of physics.

Workspace:GetNumAwakeParts():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

The number of awake parts.

Returns the number of [BaseParts](/docs/reference/engine/classes/BasePart) that are deemed
physically active, due to being recently under the influence of physics.

This function provides a measure of how many [BaseParts](/docs/reference/engine/classes/BasePart)
are being influenced by, or recently under the influence of, physical
forces.

```
local Workspace = game:GetService("Workspace")



print(Workspace:GetNumAwakeParts())
```

In order to ensure good performance, the engine sets
[BaseParts](/docs/reference/engine/classes/BasePart) in which physics are not being applied to a
"sleeping" state. [BaseParts](/docs/reference/engine/classes/BasePart) with
[BasePart.Anchored](/docs/reference/engine/classes/BasePart#Anchored) set to true, for example, will always be
sleeping as physics doesn't apply to them. When a force is applied to a
non‑anchored [BasePart](/docs/reference/engine/classes/BasePart), an "awake" state will be applied. Whilst a
[BasePart](/docs/reference/engine/classes/BasePart) is awake, the physics engine will perform continuous
calculations to ensure physical forces interact correctly with the part.
Once the [BasePart](/docs/reference/engine/classes/BasePart) is no longer subject to physical forces, it will
revert to a "sleeping" state.

Provide feedback

---

GetPhysicsThrottling

Write Parallel

Returns an integer, between 0 and 100, representing the percentage of real
time that physics simulation is currently being throttled to.

Workspace:GetPhysicsThrottling():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

The percentage of real time that physics simulation is currently being
throttled to.

Returns an integer, between 0 and 100, representing the percentage of real
time that physics simulation is currently being throttled to.

This function can be used to determine whether, and to what degree,
physics throttling is occurring.

#### What is physics throttling?

Physics throttling occurs when the physics engine detects it cannot keep
up with the game in real time. When physics is being throttled, it will
update less frequently causing [BaseParts](/docs/reference/engine/classes/BasePart) to appear to
move slower.

Without throttling, the physics simulation would fall further behind out
of sync with the game. This can lead to lower frame rates and other
undesirable behavior.

Objects associated with [Humanoids](/docs/reference/engine/classes/Humanoid) are exempt from physics
throttling.

See also [Workspace:SetPhysicsThrottleEnabled()](/docs/reference/engine/classes/Workspace#SetPhysicsThrottleEnabled).

#### Demonstrating physics throttling

Developers should always avoid creating places that overload the physics
engine, as it leads to sub-par experience for players. Those wishing to
simulate physics throttling for research purposes however, need only
create a lot of [Parts](/docs/reference/engine/classes/Part) very quickly.

```
local Workspace = game:GetService("Workspace")



local i = 0



while true do



i += 1



if i % 5 == 0 then



task.wait()



end



local part = Instance.new("Part", Workspace)



end
```

Provide feedback

---

GetRealPhysicsFPS

Write Parallel

Returns the number of frames per second that physics is currently being
simulated at.

Workspace:GetRealPhysicsFPS():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the number of frames per second that physics is currently
being simulated at.

Returns the number of frames per second that physics is currently being
simulated at.

#### Using GetRealPhysicsFPS to combat exploiters

A common use of this function is to detect if exploiters are increasing
their local physics frame rate to move faster. This is generally done by
comparing the result returned by a client's GetRealPhysicsFPS to a maximum
that will not be breached in normal circumstances (usually 65 or 70). If
this limit is breached, developers can use the [Player:Kick()](/docs/reference/engine/classes/Player#Kick)
function to remove that [Player](/docs/reference/engine/classes/Player) from the game. It is important to
remember that, although this practice may be effective sometimes,
client-side anti-exploiter measures are never 100% reliable.

Code Samples

Workspace:GetRealPhysicsFPS

Speed exploiters commonly increase their local physics FPS in order to
increase their character speed. This can be detected from a LocalScript by
checking if the player's physics FPS is over the maximum:

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



while task.wait(1) do



if workspace:GetRealPhysicsFPS() > 65 then



player:Kick()



end



end
```

Provide feedback

---

GetServerTimeNow

Write Parallel

Returns the server's Unix time in seconds.

Workspace:GetServerTimeNow():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

The estimated Unix timestamp on the server.

This method returns the client's best approximation of the current time on
the server. It is useful for creating synchronized experiences, as every
client will get roughly the same results regardless of their timezone or
local clock.

This method returns a Unix timestamp, similar to [os.time()](/docs/reference/engine/libraries/os),
that you can use with [os.date()](/docs/reference/engine/libraries/os) or
[DateTime.fromUnixTimestamp()](/docs/reference/engine/datatypes/DateTime#fromUnixTimestamp). The timestamp is smoothed so
that:

* It is monotonic; its value will never decrease.
* It moves at the same rate as the local clock to within 0.6%.

This method is useful for making sure an event starts at the right
real-world time and for periodic adjustments to keep a series of events in
sync. For benchmarking or other use cases that require higher precision,
consider [os.clock()](/docs/reference/engine/libraries/os).

This method relies on the server, so calling it from a client that isn't
connected will throw an error. Also note that this method is not suitable
for things like timed rewards, as it is not secure compared to tracking
such timers on the server.

See also:

* [DistributedGameTime](/docs/reference/engine/classes/Workspace#DistributedGameTime), a game-time
  clock
* [os.time()](/docs/reference/engine/libraries/os)
* [DateTime](/docs/reference/engine/datatypes/DateTime)

Provide feedback

---

JoinToOutsiders

Creates joints between the specified [Parts](/docs/reference/engine/classes/BasePart) and any
touching parts depending on the parts' surfaces and the specified joint
creation mode.

Workspace:JoinToOutsiders(

objects:Instances, jointType:[Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode)

):()

Parameters

|  |
| --- |
| objects:Instances  An array of [BaseParts](/docs/reference/engine/classes/BasePart) for whom joints are to be made. |
| jointType:[Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode)  The [Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode) to be used. Passing in [Enum.JointCreationMode.All](/docs/reference/engine/enums/JointCreationMode) or [Enum.JointCreationMode.Surface](/docs/reference/engine/enums/JointCreationMode) has the same behavior which equates to Join Always. |

Returns

()

This function creates joints between the specified [Parts](/docs/reference/engine/classes/BasePart)
and any touching parts depending on the parts' surfaces and the specified
joint creation mode.

This function creates joints between the specified Parts and any planar
touching surfaces, depending on the parts' surfaces and the specified
joint creation mode.

* Glue, Studs, Inlets, Universal, Weld, and Smooth surfaces will all
  create Weld instances.
* Spheres will not surface-weld to anything. The rounded sides of
  cylinders will not surface-weld, but the flat end sides will.
* Hinge and Motor surfaces will still create [Rotate](/docs/reference/engine/classes/Rotate) and
  [RotateP](/docs/reference/engine/classes/RotateP) joint instances, regardless of part shape.

The first parameter is an array of [BaseParts](/docs/reference/engine/classes/BasePart). Joints will
only be created between the parts in the array and not in the array.
Joints will not be created between the parts in the array.

The second parameter is a [Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode) that determines how
joints will be created. Passing in either enum value,
[Enum.JointCreationMode.All](/docs/reference/engine/enums/JointCreationMode) or
[Enum.JointCreationMode.Surface](/docs/reference/engine/enums/JointCreationMode), has the same
behavior which equates to Join Always

This function is used by the Roblox Studio Move tool when the user
finishes moving a selection. In conjunction with
[Plugin:GetJoinMode()](/docs/reference/engine/classes/Plugin#GetJoinMode) and [Workspace:UnjoinFromOutsiders()](/docs/reference/engine/classes/Workspace#UnjoinFromOutsiders)
it can be used to retain join functionality when developing custom studio
build tools. See the snippets below for an example.

```
local Workspace = game:GetService("Workspace")



-- Finished moving a selection; make joints



local function finishedMovingParts(parts)



local joinMode = Plugin:GetJoinMode()



Workspace:JoinToOutsiders(parts, joinMode)



end
```

```
local Workspace = game:GetService("Workspace")



-- Started moving a selection; break joints



local function startMovingParts(parts)



Workspace:UnjoinFromOutsiders(parts)



end
```

Provide feedback

---

MakeJoints

Deprecated

Show details

---

PGSIsEnabled

Returns true if the game has the PGS Physics solver enabled.

Workspace:PGSIsEnabled():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

True if the PGS solver is enabled.

Returns true if the game has the PGS Physics solver enabled.

As [Workspace.PGSPhysicsSolverEnabled](/docs/reference/engine/classes/Workspace#PGSPhysicsSolverEnabled) cannot be accessed by
scripts, the PGSIsEnabled function allows developers to tell which physics
solver the game is using.

Provide feedback

---

UnjoinFromOutsiders

Breaks all joints between the specified [BaseParts](/docs/reference/engine/classes/BasePart) and
other [BaseParts](/docs/reference/engine/classes/BasePart).

Workspace:UnjoinFromOutsiders(objects:Instances):()

Parameters

|  |
| --- |
| objects:Instances  An array of [BaseParts](/docs/reference/engine/classes/BasePart) for whom joints are to be broken. |

Returns

()

Breaks all joints between the specified [BaseParts](/docs/reference/engine/classes/BasePart) and
other [BaseParts](/docs/reference/engine/classes/BasePart).

This function requires an array of [BaseParts](/docs/reference/engine/classes/BasePart). Note,
joints will not be broken between these [BaseParts](/docs/reference/engine/classes/BasePart) (each
other), only between these [BaseParts](/docs/reference/engine/classes/BasePart) and other
[BaseParts](/docs/reference/engine/classes/BasePart) not in the array.

This function is used by the Roblox Studio Move tool when the user
starts moving a selection. In conjunction with
[Plugin:GetJoinMode()](/docs/reference/engine/classes/Plugin#GetJoinMode) and [Workspace:JoinToOutsiders()](/docs/reference/engine/classes/Workspace#JoinToOutsiders) it
can be used to retain join functionality when developing custom Studio
build tools. See the snippets below for an example.

```
local Workspace = game:GetService("Workspace")



-- Finished moving a selection; make joints



local function finishedMovingParts(parts)



local joinMode = Plugin:GetJoinMode()



Workspace:JoinToOutsiders(parts, joinMode)



end
```

```
local Workspace = game:GetService("Workspace")



-- Started moving a selection; break joints



local function startMovingParts(parts)



Workspace:UnjoinFromOutsiders(parts)



end
```

Provide feedback

---

ZoomToExtents

Plugin Security

Positions and zooms the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) to show the extent
of [BaseParts](/docs/reference/engine/classes/BasePart) currently in the [Workspace](/docs/reference/engine/classes/Workspace).

Workspace:ZoomToExtents():()

Returns

()

Positions and zooms the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera) to show the extent
of [BaseParts](/docs/reference/engine/classes/BasePart) currently in the [Workspace](/docs/reference/engine/classes/Workspace). It
exhibits similar behavior to the "focus" command but it shows the extents
of the [Workspace](/docs/reference/engine/classes/Workspace) rather than the currently selected object.

This function cannot be used in scripts but will function in the command
bar or plugins.

Provide feedback

---

Events

PersistentLoaded

Fires when persistent models have been sent to the specified player.

Workspace.PersistentLoaded(player:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |

This event fires every time a player has been sent all current persistent
models and part-less atomic models. The player parameter indicates which
player has received all applicable instances.

Note that experience loading happens before persistent loading, and firing
of the [DataModel.Loaded](/docs/reference/engine/classes/DataModel#Loaded) event does not indicate that all
persistent models are present.

Provide feedback

---