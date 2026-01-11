# NetworkSettings | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NetworkSettings
Scraped: 2026-01-11T02:40:02.340316Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- NetworkSettings
- Object
- Instance:GetDebugId()
- Workspace.StreamingEnabled
- Player.ReplicationFocus
- Humanoid
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [NetworkSettings](/docs/reference/engine/classes/NetworkSettings)

English

Feedback

Engine Class

NetworkSettings

Settings related to networked engine behaviors.

Not Creatable

Service

Not Replicated

Not Browsable

---

Summary

Properties

|  |
| --- |
| [EmulatedTotalMemoryInMB](#EmulatedTotalMemoryInMB):[number](/docs/luau/numbers) |
| [FreeMemoryMBytes](#FreeMemoryMBytes):[number](/docs/luau/numbers) |
| [HttpProxyEnabled](#HttpProxyEnabled):[boolean](/docs/luau/booleans) |
| [HttpProxyURL](#HttpProxyURL):[string](/docs/luau/strings) |
| [IncomingReplicationLag](#IncomingReplicationLag):[number](/docs/luau/numbers) |
| [PrintJoinSizeBreakdown](#PrintJoinSizeBreakdown):[boolean](/docs/luau/booleans) |
| [PrintPhysicsErrors](#PrintPhysicsErrors):[boolean](/docs/luau/booleans) |
| [PrintStreamInstanceQuota](#PrintStreamInstanceQuota):[boolean](/docs/luau/booleans) |
| [RandomizeJoinInstanceOrder](#RandomizeJoinInstanceOrder):[boolean](/docs/luau/booleans) |
| [RenderStreamedRegions](#RenderStreamedRegions):[boolean](/docs/luau/booleans) |
| [ShowActiveAnimationAsset](#ShowActiveAnimationAsset):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

NetworkSettings is a settings class that allow you to debug a lot of features
with Roblox's server/client networking. It can be found in Roblox Studio's
settings, under the Network tab.

---

API Reference

Properties

EmulatedTotalMemoryInMB

Hidden

Not Replicated

Plugin Security

Read Parallel

NetworkSettings.EmulatedTotalMemoryInMB:[number](/docs/luau/numbers)

Provide feedback

---

FreeMemoryMBytes

Hidden

Read Only

Not Replicated

Plugin Security

Read Parallel

Describes how much free memory is available, in MBs.

NetworkSettings.FreeMemoryMBytes:[number](/docs/luau/numbers)

FreeMemoryMBytes is a read-only property that describes how much free
memory is available, in MBs. It is stored as a floating point number, so
it can be read down at the level of available bytes by multiplying its
value by 1024 \* 1024.

Provide feedback

---

HttpProxyEnabled

Roblox Script Security

Read Parallel

NetworkSettings.HttpProxyEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

HttpProxyURL

Roblox Script Security

Read Parallel

NetworkSettings.HttpProxyURL:[string](/docs/luau/strings)

Provide feedback

---

IncomingReplicationLag

Read Parallel

Simulate additional network latency in the network receiving path.

NetworkSettings.IncomingReplicationLag:[number](/docs/luau/numbers)

Instruct the engine to simulate additional lag by delaying all incoming
messages. Units are seconds.

Provide feedback

---

PrintJoinSizeBreakdown

Read Parallel

Print diagnostic information about data sent on connect.

NetworkSettings.PrintJoinSizeBreakdown:[boolean](/docs/luau/booleans)

Print diagnostic information to the Output window after connecting. The
data will indicate the largest individual Instances sent, as well as
aggregate data about data sent by Instance type. The data sent for initial
loading is compressed so the contributions are approximate.

Provide feedback

---

PrintPhysicsErrors

Read Parallel

When set to true, debug messages will be printed into the output
pertaining to physics replication errors.

NetworkSettings.PrintPhysicsErrors:[boolean](/docs/luau/booleans)

When set to true, debug messages will be printed into the output,
pertaining to physics replication errors. Note that this property is
intended for Roblox engineers who are debugging network replication. The
following are debug outputs that are made available when this property is
set to true.

* Physics-in old packet prints if the PhysicsReceiver receives a
  mechanism update packet for a part that has been updated ahead of the
  packet's submission time. This happens if the packet is received late,
  and a newer packet has already been processed.
* Physics-in of unidentified {GUID} prints if the PhysicsReceiver cannot
  find the part that is trying to be updated because the provided Instance
  identifier was invalid, where {GUID} is the unknown
  [Instance:GetDebugId()](/docs/reference/engine/classes/Instance#GetDebugId) identifier that is supposed to be
  targeting the part. This typically happens if a part is removed before
  the physics update packet is received.
* Physics-in of part not in workspace {GUID} prints if the
  PhysicsReceiver receives a request to update the physics of a part that
  is not a descendant of the Workspace, where {GUID} is the
  [Instance:GetDebugId()](/docs/reference/engine/classes/Instance#GetDebugId) identifier of the target part. This
  happens if the part was just moved out of the Workspace, and was
  previously being simulated.

Provide feedback

---

PrintStreamInstanceQuota

Read Parallel

When set to true, debug information is printed to the output regarding the
replication of instances when [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) is set to
true.

NetworkSettings.PrintStreamInstanceQuota:[boolean](/docs/luau/booleans)

When set to true, debug information is printed to the output regarding the
replication of instances when [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) is set to
true. There are several debug outputs that are made available when this
property is set to true, as listed below.

Note that this property is intended for Roblox engineers who are debugging
network replication. This documentation may become outdated in the future,
as Roblox's network code is always changing behind the scenes.

#### Streaming Capacity Update

When the client's streaming capacity is updated, the following debug
message will be printed:
clientInstanceQuota {1}, packet in queue {2}, predictedTotalInstanceProcessTime {3}, avgStreamDataReadTime {4}, avgInstancesPerStreamData {5}

The numbers in curly braces are substituted, and can be described as:

* {1} – The ID of the client instance quota.
* {2} – The current number of incoming packets that have been queued.
* {3} – A prediction for how long it will take to update the quota.
* {4} – The current average time it takes to read the stream data.
* {5} – The average number of instances in the stream data.

#### Instance Quota Update

When the client receives an instance quota update, the following debug
message will be printed:
Received new client instance quota: {1}, max region radius: {2}

The numbers in curly braces are substituted, and can be described as:

* {1} – The ID of the client instance quota.
* {2} – The maximum radius of space around the client's
  [Player.ReplicationFocus](/docs/reference/engine/classes/Player#ReplicationFocus) that can have physical instances
  streamed in.

Provide feedback

---

RandomizeJoinInstanceOrder

Read Parallel

Special facility to help catch bugs related to how your experience loads.

NetworkSettings.RandomizeJoinInstanceOrder:[boolean](/docs/luau/booleans)

Emulate the behavior of a server that has been online a long time by
randomizing the order that instances initially arrive on clients. It is
recommended to keep this setting enabled to help discover potential bugs
while testing in Studio.

Provide feedback

---

RenderStreamedRegions

Read Parallel

When set to true, regions of space that are being streamed to the client
will be outlined in red.

NetworkSettings.RenderStreamedRegions:[boolean](/docs/luau/booleans)

When set to true, regions of space that are being streamed to the client
will be outlined in red. This will only be shown if
[Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) is set to true.

Provide feedback

---

ShowActiveAnimationAsset

Read Parallel

When set to true, a label will be shown above each player's head, showing
the current animation being played by the Player's [Humanoid](/docs/reference/engine/classes/Humanoid), if
any.

NetworkSettings.ShowActiveAnimationAsset:[boolean](/docs/luau/booleans)

When set to true, a label will be shown above each player's head, showing
the current animation being played by the Player's [Humanoid](/docs/reference/engine/classes/Humanoid), if
any.

Provide feedback

---