# Stats | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Stats
Scraped: 2026-01-11T02:37:05.909712Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- Stats
- StatsItem
- BasePart:GetTouchingParts()
- DataModel
- Stats:GetMemoryUsageMbForTag()
- Stats:GetMemoryUsageMbAllCategories()
- MemoryTrackingEnabled
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Stats](/docs/reference/engine/classes/Stats)

English

Feedback

Engine Class

Stats

Performance metrics for a game.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [ContactsCount](#ContactsCount):[number](/docs/luau/numbers) |
| [DataReceiveKbps](#DataReceiveKbps):[number](/docs/luau/numbers) |
| [DataSendKbps](#DataSendKbps):[number](/docs/luau/numbers) |
| [FrameTime](#FrameTime):[number](/docs/luau/numbers) |
| [HeartbeatTime](#HeartbeatTime):[number](/docs/luau/numbers) |
| [HeartbeatTimeMs](#HeartbeatTimeMs):[number](/docs/luau/numbers)  Deprecated |
| [InstanceCount](#InstanceCount):[number](/docs/luau/numbers) |
| [MemoryTrackingEnabled](#MemoryTrackingEnabled):[boolean](/docs/luau/booleans) |
| [MovingPrimitivesCount](#MovingPrimitivesCount):[number](/docs/luau/numbers) |
| [PhysicsReceiveKbps](#PhysicsReceiveKbps):[number](/docs/luau/numbers) |
| [PhysicsSendKbps](#PhysicsSendKbps):[number](/docs/luau/numbers) |
| [PhysicsStepTime](#PhysicsStepTime):[number](/docs/luau/numbers) |
| [PhysicsStepTimeMs](#PhysicsStepTimeMs):[number](/docs/luau/numbers)  Deprecated |
| [PrimitivesCount](#PrimitivesCount):[number](/docs/luau/numbers) |
| [RenderCPUFrameTime](#RenderCPUFrameTime):[number](/docs/luau/numbers) |
| [RenderGPUFrameTime](#RenderGPUFrameTime):[number](/docs/luau/numbers) |
| [SceneDrawcallCount](#SceneDrawcallCount):[number](/docs/luau/numbers) |
| [SceneTriangleCount](#SceneTriangleCount):[number](/docs/luau/numbers) |
| [ShadowsDrawcallCount](#ShadowsDrawcallCount):[number](/docs/luau/numbers) |
| [ShadowsTriangleCount](#ShadowsTriangleCount):[number](/docs/luau/numbers) |
| [UI2DDrawcallCount](#UI2DDrawcallCount):[number](/docs/luau/numbers) |
| [UI2DTriangleCount](#UI2DTriangleCount):[number](/docs/luau/numbers) |
| [UI3DDrawcallCount](#UI3DDrawcallCount):[number](/docs/luau/numbers) |
| [UI3DTriangleCount](#UI3DTriangleCount):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetHarmonyQualityLevel](#GetHarmonyQualityLevel)():[number](/docs/luau/numbers) |
| [GetMemoryCategoryNames](#GetMemoryCategoryNames)():[Array](/docs/luau/tables#arrays) |
| [GetMemoryUsageMbAllCategories](#GetMemoryUsageMbAllCategories)():[Array](/docs/luau/tables#arrays) |
| [GetMemoryUsageMbForTag](#GetMemoryUsageMbForTag)(tag: [Enum.DeveloperMemoryTag](/docs/reference/engine/enums/DeveloperMemoryTag)):[number](/docs/luau/numbers) |
| [GetTotalMemoryUsageMb](#GetTotalMemoryUsageMb)():[number](/docs/luau/numbers) |
| [ResetHarmonyMemoryTarget](#ResetHarmonyMemoryTarget)():() |
| [SetHarmonyMemoryTarget](#SetHarmonyMemoryTarget)(targetMB: [number](/docs/luau/numbers)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[Stats](/docs/reference/engine/classes/Stats) is a service that provides real-time performance information
about the current running game instance. Its primary purpose is to provide an
end point to measure where resources are being consumed, as well as how much
memory is being consumed overall.

The service also stores a tree of [StatsItem](/docs/reference/engine/classes/StatsItem) objects which can have
their values read by plugins.

---

API Reference

Properties

ContactsCount

Read Only

Not Replicated

Read Parallel

A measurement of how many parts are currently in contact with one another.

Stats.ContactsCount:[number](/docs/luau/numbers)

This property describes how many parts are currently in contact with each
other, such that one of the two parts are being physically simulated, and
thus can be recognized by the [BasePart:GetTouchingParts()](/docs/reference/engine/classes/BasePart#GetTouchingParts) method.

Provide feedback

---

DataReceiveKbps

Read Only

Not Replicated

Read Parallel

In a networked game, this describes roughly how many kilobytes of data are
being received by the current instance, per second.

Stats.DataReceiveKbps:[number](/docs/luau/numbers)

In a networked game, this property describes roughly how many kilobytes of
data are being received by the current instance, per second. If from the
server's perspective, this represents the total amount of data being
received from the clients connected to the server. If from a client's
perspective, this represents the total amount of data being received from
the server.

Provide feedback

---

DataSendKbps

Read Only

Not Replicated

Read Parallel

In a networked game, this describes roughly how many kilobytes of data are
being sent by the current instance, per second.

Stats.DataSendKbps:[number](/docs/luau/numbers)

In a networked game, this property describes roughly how many kilobytes of
data are being sent by the current instance, per second. If from the
server's perspective, this represents the total amount of data being sent
to the clients connected to the server. If from a client's perspective,
this represents the total amount of data being sent to the server.

Provide feedback

---

FrameTime

Read Only

Not Replicated

Read Parallel

A measurement of how long it takes for the engine to process all tasks
required to render a frame.

Stats.FrameTime:[number](/docs/luau/numbers)

This property is only available in client scripts and is a measurement of
how long it took to render the most-recent frame in seconds. Divide 1 by
this value to calculate an FPS value for the frame time. High frame times
are indicative of performance problems on the device. Consider using the
[MicroProfiler](/docs/studio/microprofiler) to troubleshoot.

Provide feedback

---

HeartbeatTime

Read Only

Not Replicated

Read Parallel

A measurement of the total amount of time it takes for the server to
update its task scheduler jobs in seconds.

Stats.HeartbeatTime:[number](/docs/luau/numbers)

This property is a measurement of the total amount of time it takes for
the server to update its task scheduler jobs in seconds. If this value is
high, examine
[server compute](/docs/performance-optimization/identifying#server-compute).

Provide feedback

---

HeartbeatTimeMs

Deprecated

Show details

---

InstanceCount

Read Only

Not Replicated

Read Parallel

A measurement of how many [Instance](/docs/reference/engine/classes/Instance) are currently in memory.

Stats.InstanceCount:[number](/docs/luau/numbers)

InstanceCount is a read-only measurement of how many [Instance](/docs/reference/engine/classes/Instance)
are currently in memory. This includes the [DataModel](/docs/reference/engine/classes/DataModel), its
descendants, as well as any object created with [Instance.new()](/docs/reference/engine/datatypes/Instance#new)
which is still present in memory.

Provide feedback

---

MemoryTrackingEnabled

Read Only

Not Replicated

Read Parallel

An indication of whether memory tracking is enabled. This is guaranteed to
be unchanged until the next time the Client is started.

Stats.MemoryTrackingEnabled:[boolean](/docs/luau/booleans)

If MemoryTrackingEnabled returns false, any API that returns
category-based memory usage such as [Stats:GetMemoryUsageMbForTag()](/docs/reference/engine/classes/Stats#GetMemoryUsageMbForTag)
or [Stats:GetMemoryUsageMbAllCategories()](/docs/reference/engine/classes/Stats#GetMemoryUsageMbAllCategories) will return 0 and emit
a warning. Therefore, usage of category-based memory usage API should be
conditional on MemoryTrackingEnabled returning true. The value of
MemoryTrackingEnabled will not change from one experience to the next;
it will only potentially change after restarting the Roblox client
application.

Provide feedback

---

MovingPrimitivesCount

Read Only

Not Replicated

Read Parallel

A measurement of how many physically simulated components are currently
moving in the game world.

Stats.MovingPrimitivesCount:[number](/docs/luau/numbers)

A measurement of how many physically simulated components are currently
moving in the game world.

Provide feedback

---

PhysicsReceiveKbps

Read Only

Not Replicated

Read Parallel

In a networked game, this describes roughly how many kilobytes of physics
data are being received by the current instance, per second.

Stats.PhysicsReceiveKbps:[number](/docs/luau/numbers)

PhysicsReceiveKbps is a measurement of roughly how many kilobytes of
physics data are being received by the current instance, per second.If
from the server's perspective, this represents the total amount of physics
data being received from the clients connected to the server.If from a
client's perspective, this represents the total amount of physics data
being received from the server.

Provide feedback

---

PhysicsSendKbps

Read Only

Not Replicated

Read Parallel

In a networked game, this describes roughly how many kilobytes of physics
data are being sent by the current instance, per second.

Stats.PhysicsSendKbps:[number](/docs/luau/numbers)

PhysicsSendKbps describes roughly how many kilobytes of physics data are
being sent by the current instance, per second. If from the server's
perspective, this represents the total amount of physics data being sent
to the clients connected to the server. If from a client's perspective,
this represents the total amount of physics data being sent to the server.

Provide feedback

---

PhysicsStepTime

Read Only

Not Replicated

Read Parallel

A measurement of how long it takes for the physics engine to update its
current state.

Stats.PhysicsStepTime:[number](/docs/luau/numbers)

This property is a measurement of how long it takes for the physics engine
to update its current state. If this value is high, it means the game
instance is under stress from the physics simulations taking place.

Provide feedback

---

PhysicsStepTimeMs

Deprecated

Show details

---

PrimitivesCount

Read Only

Not Replicated

Read Parallel

A measurement of how many physically simulated components currently exist
in the game world.

Stats.PrimitivesCount:[number](/docs/luau/numbers)

A measurement of how many physically simulated components currently exist
in the game world.

Provide feedback

---

RenderCPUFrameTime

Read Only

Not Replicated

Read Parallel

A measurement of how long it takes for the CPU to process all of its
rendering tasks for a frame.

Stats.RenderCPUFrameTime:[number](/docs/luau/numbers)

This property is a measurement of how long it takes for the CPU to process
all of its rendering tasks for a frame.

Provide feedback

---

RenderGPUFrameTime

Read Only

Not Replicated

Read Parallel

A measurement of how long it takes for the GPU to process all of its tasks
required to render a frame.

Stats.RenderGPUFrameTime:[number](/docs/luau/numbers)

This property is a measurement of how long it takes for the GPU to process
all of its tasks required to render a frame.

Provide feedback

---

SceneDrawcallCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of draw calls made by the game's current
scene.

Stats.SceneDrawcallCount:[number](/docs/luau/numbers)

This property is a measurement of the number of draw calls made by the
game's current scene. A draw call is a single rendering operation, such as
drawing a mesh. A high draw call count could mean a scene is too complex
or unoptimized, which can lead to performance issues.

Provide feedback

---

SceneTriangleCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of triangles rendered by the game's current
scene.

Stats.SceneTriangleCount:[number](/docs/luau/numbers)

This property is a measurement of the number of triangles rendered by the
game's current scene. A count of triangles rendered is useful when trying
to estimate the complexity and performance of a scene.

Provide feedback

---

ShadowsDrawcallCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of draw calls being made for shadows by the
game's current scene.

Stats.ShadowsDrawcallCount:[number](/docs/luau/numbers)

This property is a measurement of the number of draw calls being made for
shadows by the game's current scene. A high count means more shadows are
being created by the amount of rendered objects in a scene.

Provide feedback

---

ShadowsTriangleCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of triangles rendered as shadows in the game's
current scene.

Stats.ShadowsTriangleCount:[number](/docs/luau/numbers)

This property is a measurement of the number of triangles rendered as
shadows in the game's current scene. A high count means there are a lot of
triangles used to cast shadows, which can hinder performance.

Provide feedback

---

UI2DDrawcallCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of 2D draw calls made for UI elements in the
game's current scene.

Stats.UI2DDrawcallCount:[number](/docs/luau/numbers)

This property is a measurement of the number of 2D draw calls made for UI
elements in the game's current scene. A high count can mean there are a
lot of 2D UI elements being used.

Provide feedback

---

UI2DTriangleCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of triangles that are being rendered for 2D UI
elements in the game's current scene.

Stats.UI2DTriangleCount:[number](/docs/luau/numbers)

This property is a measurement of the number of triangles that are being
rendered for 2D UI elements in the game's current scene. A high count can
mean there are many or complex 2D UI elements used, which can contribute
to performance loss in regards to rendering.

Provide feedback

---

UI3DDrawcallCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of 3D draw calls made for UI elements in the
game's current scene.

Stats.UI3DDrawcallCount:[number](/docs/luau/numbers)

This property is a measurement of the number of 3D draw calls made for UI
elements in the game's current scene. A high count could indicate a high
amount of 3D objects being used within UI, potentially hurting
performance; however, it is very unlikely you would see a significant
count since UI elements are typically 2D.

Provide feedback

---

UI3DTriangleCount

Read Only

Not Replicated

Read Parallel

A measurement of the number of triangles being rendered for 3D UI elements
in the game's current scene.

Stats.UI3DTriangleCount:[number](/docs/luau/numbers)

This property is a measurement of the number of triangles being rendered
for 3D UI elements in the game's current scene; however, it is very
unlikely you would see a significant count since UI elements are typically
2D.

Provide feedback

---

Methods

GetHarmonyQualityLevel

Stats:GetHarmonyQualityLevel():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Provide feedback

---

GetMemoryCategoryNames

Stats:GetMemoryCategoryNames():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetMemoryUsageMbAllCategories

Returns the number of megabytes that are being consumed by all available
categories, or an empty array if
[MemoryTrackingEnabled](/docs/reference/engine/classes/Stats#MemoryTrackingEnabled) is false.

Stats:GetMemoryUsageMbAllCategories():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns the number of megabytes that are being consumed by all available
categories. If [MemoryTrackingEnabled](/docs/reference/engine/classes/Stats#MemoryTrackingEnabled)
is false, calling GetMemoryUsageMbAllCategories() will return an empty
array and emit a warning to the console.

Provide feedback

---

GetMemoryUsageMbForTag

Returns the number of megabytes that are being consumed in the specified
[Enum.DeveloperMemoryTag](/docs/reference/engine/enums/DeveloperMemoryTag) category, or 0 if
[MemoryTrackingEnabled](/docs/reference/engine/classes/Stats#MemoryTrackingEnabled) is false.

Stats:GetMemoryUsageMbForTag(tag:[Enum.DeveloperMemoryTag](/docs/reference/engine/enums/DeveloperMemoryTag)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| tag:[Enum.DeveloperMemoryTag](/docs/reference/engine/enums/DeveloperMemoryTag) |

Returns

[number](/docs/luau/numbers)

Returns the number of megabytes that are being consumed in the specified
[Enum.DeveloperMemoryTag](/docs/reference/engine/enums/DeveloperMemoryTag) category. If
[MemoryTrackingEnabled](/docs/reference/engine/classes/Stats#MemoryTrackingEnabled) is false,
calling GetMemoryUsageMbForTag() will return 0 and emit a warning to
the console.

Provide feedback

---

GetTotalMemoryUsageMb

Returns the total amount of memory being consumed by the current game
session, in megabytes.

Stats:GetTotalMemoryUsageMb():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the total amount of memory being consumed by the current game
session, in megabytes.

This method gets memory usage from the operating system, which may exclude
memory that has been paged out to disk. As such, the return value tends to
differ significantly from the sum of usage for all
[DeveloperMemoryTags](/docs/reference/engine/enums/DeveloperMemoryTag). The return value should be
very similar to memory usage for Roblox in the Windows Task Manager or
macOS Activity Monitor.

Provide feedback

---

ResetHarmonyMemoryTarget

Stats:ResetHarmonyMemoryTarget():()

Returns

()

Provide feedback

---

SetHarmonyMemoryTarget

Stats:SetHarmonyMemoryTarget(targetMB:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| targetMB:[number](/docs/luau/numbers) |

Returns

()

Provide feedback

---