# OverlapParams | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/OverlapParams
Scraped: 2026-01-11T02:42:07.285109Z

## Inherits
- WorldRoot
- WorldRoot:GetPartBoundsInBox()
- WorldRoot:GetPartBoundsInRadius()
- WorldRoot:GetPartsInPart()
- BasePart.CanCollide
- BasePart.CanQuery
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [OverlapParams](/docs/reference/engine/datatypes/OverlapParams)

English

Feedback

Engine Data Type

OverlapParams

Stores parameters used in boundary-querying functions.

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
| [MaxParts](#MaxParts):[number](/docs/luau/numbers) |
| [CollisionGroup](#CollisionGroup):[string](/docs/luau/strings) |
| [Tolerance](#Tolerance):[number](/docs/luau/numbers) |
| [RespectCanCollide](#RespectCanCollide):[boolean](/docs/luau/booleans) |
| [BruteForceAllSlow](#BruteForceAllSlow):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [AddToFilter](#AddToFilter)(instances: [Instance](/docs/reference/engine/datatypes/Instance) | [Array](/docs/luau/tables#arrays)):() |

The [OverlapParams](/docs/reference/engine/datatypes/OverlapParams) data type stores parameters for use with
[WorldRoot](/docs/reference/engine/classes/WorldRoot) boundary-querying functions, in particular
[WorldRoot:GetPartBoundsInBox()](/docs/reference/engine/classes/WorldRoot#GetPartBoundsInBox),
[WorldRoot:GetPartBoundsInRadius()](/docs/reference/engine/classes/WorldRoot#GetPartBoundsInRadius) and
[WorldRoot:GetPartsInPart()](/docs/reference/engine/classes/WorldRoot#GetPartsInPart). The
[OverlapParams.FilterDescendantsInstances](/docs/reference/engine/datatypes/OverlapParams#FilterDescendantsInstances) property stores an array
of objects to use as either an inclusion or exclusion list based on the
[OverlapParams.FilterType](/docs/reference/engine/datatypes/OverlapParams#FilterType) enum, and the
[OverlapParams.CollisionGroup](/docs/reference/engine/datatypes/OverlapParams#CollisionGroup) property can specify a collision group
for the boundary query operation.

Unlike most data types in Luau, you can change all of the members of
[OverlapParams](/docs/reference/engine/datatypes/OverlapParams) without creating a new object, allowing you to reuse
the same object repeatedly.

---

API Reference

Constructors

new

Returns a blank [OverlapParams](/docs/reference/engine/datatypes/OverlapParams) object.

OverlapParams.new()

Returns a blank [OverlapParams](/docs/reference/engine/datatypes/OverlapParams) object. Unlike other data type
constructors, this constructor does not have any parameters, so you should
set its properties appropriately.

Provide feedback

---

Properties

FilterDescendantsInstances

An array of objects whose descendants is used in filtering candidates.

OverlapParams.FilterDescendantsInstances:[Array](/docs/luau/tables#arrays)

An array of objects whose descendants is used in filtering candidates.

Provide feedback

---

FilterType

Determines how the [OverlapParams.FilterDescendantsInstances](/docs/reference/engine/datatypes/OverlapParams#FilterDescendantsInstances)
list is used.

OverlapParams.FilterType:[Enum.RaycastFilterType](/docs/reference/engine/enums/RaycastFilterType)

Determines how the [OverlapParams.FilterDescendantsInstances](/docs/reference/engine/datatypes/OverlapParams#FilterDescendantsInstances)
array is used, depending on the [Enum.RaycastFilterType](/docs/reference/engine/enums/RaycastFilterType) provided. Default
is [Enum.RaycastFilterType.Exclude](/docs/reference/engine/enums/RaycastFilterType#Exclude).

Provide feedback

---

MaxParts

The maximum amount of parts to be returned by the query.

OverlapParams.MaxParts:[number](/docs/luau/numbers)

The maximum amount of parts to be returned by the query. The default value
of zero (0) represents no limit.

Provide feedback

---

CollisionGroup

The collision group used for the operation.

OverlapParams.CollisionGroup:[string](/docs/luau/strings)

Specifies a collision group for the operation. Parts in collision groups
that are set to not collide with this group are ignored. If this
property is omitted, the operation assumes the Default collision
group.

Provide feedback

---

Tolerance

Slightly increases the volume of the boundary-querying operation.

OverlapParams.Tolerance:[number](/docs/luau/numbers)

Slightly increases the volume of the boundary-querying operation, clamped
between 0 and 0.05 studs.

Provide feedback

---

RespectCanCollide

Determines whether the boundary-querying operation considers a part's
[BasePart.CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) property value over its
[BasePart.CanQuery](/docs/reference/engine/classes/BasePart#CanQuery) value.

OverlapParams.RespectCanCollide:[boolean](/docs/luau/booleans)

This property, if true, makes the boundary-querying operation use an
intersected part's [BasePart.CanCollide](/docs/reference/engine/classes/BasePart#CanCollide) value in favor of its
[BasePart.CanQuery](/docs/reference/engine/classes/BasePart#CanQuery) value when determining whether that part is
included in the array of spatial query results.

Provide feedback

---

BruteForceAllSlow

When enabled, the query will ignore all part collision properties and
perform a brute-force check on every part.

OverlapParams.BruteForceAllSlow:[boolean](/docs/luau/booleans)

When enabled, the query will ignore all part collision properties and
perform a brute-force check on every part. This will negatively impact
performance and should not be used in live experiences.

Provide feedback

---

Methods

AddToFilter

Adds the instances provided to
[FilterDescendantsInstances](/docs/reference/engine/datatypes/OverlapParams#FilterDescendantsInstances).

OverlapParams:AddToFilter(instances:[Instance](/docs/reference/engine/datatypes/Instance) | [Array](/docs/luau/tables#arrays)):()

Parameters

|  |
| --- |
| instances:[Instance](/docs/reference/engine/datatypes/Instance) | [Array](/docs/luau/tables#arrays)  An instance or an array containing instances to add. |

Returns

()

For efficiency and simplicity, this method is the preferred way to add
instances to the filter. It has the additional advantage that it allows
[FilterDescendantsInstances](/docs/reference/engine/datatypes/OverlapParams#FilterDescendantsInstances)
to be updated from a parallel context.

Provide feedback

---