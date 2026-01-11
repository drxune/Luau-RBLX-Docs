# AudioDeviceInput | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioDeviceInput
Scraped: 2026-01-11T02:38:13.581126Z

## Tags
- Not Replicated

## Inherits
- Instance
- AudioDeviceInput
- Player
- Wire
- Object
- Wires
- SetUserIdAccessList
- AccessType
- Active
- Muted
- Players.LocalPlayer
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput)

English

Feedback

Engine Class

![AudioDeviceInput](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioDeviceInput-Dark.webp)AudioDeviceInput

Produces audio streams from physical devices, such as microphones.

---

Summary

Properties

|  |
| --- |
| [AccessType](#AccessType):[Enum.AccessModifierType](/docs/reference/engine/enums/AccessModifierType) |
| [Active](#Active):[boolean](/docs/luau/booleans) |
| [IsReady](#IsReady):[boolean](/docs/luau/booleans) |
| [Muted](#Muted):[boolean](/docs/luau/booleans) |
| [MutedByLocalUser](#MutedByLocalUser):[boolean](/docs/luau/booleans) |
| [Player](#Player):[Player](/docs/reference/engine/classes/Player) |
| [Volume](#Volume):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |
| [GetUserIdAccessList](#GetUserIdAccessList)():[Array](/docs/luau/tables#arrays) |
| [SetUserIdAccessList](#SetUserIdAccessList)(userIds: [Array](/docs/luau/tables#arrays)):() |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) produces audio streams from physical devices, such as
microphones. It provides a single Output pin which can be connected to
other pins via [Wires](/docs/reference/engine/classes/Wire). [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) has properties for
selecting which [Player](/docs/reference/engine/classes/Player) is producing the stream, and controlling
whether or not they are muted.

---

API Reference

Properties

AccessType

Read Parallel

Determines whether the list of user IDs provided to
[SetUserIdAccessList](/docs/reference/engine/classes/AudioDeviceInput#SetUserIdAccessList) is
treated as an allow-list or deny-list.

AudioDeviceInput.AccessType:[Enum.AccessModifierType](/docs/reference/engine/enums/AccessModifierType)

Determines whether the list of user IDs provided to
[SetUserIdAccessList](/docs/reference/engine/classes/AudioDeviceInput#SetUserIdAccessList) is
treated as an allow-list or deny-list.

If [AccessType](/docs/reference/engine/classes/AudioDeviceInput#AccessType) is
[Enum.AccessModifierType.Allow](/docs/reference/engine/enums/AccessModifierType#Allow), then only the supplied user IDs are
permitted to hear this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput). If
[AccessType](/docs/reference/engine/classes/AudioDeviceInput#AccessType) is
[Enum.AccessModifierType.Deny](/docs/reference/engine/enums/AccessModifierType#Deny), then only the supplied user IDs are
blocked from hearing this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput).

Since player voices are networked, this property should only be assigned
from the server in order to replicate properly.

Provide feedback

---

Active

Roblox Script Security

Read Parallel

Controls whether the physical device is actively recording.

AudioDeviceInput.Active:[boolean](/docs/luau/booleans)

Controls whether the physical device is actively recording. This property
is only set by Roblox core scripts, but it may be read by user scripts.
Generally, an [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) may only be producing sound if
[Active](/docs/reference/engine/classes/AudioDeviceInput#Active) is true and
[Muted](/docs/reference/engine/classes/AudioDeviceInput#Muted) is false.

Provide feedback

---

IsReady

Read Only

Not Replicated

Roblox Script Security

Read Parallel

Denotes whether this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) is ready to produce sound.

AudioDeviceInput.IsReady:[boolean](/docs/luau/booleans)

Denotes whether this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) is ready to produce sound,
meaning all network connections have been established.

Provide feedback

---

Muted

Read Parallel

Controls whether this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) is muted.

AudioDeviceInput.Muted:[boolean](/docs/luau/booleans)

Controls whether this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) is muted. Unlike
[Active](/docs/reference/engine/classes/AudioDeviceInput#Active), this property is publicly
scriptable.

Generally, an [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) may only be heard if
[Active](/docs/reference/engine/classes/AudioDeviceInput#Active) is true and
[Muted](/docs/reference/engine/classes/AudioDeviceInput#Muted) is false.

Code Samples

Push-to-talk

```
local players = game:GetService("Players")



local userInput = game:GetService("UserInputService")



local audioIn: AudioDeviceInput = players.LocalPlayer:WaitForChild("AudioDeviceInput")



audioIn.Muted = true



local pushToTalkKey = Enum.KeyCode.V



userInput.InputBegan:Connect(function(input: InputObject)



if input.KeyCode == pushToTalkKey then



audioIn.Muted = false



end



end)



userInput.InputEnded:Connect(function(input: InputObject)



if input.KeyCode == pushToTalkKey then



audioIn.Muted = true



end



end)
```

Provide feedback

---

MutedByLocalUser

Not Replicated

Roblox Script Security

Read Parallel

AudioDeviceInput.MutedByLocalUser:[boolean](/docs/luau/booleans)

Provide feedback

---

Player

Read Parallel

Determines whose device is producing sound.

AudioDeviceInput.Player:[Player](/docs/reference/engine/classes/Player)

Determines whose device is producing sound. In order to replicate
properly, this should only be assigned from the server. Assigning this
property locally generally does not work, unless
[Player](/docs/reference/engine/classes/AudioDeviceInput#Player) is [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer).

Provide feedback

---

Volume

Read Parallel

Volume level which is multiplied onto the output audio stream.

AudioDeviceInput.Volume:[number](/docs/luau/numbers)

Volume level which is multiplied onto the output audio stream. Ranges from
0 to 3.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioDeviceInput:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) has one "Output" pin.

Provide feedback

---

GetInputPins

AudioDeviceInput:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioDeviceInput:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetUserIdAccessList

Returns a list of user IDs that are either permitted to hear or blocked
from hearing this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput).

AudioDeviceInput:GetUserIdAccessList():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns a list of user IDs that are either permitted to hear or blocked
from hearing this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput), depending on the
[AccessType](/docs/reference/engine/classes/AudioDeviceInput#AccessType).

Provide feedback

---

SetUserIdAccessList

Sets a list of user IDs that are either permitted to hear or blocked from
hearing this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput).

AudioDeviceInput:SetUserIdAccessList(userIds:[Array](/docs/luau/tables#arrays)):()

Parameters

|  |
| --- |
| userIds:[Array](/docs/luau/tables#arrays) |

Returns

()

Sets a list of user IDs that are either permitted to hear or blocked from
hearing this [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput), depending on the
[AccessType](/docs/reference/engine/classes/AudioDeviceInput#AccessType).

Note that this method replicates from server to client; in general, it
should only be called from the server in order to replicate properly.

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) via a [Wire](/docs/reference/engine/classes/Wire).

AudioDeviceInput.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioDeviceInput](/docs/reference/engine/classes/AudioDeviceInput) and to some other wirable instance.

Provide feedback

---