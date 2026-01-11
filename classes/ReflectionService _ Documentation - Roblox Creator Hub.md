# ReflectionService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ReflectionService
Scraped: 2026-01-11T02:29:18.683276Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- ReflectionService
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ReflectionService](/docs/reference/engine/classes/ReflectionService)

English

Feedback

Engine Class

ReflectionService

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetClass](#GetClass)(className: [string](/docs/luau/strings),filter: [Dictionary](/docs/luau/tables#dictionaries)):[Dictionary](/docs/luau/tables#dictionaries)? |
| [GetClasses](#GetClasses)(filter: [Dictionary](/docs/luau/tables#dictionaries)):[Array](/docs/luau/tables#arrays) |
| [GetPropertiesOfClass](#GetPropertiesOfClass)(className: [string](/docs/luau/strings),filter: [Dictionary](/docs/luau/tables#dictionaries)):[Array](/docs/luau/tables#arrays) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

ReflectionService allows scripts to query the engine for details about its
API, including required security permissions, functionality, and inheritance
structure. You can use this service to dynamically inspect classes and their
properties, which can be useful for debugging, tooling, or creating dynamic
behaviors based on the engine's capabilities.

The following is an example script that inspects classes and their properties:

```
local ReflectionService = game:GetService("ReflectionService")



-- Create a SecurityCapabilities object with all capabilities



local allCapabilities = SecurityCapabilities.new(table.unpack(Enum.SecurityCapability:GetEnumItems()))



-- Get all classes accessible with all capabilities



local allClasses = ReflectionService:GetClasses({ Security = allCapabilities })



print("Total classes:", #allClasses)



-- Get a specific class



local partClass = ReflectionService:GetClass("Part")



if partClass then



print("\nPart class:")



print("  Name:", partClass.Name)



print("  Superclass:", partClass.Superclass and tostring(partClass.Superclass) or "none")



end



-- Get the first 5 properties of a class



local properties = ReflectionService:GetPropertiesOfClass("Part", { Security = allCapabilities })



print("\nPart properties:", #properties)



for i = 1, math.min(5, #properties) do



print("  -", properties[i].Name)



end
```

---

API Reference

Methods

GetClass

Returns information about a class when given its name, assuming that class
is accessible.

ReflectionService:GetClass(

className:[string](/docs/luau/strings), filter:[Dictionary](/docs/luau/tables#dictionaries)

):[Dictionary](/docs/luau/tables#dictionaries)?

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  The name of the class for which you wish to retrieve information. |
| filter:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" An optional filter to restrict or expand the set of classes that this method can return and change the method's behavior. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)?

A ReflectedClass dictionary with reflection information if the class
exists; otherwise, nil.

Given a class name in the Roblox API, returns a ReflectedClass
dictionary with information about the associated class's reflection state.
If no such class name exists, returns nil.

If you pass in a ReflectionClassFilter dictionary, you can adjust the
set of eligible classes and adjust the output behavior:

```
{



-- The security context to use. Can be more expansive than the current script's security.



Security: SecurityCapabilities?, -- default: SecurityCapabilities.fromCurrent()



-- Require classes to derive from the passed-in class name.



IsA: string?, -- default: nil



-- Whether to exclude Studio display information about the class.



ExcludeDisplay: boolean?, -- default: false



}
```

If the class name is valid, you'll get the following ReflectedClass
dictionary as output:

```
{



-- The name of the class.



Name: string,



-- The class's parent in the instance hierarchy (unless it's the root).



Superclass: string?,



-- The names of the class's direct children in the instance hierarchy.



Subclasses: {string},



-- Studio display information.



Display: {



-- Always "General" for classes.



Category: string,



-- A message indicating that the class is deprecated, if applicable.



DeprecationMessage: string?,



}?,



-- The security permissions required to access this class.



Permits: {



-- If the class is a Service, the security capabilities required to obtain access. If not applicable, this field isn't present.



GetService: SecurityCapabilities?,



-- The security capabilities required to create an instance of this class. If not possible, this field isn't present.



New: SecurityCapabilities?,



}



}
```

Provide feedback

---

GetClasses

Returns a list of all classes accessible with filters applied.

ReflectionService:GetClasses(filter:[Dictionary](/docs/luau/tables#dictionaries)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| filter:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" An optional filter to restrict or expand the set of classes that this method can return and change the method's behavior. |

Returns

[Array](/docs/luau/tables#arrays)

A list of ReflectedClass dictionaries with reflection information
for each class that matches the filter criteria.

Returns a list of ReflectedClass dictionaries for all classes in the
Roblox API that match the provided filter criteria.

If you pass in a ReflectionClassFilter dictionary, you can adjust the
set of eligible classes and adjust the output behavior:

```
{



-- The security context to use. Can be more expansive than the current script's security.



Security: SecurityCapabilities?, -- default: SecurityCapabilities.fromCurrent()



-- Require classes to derive from the passed-in class name.



IsA: string?, -- default: nil



-- Whether to exclude Studio display information about the classes.



ExcludeDisplay: boolean?, -- default: false



}
```

You'll get a list of ReflectedClass dictionaries as output, each with
the same structure as described in the GetClass method. If there are no
classes that match the filter criteria, you'll receive an empty list.

Provide feedback

---

GetPropertiesOfClass

Returns a list of properties for a given class with filters applied.

ReflectionService:GetPropertiesOfClass(

className:[string](/docs/luau/strings), filter:[Dictionary](/docs/luau/tables#dictionaries)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| className:[string](/docs/luau/strings)  The name of the class for which you wish to retrieve properties. |
| filter:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" An optional filter to restrict or expand the set of properties that this method can return and change the method's behavior. |

Returns

[Array](/docs/luau/tables#arrays)

A list of ReflectedProperty dictionaries with reflection information
for each property of the class that matches the filter criteria.

Given a class name in the Roblox API, returns a list of
ReflectedProperty dictionaries for all properties of that class that
match the provided filter criteria. If no such class name exists, returns
nil.

If you pass in a ReflectionMemberFilter dictionary, you can adjust the
set of eligible properties and adjust the output behavior:

```
{



-- The security context to use. Can be more expansive than the current script's security.



Security: SecurityCapabilities?, -- default: SecurityCapabilities.fromCurrent()



-- Whether to exclude inherited properties from superclasses.



ExcludeInherited: boolean?, -- default: false



-- Whether to exclude Studio display information about the properties.



ExcludeDisplay: boolean?, -- default: false



}
```

If the class name is valid and that class has properties, you'll get a
list of ReflectedProperty dictionaries as output, each with the
following structure:

```
{



-- The name of the property.



Name: string,



-- Whether the property is serialized (able to be saved to disk or sent over the network).



Serialized: boolean,



-- The type of the property.



Type: ReflectionType,



-- The content type of the property, if applicable.



ContentType: Enum.AssetType?,



-- Studio display information.



Display: {



-- The category under which the property is listed in Studio.



Category: string,



-- A message indicating that the property is deprecated, if applicable.



DeprecationMessage: string?,



-- The order in which the property appears in Studio.



LayoutOrder: number,



}?,



-- The security permissions required to access this property.



Permits: {



-- The security context required to read this property.



Read: SecurityCapabilities?,



-- The security context required to read this property while thread-safe.



ReadParallel: SecurityCapabilities?,



-- The security context required to write to this property.



Write: SecurityCapabilities?,



-- The security context required to write to this property while thread-safe.



WriteParallel: SecurityCapabilities?,



},



}
```

Provide feedback

---