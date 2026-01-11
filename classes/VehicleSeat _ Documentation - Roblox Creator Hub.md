# VehicleSeat | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VehicleSeat
Scraped: 2026-01-11T02:29:17.214284Z

## Tags
- Not Replicated

## Inherits
- BasePart
- VehicleSeat
- Humanoid
- PVInstance
- Instance
- Object
- VehicleSeat.Steer
- VehicleSeat.Throttle
- VehicleSeat.MaxSpeed
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BasePart](/docs/reference/engine/classes/BasePart)
6. /
7. [VehicleSeat](/docs/reference/engine/classes/VehicleSeat)

English

Feedback

Engine Class

![VehicleSeat](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/VehicleSeat-Dark.webp)VehicleSeat

A seat object that can be used to control a vehicle.

---

Summary

Properties

|  |
| --- |
| [AreHingesDetected](#AreHingesDetected):[number](/docs/luau/numbers) |
| [Disabled](#Disabled):[boolean](/docs/luau/booleans) |
| [HeadsUpDisplay](#HeadsUpDisplay):[boolean](/docs/luau/booleans) |
| [MaxSpeed](#MaxSpeed):[number](/docs/luau/numbers) |
| [Occupant](#Occupant):[Humanoid](/docs/reference/engine/classes/Humanoid) |
| [Steer](#Steer):[number](/docs/luau/numbers)  Deprecated |
| [SteerFloat](#SteerFloat):[number](/docs/luau/numbers) |
| [Throttle](#Throttle):[number](/docs/luau/numbers)  Deprecated |
| [ThrottleFloat](#ThrottleFloat):[number](/docs/luau/numbers) |
| [Torque](#Torque):[number](/docs/luau/numbers) |
| [TurnSpeed](#TurnSpeed):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Sit](#Sit)(humanoid: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The VehicleSeat objects welds a player to the seat when the player touches the
seat. It then forwards the movement keys to any connected motor joints,
allowing control of a vehicle.

While VehicleSeats are great for making simple vehicles they do have some
limitations. Movement control will only detect motors connected directly to
the vehicle seat, or through another rigid connection. This means that if you
have a wheel connected to a beam which is then welded to the seat it will work
fine, however if you have the wheel connected to a part, which is connected by
a hinge to the rest of the car, it will not work.

---

API Reference

Properties

AreHingesDetected

Read Only

Not Replicated

Read Parallel

Displays how many hinges are detected by the VehicleSeat. Useful for
debugging vehicle designs.

VehicleSeat.AreHingesDetected:[number](/docs/luau/numbers)

Displays how many hinges are detected by the VehicleSeat. Useful for
debugging vehicle designs.

Provide feedback

---

Disabled

Read Parallel

Toggles whether the [VehicleSeat](/docs/reference/engine/classes/VehicleSeat) is active or not.

VehicleSeat.Disabled:[boolean](/docs/luau/booleans)

Toggles whether the [VehicleSeat](/docs/reference/engine/classes/VehicleSeat) is active or not. If the seat is
disabled then it will not automatically weld a character to it on
collision and will not allow a character to control the connected vehicle.

Provide feedback

---

HeadsUpDisplay

Read Parallel

If true, a fancy speed bar will be displayed speed on screen that tells
you what speed the Vehicle is moving at.

VehicleSeat.HeadsUpDisplay:[boolean](/docs/luau/booleans)

If true, a fancy speed bar will be displayed speed on screen that tells
you what speed the Vehicle is moving at.

Provide feedback

---

MaxSpeed

Read Parallel

The maximum speed that can be attained.

VehicleSeat.MaxSpeed:[number](/docs/luau/numbers)

The maximum speed that can be attained.

Provide feedback

---

Occupant

Read Only

Not Replicated

Read Parallel

The humanoid that is sitting in the seat.

VehicleSeat.Occupant:[Humanoid](/docs/reference/engine/classes/Humanoid)

The humanoid that is sitting in the seat

Provide feedback

---

Steer

Deprecated

Show details

---

SteerFloat

Read Parallel

Functions identically to [VehicleSeat.Steer](/docs/reference/engine/classes/VehicleSeat#Steer), but the value is not
an integer.

VehicleSeat.SteerFloat:[number](/docs/luau/numbers)

Functions identically to [VehicleSeat.Steer](/docs/reference/engine/classes/VehicleSeat#Steer), but the value is not
an integer.

Provide feedback

---

Throttle

Deprecated

Show details

---

ThrottleFloat

Read Parallel

Functions identically to [VehicleSeat.Throttle](/docs/reference/engine/classes/VehicleSeat#Throttle), but the value is
not an integer.

VehicleSeat.ThrottleFloat:[number](/docs/luau/numbers)

Functions identically to [VehicleSeat.Throttle](/docs/reference/engine/classes/VehicleSeat#Throttle), but the value is
not an integer.

Provide feedback

---

Torque

Read Parallel

How fast the vehicles will be able to attain [VehicleSeat.MaxSpeed](/docs/reference/engine/classes/VehicleSeat#MaxSpeed).
The greater the number, the faster it will reach the maximum speed.

VehicleSeat.Torque:[number](/docs/luau/numbers)

How fast the vehicles will be able to attain [VehicleSeat.MaxSpeed](/docs/reference/engine/classes/VehicleSeat#MaxSpeed).
The greater the number, the faster it will reach the maximum speed.

Provide feedback

---

TurnSpeed

Read Parallel

The speed at which the vehicle will turn. Higher numbers can cause
problems and are not necessarily better.

VehicleSeat.TurnSpeed:[number](/docs/luau/numbers)

The speed at which the vehicle will turn. Higher numbers can cause
problems and are not necessarily better.

Provide feedback

---

Methods

Sit

Forces the character with the specified [Humanoid](/docs/reference/engine/classes/Humanoid) to sit in the
VehicleSeat.

VehicleSeat:Sit(humanoid:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| humanoid:[Instance](/docs/reference/engine/datatypes/Instance)  The humanoid being forced to sit in the VehicleSeat. |

Returns

()

Forces the character with the specified [Humanoid](/docs/reference/engine/classes/Humanoid) to sit in the
VehicleSeat.

Provide feedback

---