# GuiBase2d | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GuiBase2d
Scraped: 2026-01-11T02:29:53.876713Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- GuiBase
- GuiBase2d
- GuiObjects
- LocalizationTable
- GuiObject
- Instance
- Object
- LayerCollector
- AbsolutePosition
- ScreenGui
- InputObject.Position
- AbsoluteRotation
- AbsoluteSize
- LocalizationService:GetTableEntries()
- AutoLocalize
- RootLocalizationTable
- DataModel
- LocalizationService
- SelectionGroup
- SelectionBehaviorUp
- SelectionBehaviorDown
- SelectionBehaviorLeft
- SelectionBehaviorRight
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiBase](/docs/reference/engine/classes/GuiBase)
6. /
7. [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

English

Feedback

Engine Class

GuiBase2d

An abstract class inherited by 2D [GuiObjects](/docs/reference/engine/classes/GuiObject).

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [AbsolutePosition](#AbsolutePosition):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AbsoluteRotation](#AbsoluteRotation):[number](/docs/luau/numbers) |
| [AbsoluteSize](#AbsoluteSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AutoLocalize](#AutoLocalize):[boolean](/docs/luau/booleans) |
| [Localize](#Localize):[boolean](/docs/luau/booleans)  Deprecated |
| [RootLocalizationTable](#RootLocalizationTable):[LocalizationTable](/docs/reference/engine/classes/LocalizationTable) |
| [SelectionBehaviorDown](#SelectionBehaviorDown):[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior) |
| [SelectionBehaviorLeft](#SelectionBehaviorLeft):[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior) |
| [SelectionBehaviorRight](#SelectionBehaviorRight):[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior) |
| [SelectionBehaviorUp](#SelectionBehaviorUp):[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior) |
| [SelectionGroup](#SelectionGroup):[boolean](/docs/luau/booleans) |

Events

|  |
| --- |
| [SelectionChanged](#SelectionChanged)(amISelected: [boolean](/docs/luau/booleans),previousSelection: [GuiObject](/docs/reference/engine/classes/GuiObject),newSelection: [GuiObject](/docs/reference/engine/classes/GuiObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[GuiObject](/docs/reference/engine/classes/GuiObject), [LayerCollector](/docs/reference/engine/classes/LayerCollector)

[GuiBase2d](/docs/reference/engine/classes/GuiBase2d) is an abstract class inherited by 2D
[GuiObjects](/docs/reference/engine/classes/GuiObject).

---

API Reference

Properties

AbsolutePosition

Read Only

Not Replicated

Describes the actual screen position of a [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) element, in
pixels.

GuiBase2d.AbsolutePosition:[Vector2](/docs/reference/engine/datatypes/Vector2)

[AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition) is a read-only
property that provides the screen position of a [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) element
in pixels. This represents the actual pixel position at which an element
renders as a result of its ancestors' sizes and positions. Note that
[AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition) always represents the
top-left corner of the [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) element.

If the [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) is in a [ScreenGui](/docs/reference/engine/classes/ScreenGui), the
[AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition) property uses the
[CoreUISafeInsets](/docs/reference/engine/enums/ScreenInsets) viewport coordinate system. The
origin of this coordinate system is located at the bottom-left corner of
the Roblox top bar. Note that this is the same coordinate system used by
the [InputObject.Position](/docs/reference/engine/classes/InputObject#Position) property.

![Diagram showing the origin of the AbsolutePosition coordinate system.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/GuiBase2d/AbsolutePositionCoordinateSystem.png)

See also [AbsoluteRotation](/docs/reference/engine/classes/GuiBase2d#AbsoluteRotation) and
[AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).

Provide feedback

---

AbsoluteRotation

Read Only

Not Replicated

Describes the actual screen rotation of a [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) element, in
degrees.

GuiBase2d.AbsoluteRotation:[number](/docs/luau/numbers)

[AbsoluteRotation](/docs/reference/engine/classes/GuiBase2d#AbsoluteRotation) is a read-only
property that describes the actual screen rotation of a [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)
element, in degrees. It does not perform bounds checking, so its value
may not be in the range 0 to 360.

See also [AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition) and
[AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).

Provide feedback

---

AbsoluteSize

Read Only

Not Replicated

Describes the actual screen size of a [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) element, in
pixels.

GuiBase2d.AbsoluteSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

[AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize) is a read-only property that
describes the actual screen size of a [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) element, in
pixels.

See also [AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition) and
[AbsoluteRotation](/docs/reference/engine/classes/GuiBase2d#AbsoluteRotation).

Provide feedback

---

AutoLocalize

Read Parallel

When set to true, localization will be applied to this [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)
and its descendants.

GuiBase2d.AutoLocalize:[boolean](/docs/luau/booleans)

When set to true, localization will be applied to this [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)
and its descendants. The entries used for localization are the same set of
entries returned by [LocalizationService:GetTableEntries()](/docs/reference/engine/classes/LocalizationService#GetTableEntries). Entries
with [AutoLocalize](/docs/reference/engine/classes/GuiBase2d#AutoLocalize) enabled are automatically
re-translated after the cloud table loads if necessary.

See also [RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable).

Provide feedback

---

Localize

Deprecated

Show details

---

RootLocalizationTable

Read Parallel

A reference to a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) to be used to apply automated
localization to this [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) and its descendants.

GuiBase2d.RootLocalizationTable:[LocalizationTable](/docs/reference/engine/classes/LocalizationTable)

A reference to a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) to be used to apply automated
localization to this [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) and its descendants.
[AutoLocalize](/docs/reference/engine/classes/GuiBase2d#AutoLocalize) must be set to true on the
[GuiBase2d](/docs/reference/engine/classes/GuiBase2d) and its ancestors for automated localization to be
applied.

You can set this to reference a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) anywhere in the
[DataModel](/docs/reference/engine/classes/DataModel). The [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) object and all of its children
will try to use that specific [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) and its ancestors
for automatic text replacement before using the tables under
[LocalizationService](/docs/reference/engine/classes/LocalizationService) in an undefined order and the cloud table.

If there is no translation available in the referenced table, it will look
for a translation in the parent of that table, if it is also a
[LocalizationTable](/docs/reference/engine/classes/LocalizationTable), and so on.

See also [LocalizationService:GetTableEntries()](/docs/reference/engine/classes/LocalizationService#GetTableEntries) which explains how
the [RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable) is used
for automated localization.

Provide feedback

---

SelectionBehaviorDown

Read Parallel

Customizes gamepad selection behavior in the down direction.

GuiBase2d.SelectionBehaviorDown:[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior)

Customizes gamepad selection behavior in the down direction.

Provide feedback

---

SelectionBehaviorLeft

Read Parallel

Customizes gamepad selection behavior in the left direction.

GuiBase2d.SelectionBehaviorLeft:[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior)

Customizes gamepad selection behavior in the left direction.

Provide feedback

---

SelectionBehaviorRight

Read Parallel

Customizes gamepad selection behavior in the right direction.

GuiBase2d.SelectionBehaviorRight:[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior)

Customizes gamepad selection behavior in the right direction.

Provide feedback

---

SelectionBehaviorUp

Read Parallel

Customizes gamepad selection behavior in the up direction.

GuiBase2d.SelectionBehaviorUp:[Enum.SelectionBehavior](/docs/reference/engine/enums/SelectionBehavior)

Customizes gamepad selection behavior in the up direction.

Provide feedback

---

SelectionGroup

Read Parallel

Allows customization of gamepad selection movement.

GuiBase2d.SelectionGroup:[boolean](/docs/luau/booleans)

Allows for customization of how gamepad selection can move between
buttons, which are descendants of the selection group, leave the group,
and select other buttons.

Setting [SelectionGroup](/docs/reference/engine/classes/GuiBase2d#SelectionGroup) to true exposes
the [SelectionBehaviorUp](/docs/reference/engine/classes/GuiBase2d#SelectionBehaviorUp),
[SelectionBehaviorDown](/docs/reference/engine/classes/GuiBase2d#SelectionBehaviorDown),
[SelectionBehaviorLeft](/docs/reference/engine/classes/GuiBase2d#SelectionBehaviorLeft), and
[SelectionBehaviorRight](/docs/reference/engine/classes/GuiBase2d#SelectionBehaviorRight)
properties. For these selection behaviors, a setting of
[Enum.SelectionBehavior.Escape](/docs/reference/engine/enums/SelectionBehavior#Escape) (default) means the gamepad selection
tries to first find a selection within the selection group and only moves
outside if it does not find a suitable button. Alternatively, a setting of
[Enum.SelectionBehavior.Stop](/docs/reference/engine/enums/SelectionBehavior#Stop) means gamepad selection only looks within
the selection group and does not move outside of the group from the
selection behavior direction.

Provide feedback

---

Events

SelectionChanged

Fires when the gamepad selection moves to, leaves, or changes within the
connected [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) or any descendant
[GuiObjects](/docs/reference/engine/classes/GuiObject).

GuiBase2d.SelectionChanged(

amISelected:[boolean](/docs/luau/booleans), previousSelection:[GuiObject](/docs/reference/engine/classes/GuiObject), newSelection:[GuiObject](/docs/reference/engine/classes/GuiObject)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| amISelected:[boolean](/docs/luau/booleans)  True if the new selection matches the attached GuiBase2d. |
| previousSelection:[GuiObject](/docs/reference/engine/classes/GuiObject) |
| newSelection:[GuiObject](/docs/reference/engine/classes/GuiObject) |

This event fires when the gamepad selection moves to, leaves, or changes
within the connected [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) or any descendant
[GuiObjects](/docs/reference/engine/classes/GuiObject). When the selection highlight moves to a
[GuiObject](/docs/reference/engine/classes/GuiObject), the event bubbles from that [GuiObject](/docs/reference/engine/classes/GuiObject) to all of
its ancestors, informing them that the selection has
changed/entered/exited to a [GuiObject](/docs/reference/engine/classes/GuiObject) in their descendant tree.

Provide feedback

---