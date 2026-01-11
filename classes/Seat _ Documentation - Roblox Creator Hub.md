# Seat | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Seat
Scraped: 2026-01-11T02:33:40.852611Z

## Tags
- Not Replicated

## Inherits
- Part
- Seat
- BasePart
- Weld
- Humanoid
- FormFactorPart
- PVInstance
- Instance
- Object
- C0
- C1
- Seat.Occupant
- Humanoid.SeatPart
- Seat:Sit()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Part](/docs/reference/engine/classes/Part)
6. /
7. [Seat](/docs/reference/engine/classes/Seat)

English

Feedback

Engine Class

![Seat](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Seat-Dark.webp)Seat

A type of [BasePart](/docs/reference/engine/classes/BasePart) that characters can 'sit' in. When a character
touches an enabled Seat object, it will be attached to the part by a
[Weld](/docs/reference/engine/classes/Weld) and the default character scripts will play a sitting animation.

---

Summary

Properties

|  |
| --- |
| [Disabled](#Disabled):[boolean](/docs/luau/booleans) |
| [Occupant](#Occupant):[Humanoid](/docs/reference/engine/classes/Humanoid) |

Methods

|  |
| --- |
| [Sit](#Sit)(humanoid: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

1 inherited from [Part](/docs/reference/engine/classes/Part)

2 inherited from [FormFactorPart](/docs/reference/engine/classes/FormFactorPart)

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A type of [BasePart](/docs/reference/engine/classes/BasePart) that a player character can 'sit' in. When a
character touches an enabled Seat object, it will be attached to the part by a
[Weld](/docs/reference/engine/classes/Weld) and the default character scripts will play a sitting animation.

How do Seats work?
------------------

When a model containing a [Humanoid](/docs/reference/engine/classes/Humanoid) and a [BasePart](/docs/reference/engine/classes/BasePart) called
'HumanoidRootPart' (generally a player character) touches a seat, a
[Weld](/docs/reference/engine/classes/Weld) is created between the seat and the part. The
[C0](/docs/reference/engine/classes/JointInstance#C0) and [C1](/docs/reference/engine/classes/JointInstance#C1) properties are
configured so that the character is welded 2 studs above the seat. This weld
is named 'SeatWeld' and parented to the seat.

When sitting the [Seat.Occupant](/docs/reference/engine/classes/Seat#Occupant) property is set to the [Humanoid](/docs/reference/engine/classes/Humanoid)
that is 'sitting' in the seat. Furthermore the [Humanoid.SeatPart](/docs/reference/engine/classes/Humanoid#SeatPart)
property of the humanoid is set to the seat.

A character can also be forced to sit in a seat using the [Seat:Sit()](/docs/reference/engine/classes/Seat#Sit)
function.

There are two ways for a character to get out of a seat. When a player jumps,
they are removed from the seat. However this can also be done manually by
destroying the seat weld, for example:

```
seat:FindFirstChild("SeatWeld"):Destroy()
```

Note seats have a cooldown (currently 3 seconds) that is on a per-character
per-seat basis. This means once a character has gotten out of a seat they
cannot sit back on the same seat for 3 seconds. This cooldown behavior may
change and should not be relied upon by developers.

What can Seats be used for?
---------------------------

Seats have a diverse range of uses, ranging from the obvious to the more
unconventional.

* Creating chairs or benches without the need for any programming
* Allowing characters to 'sit' in moving objects such as vehicles without
  getting flung around
* Creating interfaces that are controlled by the character in the seat using
  the [Seat.Occupant](/docs/reference/engine/classes/Seat#Occupant) property

Code Samples

Detecting Seat Occupant

This code sample includes a demonstration of how the [Seat.Occupant](/docs/reference/engine/classes/Seat#Occupant)
property can be used to track which player is sitting in a seat and when they
sit down or sit up.

```
local Players = game:GetService("Players")



local seat = Instance.new("Seat")



seat.Anchored = true



seat.Position = Vector3.new(0, 1, 0)



seat.Parent = workspace



local currentPlayer = nil



local function onOccupantChanged()



local humanoid = seat.Occupant



if humanoid then



local character = humanoid.Parent



local player = Players:GetPlayerFromCharacter(character)



if player then



print(player.Name .. " has sat down")



currentPlayer = player



return



end



end



if currentPlayer then



print(currentPlayer.Name .. " has got up")



currentPlayer = nil



end



end



seat:GetPropertyChangedSignal("Occupant"):Connect(onOccupantChanged)
```

---

API Reference

Properties

Disabled

Read Parallel

Whether or not the seat is usable. If set to true, the seat will act as a
normal part.

Seat.Disabled:[boolean](/docs/luau/booleans)

Whether or not the seat is usable. If set to true, the seat will act as a
normal part.

Provide feedback

---

Occupant

Read Only

Not Replicated

Read Parallel

The humanoid that is sitting in the seat.

Seat.Occupant:[Humanoid](/docs/reference/engine/classes/Humanoid)

The humanoid that is sitting in the seat

Provide feedback

---

Methods

Sit

Forces the character with the specified [Humanoid](/docs/reference/engine/classes/Humanoid) to sit in the
Seat.

Seat:Sit(humanoid:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| humanoid:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

Forces the character with the specified [Humanoid](/docs/reference/engine/classes/Humanoid) to sit in the
Seat.

Provide feedback

---