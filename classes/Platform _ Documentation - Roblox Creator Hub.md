# Platform | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Platform
Scraped: 2026-01-11T02:27:16.203299Z

## Tags
- Not Creatable

## Inherits
- Part
- Platform
- Seat
- FormFactorPart
- BasePart
- PVInstance
- Instance
- Object
- Player
- Weld
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Part](/docs/reference/engine/classes/Part)
6. /
7. [Platform](/docs/reference/engine/classes/Platform)

English

Feedback

Engine Class

Platform

Deprecated

Historically a form of [Seat](/docs/reference/engine/classes/Seat) that wouldn't place the player in a
sitting pose. This object is no longer create-able and cannot be used by
developers.

Not Creatable

Historically a form of [Seat](/docs/reference/engine/classes/Seat) that wouldn't place the player in a
sitting pose. This object is no longer create-able and cannot be used by
developers.

---

Summary

Inherited Members

1 inherited from [Part](/docs/reference/engine/classes/Part)

2 inherited from [FormFactorPart](/docs/reference/engine/classes/FormFactorPart)

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Platform object creates a brick that when touched by a [Player](/docs/reference/engine/classes/Player) will
anchor their torso to the brick. This allows for the creation of vehicles that
players can stand in and not be flung about the cabin/deck of the vehicle.

The Platform is almost identical to the [Seat](/docs/reference/engine/classes/Seat) object, except that
instead of sitting down the player will be standing while locked in place.
Good for ships.

The Platform object is very useful for making people's characters staying in
one spot while they move around, such as a ship or truck. When a player
touches the Platform a [Weld](/docs/reference/engine/classes/Weld) constraint is created, so they are
'attached' to the Platform and can't move until that weld is broken. It can be
removed by hitting the spacebar, when the player jumps to exit the Platform.