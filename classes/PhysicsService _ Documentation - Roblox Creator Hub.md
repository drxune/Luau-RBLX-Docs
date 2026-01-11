# PhysicsService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PhysicsService
Scraped: 2026-01-11T02:34:26.366887Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- PhysicsService
- BasePart
- RegisterCollisionGroup()
- CollisionGroup
- Scripts
- PhysicsService:IsCollisionGroupRegistered()
- PhysicsService:CollisionGroupSetCollidable()
- BaseParts
- UnregisterCollisionGroup()
- RenameCollisionGroup()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PhysicsService](/docs/reference/engine/classes/PhysicsService)

English

Feedback

Engine Class

PhysicsService

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [CollisionGroupContainsPart](#CollisionGroupContainsPart)(name: [string](/docs/luau/strings),part: [BasePart](/docs/reference/engine/classes/BasePart)):[boolean](/docs/luau/booleans)  Deprecated |
| [CollisionGroupsAreCollidable](#CollisionGroupsAreCollidable)(name1: [string](/docs/luau/strings),name2: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [CollisionGroupSetCollidable](#CollisionGroupSetCollidable)(name1: [string](/docs/luau/strings),name2: [string](/docs/luau/strings),collidable: [boolean](/docs/luau/booleans)):() |
| [CreateCollisionGroup](#CreateCollisionGroup)(name: [string](/docs/luau/strings)):[number](/docs/luau/numbers)  Deprecated |
| [GetCollisionGroupId](#GetCollisionGroupId)(name: [string](/docs/luau/strings)):[number](/docs/luau/numbers)  Deprecated |
| [GetCollisionGroupName](#GetCollisionGroupName)(name: [number](/docs/luau/numbers)):[string](/docs/luau/strings)  Deprecated |
| [GetCollisionGroups](#GetCollisionGroups)():[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetMaxCollisionGroups](#GetMaxCollisionGroups)():[number](/docs/luau/numbers) |
| [GetRegisteredCollisionGroups](#GetRegisteredCollisionGroups)():[Array](/docs/luau/tables#arrays) |
| [IsCollisionGroupRegistered](#IsCollisionGroupRegistered)(name: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [RegisterCollisionGroup](#RegisterCollisionGroup)(name: [string](/docs/luau/strings)):() |
| [RemoveCollisionGroup](#RemoveCollisionGroup)(name: [string](/docs/luau/strings)):()  Deprecated |
| [RenameCollisionGroup](#RenameCollisionGroup)(from: [string](/docs/luau/strings),to: [string](/docs/luau/strings)):() |
| [SetPartCollisionGroup](#SetPartCollisionGroup)(part: [BasePart](/docs/reference/engine/classes/BasePart),name: [string](/docs/luau/strings)):()  Deprecated |
| [UnregisterCollisionGroup](#UnregisterCollisionGroup)(name: [string](/docs/luau/strings)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[PhysicsService](/docs/reference/engine/classes/PhysicsService) primarily contains methods for working with collision
groups which define whether a set of parts may or may not collide with parts
in other collision groups. You can register a collision group through
[RegisterCollisionGroup()](/docs/reference/engine/classes/PhysicsService#RegisterCollisionGroup) and
assign parts to it by setting those parts'
[CollisionGroup](/docs/reference/engine/classes/BasePart#CollisionGroup) property to the name of the
collision group.

Creating, deleting, and modifying collision relationships between collision
groups is limited to server-side [Scripts](/docs/reference/engine/classes/Script).

See
[Collision Filtering](/docs/workspace/collisions#collision-filtering)
for usage details in Studio and within scripts.

---

API Reference

Methods

CollisionGroupContainsPart

Deprecated

Show details

---

CollisionGroupsAreCollidable

Returns whether the two groups will collide.

PhysicsService:CollisionGroupsAreCollidable(

name1:[string](/docs/luau/strings), name2:[string](/docs/luau/strings)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| name1:[string](/docs/luau/strings) |
| name2:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

Returns whether the two specified collision groups will collide. This
method will also return true if either of the groups are unregistered, as
the default collision mask collides with all groups.

Provide feedback

---

CollisionGroupSetCollidable

Sets the collision status between two groups.

PhysicsService:CollisionGroupSetCollidable(

name1:[string](/docs/luau/strings), name2:[string](/docs/luau/strings), collidable:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| name1:[string](/docs/luau/strings) |
| name2:[string](/docs/luau/strings) |
| collidable:[boolean](/docs/luau/booleans) |

Returns

()

Sets the collision status between two groups. This method will throw an
error if either of the groups is unregistered, so it's recommended that
you confirm each group's registration through
[PhysicsService:IsCollisionGroupRegistered()](/docs/reference/engine/classes/PhysicsService#IsCollisionGroupRegistered) before making this
call.

Provide feedback

---

CreateCollisionGroup

Deprecated

Show details

---

GetCollisionGroupId

Deprecated

Show details

---

GetCollisionGroupName

Deprecated

Show details

---

GetCollisionGroups

Deprecated

Show details

---

GetMaxCollisionGroups

Returns the maximum number of collision groups.

PhysicsService:GetMaxCollisionGroups():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the maximum number of collision groups the engine supports. This
value is currently 32.

Provide feedback

---

GetRegisteredCollisionGroups

Returns a table with info on all of the place's collision groups.

PhysicsService:GetRegisteredCollisionGroups():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns a table with info on all of the place's collision groups. Each
value in the returned table is itself a table and containing two members:

| Member | Type | Description |
| --- | --- | --- |
| mask | integer | The collision group's mask; only for internal use. |
| name | string | Name of the collision group. |

Provide feedback

---

IsCollisionGroupRegistered

Checks if a collision group is registered.

PhysicsService:IsCollisionGroupRegistered(name:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

Checks if a collision group is registered. It's recommended that you call
this method before calling methods that throw errors for unregistered
collision groups, such as
[PhysicsService:CollisionGroupSetCollidable()](/docs/reference/engine/classes/PhysicsService#CollisionGroupSetCollidable).

Provide feedback

---

RegisterCollisionGroup

Registers a new collision group with the given name.

PhysicsService:RegisterCollisionGroup(name:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

()

Registers a new collision group with the given name. The name cannot be
"Default".

Note that this method has a slight performance overhead based on the
number of [BaseParts](/docs/reference/engine/classes/BasePart) in the workspace, so it's recommended
that you register all collision groups at edit time through the Studio
[editor](/docs/workspace/collisions#collision-groups) and call
[UnregisterCollisionGroup()](/docs/reference/engine/classes/PhysicsService#UnregisterCollisionGroup)
and [RenameCollisionGroup()](/docs/reference/engine/classes/PhysicsService#RenameCollisionGroup)
as infrequently as possible.

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

RemoveCollisionGroup

Deprecated

Show details

---

RenameCollisionGroup

Renames specified collision group.

PhysicsService:RenameCollisionGroup(

from:[string](/docs/luau/strings), to:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| from:[string](/docs/luau/strings) |
| to:[string](/docs/luau/strings) |

Returns

()

Renames the specified registered collision group, but does not rename
the [CollisionGroup](/docs/reference/engine/classes/BasePart#CollisionGroup) property of parts that
utilize the group. The first argument of this method is the name of the
group to rename, the second argument is the new name for the group. If the
specified group does not exist, this method will not do anything. The
naming conventions for the new name follow the same rules as if the group
was being created with
[RegisterCollisionGroup()](/docs/reference/engine/classes/PhysicsService#RegisterCollisionGroup).

This method will throw a runtime error in the following circumstances:

* Invalid or empty name provided for either argument.
* The method is called from a client.

Note that this method has a slight performance overhead based on the
number of [BaseParts](/docs/reference/engine/classes/BasePart) in the workspace, so it's recommended
that you register all collision groups at edit time through the Studio
[editor](/docs/workspace/collisions#collision-groups) and rename
them as infrequently as possible.

Provide feedback

---

SetPartCollisionGroup

Deprecated

Show details

---

UnregisterCollisionGroup

Unregisters the collision group for the given name.

PhysicsService:UnregisterCollisionGroup(name:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

()

Unregisters the collision group for the given name, with the following
behaviors:

* If an invalid name is provided, the method will not do anything.
* If the reserved name "Default" is provided or if the method is
  called from a client, it will throw an error.
* If there are any parts in the collision group when it is removed, those
  parts will still maintain the same collision group name. The physical
  behavior of parts in a removed group is undefined, so it's recommended
  to move any parts in a removed group to another group, such as the
  "Default" group.

Note that this method has a slight performance overhead based on the
number of [BaseParts](/docs/reference/engine/classes/BasePart) in the workspace, so it's recommended
that you register all collision groups at edit time through the Studio
[editor](/docs/workspace/collisions#collision-groups) and call this
method as infrequently as possible.

Provide feedback

---