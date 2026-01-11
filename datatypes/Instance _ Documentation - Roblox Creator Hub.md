# Instance | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Instance
Scraped: 2026-01-11T02:42:16.986612Z

## Inherits
- Instance
- Parent
- Instance:Clone()
- Instances
- Instance.Archivable
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Instance](/docs/reference/engine/datatypes/Instance)

English

Feedback

Engine Data Type

Instance

Holds the constructor for Instances.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(className: [string](/docs/luau/strings),parent: [Instance](/docs/reference/engine/datatypes/Instance)?) |
| [fromExisting](#fromExisting)(existingInstance: [Instance](/docs/reference/engine/datatypes/Instance)) |

The [Instance](/docs/reference/engine/classes/Instance) data type holds constructors for [Instance](/docs/reference/engine/classes/Instance)
objects.

---

API Reference

Constructors

new

Returns an [Instance](/docs/reference/engine/classes/Instance) of the specified class.

Instance.new(

className:[string](/docs/luau/strings), parent:[Instance](/docs/reference/engine/datatypes/Instance)? )

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  Class name of the new instance to create. |
| parent:[Instance](/docs/reference/engine/datatypes/Instance)?  Optional object to parent the new instance to. Not recommended for performance reasons (see description above). |

Creates a new [Instance](/docs/reference/engine/classes/Instance) of type className. Abstract classes and
services cannot be created with this constructor.

Note that when the [Parent](/docs/reference/engine/classes/Instance#Parent) of an object is set,
Luau listens to a variety of different property changes for replication,
rendering, and physics. For performance reasons, it's recommended to set
the instance's [Parent](/docs/reference/engine/classes/Instance#Parent) property last when
creating new objects, instead of specifying the second argument (parent)
of this constructor.

```
local Workspace = game:GetService("Workspace")



-- Set new instance's parent last (recommended)



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Parent = Workspace



-- Set new instance's parent in constructor (discouraged)



local part = Instance.new("Part", Workspace)



part.Position = Vector3.new(0, 10, 0)
```

Provide feedback

---

fromExisting

Returns an [Instance](/docs/reference/engine/classes/Instance) which is a copy of an existing
[Instance](/docs/reference/engine/classes/Instance).

Instance.fromExisting(existingInstance:[Instance](/docs/reference/engine/datatypes/Instance))

Parameters

|  |
| --- |
| existingInstance:[Instance](/docs/reference/engine/datatypes/Instance)  The existing [Instance](/docs/reference/engine/classes/Instance) to copy property values from. |

Creates a new object with the same type and property values as an existing
object. In most cases using [Instance:Clone()](/docs/reference/engine/classes/Instance#Clone) is more appropriate,
but this constructor is useful when implementing low‑level libraries or
systems.

There are two behavioral differences between this constructor and the
[Instance:Clone()](/docs/reference/engine/classes/Instance#Clone) method:

* This constructor will not copy any of the descendant [Instances](/docs/reference/engine/classes/Instance) parented to the existing object.
* This constructor will return a new object even if the existing object had [Instance.Archivable](/docs/reference/engine/classes/Instance#Archivable) set to false.

Provide feedback

---