# RaycastParams | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/RaycastParams
Scraped: 2026-01-11T02:42:27.002486Z

## Inherits
- WorldRoot:Raycast()
- Terrain
- CanCollide
- CanQuery
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [RaycastParams](/docs/reference/engine/datatypes/RaycastParams)

English

Feedback

Engine Data Type

RaycastParams

A container for parameters used in raycasting operations.

---

Summary

Constructors

|  |
| --- |
| [new](#new)() |

Properties

|  |
| --- |
| [FilterDescendantsInstances](#FilterDescendantsInstances):[Array](/docs/luau/tables#arrays) |
| [FilterType](#FilterType):[Enum.RaycastFilterType](/docs/reference/engine/enums/RaycastFilterType) |
| [IgnoreWater](#IgnoreWater):[boolean](/docs/luau/booleans) |
| [CollisionGroup](#CollisionGroup):[string](/docs/luau/strings) |
| [RespectCanCollide](#RespectCanCollide):[boolean](/docs/luau/booleans) |
| [BruteForceAllSlow](#BruteForceAllSlow):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [AddToFilter](#AddToFilter)(instances: [Instance](/docs/reference/engine/datatypes/Instance) | [Array](/docs/luau/tables#arrays)):() |

The [RaycastParams](/docs/reference/engine/datatypes/RaycastParams) data type stores parameters for
[WorldRoot:Raycast()](/docs/reference/engine/classes/WorldRoot#Raycast) operations. The
[FilterDescendantsInstances](/docs/reference/engine/datatypes/RaycastParams#FilterDescendantsInstances)
property stores an array of objects to use as either an inclusion or exclusion
list based on the [RaycastParams.FilterType](/docs/reference/engine/datatypes/RaycastParams#FilterType) enum. If desired, the
[RaycastParams.IgnoreWater](/docs/reference/engine/datatypes/RaycastParams#IgnoreWater) property can be used to ignore
[Terrain](/docs/reference/engine/classes/Terrain) water, and the [RaycastParams.CollisionGroup](/docs/reference/engine/datatypes/RaycastParams#CollisionGroup)
property can specify a collision group for the raycasting operation.

This object is different from the similarly named [RaycastResult](/docs/reference/engine/datatypes/RaycastResult)
which provides the results of a raycast.

Unlike most data types in Luau, you can change all of the members of
[RaycastParams](/docs/reference/engine/datatypes/RaycastParams) without creating a new object, allowing you to reuse
the same object repeatedly.

---

API Reference

Constructors

new

Returns a blank [RaycastParams](/docs/reference/engine/datatypes/RaycastParams).

RaycastParams.new()

Returns a blank [RaycastParams](/docs/reference/engine/datatypes/RaycastParams) object. Unlike other data type
constructors, this constructor does not have any parameters, so you should
set its properties appropriately.

Provide feedback

---

Properties

FilterDescendantsInstances

An array of objects whose descendants are used in filtering raycasting
candidates.

RaycastParams.FilterDescendantsInstances:[Array](/docs/luau/tables#arrays)

An array of objects whose descendants are used in filtering raycasting
candidates.

Provide feedback

---

FilterType

Determines how the
[FilterDescendantsInstances](/docs/reference/engine/datatypes/RaycastParams#FilterDescendantsInstances)
array is used.

RaycastParams.FilterType:[Enum.RaycastFilterType](/docs/reference/engine/enums/RaycastFilterType)

Determines how the
[FilterDescendantsInstances](/docs/reference/engine/datatypes/RaycastParams#FilterDescendantsInstances)
array is used, depending on the [Enum.RaycastFilterType](/docs/reference/engine/enums/RaycastFilterType) provided.

Provide feedback

---

IgnoreWater

Determines whether the water material is considered when raycasting
against [Terrain](/docs/reference/engine/classes/Terrain).

RaycastParams.IgnoreWater:[boolean](/docs/luau/booleans)

Determines whether the water material is considered when raycasting
against [Terrain](/docs/reference/engine/classes/Terrain).

Provide feedback

---

CollisionGroup

The collision group used for the operation.

RaycastParams.CollisionGroup:[string](/docs/luau/strings)

Specifies a collision group for the raycasting operation. Parts in
collision groups that are set to not collide with this group are
ignored. If this property is omitted, the raycast assumes the Default
collision group.

Provide feedback

---

RespectCanCollide

Determines whether the raycast operation considers a part's
[CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) property value over its
[CanQuery](/docs/reference/engine/classes/BasePart#CanQuery) value.

RaycastParams.RespectCanCollide:[boolean](/docs/luau/booleans)

This property, if true, makes the raycast operation use an intersected
part's [CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) value in favor of its
[CanQuery](/docs/reference/engine/classes/BasePart#CanQuery) value when determining whether that
part is included in the [RaycastResult](/docs/reference/engine/datatypes/RaycastResult).

Provide feedback

---

BruteForceAllSlow

When enabled, the query will ignore all part collision properties and
perform a brute-force check on every part.

RaycastParams.BruteForceAllSlow:[boolean](/docs/luau/booleans)

When enabled, the query will ignore all part collision properties and
perform a brute-force check on every part. This will negatively impact
performance and should not be used in live experiences.

Provide feedback

---

Methods

AddToFilter

Adds the instances provided to
[FilterDescendantsInstances](/docs/reference/engine/datatypes/RaycastParams#FilterDescendantsInstances).

RaycastParams:AddToFilter(instances:[Instance](/docs/reference/engine/datatypes/Instance) | [Array](/docs/luau/tables#arrays)):()

Parameters

|  |
| --- |
| instances:[Instance](/docs/reference/engine/datatypes/Instance) | [Array](/docs/luau/tables#arrays)  An instance or an array containing instances to add. |

Returns

()

For efficiency and simplicity, this method is the preferred way to add
instances to the filter. It has the additional advantage that it allows
[FilterDescendantsInstances](/docs/reference/engine/datatypes/RaycastParams#FilterDescendantsInstances)
to be updated from a parallel context.

Provide feedback

---