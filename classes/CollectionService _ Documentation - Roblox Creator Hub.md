# CollectionService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CollectionService
Scraped: 2026-01-11T02:39:19.473008Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- CollectionService
- Object
- AddTag()
- RemoveTag()
- StreamingEnabled
- LocalScripts
- GetInstanceAddedSignal()
- Instance:Destroy()
- GetInstanceRemovedSignal()
- DataModel
- CollectionService:AddTag()
- Instance:AddTag()
- Instance.Parent
- GetTagged()
- BasePart
- Humanoid
- CollectionService:RemoveTag()
- Instance:RemoveTag()
- HasTag()
- GetTags()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [CollectionService](/docs/reference/engine/classes/CollectionService)

English

Feedback

Engine Class

CollectionService

A service which manages instance collections using assigned tags.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [AddTag](#AddTag)(instance: [Instance](/docs/reference/engine/datatypes/Instance),tag: [string](/docs/luau/strings)):() |
| [GetAllTags](#GetAllTags)():[Array](/docs/luau/tables#arrays) |
| [GetCollection](#GetCollection)(class: [string](/docs/luau/strings)):Instances  Deprecated |
| [GetInstanceAddedSignal](#GetInstanceAddedSignal)(tag: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GetInstanceRemovedSignal](#GetInstanceRemovedSignal)(tag: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GetTagged](#GetTagged)(tag: [string](/docs/luau/strings)):Instances |
| [GetTags](#GetTags)(instance: [Instance](/docs/reference/engine/datatypes/Instance)):[Array](/docs/luau/tables#arrays) |
| [HasTag](#HasTag)(instance: [Instance](/docs/reference/engine/datatypes/Instance),tag: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [RemoveTag](#RemoveTag)(instance: [Instance](/docs/reference/engine/datatypes/Instance),tag: [string](/docs/luau/strings)):() |

Events

|  |
| --- |
| [ItemAdded](#ItemAdded)(instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [ItemRemoved](#ItemRemoved)(instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [TagAdded](#TagAdded)(tag: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TagRemoved](#TagRemoved)(tag: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

CollectionService manages groups (collections) of instances with tags.
Tags are sets of strings applied to instances that replicate from the server
to the client. They are also serialized when places are saved.

The primary use of CollectionService is to register instances with specific
tags that you can use to extend their behavior. If you find yourself adding
the same script to many different instances, a script that uses
CollectionService may be better.

Tags can be added or removed through this class' methods such as
[AddTag()](/docs/reference/engine/classes/CollectionService#AddTag) or
[RemoveTag()](/docs/reference/engine/classes/CollectionService#RemoveTag). They can also be managed
directly in Studio through the
[Tags](/docs/studio/properties#instance-tags) section of an instance's
properties.

##### Replication

When tags replicate, all tags on an instance replicate at the same time.
Therefore, if you set a tag on an instance from the client then add/remove a
different tag on the same instance from the server, the client's local
tags on the instance are overwritten. In
[StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) places, instances can be
unloaded as they leave the client's streamed area. If such an instance
re-enters the streamed area, properties and tags will be re-synchronized from
the server. This can cause changes made by [LocalScripts](/docs/reference/engine/classes/LocalScript) to
be overwritten/removed.

---

API Reference

Methods

AddTag

Applies a tag to an [Instance](/docs/reference/engine/classes/Instance).

CollectionService:AddTag(

instance:[Instance](/docs/reference/engine/datatypes/Instance), tag:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance) |
| tag:[string](/docs/luau/strings) |

Returns

()

This method applies a tag to an [Instance](/docs/reference/engine/classes/Instance), doing nothing if the tag
is already applied to that instance. Successfully adding a tag will fire a
signal created by
[GetInstanceAddedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceAddedSignal)
with the given tag.

##### Warnings

* An instance's tags that were added client-side will be dropped if the
  server later adds or removes a tag on that instance because the server
  replicates all tags together and overwrites previous tags.
* When tagging an instance, it is common that some resources are used to
  give the tag its functionality, for example event connections or tables.
  To prevent memory leaks, it's a good idea to clean these up (disconnect,
  set to nil, etc.) when no longer needed for a tag. Do this when
  calling [RemoveTag()](/docs/reference/engine/classes/CollectionService#RemoveTag), calling
  [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy) or in a function connected to a signal
  returned by
  [GetInstanceRemovedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceRemovedSignal).

Provide feedback

---

GetAllTags

Write Parallel

Returns an array of all tags in the experience.

CollectionService:GetAllTags():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Returns an array of all tags in the experience.

Provide feedback

---

GetCollection

Deprecated

Show details

---

GetInstanceAddedSignal

Returns a signal that fires when a given tag is added to an instance.

CollectionService:GetInstanceAddedSignal(tag:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings)  The tag to watch for. |

Returns

[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

An event that fires when you add the tag to an instance.

Given a tag (string), this method returns a signal which fires under two
conditions:

* The tag is assigned to an instance within the [DataModel](/docs/reference/engine/classes/DataModel) using
  [CollectionService:AddTag()](/docs/reference/engine/classes/CollectionService#AddTag) or [Instance:AddTag()](/docs/reference/engine/classes/Instance#AddTag).
* An instance with the given tag is added as a descendant of the
  [DataModel](/docs/reference/engine/classes/DataModel), for example by setting [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) or
  similar.

Subsequent calls to this method with the same tag return the same signal
object. Consider also calling
[GetTagged()](/docs/reference/engine/classes/CollectionService#GetTagged) to get a list of
instances that already have a tag (and thus won't fire the event if they
already are in the [DataModel](/docs/reference/engine/classes/DataModel)).

See also
[GetInstanceRemovedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceRemovedSignal)
which returns an event that fires under similar conditions.

Code Samples

Deadly Bricks using CollectionService

This code sample causes any [BasePart](/docs/reference/engine/classes/BasePart) with the tag Deadly to kill
any [Humanoid](/docs/reference/engine/classes/Humanoid) that touches it. It does this using a common pattern with
[CollectionService](/docs/reference/engine/classes/CollectionService) to listen for all parts with the tag and make a
connection, then disconnect the connection when the tag is removed.

```
local CollectionService = game:GetService("CollectionService")



local tag = "Deadly"



local function onDeadlyPartTouched(otherPart)



if not otherPart.Parent then



return



end



local humanoid = otherPart.Parent:FindFirstChildOfClass("Humanoid")



if humanoid then



humanoid.Health = 0



end



end



-- Save the connections so they can be disconnected when the tag is removed



local connections = {}



local function onInstanceAdded(object)



-- Confirm that the object with this tag is a BasePart



if object:IsA("BasePart") then



connections[object] = object.Touched:Connect(onDeadlyPartTouched)



end



end



local function onInstanceRemoved(object)



-- If there is a stored connection on this object, disconnect/remove it



if connections[object] then



connections[object]:Disconnect()



connections[object] = nil



end



end



-- Listen for this tag being applied to objects



CollectionService:GetInstanceAddedSignal(tag):Connect(onInstanceAdded)



CollectionService:GetInstanceRemovedSignal(tag):Connect(onInstanceRemoved)



-- Also detect any objects that already have the tag



for _, object in pairs(CollectionService:GetTagged(tag)) do



onInstanceAdded(object)



end
```

Provide feedback

---

GetInstanceRemovedSignal

Returns a signal that fires when a given tag is removed from an instance.

CollectionService:GetInstanceRemovedSignal(tag:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings)  The tag to watch for. |

Returns

[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

An event that fires when you remove the tag from an instance.

Given a tag (string), this method returns a signal which fires under two
conditions:

* The tag is removed from an instance within the [DataModel](/docs/reference/engine/classes/DataModel) using
  [CollectionService:RemoveTag()](/docs/reference/engine/classes/CollectionService#RemoveTag) or [Instance:RemoveTag()](/docs/reference/engine/classes/Instance#RemoveTag).
* An instance with the given tag is removed as a descendant of the
  [DataModel](/docs/reference/engine/classes/DataModel), for example by un‑setting [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) or
  similar.

Subsequent calls to this method with the same tag return the same signal
object. The signal is useful for cleaning up resources used by instances
that once had tags, such as disconnecting connections.

See also
[GetInstanceAddedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceAddedSignal)
which returns an event that fires under similar conditions.

Code Samples

Deadly Bricks using CollectionService

This code sample causes any [BasePart](/docs/reference/engine/classes/BasePart) with the tag Deadly to kill
any [Humanoid](/docs/reference/engine/classes/Humanoid) that touches it. It does this using a common pattern with
[CollectionService](/docs/reference/engine/classes/CollectionService) to listen for all parts with the tag and make a
connection, then disconnect the connection when the tag is removed.

```
local CollectionService = game:GetService("CollectionService")



local tag = "Deadly"



local function onDeadlyPartTouched(otherPart)



if not otherPart.Parent then



return



end



local humanoid = otherPart.Parent:FindFirstChildOfClass("Humanoid")



if humanoid then



humanoid.Health = 0



end



end



-- Save the connections so they can be disconnected when the tag is removed



local connections = {}



local function onInstanceAdded(object)



-- Confirm that the object with this tag is a BasePart



if object:IsA("BasePart") then



connections[object] = object.Touched:Connect(onDeadlyPartTouched)



end



end



local function onInstanceRemoved(object)



-- If there is a stored connection on this object, disconnect/remove it



if connections[object] then



connections[object]:Disconnect()



connections[object] = nil



end



end



-- Listen for this tag being applied to objects



CollectionService:GetInstanceAddedSignal(tag):Connect(onInstanceAdded)



CollectionService:GetInstanceRemovedSignal(tag):Connect(onInstanceRemoved)



-- Also detect any objects that already have the tag



for _, object in pairs(CollectionService:GetTagged(tag)) do



onInstanceAdded(object)



end
```

Provide feedback

---

GetTagged

Write Parallel

Returns an array of instances in the game with a given tag.

CollectionService:GetTagged(tag:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings)  The tag to search for. |

Returns

Instances

An array of all instances with the tag.

This method returns an array of instances with a given tag which are
descendants of the [DataModel](/docs/reference/engine/classes/DataModel). Removing a tag using
[CollectionService:RemoveTag()](/docs/reference/engine/classes/CollectionService#RemoveTag) or [Instance:RemoveTag()](/docs/reference/engine/classes/Instance#RemoveTag)
ensures this method does not return them.

If you want to detect all instances with a tag, both present and
future, use this method to iterate over instances while also making a
connection to a signal returned by
[GetInstanceAddedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceAddedSignal).

This method does not guarantee any ordering of the returned instances.
Additionally, it's possible that instances can have the given tag assigned
to them but not be a descendant of the [DataModel](/docs/reference/engine/classes/DataModel), for example its
parent is nil; this method will not return such instances.

Code Samples

Deadly Bricks using CollectionService

This code sample causes any [BasePart](/docs/reference/engine/classes/BasePart) with the tag Deadly to kill
any [Humanoid](/docs/reference/engine/classes/Humanoid) that touches it. It does this using a common pattern with
[CollectionService](/docs/reference/engine/classes/CollectionService) to listen for all parts with the tag and make a
connection, then disconnect the connection when the tag is removed.

```
local CollectionService = game:GetService("CollectionService")



local tag = "Deadly"



local function onDeadlyPartTouched(otherPart)



if not otherPart.Parent then



return



end



local humanoid = otherPart.Parent:FindFirstChildOfClass("Humanoid")



if humanoid then



humanoid.Health = 0



end



end



-- Save the connections so they can be disconnected when the tag is removed



local connections = {}



local function onInstanceAdded(object)



-- Confirm that the object with this tag is a BasePart



if object:IsA("BasePart") then



connections[object] = object.Touched:Connect(onDeadlyPartTouched)



end



end



local function onInstanceRemoved(object)



-- If there is a stored connection on this object, disconnect/remove it



if connections[object] then



connections[object]:Disconnect()



connections[object] = nil



end



end



-- Listen for this tag being applied to objects



CollectionService:GetInstanceAddedSignal(tag):Connect(onInstanceAdded)



CollectionService:GetInstanceRemovedSignal(tag):Connect(onInstanceRemoved)



-- Also detect any objects that already have the tag



for _, object in pairs(CollectionService:GetTagged(tag)) do



onInstanceAdded(object)



end
```

Provide feedback

---

GetTags

Write Parallel

Gets an array of all tags applied to a given instance.

CollectionService:GetTags(instance:[Instance](/docs/reference/engine/datatypes/Instance)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The instance whose tags should be returned. |

Returns

[Array](/docs/luau/tables#arrays)

An array of strings which are the tags applied to the given instance.

Given an [Instance](/docs/reference/engine/classes/Instance), this method returns an array of strings which
are the tags applied to the instance.

This method is useful when you want to do something with multiple instance
tags at once, but it's inefficient to check for the existence of a single
tag. For this, use [HasTag()](/docs/reference/engine/classes/CollectionService#HasTag) to check
for a single tag.

Code Samples

Using Tags and CollectionService

This code sample demonstrates adding, removing and querying a tag from an
object using [CollectionService](/docs/reference/engine/classes/CollectionService).

```
local CollectionService = game:GetService("CollectionService")



local Workspace = game:GetService("Workspace")



local object = Workspace.Part



-- Add a tag



CollectionService:AddTag(object, "Deadly")



-- Query for a tag



if CollectionService:HasTag(object, "Deadly") then



print(object:GetFullName() .. " is deadly")



end



-- List tags on an object



local tags = CollectionService:GetTags(object)



print("The object " .. object:GetFullName() .. " has tags: " .. table.concat(tags, ", "))



-- Remove a tag



CollectionService:RemoveTag(object, "Deadly")
```

Provide feedback

---

HasTag

Write Parallel

Check whether an instance has a given tag.

CollectionService:HasTag(

instance:[Instance](/docs/reference/engine/datatypes/Instance), tag:[string](/docs/luau/strings)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The instance to check for the presence of a tag. |
| tag:[string](/docs/luau/strings)  The tag to check for. |

Returns

[boolean](/docs/luau/booleans)

Whether the instance has the tag.

This method returns whether a given [Instance](/docs/reference/engine/classes/Instance) has a tag.

By extension, any tags returned by a call to
[GetTags()](/docs/reference/engine/classes/CollectionService#GetTags) on an instance will return
true when used with this method.

Code Samples

Using Tags and CollectionService

This code sample demonstrates adding, removing and querying a tag from an
object using [CollectionService](/docs/reference/engine/classes/CollectionService).

```
local CollectionService = game:GetService("CollectionService")



local Workspace = game:GetService("Workspace")



local object = Workspace.Part



-- Add a tag



CollectionService:AddTag(object, "Deadly")



-- Query for a tag



if CollectionService:HasTag(object, "Deadly") then



print(object:GetFullName() .. " is deadly")



end



-- List tags on an object



local tags = CollectionService:GetTags(object)



print("The object " .. object:GetFullName() .. " has tags: " .. table.concat(tags, ", "))



-- Remove a tag



CollectionService:RemoveTag(object, "Deadly")
```

Provide feedback

---

RemoveTag

Removes a tag from an instance.

CollectionService:RemoveTag(

instance:[Instance](/docs/reference/engine/datatypes/Instance), tag:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The instance to remove the tag from. |
| tag:[string](/docs/luau/strings)  The tag to remove from the instance. |

Returns

()

This method removes a tag from an instance. Successfully removing a tag
will fire a signal created by
[GetInstanceRemovedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceRemovedSignal)
with the given tag.

When removing a tag, it's common that some resources are used to give the
tag its functionality, for example event connections or tables. To prevent
memory leaks, it's a good idea to clean these up (disconnect, set to
nil, etc.) when no longer needed for a tag.

Code Samples

Using Tags and CollectionService

This code sample demonstrates adding, removing and querying a tag from an
object using [CollectionService](/docs/reference/engine/classes/CollectionService).

```
local CollectionService = game:GetService("CollectionService")



local Workspace = game:GetService("Workspace")



local object = Workspace.Part



-- Add a tag



CollectionService:AddTag(object, "Deadly")



-- Query for a tag



if CollectionService:HasTag(object, "Deadly") then



print(object:GetFullName() .. " is deadly")



end



-- List tags on an object



local tags = CollectionService:GetTags(object)



print("The object " .. object:GetFullName() .. " has tags: " .. table.concat(tags, ", "))



-- Remove a tag



CollectionService:RemoveTag(object, "Deadly")
```

Provide feedback

---

Events

ItemAdded

Deprecated

Show details

---

ItemRemoved

Deprecated

Show details

---

TagAdded

Fires when a tag is added to an instance and the added tag is the only
occurrence of that tag in the place.

CollectionService.TagAdded(tag:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings) |

This event fires when a tag is added to an instance and the added tag is
the only occurrence of that tag in the place.

Provide feedback

---

TagRemoved

Fires when a tag is removed from an instance and the removed tag is no
longer used anywhere in the place.

CollectionService.TagRemoved(tag:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings) |

This event fires when a tag is removed from an instance and the removed
tag is no longer used anywhere in the place.

Provide feedback

---