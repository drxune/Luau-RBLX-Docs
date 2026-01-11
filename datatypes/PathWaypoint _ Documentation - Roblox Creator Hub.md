# PathWaypoint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/PathWaypoint
Scraped: 2026-01-11T02:42:24.623695Z

## Inherits
- PathfindingService
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [PathWaypoint](/docs/reference/engine/datatypes/PathWaypoint)

English

Feedback

Engine Data Type

PathWaypoint

A description of the steps required to reach the next waypoint in a path.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(position: [Vector3](/docs/reference/engine/datatypes/Vector3),action: [Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction),label: [string](/docs/luau/strings)) |

Properties

|  |
| --- |
| [Action](#Action):[Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Label](#Label):[string](/docs/luau/strings) |

The [PathWaypoint](/docs/reference/engine/datatypes/PathWaypoint) data type constructed by a
[Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction) action, [Vector3](/docs/reference/engine/datatypes/Vector3) position, and
[string](/docs/reference/engine/libraries/string) label which is used by the [PathfindingService](/docs/reference/engine/classes/PathfindingService) to
create points along a generated path.

The code block below constructs a [PathWaypoint](/docs/reference/engine/datatypes/PathWaypoint) variable with
Vector3.new(10, 10, 10) as its position, [Enum.PathWaypointAction.Walk](/docs/reference/engine/enums/PathWaypointAction#Walk) as
its action, and Custom Label as its label:

```
local pos = Vector3.new(10, 10, 10)



local waypoint = PathWaypoint.new(pos, Enum.PathWaypointAction.Walk, "Custom Label")
```

PathWaypoint can also be constructed by passing position and action. Label
property will be set to default as empty string.

```
local pos = Vector3.new(10, 10, 10)



local waypoint = PathWaypoint.new(pos, Enum.PathWaypointAction.Walk)
```

Action
------

The [Action](/docs/reference/engine/enums/PathWaypointAction) describes the action to take in order to
reach this PathWaypoint. It can be set to one of the following enum values:

| Name | Value | Description |
| --- | --- | --- |
| Walk | 0 | Walk action needed to reach this waypoint from the previous one. |
| Jump | 1 | Jump action needed to reach this waypoint from the previous one. |

---

API Reference

Constructors

new

Returns a [PathWaypoint](/docs/reference/engine/datatypes/PathWaypoint) object from the given [Vector3](/docs/reference/engine/datatypes/Vector3) position, [Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction) action, and optional string label.

PathWaypoint.new(

position:[Vector3](/docs/reference/engine/datatypes/Vector3), action:[Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction), label:[string](/docs/luau/strings) )

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3) Default Value: Vector3.new(0, 0, 0) The 3D position of the waypoint. |
| action:[Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction) Default Value: Enum.PathWaypointAction.Walk The action to perform at the waypoint. |
| label:[string](/docs/luau/strings)  The name of the navigation area that generates the waypoint. |

Returns a [PathWaypoint](/docs/reference/engine/datatypes/PathWaypoint) object from the given [Vector3](/docs/reference/engine/datatypes/Vector3) position, [Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction) action, and optional string label.

Provide feedback

---

Properties

Action

The action to perform at this waypoint.

PathWaypoint.Action:[Enum.PathWaypointAction](/docs/reference/engine/enums/PathWaypointAction)

The action to perform at this waypoint.

Provide feedback

---

Position

The 3D position of this waypoint.

PathWaypoint.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

The 3D position of this waypoint.

Provide feedback

---

Label

The name of the navigation area that generates this waypoint.

PathWaypoint.Label:[string](/docs/luau/strings)

The name of the navigation area that generates this waypoint. You can use
PathwayPoint.Label to decide the custom action to take to reach the
waypoint. PathfindingModifier and Material each have a Label. Automatic
jump links have "Jump" as their Label.

Provide feedback

---