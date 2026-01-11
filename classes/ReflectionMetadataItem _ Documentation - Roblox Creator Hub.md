# ReflectionMetadataItem | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ReflectionMetadataItem
Scraped: 2026-01-11T02:31:13.685587Z

## Tags
- Not Creatable

## Inherits
- Instance
- ReflectionMetadataItem
- Object
- ReflectionMetadataClass
- ReflectionMetadataEnum
- ReflectionMetadataEnumItem
- ReflectionMetadataMember
- Object.ClassName
- LocalScript
- Script
- ReflectionMetadataItem.UIMinimum
- ReflectionMetadataItem.UIMaximum
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ReflectionMetadataItem](/docs/reference/engine/classes/ReflectionMetadataItem)

English

Feedback

Engine Class

ReflectionMetadataItem

Acts as abstract properties for generic information about Classes, Members,
Enums, and EnumItems.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Browsable](#Browsable):[boolean](/docs/luau/booleans) |
| [ClassCategory](#ClassCategory):[string](/docs/luau/strings) |
| [ClientOnly](#ClientOnly):[boolean](/docs/luau/booleans) |
| [Constraint](#Constraint):[string](/docs/luau/strings) |
| [Deprecated](#Deprecated):[boolean](/docs/luau/booleans) |
| [EditingDisabled](#EditingDisabled):[boolean](/docs/luau/booleans) |
| [EditorType](#EditorType):[string](/docs/luau/strings) |
| [FFlag](#FFlag):[string](/docs/luau/strings) |
| [IsBackend](#IsBackend):[boolean](/docs/luau/booleans) |
| [PropertyOrder](#PropertyOrder):[number](/docs/luau/numbers) |
| [ScriptContext](#ScriptContext):[string](/docs/luau/strings) |
| [ServerOnly](#ServerOnly):[boolean](/docs/luau/booleans) |
| [SliderScaling](#SliderScaling):[string](/docs/luau/strings) |
| [UIMaximum](#UIMaximum):[number](/docs/luau/numbers) |
| [UIMinimum](#UIMinimum):[number](/docs/luau/numbers) |
| [UINumTicks](#UINumTicks):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[ReflectionMetadataClass](/docs/reference/engine/classes/ReflectionMetadataClass), [ReflectionMetadataEnum](/docs/reference/engine/classes/ReflectionMetadataEnum), [ReflectionMetadataEnumItem](/docs/reference/engine/classes/ReflectionMetadataEnumItem), [ReflectionMetadataMember](/docs/reference/engine/classes/ReflectionMetadataMember)

Acts as abstract properties for generic information about Classes, Members,
Enums, and EnumItems.

---

API Reference

Properties

Browsable

Read Parallel

Whether or not this can be seen in studio.

ReflectionMetadataItem.Browsable:[boolean](/docs/luau/booleans)

When this value is true, it means that this property/class can be seen in
Studio, e.g. in the explorer.

Provide feedback

---

ClassCategory

Read Parallel

Describes the category of this class.

ReflectionMetadataItem.ClassCategory:[string](/docs/luau/strings)

Describes the category of this class.

Provide feedback

---

ClientOnly

Read Parallel

ReflectionMetadataItem.ClientOnly:[boolean](/docs/luau/booleans)

Provide feedback

---

Constraint

Read Parallel

Describes a constraint for a single-argument function whose argument type
is a [Object.ClassName](/docs/reference/engine/classes/Object#ClassName).

ReflectionMetadataItem.Constraint:[string](/docs/luau/strings)

Describes a constraint for a single-argument function whose argument type
is a [Object.ClassName](/docs/reference/engine/classes/Object#ClassName). Currently there are two constraints
available:

|  |  |
| --- | --- |
| Constraint | Description |
| isScriptCreatable | The specified class must be creatable with Instance.new |
| isService | The specified class must be a service. |

Provide feedback

---

Deprecated

Read Parallel

Whether or not this item is deprecated.

ReflectionMetadataItem.Deprecated:[boolean](/docs/luau/booleans)

When an object is deprecated, it should not be used anymore for new
scripts.

Provide feedback

---

EditingDisabled

Read Parallel

Toggles whether this property can be edited from the Properties window.

ReflectionMetadataItem.EditingDisabled:[boolean](/docs/luau/booleans)

Toggles whether this property can be edited from the Properties window.

Provide feedback

---

EditorType

Read Parallel

ReflectionMetadataItem.EditorType:[string](/docs/luau/strings)

Provide feedback

---

FFlag

Read Parallel

ReflectionMetadataItem.FFlag:[string](/docs/luau/strings)

Provide feedback

---

IsBackend

Read Parallel

Vague value for showing if this depends on backend stuff.

ReflectionMetadataItem.IsBackend:[boolean](/docs/luau/booleans)

This should determine if a method needs to use stuff on the Roblox main
servers. This property isn't applied where it should be, though.

Provide feedback

---

PropertyOrder

Read Parallel

ReflectionMetadataItem.PropertyOrder:[number](/docs/luau/numbers)

Provide feedback

---

ScriptContext

Read Parallel

Describes the context where this member can be used. If set to "Server",
this member will not be available to auto fill when editing a
[LocalScript](/docs/reference/engine/classes/LocalScript). If set to "Client", this member will not be available
to auto fill when editing a [Script](/docs/reference/engine/classes/Script).

ReflectionMetadataItem.ScriptContext:[string](/docs/luau/strings)

Describes the context where this member can be used. If set to
["Server"](/docs/luau/strings), this member will not be
available to auto fill when editing a [LocalScript](/docs/reference/engine/classes/LocalScript). If set to
["Client"](/docs/luau/strings), this member will not be
available to auto fill when editing a [Script](/docs/reference/engine/classes/Script).

Provide feedback

---

ServerOnly

Read Parallel

ReflectionMetadataItem.ServerOnly:[boolean](/docs/luau/booleans)

Provide feedback

---

SliderScaling

Read Parallel

ReflectionMetadataItem.SliderScaling:[string](/docs/luau/strings)

Provide feedback

---

UIMaximum

Read Parallel

The maximum value of this property. Used with
[ReflectionMetadataItem.UIMinimum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMinimum) to control the slider bar of this
property in the Properties window.

ReflectionMetadataItem.UIMaximum:[number](/docs/luau/numbers)

The maximum value of this property. Used with
[ReflectionMetadataItem.UIMinimum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMinimum) to control the slider bar of this
property in the Properties window.

Provide feedback

---

UIMinimum

Read Parallel

The minimum value of this property. Used with
[ReflectionMetadataItem.UIMaximum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMaximum) to control the slider bar of this
property in the Properties window.

ReflectionMetadataItem.UIMinimum:[number](/docs/luau/numbers)

The minimum value of this property. Used with
[ReflectionMetadataItem.UIMaximum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMaximum) to control the slider bar of this
property in the Properties window.

Provide feedback

---

UINumTicks

Read Parallel

The number of potential values the property's slider bar can be set to,
[ReflectionMetadataItem.UIMinimum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMinimum) and
[ReflectionMetadataItem.UIMaximum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMaximum).

ReflectionMetadataItem.UINumTicks:[number](/docs/luau/numbers)

The number of potential values the property's slider bar can be set to,
[ReflectionMetadataItem.UIMinimum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMinimum) and
[ReflectionMetadataItem.UIMaximum](/docs/reference/engine/classes/ReflectionMetadataItem#UIMaximum).

Provide feedback

---