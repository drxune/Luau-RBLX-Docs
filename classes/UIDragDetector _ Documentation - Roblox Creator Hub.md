# UIDragDetector | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIDragDetector
Scraped: 2026-01-11T02:28:14.601730Z

## Inherits
- UIComponent
- UIDragDetector
- GuiBase2d
- GuiObject
- Instance
- Object
- DragStyle
- ResponseStyle
- UIDragDetectors
- BoundingUI
- ReferenceUIInstance
- SetDragStyleFunction()
- AddConstraintFunction()
- DragSpace
- LayerCollector
- DragRelativity
- MinDragAngle
- MaxDragAngle
- MinDragTranslation
- MaxDragTranslation
- DragUDim2
- DragRotation
- DragAxis
- ScreenGui
- SurfaceGui
- DragContinue
- DragStart
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIComponent](/docs/reference/engine/classes/UIComponent)
6. /
7. [UIDragDetector](/docs/reference/engine/classes/UIDragDetector)

English

Feedback

Engine Class

![UIDragDetector](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIDragDetector-Dark.webp)UIDragDetector

Instance which facilitates and encourages interaction with UI elements in an
experience.

---

Summary

Properties

|  |
| --- |
| [ActivatedCursorIcon](#ActivatedCursorIcon):ContentId |
| [ActivatedCursorIconContent](#ActivatedCursorIconContent):[Content](/docs/reference/engine/datatypes/Content) |
| [BoundingBehavior](#BoundingBehavior):[Enum.UIDragDetectorBoundingBehavior](/docs/reference/engine/enums/UIDragDetectorBoundingBehavior) |
| [BoundingUI](#BoundingUI):[GuiBase2d](/docs/reference/engine/classes/GuiBase2d) |
| [CursorIcon](#CursorIcon):ContentId |
| [CursorIconContent](#CursorIconContent):[Content](/docs/reference/engine/datatypes/Content) |
| [DragAxis](#DragAxis):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [DragRelativity](#DragRelativity):[Enum.UIDragDetectorDragRelativity](/docs/reference/engine/enums/UIDragDetectorDragRelativity) |
| [DragRotation](#DragRotation):[number](/docs/luau/numbers) |
| [DragSpace](#DragSpace):[Enum.UIDragDetectorDragSpace](/docs/reference/engine/enums/UIDragDetectorDragSpace) |
| [DragStyle](#DragStyle):[Enum.UIDragDetectorDragStyle](/docs/reference/engine/enums/UIDragDetectorDragStyle) |
| [DragUDim2](#DragUDim2):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [MaxDragAngle](#MaxDragAngle):[number](/docs/luau/numbers) |
| [MaxDragTranslation](#MaxDragTranslation):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [MinDragAngle](#MinDragAngle):[number](/docs/luau/numbers) |
| [MinDragTranslation](#MinDragTranslation):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [ReferenceUIInstance](#ReferenceUIInstance):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [ResponseStyle](#ResponseStyle):[Enum.UIDragDetectorResponseStyle](/docs/reference/engine/enums/UIDragDetectorResponseStyle) |
| [SelectionModeDragSpeed](#SelectionModeDragSpeed):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [SelectionModeRotateSpeed](#SelectionModeRotateSpeed):[number](/docs/luau/numbers) |
| [UIDragSpeedAxisMapping](#UIDragSpeedAxisMapping):[Enum.UIDragSpeedAxisMapping](/docs/reference/engine/enums/UIDragSpeedAxisMapping) |

Methods

|  |
| --- |
| [AddConstraintFunction](#AddConstraintFunction)(priority: [number](/docs/luau/numbers),function: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [GetReferencePosition](#GetReferencePosition)():[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [GetReferenceRotation](#GetReferenceRotation)():[number](/docs/luau/numbers) |
| [SetDragStyleFunction](#SetDragStyleFunction)(function: [function](/docs/luau/functions)):() |

Events

|  |
| --- |
| [DragContinue](#DragContinue)(inputPosition: [Vector2](/docs/reference/engine/datatypes/Vector2)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DragEnd](#DragEnd)(inputPosition: [Vector2](/docs/reference/engine/datatypes/Vector2)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DragStart](#DragStart)(inputPosition: [Vector2](/docs/reference/engine/datatypes/Vector2)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) instance facilitates and encourages interaction
with 2D user interface elements in an experience, such as sliders and
spinners. Key features include:

* Place a [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) under any [GuiObject](/docs/reference/engine/classes/GuiObject) instance to make
  it draggable via all inputs without a single line of code.
* Choose from several [DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) options,
  define how the object responds to motion via
  [ResponseStyle](/docs/reference/engine/classes/UIDragDetector#ResponseStyle), and optionally apply
  axis, movement limits, or drag boundaries.
* Scripts can respond to manipulation of dragged objects to drive logic
  responses, such as adjusting settings.
* [UIDragDetectors](/docs/reference/engine/classes/UIDragDetector) work in Studio as long as you're
  not using the Select, Move, Scale, or Rotate tools, nor
  certain plugins or Studio's UI editor tools.

---

API Reference

Properties

ActivatedCursorIcon

Read Parallel

Sets the cursor icon to display when the mouse is activated over the
parent of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector).

UIDragDetector.ActivatedCursorIcon:ContentId

Sets the cursor icon to display when the mouse is activated over the
parent of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector). If this property is left blank, the
detector will use the default icon.

To change the activated cursor icon, set this property to the asset ID of
the image you'd like to use.

Provide feedback

---

ActivatedCursorIconContent

Read Parallel

Sets the cursor icon to display when the mouse is activated over the
parent of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector). Only supports asset URIs

UIDragDetector.ActivatedCursorIconContent:[Content](/docs/reference/engine/datatypes/Content)

Sets the cursor icon to display when the mouse is activated over the
parent of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector). If this property is left blank, the
detector will use the default icon.

To change the activated cursor icon, set this property to the asset ID of
the image you'd like to use. Only asset URIs are supported for this
property.

Provide feedback

---

BoundingBehavior

Read Parallel

Determines bounding behavior of the dragged UI object when the detector's
[BoundingUI](/docs/reference/engine/classes/UIDragDetector#BoundingUI) is set.

UIDragDetector.BoundingBehavior:[Enum.UIDragDetectorBoundingBehavior](/docs/reference/engine/enums/UIDragDetectorBoundingBehavior)

Determines bounding behavior of the dragged UI object when the detector's
[BoundingUI](/docs/reference/engine/classes/UIDragDetector#BoundingUI) is set. See
[Enum.UIDragDetectorBoundingBehavior](/docs/reference/engine/enums/UIDragDetectorBoundingBehavior) for details on each setting's
behavior.

Provide feedback

---

BoundingUI

Read Parallel

Instance whose bounding area defines the drag boundaries for the parent
[GuiObject](/docs/reference/engine/classes/GuiObject).

UIDragDetector.BoundingUI:[GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

When set, the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) instance will not allow the bounds of
the parent [GuiObject](/docs/reference/engine/classes/GuiObject) to be dragged outside the bounds of the
BoundingUI instance.

Note that if a portion of the parent [GuiObject](/docs/reference/engine/classes/GuiObject) is outside the
BoundingUI bounds, the initial input position at drag start and its
relative position during drag will be used for bounding detection until
the entirety of the dragged object is within the bounds, after which the
object will be constrained inside the bounds.

Provide feedback

---

CursorIcon

Read Parallel

Sets the cursor icon to display when the mouse is hovered over the parent
of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector).

UIDragDetector.CursorIcon:ContentId

Sets the cursor icon to display when the mouse is hovered over the parent
of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector). If this property is left blank, the
detector will use the default icon.

To change the cursor icon, set this property to the asset ID of the image
you'd like to use.

Provide feedback

---

CursorIconContent

Read Parallel

Sets the cursor icon to display when the mouse is hovered over the parent
of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector). Only asset URIs are supported.

UIDragDetector.CursorIconContent:[Content](/docs/reference/engine/datatypes/Content)

Sets the cursor icon to display when the mouse is hovered over the parent
of this [UIDragDetector](/docs/reference/engine/classes/UIDragDetector). If this property is left blank, the
detector will use the default icon.

To change the cursor icon, set this property to the asset ID of the image
you'd like to use. Only asset URIs are supported for this property.

Provide feedback

---

DragAxis

Read Parallel

The drag axis for the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) instance when
[DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is set to
[Enum.UIDragDetectorDragStyle.TranslateLine](/docs/reference/engine/enums/UIDragDetectorDragStyle#TranslateLine).

UIDragDetector.DragAxis:[Vector2](/docs/reference/engine/datatypes/Vector2)

[Vector2](/docs/reference/engine/datatypes/Vector2) value that defines the axis of movement for the dragged
object when [DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is set to
[Enum.UIDragDetectorDragStyle.TranslateLine](/docs/reference/engine/enums/UIDragDetectorDragStyle#TranslateLine). The axis is defined in the
local space of the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) unless
[ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is defined,
in which case the axis is defined in that instance's local space.

Provide feedback

---

DragRelativity

Read Parallel

Sets the paradigm which defines the relativity of inputs/outputs from a
custom drag function.

UIDragDetector.DragRelativity:[Enum.UIDragDetectorDragRelativity](/docs/reference/engine/enums/UIDragDetectorDragRelativity)

Only applies if a custom drag function is registered through
[SetDragStyleFunction()](/docs/reference/engine/classes/UIDragDetector#SetDragStyleFunction) or
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction).
Sets the paradigm which defines the relativity of the registered
function's inputs/outputs.

For example, returning a [UDim2.fromOffset(1, 0)](/docs/reference/engine/datatypes/UDim2#fromOffset) from a
registered function with this property set to
[Enum.UIDragDetectorDragRelativity.Absolute](/docs/reference/engine/enums/UIDragDetectorDragRelativity#Absolute) will move the detector's
parent to (1, 0) in the designated
[DragSpace](/docs/reference/engine/classes/UIDragDetector#DragSpace), while returning the same
[UDim2](/docs/reference/engine/datatypes/UDim2) with this property set to
[Enum.UIDragDetectorDragRelativity.Relative](/docs/reference/engine/enums/UIDragDetectorDragRelativity#Relative) will move the detector's
parent by (1, 0) in the designated
[DragSpace](/docs/reference/engine/classes/UIDragDetector#DragSpace).

Provide feedback

---

DragRotation

Read Parallel

The rotation performed by the current drag.

UIDragDetector.DragRotation:[number](/docs/luau/numbers)

The rotation performed by the current drag. This value is defined in
degrees relative to the local space of the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) unless
[ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is defined,
in which case the rotation is defined in the local space of that instance
and from its positive X axis.

This property can be changed while there is no active drag to rotate the
dragged object.

Provide feedback

---

DragSpace

Read Parallel

Sets the paradigm which defines the space of inputs/outputs from a custom
drag function.

UIDragDetector.DragSpace:[Enum.UIDragDetectorDragSpace](/docs/reference/engine/enums/UIDragDetectorDragSpace)

Only applies if a custom drag function is registered through
[SetDragStyleFunction()](/docs/reference/engine/classes/UIDragDetector#SetDragStyleFunction) or
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction).
Sets the paradigm which defines the space of the registered function's
inputs/outputs.

For example, if the detector's parent [GuiObject](/docs/reference/engine/classes/GuiObject) is a child of a
parent [GuiObject](/docs/reference/engine/classes/GuiObject) that's rotated:

* Returning a [UDim2.fromOffset(1, 0)](/docs/reference/engine/datatypes/UDim2#fromOffset) from a registered function
  with this property set to [Enum.UIDragDetectorDragSpace.Parent](/docs/reference/engine/enums/UIDragDetectorDragSpace#Parent) will
  move the detector's parent [GuiObject](/docs/reference/engine/classes/GuiObject) to the right by 1 pixel in
  the local space affected by its parent's rotation.
* Returning a [UDim2.fromOffset(1, 0)](/docs/reference/engine/datatypes/UDim2#fromOffset) from a registered function
  with this property set to [Enum.UIDragDetectorDragSpace.LayerCollector](/docs/reference/engine/enums/UIDragDetectorDragSpace#LayerCollector)
  will move the detector's parent [GuiObject](/docs/reference/engine/classes/GuiObject) to the right by 1
  pixel in the space of the [LayerCollector](/docs/reference/engine/classes/LayerCollector).

Provide feedback

---

DragStyle

Read Parallel

The paradigm used to generate proposed motion.

UIDragDetector.DragStyle:[Enum.UIDragDetectorDragStyle](/docs/reference/engine/enums/UIDragDetectorDragStyle)

The paradigm used to generate proposed motion, given a stream of input
position vectors. See [Enum.UIDragDetectorDragStyle](/docs/reference/engine/enums/UIDragDetectorDragStyle) for options.

Provide feedback

---

DragUDim2

Read Parallel

The translation performed by the current drag expressed in a
[UDim2](/docs/reference/engine/datatypes/UDim2) value.

UIDragDetector.DragUDim2:[UDim2](/docs/reference/engine/datatypes/UDim2)

The translation performed by the current drag expressed in a
[UDim2](/docs/reference/engine/datatypes/UDim2) value. Translation is done through
[Offset](/docs/reference/engine/datatypes/UDim#Offset) or [Scale](/docs/reference/engine/datatypes/UDim#Scale) value changes
depending on the [DragRelativity](/docs/reference/engine/classes/UIDragDetector#DragRelativity)
value, and it is relative to the detector's local space unless a
[ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is defined.

This property can be changed while there is no active drag to move the
dragged object.

Provide feedback

---

Enabled

Read Parallel

Whether the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) responds to user input.

UIDragDetector.Enabled:[boolean](/docs/luau/booleans)

If true, the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) responds to user input; if false,
it does not.

Provide feedback

---

MaxDragAngle

Read Parallel

Along with [MinDragAngle](/docs/reference/engine/classes/UIDragDetector#MinDragAngle), impedes the
detector's attempts to generate rotational motion.

UIDragDetector.MaxDragAngle:[number](/docs/luau/numbers)

If this property is greater than
[MinDragAngle](/docs/reference/engine/classes/UIDragDetector#MinDragAngle), rotation will be clamped
within the range of [MinDragAngle](/docs/reference/engine/classes/UIDragDetector#MinDragAngle) and
[MaxDragAngle](/docs/reference/engine/classes/UIDragDetector#MaxDragAngle). Positive values impede
clockwise rotation while negative values impede counterclockwise rotation.

This is not a constraint; it merely impedes the detector's attempts to
generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Only relevant if [DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is
[Enum.UIDragDetectorDragStyle.Rotate](/docs/reference/engine/enums/UIDragDetectorDragStyle#Rotate).

Provide feedback

---

MaxDragTranslation

Read Parallel

Along with [MinDragTranslation](/docs/reference/engine/classes/UIDragDetector#MinDragTranslation),
impedes the detector's attempts to generate linear/planar motion.

UIDragDetector.MaxDragTranslation:[UDim2](/docs/reference/engine/datatypes/UDim2)

If the corresponding [Offset](/docs/reference/engine/datatypes/UDim#Offset) and/or
[Scale](/docs/reference/engine/datatypes/UDim#Scale) values are greater than those of
[MinDragTranslation](/docs/reference/engine/classes/UIDragDetector#MinDragTranslation) in all
dimensions, linear/planar translation will be clamped within the range of
[MinDragTranslation](/docs/reference/engine/classes/UIDragDetector#MinDragTranslation) and
[MaxDragTranslation](/docs/reference/engine/classes/UIDragDetector#MaxDragTranslation).

This is not a constraint; it merely impedes the detector's attempts to
generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Only relevant if [DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is
[Enum.UIDragDetectorDragStyle.TranslateLine](/docs/reference/engine/enums/UIDragDetectorDragStyle#TranslateLine) or
[Enum.UIDragDetectorDragStyle.TranslatePlane](/docs/reference/engine/enums/UIDragDetectorDragStyle#TranslatePlane).

Provide feedback

---

MinDragAngle

Read Parallel

Along with [MaxDragAngle](/docs/reference/engine/classes/UIDragDetector#MaxDragAngle), impedes the
detector's attempts to generate rotational motion.

UIDragDetector.MinDragAngle:[number](/docs/luau/numbers)

If this property is less than
[MaxDragAngle](/docs/reference/engine/classes/UIDragDetector#MaxDragAngle), rotation will be clamped
within the range of [MinDragAngle](/docs/reference/engine/classes/UIDragDetector#MinDragAngle) and
[MaxDragAngle](/docs/reference/engine/classes/UIDragDetector#MaxDragAngle). Positive values impede
clockwise rotation while negative values impede counterclockwise rotation.

This is not a constraint; it merely impedes the detector's attempts to
generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Only relevant if [DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is
[Enum.UIDragDetectorDragStyle.Rotate](/docs/reference/engine/enums/UIDragDetectorDragStyle#Rotate).

Provide feedback

---

MinDragTranslation

Read Parallel

Along with [MaxDragTranslation](/docs/reference/engine/classes/UIDragDetector#MaxDragTranslation),
impedes the detector's attempts to generate linear/planar motion.

UIDragDetector.MinDragTranslation:[UDim2](/docs/reference/engine/datatypes/UDim2)

If the corresponding [Offset](/docs/reference/engine/datatypes/UDim#Offset) and/or
[Scale](/docs/reference/engine/datatypes/UDim#Scale) values are less than those of
[MaxDragTranslation](/docs/reference/engine/classes/UIDragDetector#MaxDragTranslation) in all
dimensions, linear/planar translation will be clamped within the range of
[MinDragTranslation](/docs/reference/engine/classes/UIDragDetector#MinDragTranslation) and
[MaxDragTranslation](/docs/reference/engine/classes/UIDragDetector#MaxDragTranslation).

This is not a constraint; it merely impedes the detector's attempts to
generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Only relevant if [DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is
[Enum.UIDragDetectorDragStyle.TranslateLine](/docs/reference/engine/enums/UIDragDetectorDragStyle#TranslateLine) or
[Enum.UIDragDetectorDragStyle.TranslatePlane](/docs/reference/engine/enums/UIDragDetectorDragStyle#TranslatePlane).

Provide feedback

---

ReferenceUIInstance

Read Parallel

A [GuiObject](/docs/reference/engine/classes/GuiObject) instance whose local space and absolute center
position is the reference space and origin for the detector.

UIDragDetector.ReferenceUIInstance:[GuiObject](/docs/reference/engine/classes/GuiObject)

A [GuiObject](/docs/reference/engine/classes/GuiObject) instance whose local space and absolute center
position is the reference space and origin for the detector. Setting this
reference affects properties such as
[DragUDim2](/docs/reference/engine/classes/UIDragDetector#DragUDim2),
[DragRotation](/docs/reference/engine/classes/UIDragDetector#DragRotation), and the behavior of
[DragAxis](/docs/reference/engine/classes/UIDragDetector#DragAxis).

Provide feedback

---

ResponseStyle

Read Parallel

The paradigm used to define the response to proposed motion.

UIDragDetector.ResponseStyle:[Enum.UIDragDetectorResponseStyle](/docs/reference/engine/enums/UIDragDetectorResponseStyle)

Once the proposed motion has been computed and potentially constrained,
this paradigm is used to deterimine how to move (or not move) the
[GuiObject](/docs/reference/engine/classes/GuiObject) affected by the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector). See
[Enum.UIDragDetectorResponseStyle](/docs/reference/engine/enums/UIDragDetectorResponseStyle) for options.

Provide feedback

---

SelectionModeDragSpeed

Read Parallel

Maximum drag speed for translation.

UIDragDetector.SelectionModeDragSpeed:[UDim2](/docs/reference/engine/datatypes/UDim2)

Defines the maximum drag speed for translation as a combination of
[Scale](/docs/reference/engine/datatypes/UDim#Scale) and [Offset](/docs/reference/engine/datatypes/UDim#Offset) of the first
ancestor [ScreenGui](/docs/reference/engine/classes/ScreenGui) or [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) the
[UIDragDetector](/docs/reference/engine/classes/UIDragDetector) belongs to. This value must be positive and any
value below 0 will be clamped to 0.

Provide feedback

---

SelectionModeRotateSpeed

Read Parallel

Maximum angle per second the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) can rotate at.

UIDragDetector.SelectionModeRotateSpeed:[number](/docs/luau/numbers)

Defines the maximum angle per second at which the [UIDragDetector](/docs/reference/engine/classes/UIDragDetector)
can rotate. This value must be positive and any value below 0 will be
clamped to 0.

Provide feedback

---

UIDragSpeedAxisMapping

Read Parallel

[Enum.UIDragSpeedAxisMapping](/docs/reference/engine/enums/UIDragSpeedAxisMapping) value that determines the X/Y
dimension dragging speeds.

UIDragDetector.UIDragSpeedAxisMapping:[Enum.UIDragSpeedAxisMapping](/docs/reference/engine/enums/UIDragSpeedAxisMapping)

[Enum.UIDragSpeedAxisMapping](/docs/reference/engine/enums/UIDragSpeedAxisMapping) value that determines the X/Y
dimension dragging speeds.

Provide feedback

---

Methods

AddConstraintFunction

Adds a function to modify or constrain proposed motion.

UIDragDetector:AddConstraintFunction(

priority:[number](/docs/luau/numbers), function:[function](/docs/luau/functions)

):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| priority:[number](/docs/luau/numbers)  The order of priority for functions added via this method. Higher values take precedence over lower values. |
| function:[function](/docs/luau/functions)  Function for modifying or constraining proposed motion. This function takes in input [UDim2](/docs/reference/engine/datatypes/UDim2) and float of proposed motion and returns a [UDim2](/docs/reference/engine/datatypes/UDim2) and float of modified or unmodified motion. It can optionally return an [Enum.UIDragDetectorDragRelativity](/docs/reference/engine/enums/UIDragDetectorDragRelativity) and [Enum.UIDragDetectorDragSpace](/docs/reference/engine/enums/UIDragDetectorDragSpace) as the third and fourth return values as output overrides. |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Use this connection object to remove the constraint function.

Adds a function to modify or constrain proposed motion. The function takes
an input [UDim2](/docs/reference/engine/datatypes/UDim2) (position) and float (rotation) of proposed
motion and returns a [UDim2](/docs/reference/engine/datatypes/UDim2) and float of modified or
unmodified motion. You can add multiple functions which will be called in
order by priority, passing the results along in a chain.

The input is expressed in the space defined by the
[DragSpace](/docs/reference/engine/classes/UIDragDetector#DragSpace) property, either as a delta or
the final desired position/rotation based on the
[DragRelativity](/docs/reference/engine/classes/UIDragDetector#DragRelativity) property. The output
should be expressed in the same space and relativity, unless overridden by
returning a specified [Enum.UIDragDetectorDragRelativity](/docs/reference/engine/enums/UIDragDetectorDragRelativity) and
[Enum.UIDragDetectorDragSpace](/docs/reference/engine/enums/UIDragDetectorDragSpace) as the third and fourth return values.

To remove an added constraint function, call
[Disconnect()](/docs/reference/engine/datatypes/RBXScriptConnection#Disconnect) on the returned
connection object.

Provide feedback

---

GetReferencePosition

Returns the reference [UDim2](/docs/reference/engine/datatypes/UDim2) position of the current drag's
reference origin.

UIDragDetector:GetReferencePosition():[UDim2](/docs/reference/engine/datatypes/UDim2)

Returns

[UDim2](/docs/reference/engine/datatypes/UDim2)

[UDim2](/docs/reference/engine/datatypes/UDim2) position of the current drag's reference element.

When no [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is
set, this function returns the [UDim2](/docs/reference/engine/datatypes/UDim2) position of the dragged
object's immediate parent [GuiObject](/docs/reference/engine/classes/GuiObject) (if one exists), or else the
[UDim2](/docs/reference/engine/datatypes/UDim2) position of the dragged object.

When a [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is
set, this function returns the [UDim2](/docs/reference/engine/datatypes/UDim2) position of that reference
instance.

Provide feedback

---

GetReferenceRotation

Returns the reference rotation of the current drag's reference element.

UIDragDetector:GetReferenceRotation():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Rotation of the current drag's reference element.

When no [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is
set, this function returns the rotation of the dragged object's immediate
parent [GuiObject](/docs/reference/engine/classes/GuiObject) (if one exists), or else the rotation of the
dragged object.

When a [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is
set, this function returns the rotation of that reference instance.

Provide feedback

---

SetDragStyleFunction

Passes a function to be used if and only if
[DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is set to
[Enum.UIDragDetectorDragStyle.Scriptable](/docs/reference/engine/enums/UIDragDetectorDragStyle#Scriptable).

UIDragDetector:SetDragStyleFunction(function:[function](/docs/luau/functions)):()

Parameters

|  |
| --- |
| function:[function](/docs/luau/functions)  Function for monitoring [DragContinue](/docs/reference/engine/classes/UIDragDetector#DragContinue) signals. This function receives the signal's screen space input position and returns a [UDim2](/docs/reference/engine/datatypes/UDim2) and float containing the desired motion of the drag in the desired space and relativity. If this function returns nil, the object will not be moved. |

Returns

()

Passes a function to be used if and only if
[DragStyle](/docs/reference/engine/classes/UIDragDetector#DragStyle) is set to
[Enum.UIDragDetectorDragStyle.Scriptable](/docs/reference/engine/enums/UIDragDetectorDragStyle#Scriptable). The given function receives the
signal's screen space input position with type [Vector2](/docs/reference/engine/datatypes/Vector2), and it
returns a [UDim2](/docs/reference/engine/datatypes/UDim2) (position) and float (rotation) containing the
desired motion of the drag. The space of the return values and the
relativity of the motion are determined by the
[DragSpace](/docs/reference/engine/classes/UIDragDetector#DragSpace) and
[DragRelativity](/docs/reference/engine/classes/UIDragDetector#DragRelativity) properties, unless
overridden by returning a specified [Enum.UIDragDetectorDragRelativity](/docs/reference/engine/enums/UIDragDetectorDragRelativity)
and [Enum.UIDragDetectorDragSpace](/docs/reference/engine/enums/UIDragDetectorDragSpace) as the third and fourth return values.

If the function returns nil, the object will not be moved. This is
useful if the script has not yet collected all the information it needs to
give the correct answer, or in temporary cases where you want the object
to stay where it is.

Provide feedback

---

Events

DragContinue

Fires when a user continues dragging the UI element after
[DragStart](/docs/reference/engine/classes/UIDragDetector#DragStart) has been initiated.

UIDragDetector.DragContinue(inputPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| inputPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)  [Vector2](/docs/reference/engine/datatypes/Vector2) representing the current input position. |

Fires when a user continues dragging the UI element after
[DragStart](/docs/reference/engine/classes/UIDragDetector#DragStart) has been initiated.

Provide feedback

---

DragEnd

Fires when a user stops dragging the UI element.

UIDragDetector.DragEnd(inputPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| inputPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)  [Vector2](/docs/reference/engine/datatypes/Vector2) representing the current input position. |

Fires when a user stops dragging the UI element.

Provide feedback

---

DragStart

Fires when a user starts dragging the UI element.

UIDragDetector.DragStart(inputPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| inputPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)  [Vector2](/docs/reference/engine/datatypes/Vector2) representing the current input position. |

Fires when a user starts dragging the UI element.

Provide feedback

---