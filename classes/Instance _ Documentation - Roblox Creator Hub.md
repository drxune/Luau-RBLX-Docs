# Instance | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Instance
Scraped: 2026-01-11T02:39:05.067518Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- DataModel
- Actor
- AccessoryDescription
- Accoutrement
- AdPortal
- AdService
- AdvancedDragger
- Instance:Clone()
- Clone()
- Archivable
- Instance.Sandboxed
- Instance:FindFirstChild()
- Instance:GetFullName()
- GetChildren()
- FindFirstChild()
- Destroy()
- Model
- Instance.Name
- CollectionService:GetInstanceAddedSignal()
- Instance:RemoveTag()
- Instance:Destroy()
- CollectionService:GetInstanceRemovedSignal()
- Instance:GetChildren()
- Instance:GetDescendants()
- BaseParts
- Parent
- ObjectValue.Value
- Instance.Parent
- Debris:AddItem()
- Instance:FindFirstAncestorOfClass()
- Instance:FindFirstAncestorWhichIsA()
- Object.ClassName
- BasePart
- Instance:FindFirstAncestor()
- Object:IsA()
- WedgePart
- MeshPart
- Part
- Name
- Folder
- Part.Color
- RunService.Heartbeat
- RunService.PreRender
- ChildAdded
- WaitForChild()
- ClassName
- Instance:FindFirstChildWhichIsA()
- Instance:FindFirstChildOfClass()
- Instance:SetAttribute()
- Instance:GetAttributes()
- Changed
- GetPropertyChangedSignal()
- Instance.AttributeChanged
- Instance:GetAttribute()
- GetDescendants()
- Script
- LocalScript
- QueryDescendants()
- Instance:IsA()
- Workspace
- Workspace.Part
- StyledPropertiesChanged
- AddTag()
- HasTag()
- Instance:IsDescendantOf()
- Instance:IsAncestorOf()
- BackgroundColor3
- TextLabel
- ResetPropertyToDefault()
- StyleRule
- CollectionService
- SpotLight
- PointLight
- Rotation
- Workspace.StreamingEnabled
- Instance.Destroying
- Instance.AncestryChanged
- Instance:GetAttributeChangedSignal()
- Instance:WaitForChild()
- Instance.DescendantAdded
- Instance.ChildRemoved
- Instance.DescendantRemoving
- Instance.ChildAdded
- DescendantAdded
- Workspace.SignalBehavior
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)

English

Feedback

Engine Class

Instance

Instance is the base class for all classes in the Roblox class hierarchy
which can be part of the [DataModel](/docs/reference/engine/classes/DataModel) tree.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [Archivable](#Archivable):[boolean](/docs/luau/booleans) |
| [archivable](#archivable):[boolean](/docs/luau/booleans)  Deprecated |
| [Capabilities](#Capabilities):SecurityCapabilities |
| [Name](#Name):[string](/docs/luau/strings) |
| [Parent](#Parent):[Instance](/docs/reference/engine/datatypes/Instance) |
| [PredictionMode](#PredictionMode):[Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode) |
| [RobloxLocked](#RobloxLocked):[boolean](/docs/luau/booleans)  Deprecated |
| [Sandboxed](#Sandboxed):[boolean](/docs/luau/booleans) |
| [UniqueId](#UniqueId):UniqueId |

Methods

|  |
| --- |
| [AddTag](#AddTag)(tag: [string](/docs/luau/strings)):() |
| [children](#children)():Instances  Deprecated |
| [ClearAllChildren](#ClearAllChildren)():() |
| [Clone](#Clone)():[Instance](/docs/reference/engine/datatypes/Instance) |
| [clone](#clone)():[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [Destroy](#Destroy)():() |
| [destroy](#destroy)():()  Deprecated |
| [FindFirstAncestor](#FindFirstAncestor)(name: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [FindFirstAncestorOfClass](#FindFirstAncestorOfClass)(className: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [FindFirstAncestorWhichIsA](#FindFirstAncestorWhichIsA)(className: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [FindFirstChild](#FindFirstChild)(name: [string](/docs/luau/strings),recursive: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [findFirstChild](#findFirstChild)(name: [string](/docs/luau/strings),recursive: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [FindFirstChildOfClass](#FindFirstChildOfClass)(className: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [FindFirstChildWhichIsA](#FindFirstChildWhichIsA)(className: [string](/docs/luau/strings),recursive: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [FindFirstDescendant](#FindFirstDescendant)(name: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetActor](#GetActor)():[Actor](/docs/reference/engine/classes/Actor)? |
| [GetAttribute](#GetAttribute)(attribute: [string](/docs/luau/strings)):Variant |
| [GetAttributeChangedSignal](#GetAttributeChangedSignal)(attribute: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GetAttributes](#GetAttributes)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetChildren](#GetChildren)():Instances |
| [getChildren](#getChildren)():Instances  Deprecated |
| [GetDebugId](#GetDebugId)(scopeLength: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [GetDescendants](#GetDescendants)():[Array](/docs/luau/tables#arrays) |
| [GetFullName](#GetFullName)():[string](/docs/luau/strings) |
| [GetStyled](#GetStyled)(name: [string](/docs/luau/strings)):Variant |
| [GetStyledPropertyChangedSignal](#GetStyledPropertyChangedSignal)(property: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GetTags](#GetTags)():[Array](/docs/luau/tables#arrays) |
| [HasTag](#HasTag)(tag: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [IsAncestorOf](#IsAncestorOf)(descendant: [Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans) |
| [IsDescendantOf](#IsDescendantOf)(ancestor: [Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans) |
| [isDescendantOf](#isDescendantOf)(ancestor: [Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans)  Deprecated |
| [IsPropertyModified](#IsPropertyModified)(property: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [QueryDescendants](#QueryDescendants)(selector: [string](/docs/luau/strings)):Instances |
| [Remove](#Remove)():()  Deprecated |
| [remove](#remove)():()  Deprecated |
| [RemoveTag](#RemoveTag)(tag: [string](/docs/luau/strings)):() |
| [ResetPropertyToDefault](#ResetPropertyToDefault)(property: [string](/docs/luau/strings)):() |
| [SetAttribute](#SetAttribute)(attribute: [string](/docs/luau/strings),value: Variant):() |
| [WaitForChild](#WaitForChild)(childName: [string](/docs/luau/strings),timeOut: [number](/docs/luau/numbers)):[Instance](/docs/reference/engine/datatypes/Instance) |

Events

|  |
| --- |
| [AncestryChanged](#AncestryChanged)(child: [Instance](/docs/reference/engine/datatypes/Instance),parent: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [AttributeChanged](#AttributeChanged)(attribute: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ChildAdded](#ChildAdded)(child: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [childAdded](#childAdded)(child: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [ChildRemoved](#ChildRemoved)(child: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DescendantAdded](#DescendantAdded)(descendant: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DescendantRemoving](#DescendantRemoving)(descendant: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Destroying](#Destroying)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [StyledPropertiesChanged](#StyledPropertiesChanged)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription), [Accoutrement](/docs/reference/engine/classes/Accoutrement), [AdPortal](/docs/reference/engine/classes/AdPortal), [AdService](/docs/reference/engine/classes/AdService), [AdvancedDragger](/docs/reference/engine/classes/AdvancedDragger), Show more...

Instance is the base class for all classes in the Roblox class hierarchy
which can be part of the [DataModel](/docs/reference/engine/classes/DataModel) tree.

It is not possible to directly create root Instance objects, but the special
[Instance.new()](/docs/reference/engine/datatypes/Instance#new) constructor creates objects via code, taking the
name of the class as a parameter and returning the created object.

---

API Reference

Properties

Archivable

Read Parallel

Determines if an [Instance](/docs/reference/engine/classes/Instance) and its descendants can be cloned using
[Instance:Clone()](/docs/reference/engine/classes/Instance#Clone), and can be saved/published.

Instance.Archivable:[boolean](/docs/luau/booleans)

This property determines whether the instance should be included when the
experience is published or saved, or when [Clone()](/docs/reference/engine/classes/Instance#Clone)
is called on one of the instance's ancestors. Calling
[Clone()](/docs/reference/engine/classes/Instance#Clone) directly on an instance will return nil
if that instance is not [Archivable](/docs/reference/engine/classes/Instance#Archivable).

Copying an object in Studio using the Duplicate or Copy/Paste
options will ignore its own [Archivable](/docs/reference/engine/classes/Instance#Archivable)
property and set [Archivable](/docs/reference/engine/classes/Instance#Archivable) to true for the
copy.

```
local part = Instance.new("Part")



print(part:Clone())  --> Part



part.Archivable = false



print(part:Clone())  --> nil
```

Provide feedback

---

archivable

Deprecated

Show details

---

Capabilities

Read Parallel

The set of capabilities allowed to be used for scripts inside this
container.

Instance.Capabilities:SecurityCapabilities

The set of capabilities allowed to be used for scripts inside this
instance. For the capabilities to take effect, [Instance.Sandboxed](/docs/reference/engine/classes/Instance#Sandboxed)
property must be enabled.

This property is used by an experimental feature. See
[script capabilities](/docs/scripting/capabilities) for further
details.

Provide feedback

---

Name

Read Parallel

A non-unique identifier of the [Instance](/docs/reference/engine/classes/Instance).

Instance.Name:[string](/docs/luau/strings)

A non-unique identifier of the [Instance](/docs/reference/engine/classes/Instance). Names are used to keep
the object hierarchy organized, along with allowing scripts to access
specific objects. The name of an instance cannot exceed 100 characters in
size.

The name of an object is often used to access the object through the data
model hierarchy using the following methods:

```
local Workspace = game:GetService("Workspace")



local baseplate = Workspace.Baseplate



local baseplate = Workspace["Baseplate"]



local baseplate = Workspace:FindFirstChild("BasePlate")
```

In order to make an object accessible using the dot operator (.), its
name must start with an underscore or letter, and the rest of the name can
only contain letters, numbers, or underscores (no other special
characters). If an object's name does not follow this syntax, it will not
be accessible using the dot operator and Luau will not interpret its name
as an identifier.

If more than one object with the same name are siblings, any attempt to
index an object by that name will return only one of the objects, similar
to [Instance:FindFirstChild()](/docs/reference/engine/classes/Instance#FindFirstChild), but not always the desired object.
If a specific object needs to be accessed through code, it's recommended
to give it a unique name or guarantee that none of its siblings share the
same name.

See also [Instance:GetFullName()](/docs/reference/engine/classes/Instance#GetFullName) to obtain a full name including
the object's hierarchy.

Provide feedback

---

Parent

Not Replicated

Read Parallel

Determines the hierarchical parent of the [Instance](/docs/reference/engine/classes/Instance).

Instance.Parent:[Instance](/docs/reference/engine/datatypes/Instance)

The Parent property determines the hierarchical parent of the
[Instance](/docs/reference/engine/classes/Instance). The following terminology is commonly used when talking
about how this property is set:

* An object is a child of, or is parented to, another object when
  its Parent is set to that object.
* The descendants of an [Instance](/docs/reference/engine/classes/Instance) are the children of that
  object, plus the descendants of the children as well.
* The ancestors of an [Instance](/docs/reference/engine/classes/Instance) are all the objects that the
  instance is a descendant of.

It is from the Parent property that many other API members get their
name, such as [GetChildren()](/docs/reference/engine/classes/Instance#GetChildren) and
[FindFirstChild()](/docs/reference/engine/classes/Instance#FindFirstChild). This property is also
used to manage whether an object exists in the experience or needs to be
removed. As long as an object's parent is in the [DataModel](/docs/reference/engine/classes/DataModel), is
stored in a variable, or is referenced by another object's property, the
object remains in the experience; otherwise, the object will automatically
be removed.

Calling [Destroy()](/docs/reference/engine/classes/Instance#Destroy) will set the Parent of an
[Instance](/docs/reference/engine/classes/Instance) and all of its descendants to nil, and also lock
the Parent property. An error is raised when setting the Parent of a
destroyed object.

Newly created objects using [Instance.new()](/docs/reference/engine/datatypes/Instance#new) will not have a
parent, and usually will not be visible or function until one is set.

##### Object Replication

An object created by the server will not replicate to clients until it is
parented to some object that is replicated. When creating an object and
setting many properties, it's recommended to set the Parent property
last. This ensures the object replicates once, instead of replicating
many property changes.

```
local Workspace = game:GetService("Workspace")



-- Set new instance's parent last (recommended)



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Parent = Workspace
```

However, if parenting parts to a [Model](/docs/reference/engine/classes/Model) whose parent hasn't been
set yet, parenting each part to that model is acceptable since the model
would not have replicated.

Provide feedback

---

PredictionMode

Read Only

Not Replicated

Not Scriptable

Read Parallel

Instance.PredictionMode:[Enum.PredictionMode](/docs/reference/engine/enums/PredictionMode)

Provide feedback

---

RobloxLocked

Deprecated

Show details

---

Sandboxed

Not Replicated

Read Parallel

Turns the instance to be a sandboxed container.

Instance.Sandboxed:[boolean](/docs/luau/booleans)

Turns the instance to be a sandboxed container, an experimental
feature which limits the actions that scripts inside a particular
container can perform. See
[script capabilities](/docs/scripting/capabilities) for further
details.

Provide feedback

---

UniqueId

Not Replicated

Roblox Script Security

Roblox Security

Read Parallel

A unique identifier for the instance.

Instance.UniqueId:UniqueId

A unique identifier for the instance, distinct from [Instance.Name](/docs/reference/engine/classes/Instance#Name)
which is not necessarily unique.

Provide feedback

---

Methods

AddTag

Applies a tag to the instance.

Instance:AddTag(tag:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings) |

Returns

()

This method applies a tag to the instance, with no effect if the tag is
already applied. Successfully adding a tag will fire a signal created by
[CollectionService:GetInstanceAddedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceAddedSignal) with the given tag.

##### Warnings

* An instance's tags that were added client-side will be dropped if the
  server later adds or removes a tag on that instance because the server
  replicates all tags together and overwrites previous tags.
* When tagging an instance, it is common that some resources are used to
  give the tag its functionality, for example event connections or tables.
  To prevent memory leaks, it's a good idea to clean these up (disconnect,
  set to nil, etc.) when no longer needed for a tag. Do this when
  calling [Instance:RemoveTag()](/docs/reference/engine/classes/Instance#RemoveTag), calling
  [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy), or in a function connected to a signal
  returned by [CollectionService:GetInstanceRemovedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceRemovedSignal).

Provide feedback

---

children

Deprecated

Show details

---

ClearAllChildren

This method destroys all of an instance's children.

Instance:ClearAllChildren():()

Returns

()

This method destroys all of an instance's children and descendants.

```
local part = Instance.new("Part")



-- Add some sparkles



for i = 1, 3 do



local sparkles = Instance.new("Sparkles")



sparkles.Parent = part



local sc = Instance.new("Sparkles")



sc.Parent = sparkles



end



print("Children:", #part:GetChildren())  --> Children: 3



part:ClearAllChildren()



print("Children:", #part:GetChildren())  --> Children: 0
```

If you do not wish to destroy all children and descendants, use either
[Instance:GetChildren()](/docs/reference/engine/classes/Instance#GetChildren) or [Instance:GetDescendants()](/docs/reference/engine/classes/Instance#GetDescendants) to
loop through those children/descendants and select what to destroy. For
example, the following code sample will destroy all
[BaseParts](/docs/reference/engine/classes/BasePart) descending from a [Model](/docs/reference/engine/classes/Model):

```
local Workspace = game:GetService("Workspace")



local model = Workspace:FindFirstChild("TestModel")



for _, descendant in model:GetDescendants() do



if descendant:IsA("BasePart") then



descendant:Destroy()



end



end
```

Provide feedback

---

Clone

Create a copy of an instance and all its descendants, ignoring instances
that are not [Archivable](/docs/reference/engine/classes/Instance#Archivable).

Instance:Clone():[Instance](/docs/reference/engine/datatypes/Instance)

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Clone() creates a copy of an instance and all of its descendants,
ignoring all instances that are not
[Archivable](/docs/reference/engine/classes/Instance#Archivable). The copy of the root instance is
returned by this method and its [Parent](/docs/reference/engine/classes/Instance#Parent) is set to
nil. Note that if the instance itself has
[Archivable](/docs/reference/engine/classes/Instance#Archivable) set to false, this method will
return nil.

If a reference property such as [ObjectValue.Value](/docs/reference/engine/classes/ObjectValue#Value) is set in a
cloned instance, the value of the copy's property depends on the
original's value:

* If a reference property refers to an instance that was also cloned,
  the copy will refer to the copy.
* If a reference property refers to an instance that was not cloned,
  the same value is maintained in the copy.

Code Samples

Cloning an Instance

Demonstrates cloning a model using [Instance:Clone()](/docs/reference/engine/classes/Instance#Clone).

```
local Workspace = game:GetService("Workspace")



-- Get a reference to an existing object



local model = script.Parent.Model



-- Create a clone of the model



local clone = model:Clone()



-- Move the clone so it's not overlapping the original model



clone:PivotTo(model.PrimaryPart.CFrame - (Vector3.xAxis * 10))



-- Add the clone to the Workspace



clone.Parent = Workspace
```

Provide feedback

---

clone

Deprecated

Show details

---

Destroy

Sets the [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) property to nil, locks the
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) property, disconnects all connections, and calls
Destroy() on all children.

Instance:Destroy():()

Returns

()

Sets the [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) property to nil, locks the
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) property, disconnects all connections, and calls
Destroy() on all children. This method is the correct way to dispose of
objects that are no longer required.

Disposing of unneeded objects is important, since unnecessary objects and
connections in a place use up memory which can lead to serious performance
issues over time.

As a best practice after calling Destroy() on an object, set any
variables referencing the object (or its descendants) to nil. This
prevents your code from accessing anything to do with the object.

```
local part = Instance.new("Part")



part.Name = "Hello, world"



part:Destroy()



-- Don't do this:



print(part.Name)  --> "Hello, world"



-- Do this to prevent the above line from working:



part = nil
```

Once an [Instance](/docs/reference/engine/classes/Instance) has been destroyed by this method, it cannot be
reused because the [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) property is locked. To
temporarily remove an object instead of destroying it, set
[Parent](/docs/reference/engine/classes/Instance#Parent) to nil. For example:

```
local Workspace = game:GetService("Workspace")



object.Parent = nil



task.wait(2)



object.Parent = Workspace
```

To destroy an object after a set amount of time, use
[Debris:AddItem()](/docs/reference/engine/classes/Debris#AddItem).

Code Samples

Instance:Destroy()

Demonstrates destroying a Part using the [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy) function.

This function is the correct way to dispose of objects that are no longer required.

```
local part = script.Parent.Part



part:Destroy()
```

Provide feedback

---

destroy

Deprecated

Show details

---

FindFirstAncestor

Write Parallel

Returns the first ancestor of the [Instance](/docs/reference/engine/classes/Instance) whose
[Instance.Name](/docs/reference/engine/classes/Instance#Name) is equal to the given name.

Instance:FindFirstAncestor(name:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The [Instance.Name](/docs/reference/engine/classes/Instance#Name) to be looked for. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the first ancestor of the [Instance](/docs/reference/engine/classes/Instance) whose
[Instance.Name](/docs/reference/engine/classes/Instance#Name) is equal to the given name.

This method works upwards, meaning it starts at the instance's immediate
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) and works up towards the [DataModel](/docs/reference/engine/classes/DataModel). If no
matching ancestor is found, it returns nil.

The following code snippet would find the first ancestor of the object
named Car.

```
local car = object:FindFirstAncestor("Car")
```

For variants of this method that find ancestors of a specific class,
please see [Instance:FindFirstAncestorOfClass()](/docs/reference/engine/classes/Instance#FindFirstAncestorOfClass) and
[Instance:FindFirstAncestorWhichIsA()](/docs/reference/engine/classes/Instance#FindFirstAncestorWhichIsA).

Provide feedback

---

FindFirstAncestorOfClass

Write Parallel

Returns the first ancestor of the [Instance](/docs/reference/engine/classes/Instance) whose
[Object.ClassName](/docs/reference/engine/classes/Object#ClassName) is equal to the given className.

Instance:FindFirstAncestorOfClass(className:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  The [Object.ClassName](/docs/reference/engine/classes/Object#ClassName) to be looked for. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the first ancestor of the [Instance](/docs/reference/engine/classes/Instance) whose
[Object.ClassName](/docs/reference/engine/classes/Object#ClassName) is equal to the given className.

This method works upwards, meaning it starts at the instance's immediate
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) and works up towards the [DataModel](/docs/reference/engine/classes/DataModel). If no
matching ancestor is found, it returns nil.

A common use of this method is finding the [Model](/docs/reference/engine/classes/Model) a
[BasePart](/docs/reference/engine/classes/BasePart) belongs to. For example:

```
local model = part:FindFirstAncestorOfClass("Model")
```

This method is a variant of [Instance:FindFirstAncestor()](/docs/reference/engine/classes/Instance#FindFirstAncestor) which
checks the [Object.ClassName](/docs/reference/engine/classes/Object#ClassName) property rather than
[Instance.Name](/docs/reference/engine/classes/Instance#Name). [Instance:FindFirstAncestorWhichIsA()](/docs/reference/engine/classes/Instance#FindFirstAncestorWhichIsA) also
exists, using the [Object:IsA()](/docs/reference/engine/classes/Object#IsA) method instead to respect class
inheritance.

Provide feedback

---

FindFirstAncestorWhichIsA

Write Parallel

Returns the first ancestor of the [Instance](/docs/reference/engine/classes/Instance) for whom
[Object:IsA()](/docs/reference/engine/classes/Object#IsA) returns true for the given className.

Instance:FindFirstAncestorWhichIsA(className:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  The [Object.ClassName](/docs/reference/engine/classes/Object#ClassName) to be looked for. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the first ancestor of the [Instance](/docs/reference/engine/classes/Instance) for whom
[Object:IsA()](/docs/reference/engine/classes/Object#IsA) returns true for the given className.

This method works upwards, meaning it starts at the instance's immediate
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) and works up towards the [DataModel](/docs/reference/engine/classes/DataModel). If no
matching ancestor is found, it returns nil.

Unlike [Instance:FindFirstAncestorOfClass()](/docs/reference/engine/classes/Instance#FindFirstAncestorOfClass), this method uses
[Object:IsA()](/docs/reference/engine/classes/Object#IsA) which respects class inheritance. For example:

```
print(part:IsA("Part"))  --> true



print(part:IsA("BasePart"))  --> true



print(part:IsA("Instance"))  --> true
```

Therefore, the following code sample will return the first
[BasePart](/docs/reference/engine/classes/BasePart) ancestor, regardless of if it is a [WedgePart](/docs/reference/engine/classes/WedgePart),
[MeshPart](/docs/reference/engine/classes/MeshPart) or [Part](/docs/reference/engine/classes/Part).

```
local part = object:FindFirstAncestorWhichIsA("BasePart")
```

See also [Instance:FindFirstAncestor()](/docs/reference/engine/classes/Instance#FindFirstAncestor).

Provide feedback

---

FindFirstChild

Write Parallel

Returns the first child of the [Instance](/docs/reference/engine/classes/Instance) found with the given name.

Instance:FindFirstChild(

name:[string](/docs/luau/strings), recursive:[boolean](/docs/luau/booleans)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The [Instance.Name](/docs/reference/engine/classes/Instance#Name) to be searched for. |
| recursive:[boolean](/docs/luau/booleans) Default Value: false Whether or not the search should be conducted recursively. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the first child of the [Instance](/docs/reference/engine/classes/Instance) with the given name, or
nil if no such child exists. If the optional recursive argument is
true, this method searches all descendants rather than only the
immediate children of the [Instance](/docs/reference/engine/classes/Instance).

##### Checking the Existence of an Object

FindFirstChild() is necessary if you need to verify an object exists
before continuing. Attempting to index a child by name using the dot
operator throws an error if the child doesn't exist.

```
local Workspace = game:GetService("Workspace")



-- The following line errors if the part doesn't exist in the workspace



Workspace.Part.Transparency = 0.5
```

A better approach is to use FindFirstChild() to first check for Part,
then use an if statement to run code that needs it.

```
local Workspace = game:GetService("Workspace")



local part = Workspace:FindFirstChild("Part")



if part then



part.Transparency = 0.5



end
```

##### Finding a Child Whose Name Matches a Property

Sometimes the [Name](/docs/reference/engine/classes/Instance#Name) of an object is the same as that
of a property of its [Parent](/docs/reference/engine/classes/Instance#Parent). When using the dot
operator, properties take precedence over children if they share a name.

In the following example, a [Folder](/docs/reference/engine/classes/Folder) called Color is added to a
[Part](/docs/reference/engine/classes/Part), which also has the [Part.Color](/docs/reference/engine/classes/Part#Color) property. Notice that
part.Color refers to the [Color3](/docs/reference/engine/datatypes/Color3) property value, not the child
[Folder](/docs/reference/engine/classes/Folder) instance. A benefit of using
[FindFirstChild()](/docs/reference/engine/classes/Instance#FindFirstChild) is that the
introduction of new properties does not impose a risk on your code.

```
local part = Instance.new("Part")



local folder = Instance.new("Folder")



folder.Name = "Color"



folder.Parent = part



local c1 = part.Color  -- The property



local c2 = part:FindFirstChild("Color")  -- The child folder
```

##### Performance Notes

[FindFirstChild()](/docs/reference/engine/classes/Instance#FindFirstChild) takes about 20% longer
than using the dot operator and almost 8 times longer than simply storing
a reference to an object. Therefore, you should avoid calling it in
performance-dependent code such as in tight loops or functions connected
to [RunService.Heartbeat](/docs/reference/engine/classes/RunService#Heartbeat) and [RunService.PreRender](/docs/reference/engine/classes/RunService#PreRender). Instead,
store the result in a variable, or consider using
[ChildAdded](/docs/reference/engine/classes/Instance#ChildAdded) or
[WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild) to detect when a child of a
given name becomes available.

Code Samples

Instance:FindFirstChild

The below would look in Workspace for an object name "Brick". If found, it
will change the name of the object to "Foo".

```
local found = workspace:FindFirstChild("Brick")



if found then



found.Name = "Foo"



end
```

Provide feedback

---

findFirstChild

Deprecated

Show details

---

FindFirstChildOfClass

Write Parallel

Returns the first child of the [Instance](/docs/reference/engine/classes/Instance) whose
[ClassName](/docs/reference/engine/classes/Object#ClassName) is equal to the given class name.

Instance:FindFirstChildOfClass(className:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  The [Object.ClassName](/docs/reference/engine/classes/Object#ClassName) to be looked for. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the first child of the [Instance](/docs/reference/engine/classes/Instance) whose
[ClassName](/docs/reference/engine/classes/Object#ClassName) is equal to the given className.
Unlike [Instance:FindFirstChildWhichIsA()](/docs/reference/engine/classes/Instance#FindFirstChildWhichIsA), this method only returns
objects whose class matches className, ignoring class inheritance. If no
matching child is found, this method returns nil.

Code Samples

Instance:FindFirstChildOfClass

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid



while not humanoid do



humanoid = character:FindFirstChildOfClass("Humanoid")



if not humanoid then



character.ChildAdded:Wait()



end



end
```

Provide feedback

---

FindFirstChildWhichIsA

Write Parallel

Returns the first child of the [Instance](/docs/reference/engine/classes/Instance) for whom
[Object:IsA()](/docs/reference/engine/classes/Object#IsA) returns true for the given className.

Instance:FindFirstChildWhichIsA(

className:[string](/docs/luau/strings), recursive:[boolean](/docs/luau/booleans)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  The [Object.ClassName](/docs/reference/engine/classes/Object#ClassName) to be searched for. |
| recursive:[boolean](/docs/luau/booleans) Default Value: false Whether or not the search should be conducted recursively. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the first child of the [Instance](/docs/reference/engine/classes/Instance) for whom
[Object:IsA()](/docs/reference/engine/classes/Object#IsA) returns true for the given className.

If no matching child is found, this method returns nil. If the optional
recursive argument is true, this method searches all descendants rather
than only the immediate children of the [Instance](/docs/reference/engine/classes/Instance).

Unlike [Instance:FindFirstChildOfClass()](/docs/reference/engine/classes/Instance#FindFirstChildOfClass), this method uses
[Object:IsA()](/docs/reference/engine/classes/Object#IsA) which respects class inheritance. For example:

```
print(part:IsA("Part")) --> true



print(part:IsA("BasePart")) --> true



print(part:IsA("Instance")) --> true
```

Therefore, the following code sample will return the first
[BasePart](/docs/reference/engine/classes/BasePart) child, regardless of if it is a [WedgePart](/docs/reference/engine/classes/WedgePart),
[MeshPart](/docs/reference/engine/classes/MeshPart) or [Part](/docs/reference/engine/classes/Part).

```
local part = object:FindFirstChildWhichIsA("BasePart")
```

Developers looking for a child by name, should use
[Instance:FindFirstChild()](/docs/reference/engine/classes/Instance#FindFirstChild) instead.

Provide feedback

---

FindFirstDescendant

Write Parallel

Returns the first descendant found with the given [Instance.Name](/docs/reference/engine/classes/Instance#Name).

Instance:FindFirstDescendant(name:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The [Instance.Name](/docs/reference/engine/classes/Instance#Name) to search for. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the first descendant found with the given [Instance.Name](/docs/reference/engine/classes/Instance#Name).

This method is disabled and cannot be used. To find the first descendant
of an instance, consider using the recursive parameter on
[Instance:FindFirstChild()](/docs/reference/engine/classes/Instance#FindFirstChild) instead.

Provide feedback

---

GetActor

Write Parallel

Returns the [Actor](/docs/reference/engine/classes/Actor) associated with the Instance, if any.

Instance:GetActor():[Actor](/docs/reference/engine/classes/Actor)?

Returns

[Actor](/docs/reference/engine/classes/Actor)?

The [Actor](/docs/reference/engine/classes/Actor) found.

If the [Instance](/docs/reference/engine/classes/Instance) is an [Actor](/docs/reference/engine/classes/Actor), the [Actor](/docs/reference/engine/classes/Actor) itself is
returned. Otherwise, its closest ancestor [Actor](/docs/reference/engine/classes/Actor) is returned. If no
ancestor is an [Actor](/docs/reference/engine/classes/Actor), the result is nil.

Provide feedback

---

GetAttribute

Write Parallel

Returns the value which has been assigned to the given attribute name.

Instance:GetAttribute(attribute:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| attribute:[string](/docs/luau/strings)  The name of the attribute being retrieved. |

Returns

Variant

The value which has been assigned to the given attribute name. If no
attribute has been assigned, nil is returned.

This method returns the value which has been assigned to the given
attribute name. If no attribute has been assigned, nil is returned.

For example, the following code snippet sets and then gets the value of
the instance's InitialPosition attribute:

```
local Workspace = game:GetService("Workspace")



local part = Workspace.Part



part:SetAttribute("InitialPosition", part.Position)



local initialPosition = instance:GetAttribute("InitialPosition")



print(initialPosition)
```

##### See Also

* [Instance:SetAttribute()](/docs/reference/engine/classes/Instance#SetAttribute) which sets the attribute with the given
  name to the given value.
* [Instance:GetAttributes()](/docs/reference/engine/classes/Instance#GetAttributes) which returns a dictionary of key‑value
  pairs for each of the instance's attributes.

Provide feedback

---

GetAttributeChangedSignal

Returns an event that fires when the given attribute changes.

Instance:GetAttributeChangedSignal(attribute:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| attribute:[string](/docs/luau/strings)  The name of the specified attribute for which the change signal is being returned. |

Returns

[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

An event that fires when the given attribute changes.

This method returns an event that behaves exactly like the
[Changed](/docs/reference/engine/classes/Object#Changed) event, except that it only fires when the
specific given attribute changes; effectively it is similar to
[GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal) but
for attributes.

It's generally a good idea to use this method instead of a connection to
[Changed](/docs/reference/engine/classes/Object#Changed) with a function that checks the attribute
name. Subsequent calls to this method on the same object with the same
attribute name return the same event.

The following code example returns a signal that fires the function
attributeChanged() when the part's InitialPosition attribute changes:

```
local Workspace = game:GetService("Workspace")



local part = Workspace.Part



part:SetAttribute("InitialPosition", part.Position)



local function attributeChanged()



print("Attribute changed")



end



part:GetAttributeChangedSignal("InitialPosition"):Connect(attributeChanged)
```

See also [Instance.AttributeChanged](/docs/reference/engine/classes/Instance#AttributeChanged) which fires whenever any
attribute is changed on the instance.

Provide feedback

---

GetAttributes

Write Parallel

Returns a dictionary of the instance's attributes.

Instance:GetAttributes():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary of string → variant pairs for each attribute where the
string is the name of the attribute and the variant is a non-nil
value.

This method returns a dictionary of key‑value pairs for each attribute
where the key is the attribute's name and the value is a non‑nil value.

For example, the following code snippet outputs an instance's attributes
and values:

```
local Workspace = game:GetService("Workspace")



local part = Workspace.Part



part:SetAttribute("InitialPosition", part.Position)



part:SetAttribute("CanUse", true)



for name, value in part:GetAttributes() do



print(name .. " = " .. value)



end
```

See also [Instance:GetAttribute()](/docs/reference/engine/classes/Instance#GetAttribute) which returns the value that has
been assigned to the given attribute name.

Provide feedback

---

GetChildren

Write Parallel

Returns an array containing all of the instance's children.

Instance:GetChildren():Instances

Returns

Instances

An array containing the instance's children.

Returns an array (a numerically indexed table) containing all of the
instance's direct children, or every [Instance](/docs/reference/engine/classes/Instance) whose
[Parent](/docs/reference/engine/classes/Instance#Parent) is equal to the object. The array can be
iterated upon using either a numeric or generic for loop:

```
local Workspace = game:GetService("Workspace")



-- Numeric loop example



local children = Workspace:GetChildren()



for i = 1, #children do



local child = children[i]



print(child.Name .. " is child number " .. i)



end
```

```
local Workspace = game:GetService("Workspace")



-- Generic loop example



local children = Workspace:GetChildren()



for i, child in children do



print(child.Name .. " is child number " .. i)



end
```

Note that the returned array is not sorted in any particular order, so
manual sorting (for example using [table.sort()](/docs/reference/engine/libraries/table#sort)) is advised for
sorting the children returned by this method.

See also the [GetDescendants()](/docs/reference/engine/classes/Instance#GetDescendants) method.

Code Samples

Instance:GetChildren

The below would print the name of all objects currently in Workspace when ran.

```
local children = workspace:GetChildren()



for i = 1, #children do



print(i, children[i].Name)



end
```

Provide feedback

---

getChildren

Deprecated

Show details

---

GetDebugId

Not Browsable

Plugin Security

Returns a coded string of the debug ID used internally by Roblox.

Instance:GetDebugId(scopeLength:[number](/docs/luau/numbers)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| scopeLength:[number](/docs/luau/numbers) Default Value: 4 The scope length. |

Returns

[string](/docs/luau/strings)

The Debug ID string.

Returns a coded string of the debug ID used internally by Roblox. Note
that:

* This item is protected. Attempting to use it in a [Script](/docs/reference/engine/classes/Script) or
  [LocalScript](/docs/reference/engine/classes/LocalScript) will cause an error.
* A debug ID is an ID used in debugging processes. It allows a debugger to
  read each instruction before an application processes it. All objects in
  Roblox act like processes and each run instructions (or 'code') that can
  be debugged if needed.
* This can be helpful for plugins which need to distinguish similar
  objects from one-another (such as objects that share the same name).

Code Samples

Instance:GetDebugId

```
print(workspace:GetDebugId()) --> 39FA_12



print(workspace:GetDebugId(10)) --> 39FA2FEF4D_12



print(workspace:GetDebugId(math.huge)) --> 12
```

Provide feedback

---

GetDescendants

Write Parallel

Returns an array containing all of the descendants of the instance.

Instance:GetDescendants():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array containing the instance's descendants.

This object method returns an array that contains all of the descendants
of that object. Unlike [Instance:GetChildren()](/docs/reference/engine/classes/Instance#GetChildren), which only returns
the immediate children of an object, this method finds every child of the
object, every child of those children, and so on.

Note that the returned array is not sorted in any particular order, so
manual sorting (for example using [table.sort()](/docs/reference/engine/libraries/table#sort)) is advised for
sorting the descendants returned by this method. Also consdier the
[QueryDescendants()](/docs/reference/engine/classes/Instance#QueryDescendants) method to query
descendants by a combination of selectors and combinators.

Code Samples

Instance:GetDescendants

GetDescendants is often used to do something to all the descendants that are a
particular type of object. The code in this example uses GetDescendants and
[Instance:IsA()](/docs/reference/engine/classes/Instance#IsA) to find all of the parts in the workspace and turns
them green.

```
local descendants = workspace:GetDescendants()



-- Loop through all of the descendants of the Workspace. If a



-- BasePart is found, the code changes that parts color to green



for _, descendant in pairs(descendants) do



if descendant:IsA("BasePart") then



descendant.BrickColor = BrickColor.Green()



end



end
```

Provide feedback

---

GetFullName

Write Parallel

Returns a string describing the instance's ancestry.

Instance:GetFullName():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

The full name of the [Instance](/docs/reference/engine/classes/Instance).

Returns a string describing the instance's ancestry. The string is a
concatenation of the [Name](/docs/reference/engine/classes/Instance#Name) of the object and its
ancestors, separated by periods. The [DataModel](/docs/reference/engine/classes/DataModel) (game) is not
considered. For example, a [Part](/docs/reference/engine/classes/Part) in the [Workspace](/docs/reference/engine/classes/Workspace) may
return [Workspace.Part](/docs/reference/engine/classes/Workspace#Part).

When called on an [Instance](/docs/reference/engine/classes/Instance) that is not a descendant of the
[DataModel](/docs/reference/engine/classes/DataModel), this method considers all ancestors up to and including
the topmost one without a [Parent](/docs/reference/engine/classes/Instance#Parent).

This method is useful for logging and debugging. You shouldn't attempt to
parse the returned string for any useful operation; this method does not
escape periods (or any other symbol) in object names. In other words,
although its output often appears to be a valid Luau identifier, it is not
guaranteed.

Code Samples

Instance:GetFullName

This code sample demonstrates the behavior of [Instance:GetFullName()](/docs/reference/engine/classes/Instance#GetFullName).
It shows how the function behaves when called on an object not in the
DataModel hierarchy, and it also shows how the return value does not escape
special characters.

```
-- Create a simple hierarchy



local model = Instance.new("Model")



local part = Instance.new("Part")



part.Parent = model



local fire = Instance.new("Fire")



fire.Parent = part



print(fire:GetFullName()) --> Model.Part.Fire



model.Parent = workspace



print(fire:GetFullName()) --> Workspace.Model.Part.Fire



part.Name = "Hello, world"



print(fire:GetFullName()) --> Workspace.Model.Hello, world.Fire
```

Instance:GetFullName Lua Implementation

This code sample re-implements the [Instance:GetFullName()](/docs/reference/engine/classes/Instance#GetFullName) function in
Lua.

```
local function getFullName(object)



local result = object.Name



object = object.Parent



while object and object ~= game do



-- Prepend parent name



result = object.Name .. "." .. result



-- Go up the hierarchy



object = object.Parent



end



return result



end



print(getFullName(workspace.Camera)) --> Workspace.Camera
```

Provide feedback

---

GetStyled

Returns the styled or explicitly modified value of the specified property,
or else the default property value if it hasn't been styled/modified.

Instance:GetStyled(name:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Name of the property to query. |

Returns

Variant

The styled or explicitly modified value of the specified property, or
else the default property value if it hasn't been styled/modified.

This method returns the styled or explicitly modified value of the
specified property, or else the default property value if it hasn't been
styled/modified. This differs slightly from accessing the property value
directly, such as [GuiObject].Rotation, which returns the default or
modified value of the property.

```
local Players = game:GetService("Players")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local player = Players.LocalPlayer



local playerGui = player.PlayerGui



local HUDContainer = playerGui:WaitForChild("HUDContainer")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



local rule = coreSheet:FindFirstChildWhichIsA("StyleRule")



rule.Selector = "TextButton"



-- Reference to a button



local button = HUDContainer:FindFirstChildWhichIsA("TextButton")



print(button:GetStyled("Rotation")) --> 0 (default value)



print(button.Rotation) --> 0 (default value)



-- Apply rotation through style rule property



rule:SetProperty("Rotation", 30)



print(button:GetStyled("Rotation")) --> 30 (styled value based on rule)



print(button.Rotation) --> 0 (default value)



-- Explicitly modify/override styled property



button.Rotation = 45



print(button:GetStyled("Rotation")) --> 45 (modified value)



print(button.Rotation) --> 45 (modified value)
```

Provide feedback

---

GetStyledPropertyChangedSignal

Instance:GetStyledPropertyChangedSignal(property:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| property:[string](/docs/luau/strings)  Name of the style property for which to listen for changes. |

Returns

[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Event that fires when the given style property changes.

This method returns an event that behaves exactly like the
[StyledPropertiesChanged](/docs/reference/engine/classes/Instance#StyledPropertiesChanged) event,
except that it only fires when the given style property changes. It's
generally a good idea to use this method instead of a connection to
[StyledPropertiesChanged](/docs/reference/engine/classes/Instance#StyledPropertiesChanged) with a
function that checks the property name. Subsequent calls to this method on
the same object with the same property name return the same event.

Note that this event will not pass any arguments to a connected function,
so the value of the changed property must be read directly within a
script.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local playerGui = player.PlayerGui



local HUDContainer = playerGui:WaitForChild("HUDContainer")



local meterBar = HUDContainer.MeterBar



local function stylePropertyChanged()



print("Style property changed!")



end



meterBar:GetStyledPropertyChangedSignal("AnchorPoint"):Connect(stylePropertyChanged)
```

Provide feedback

---

GetTags

Write Parallel

Gets an array of all tags applied to the instance.

Instance:GetTags():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

This method returns an array of the tags applied to the given instance, as
strings. You can add tags either in Studio in the
[Properties](/docs/studio/properties) window or at runtime with
[AddTag()](/docs/reference/engine/classes/Instance#AddTag).

This method is useful when you want to do something with multiple tags on
an instance at once. However, it is inefficient to use this method to
check for the existence of a single tag; instead, use
[HasTag()](/docs/reference/engine/classes/Instance#HasTag) to check for a specific tag.

Provide feedback

---

HasTag

Write Parallel

Check whether the instance has a given tag.

Instance:HasTag(tag:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

This method returns true if the provided tag has been added to the
object. You can add tags either in Studio in the
[Properties](/docs/studio/properties) window or at runtime with
[AddTag()](/docs/reference/engine/classes/Instance#AddTag).

Provide feedback

---

IsAncestorOf

Write Parallel

Returns true if an [Instance](/docs/reference/engine/classes/Instance) is an ancestor of the given
descendant.

Instance:IsAncestorOf(descendant:[Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| descendant:[Instance](/docs/reference/engine/datatypes/Instance)  The descendant [Instance](/docs/reference/engine/classes/Instance). |

Returns

[boolean](/docs/luau/booleans)

True if the [Instance](/docs/reference/engine/classes/Instance) is an ancestor of the given descendant.

Returns true if an [Instance](/docs/reference/engine/classes/Instance) is an ancestor of the given
descendant.

An [Instance](/docs/reference/engine/classes/Instance) is considered the ancestor of an object if the
object's [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) or one of it's parent's
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) is set to the [Instance](/docs/reference/engine/classes/Instance).

See also, [Instance:IsDescendantOf()](/docs/reference/engine/classes/Instance#IsDescendantOf).

Code Samples

Instance:IsAncestorOf()

Demonstrates determining if one instance is the ancestor of another using [Instance:IsAncestorOf()](/docs/reference/engine/classes/Instance#IsAncestorOf)

Workspace and SpawnLocation are ancestors of the SpawnLocation's decal.
Workspace is an ancestor of SpawnLocation.

SpawnLocation and its decal are descendants of Workspace, not ancenstors.
Decal is a descendant to SpawnLocation, not an ancestor.

```
local Workspace = game:GetService("Workspace")



local spawnLocation = Workspace.SpawnLocation



local decal = spawnLocation.Decal



-- These statements are true



print(Workspace:IsAncestorOf(spawnLocation))



print(Workspace:IsAncestorOf(decal))



print(spawnLocation:IsAncestorOf(decal))



-- These statements are false



print(spawnLocation:IsAncestorOf(Workspace))



print(decal:IsAncestorOf(Workspace))



print(decal:IsAncestorOf(spawnLocation))
```

Provide feedback

---

IsDescendantOf

Write Parallel

Returns true if an [Instance](/docs/reference/engine/classes/Instance) is a descendant of the given
ancestor.

Instance:IsDescendantOf(ancestor:[Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| ancestor:[Instance](/docs/reference/engine/datatypes/Instance)  The ancestor [Instance](/docs/reference/engine/classes/Instance). |

Returns

[boolean](/docs/luau/booleans)

True if the [Instance](/docs/reference/engine/classes/Instance) is a descendant of the given ancestor.

Returns true if an [Instance](/docs/reference/engine/classes/Instance) is a descendant of the given
ancestor.

Note that IsDescendantOf() cannot be used with a parameter of nil to
check if an object has been removed.

See also [Instance:IsAncestorOf()](/docs/reference/engine/classes/Instance#IsAncestorOf).

Code Samples

Instance:IsDescendantOf

```
local part = Instance.new("Part")



print(part:IsDescendantOf(game))



--> false



part.Parent = workspace



print(part:IsDescendantOf(game))



--> true



part.Parent = game



print(part:IsDescendantOf(game))



--> true
```

Provide feedback

---

isDescendantOf

Deprecated

Show details

---

IsPropertyModified

Returns true if the value stored in the specified property is not equal
to the code-instantiated default.

Instance:IsPropertyModified(property:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| property:[string](/docs/luau/strings)  Name of the property to query. |

Returns

[boolean](/docs/luau/booleans)

Boolean indicating whether the property is modified from its
code‑instantiated default.

This method indicates whether a specific property has been modified from
the code‑instantiated default. If called on an instance newly created via
code ([Instance.new()](/docs/reference/engine/datatypes/Instance#new)), this method will return false. If
called on an object newly created by Studio workflows such as
[Explorer](/docs/studio/explorer) window insertion, the result may
differ.

For example, querying the
[BackgroundColor3](/docs/reference/engine/classes/TextLabel#BackgroundColor3) property of a
[TextLabel](/docs/reference/engine/classes/TextLabel) inserted via the [Explorer](/docs/studio/explorer)
will return true, but querying the same property of a [TextLabel](/docs/reference/engine/classes/TextLabel)
created through [Instance.new()](/docs/reference/engine/datatypes/Instance#new) will return false, assuming no
other changes were made to its
[BackgroundColor3](/docs/reference/engine/classes/TextLabel#BackgroundColor3).

Note that if this method returns true, styling will not affect the
property because explicitly modifying a property takes precedence over
styling it. To reset a property to its code‑instantiated default and allow
styling on it, use
[ResetPropertyToDefault()](/docs/reference/engine/classes/Instance#ResetPropertyToDefault).

Provide feedback

---

QueryDescendants

Instance:QueryDescendants(selector:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| selector:[string](/docs/luau/strings)  Selector string used to filter elements. |

Returns

Instances

An array of instances (empty if nothing matched the selector).

This object method returns an array which contains the descendants of that
object matching the provided selector string. The selector string can
include multiple selectors and combinators to match characteristics such
as the class name, instance name, hierarchy relationships, as well as
specific values of instance properties and attributes. The selector
grammar is similar to the one used in [StyleRule](/docs/reference/engine/classes/StyleRule) with only a few
differences regarding which parts of the grammar are supported or not.

#### Selectors

| Selector | Description | Examples |
| --- | --- | --- |
| ClassName | Matches instances of the specified class in a [Object:IsA()](/docs/reference/engine/classes/Object#IsA) relationship. | SpotLight ImageButton Part |
| .Tag | Matches instances tagged with a [CollectionService](/docs/reference/engine/classes/CollectionService) tag. | .Fruit .IntenseLight |
| #Name | Matches instances of a specific [Instance.Name](/docs/reference/engine/classes/Instance#Name). | #RedTree #CloseButton |
| [property = value] | Matches instances which have the specified property and that property has the specified value. Boolean, number, and string values are supported. Letters, numbers, \_, and - can be used without putting the value in quotation marks. | [CanCollide = false]  [Brightness = "0.5"]  [Name = Folder10]  [Name = "Part.10"] |
| [$attribute = value] | Matches instances which have the specified attribute and that attribute has the specified value. Same limitations apply as for property selectors. | [$MyAttribute = 10] |
| [$attribute] | Matches instances which have the specified attribute set. | [$MyAttribute] |
| :not(complex-selector-list) | Pseudo-class selector that matches instances which do **not** match any of the specified selectors. | See examples below |
| :has(relative-selector-list) | Pseudo-class selector that matches instances which contain an instance matching the specified selector. | See examples below |

Note that selectors can be combined. For example,
Model.Apple[$Kind = "Red"][$State = 4] will match instances which are a
[Model](/docs/reference/engine/classes/Model) with a tag Apple set and which have a Kind attribute
equal to string "Red" as well as a State attribute equal to 4.

#### Combinators

| Combinator | Description | Examples |
| --- | --- | --- |
| > | Matches instances that are **direct children** of the previous filter matches. | Part > .SwordHandle |
| >> | Matches instances that are **descendants** of the previous filter matches. | Model >> .TreeOnFire |
| , | Specifies a list of multiple independent selectors for the descendant query. | Part.TagA, Part[$UseForce = true] |

Note that the default first filter is a descendant combinator >>. If the
selector starts with a >, only children are visited; for example
>Part.Apple selects direct children which are a [Part](/docs/reference/engine/classes/Part) and
have a tag Apple.

The default combinator can also be specified explicitly, as in
>>SpotLight.Red is the same as SpotLight.Red.

Only elements matching the filter are placed in the array. For example,
>#ExistingChild, >#MissingChild, >#AnotherExistingChild will return an
array with two elements and there will be no nil for the missing child.

#### Pseudo-class selectors

##### :not(complex-selector-list)

This pseudo-class selector allows selecting instances which do not
match any of the selectors inside. It performs a negation of the
selectors.

Starting with the simple cases: it is possible to query instances that do
not match the specified class using :not(SpotLight), or instances which
do not have an attribute set using :not([$MyAttribute]).

The expression inside is a list of complex selectors, so it is possible to
filter based on multiple conditions. For example,
:not(SpotLight, PointLight) will select all instances that are not a
[SpotLight](/docs/reference/engine/classes/SpotLight) or a [PointLight](/docs/reference/engine/classes/PointLight). This can also be written as
:not(SpotLight):not(PointLight).

You can also use selectors with combinators. For example, given that the
expression Model > .Red will select all descendants that are a child of
a [Model](/docs/reference/engine/classes/Model) and have a 'Red' tag, :not(Model > .Red) will select all
descendants except for those.

##### :has(relative-selector-list)

This pseudo-class selector allows selecting instances based on which
instances they contain inside. The selector list is evaluated relative to
each instance.

For example :has(Tool) will select all descendants which contain 'Tool'
as their own descendant.

To see the difference, consider the expression SpotLight > .Red which
selects descendants with the 'Red' tag that are a child of a SpotLight.
Using SpotLight:has(> .Red), it is possible to select descendants that
are SpotLight instances and contain an instance with the 'Red' tag
inside.

Provide feedback

---

Remove

Deprecated

Show details

---

remove

Deprecated

Show details

---

RemoveTag

Removes a tag from the instance.

Instance:RemoveTag(tag:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings) |

Returns

()

This method removes a tag from an instance. It will not throw an error if
the object does not have the tag. Successfully removing a tag will fire a
signal created by [CollectionService:GetInstanceRemovedSignal()](/docs/reference/engine/classes/CollectionService#GetInstanceRemovedSignal)
with the given tag.

Note that when tagging an instance, it's common that some resources are
used to give the tag its functionality, for example event connections or
tables. To prevent memory leaks, it's a good idea to clean these up
(disconnect, set to nil, etc.) when no longer needed for a tag.

Provide feedback

---

ResetPropertyToDefault

Resets a property to its default value.

Instance:ResetPropertyToDefault(property:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| property:[string](/docs/luau/strings)  Name of the property to reset. |

Returns

()

Resets a property to its default value. For example, calling
ResetPropertyToDefault("Rotation") on a [TextLabel](/docs/reference/engine/classes/TextLabel) is equivalent
to setting its [Rotation](/docs/reference/engine/classes/TextLabel#Rotation) to 0 (the property's
default value). This method can be used to ensure styling will override
this property's default value.

Provide feedback

---

SetAttribute

Sets the attribute with the given name to the given value.

Instance:SetAttribute(

attribute:[string](/docs/luau/strings), value:Variant

):()

Parameters

|  |
| --- |
| attribute:[string](/docs/luau/strings)  The name of the attribute being set. |
| value:Variant  The value to set the specified attribute to. |

Returns

()

This method sets the attribute with the given name to the given value. If
the value given is nil, the attribute will be removed, since nil is
returned by default.

For example, the following code snippet sets the instance's
InitialPosition attribute to [Vector3.new(0, 10, 0)](/docs/reference/engine/datatypes/Vector3):

```
local Workspace = game:GetService("Workspace")



local part = Workspace.Part



part:SetAttribute("InitialPosition", Vector3.new(0, 10, 0))
```

##### Limitations

Naming requirements and restrictions:

* Names must only use alphanumeric characters.
  + You may also include periods, hyphens, slashes, and underscores.
* No spaces or unique symbols (such as @, ~, !) are allowed.
* Strings must be 100 characters or less.
* Names are not allowed to start with RBX unless the caller is a
  Roblox core script (reserved for Roblox).

When attempting to set an attribute to an unsupported type, an error will
be thrown.

##### See Also

* [Instance:GetAttribute()](/docs/reference/engine/classes/Instance#GetAttribute) which returns the value that has been
  assigned to the given attribute name.
* [Instance:GetAttributes()](/docs/reference/engine/classes/Instance#GetAttributes) which returns a dictionary of key‑value
  pairs for each of the instance's attributes.

Provide feedback

---

WaitForChild

Can Yield

Returns the child of the [Instance](/docs/reference/engine/classes/Instance) with the given name. If the
child does not exist, it will yield the current thread until it does.

Instance:WaitForChild(

childName:[string](/docs/luau/strings), timeOut:[number](/docs/luau/numbers)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| childName:[string](/docs/luau/strings)  The [Instance.Name](/docs/reference/engine/classes/Instance#Name) to be looked for. |
| timeOut:[number](/docs/luau/numbers)  An optional time out parameter. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Instance](/docs/reference/engine/classes/Instance) found.

Returns the child of the [Instance](/docs/reference/engine/classes/Instance) with the given name. If the
child does not exist, it will yield the current thread until it does. If
the timeOut parameter is specified, this method will time out after the
specified number of seconds and return nil.

##### Primary Usage

[WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild) is extremely important when
working on code run by the client in a [LocalScript](/docs/reference/engine/classes/LocalScript). The Roblox
engine does not guarantee the time or order in which objects are
replicated from the server to the client. Additionally, if an experience
has [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) set to true,
[BaseParts](/docs/reference/engine/classes/BasePart) that are far away from the player's character
may not be streamed to the client, potentially causing scripts to break
when indexing objects that do not yet exist on the client.

##### Notes

* This method does not yield if a child with the given name exists when
  the call is made.
* [Instance:FindFirstChild()](/docs/reference/engine/classes/Instance#FindFirstChild) is a more efficient alternative to
  [WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild) for objects that are
  assumed to exist.
* If a call to this method exceeds 5 seconds without returning, and no
  timeOut parameter has been specified, a warning will be printed to the
  output that the thread may yield indefinitely.

Code Samples

Instance:WaitForChild

The following code waits for an instance named "Part" to be added to
Workspace.

```
local part = workspace:WaitForChild("Part")



print(part.Name .. " has been added to the Workspace")
```

Provide feedback

---

Events

AncestryChanged

Fires when the [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) property of the object or one of
its ancestors is changed.

Instance.AncestryChanged(

child:[Instance](/docs/reference/engine/datatypes/Instance), parent:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| child:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) whose [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) has been changed. |
| parent:[Instance](/docs/reference/engine/datatypes/Instance)  The new [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) of the [Instance](/docs/reference/engine/classes/Instance) whose [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) was changed. |

Fires when the [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) property of the object or one of
its ancestors is changed.

This event includes two parameters: child refers to the [Instance](/docs/reference/engine/classes/Instance)
whose [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) was actually changed, while parent refers
to this instance's new [Instance.Parent](/docs/reference/engine/classes/Instance#Parent).

You can use this event to track the deletion of an instance in Studio,
such as manual deletion in the Explorer or through a plugin. If you need
to detect when an instance is destroyed using [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy),
use the [Instance.Destroying](/docs/reference/engine/classes/Instance#Destroying) event instead.

Code Samples

Instance.AncestryChanged

Demonstrates detecting changes to an instance's ancestry by connecting to the [Instance.AncestryChanged](/docs/reference/engine/classes/Instance#AncestryChanged) event.

The ChangingPart's Parent is set to different values overtime. The parent of the part is the part's ancestor, so the [Instance.AncestryChanged](/docs/reference/engine/classes/Instance#AncestryChanged) event will fire whenever it changes.

```
local Workspace = game:GetService("Workspace")



local redPart = script.Parent.RedPart



local bluePart = script.Parent.BluePart



local changingPart = script.Parent.ChangingPart



-- Change the color of changingPart based on it's Parent



local function onAncestryChanged(part: Part, parent: Instance)



if parent == redPart then



changingPart.Color = Color3.new(1, 0, 0)



elseif parent == bluePart then



changingPart.Color = Color3.new(0, 0, 1)



else



changingPart.Color = Color3.new(1, 1, 1)



end



print(`{part.Name} is now parented to {parent.Name}`)



end



changingPart.AncestryChanged:Connect(onAncestryChanged)



-- Set changingPart's Parent property to different instances over time



while true do



task.wait(2)



changingPart.Parent = redPart



task.wait(2)



changingPart.Parent = bluePart



task.wait(2)



changingPart.Parent = Workspace



end
```

Provide feedback

---

AttributeChanged

Fires whenever an attribute is changed on the [Instance](/docs/reference/engine/classes/Instance).

Instance.AttributeChanged(attribute:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| attribute:[string](/docs/luau/strings)  The name of the attribute that has been changed. |

This event fires whenever any attribute is changed on the instance,
including when an attribute is set to nil. The name of the changed
attribute is passed to the connected function.

For example, the following code snippet connects the attributeChanged()
function to fire whenever one of the part's attributes changes:

```
local Workspace = game:GetService("Workspace")



local part = Workspace.Part



local function attributeChanged(attributeName)



print(attributeName, "changed")



end



part.AttributeChanged:Connect(attributeChanged)
```

See also [Instance:GetAttributeChangedSignal()](/docs/reference/engine/classes/Instance#GetAttributeChangedSignal) which returns an
event that fires when a specific given attribute changes.

Provide feedback

---

ChildAdded

Fires after an object is parented to this [Instance](/docs/reference/engine/classes/Instance).

Instance.ChildAdded(child:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| child:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) that has been added. |

Fires after an object is parented to this [Instance](/docs/reference/engine/classes/Instance).

Note, when using this method on a client to detect objects created by the
server it is necessary to use [Instance:WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild) when
indexing these object's descendants. This is because the object and its
descendants are not guaranteed to replicate from the server to the client
simultaneously. For example:

```
local Workspace = game:GetService("Workspace")



Workspace.ChildAdded:Connect(function(child)



-- Use WaitForChild() since descendants may not have replicated yet



local head = child:WaitForChild("Head")



end)
```

Note, this event only operates for immediate children of the
[Instance](/docs/reference/engine/classes/Instance). For an event that captures all descendants, use
[Instance.DescendantAdded](/docs/reference/engine/classes/Instance#DescendantAdded).

See also [Instance.ChildRemoved](/docs/reference/engine/classes/Instance#ChildRemoved).

Code Samples

Instance.ChildAdded

This snippet prints the names of objects as they are added to the Workspace:

```
local function onChildAdded(instance)



print(instance.Name .. " added to the workspace")



end



workspace.ChildAdded:Connect(onChildAdded)



local part = Instance.new("Part")



part.Parent = workspace --> Part added to the Workspace
```

Provide feedback

---

childAdded

Deprecated

Show details

---

ChildRemoved

Fires after a child is removed from this [Instance](/docs/reference/engine/classes/Instance).

Instance.ChildRemoved(child:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| child:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) that has been removed. |

Fires after a child is removed from this [Instance](/docs/reference/engine/classes/Instance).

Removed refers to when an object's parent is changed from this
[Instance](/docs/reference/engine/classes/Instance) to something other than this [Instance](/docs/reference/engine/classes/Instance). Note, this
event will also fire when a child is destroyed (using
[Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy)) as the destroy function sets an object's
parent to nil.

This event only operates for immediate children of the [Instance](/docs/reference/engine/classes/Instance).
For an event that captures all descendants, use
[Instance.DescendantRemoving](/docs/reference/engine/classes/Instance#DescendantRemoving).

See also [Instance.ChildAdded](/docs/reference/engine/classes/Instance#ChildAdded).

Code Samples

Instance.ChildRemoved

This snippet prints the names of objects as they are removed from the
Workspace:

```
local function onChildRemoved(instance)



print(instance.Name .. " removed from the workspace")



end



workspace.ChildRemoved:Connect(onChildRemoved)



local part = Instance.new("Part")



part.Parent = workspace



task.wait(2)



part:Destroy()
```

Provide feedback

---

DescendantAdded

Fires after a descendant is added to the [Instance](/docs/reference/engine/classes/Instance).

Instance.DescendantAdded(descendant:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| descendant:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) that has been added. |

This event fires after a descendant is added to the [Instance](/docs/reference/engine/classes/Instance).

As it fires for every descendant, parenting an object to the
[Instance](/docs/reference/engine/classes/Instance) will fire the event for this object and all of its
descendants individually.

If you're only concerned with the direct children of the
[Instance](/docs/reference/engine/classes/Instance), use [Instance.ChildAdded](/docs/reference/engine/classes/Instance#ChildAdded) instead.

See also [Instance.DescendantRemoving](/docs/reference/engine/classes/Instance#DescendantRemoving).

Code Samples

Instance.DescendantAdded

This following example will print the name of any object that is added to the
Workspace:

```
local function onDescendantAdded(descendant)



print(descendant)



end



workspace.DescendantAdded:Connect(onDescendantAdded)



local part = Instance.new("Part")



part.Parent = workspace
```

Provide feedback

---

DescendantRemoving

Fires immediately before a descendant of the [Instance](/docs/reference/engine/classes/Instance) is removed.

Instance.DescendantRemoving(descendant:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| descendant:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) that is being removed. |

This event fires immediately before the parent [Instance](/docs/reference/engine/classes/Instance)
changes such that a descendant instance will no longer be a
descendant. [Destroy()](/docs/reference/engine/classes/Instance#Destroy) changes an instance's
[Parent](/docs/reference/engine/classes/Instance#Parent) to nil, so calling that method on a
descendant of the parent will cause this event to fire.

Since this event fires before the descendant's removal, the parent of
the descendant will be unchanged at the time of this event firing. If the
descendant is also a direct child of the parent, this event will fire
before [Instance.ChildRemoved](/docs/reference/engine/classes/Instance#ChildRemoved).

If a descendant has children, this event fires with the descendant first,
followed by its descendants.

##### Warning

This event fires with the descendant object that is being removed.
Attempting to set the [Parent](/docs/reference/engine/classes/Instance#Parent) of the descendant to
something else will fail. Below is an example that demonstrates this:

```
local Workspace = game:GetService("Workspace")



Workspace.DescendantRemoving:Connect(function(descendant)



-- Do not manipulate the parent of the descendant in this function!



-- This event fires BECAUSE the parent was manipulated, and the change hasn't happened yet



-- Therefore, it is problematic to change the parent like this:



descendant.Parent = game



end)



local part = Instance.new("Part")



part.Parent = Workspace



part.Parent = nil
```

See also [DescendantAdded](/docs/reference/engine/classes/Instance#DescendantAdded).

Code Samples

Instance.DescendantRemoving

The following example prints the name of any descendant as it is being removed
from the Workspace:

```
workspace.DescendantRemoving:Connect(function(descendant)



print(descendant.Name .. " is currently parented to " .. tostring(descendant.Parent))



end)



local part = Instance.new("Part")



part.Parent = workspace



part.Parent = nil



--> Part is currently parented to Workspace



print(part.Parent)



--> nil
```

Provide feedback

---

Destroying

Fires immediately before (or is deferred until after) the instance is
destroyed via [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy).

Instance.Destroying():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

The [Instance](/docs/reference/engine/classes/Instance) will never be deleted from memory while a connected
function is still using it. However, if the function yields at any point,
the [Instance](/docs/reference/engine/classes/Instance) and its descendants will be parented to nil.

If the [Workspace.SignalBehavior](/docs/reference/engine/classes/Workspace#SignalBehavior) property is set to
[Enum.SignalBehavior.Immediate](/docs/reference/engine/enums/SignalBehavior#Immediate), this event fires immediately before the
[Instance](/docs/reference/engine/classes/Instance) or one of its ancestors is destroyed with
[Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy).

If the [Workspace.SignalBehavior](/docs/reference/engine/classes/Workspace#SignalBehavior) property is set to
[Enum.SignalBehavior.Deferred](/docs/reference/engine/enums/SignalBehavior#Deferred), this event fires at the next resumption
point, which will be after the [Instance](/docs/reference/engine/classes/Instance) or one of its ancestors is
destroyed with [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy).

With [Deferred](/docs/reference/engine/enums/SignalBehavior#Deferred) behavior, connecting a script
to its own [Instance.Destroying](/docs/reference/engine/classes/Instance#Destroying) event is problematic, as the script
will be destroyed before the callback can be called (meaning it will not
execute).

When deleting an [Instance](/docs/reference/engine/classes/Instance) in Studio, such as manually deleting
through the [Explorer](/docs/studio/explorer) or through a plugin,
the [Instance](/docs/reference/engine/classes/Instance) isn't destroyed. Instead, the parent is set to nil
which you can track with [Instance.AncestryChanged](/docs/reference/engine/classes/Instance#AncestryChanged).

Code Samples

Using the Destroying Event (Immediate signals)

This sample demonstrates how, when using Immediate signal behavior, an Instance being destroyed remains in place until the connected function yields.

```
local part = Instance.new("Part", workspace)



local function onPartDestroying()



print("Before yielding:", part:GetFullName(), #part:GetChildren())



task.wait()



print("After yielding:", part:GetFullName(), #part:GetChildren())



end



part.Destroying:Connect(onPartDestroying)



part:Destroy()
```

Using the Destroying Event (Deferred signals)

This sample demonstrates how, when using Deferred signal behavior,
an Instance is destroyed before the signal fires.

```
local part = Instance.new("Part", workspace)



local function onPartDestroying()



print("In signal:", part:GetFullName(), #part:GetChildren())



end



part.Destroying:Connect(onPartDestroying)



print("Before destroying:", part:GetFullName(), #part:GetChildren())



part:Destroy()



print("After destroying:", part:GetFullName(), #part:GetChildren())
```

Provide feedback

---

StyledPropertiesChanged

Fires whenever any style property is changed on the instance, including
when a property is set to nil.

Instance.StyledPropertiesChanged():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires whenever any style property is changed on the instance,
including when a property is set to nil.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local playerGui = player.PlayerGui



local HUDContainer = playerGui:WaitForChild("HUDContainer")



local meterBar = HUDContainer.MeterBar



local function stylePropertyChanged()



print("Styled properties changed")



end



meterBar:StyledPropertiesChanged():Connect(stylePropertyChanged)
```

Provide feedback

---