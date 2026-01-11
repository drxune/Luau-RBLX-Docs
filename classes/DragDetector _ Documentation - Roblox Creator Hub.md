# DragDetector | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DragDetector
Scraped: 2026-01-11T02:30:55.257181Z

## Tags
- Not Replicated

## Inherits
- ClickDetector
- DragDetector
- Player
- BasePart
- Instance
- Object
- Model
- DragStyle
- ResponseStyle
- DragDetectors
- Orientation
- ReferenceInstance
- MinDragAngle
- AddConstraintFunction()
- MinDragTranslation
- MaxDragAngle
- MaxDragTranslation
- Axis
- DragFrame
- GetReferenceFrame()
- PVInstance
- Attachment
- DragStart
- DragContinue
- DragEnd
- LocalScripts
- RemoteEvents
- Attachments
- SecondaryAxis
- PermissionPolicy
- Name
- Color
- HasTag()
- Camera
- KeyboardModeSwitchKeyCode
- GamepadModeSwitchKeyCode
- VRSwitchKeyCode
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ClickDetector](/docs/reference/engine/classes/ClickDetector)
6. /
7. [DragDetector](/docs/reference/engine/classes/DragDetector)

English

Feedback

Engine Class

![DragDetector](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/DragDetector-Dark.webp)DragDetector

Instance which facilitates and encourages interaction with 3D objects in an
experience.

---

Summary

Properties

|  |
| --- |
| [ActivatedCursorIcon](#ActivatedCursorIcon):ContentId |
| [ActivatedCursorIconContent](#ActivatedCursorIconContent):[Content](/docs/reference/engine/datatypes/Content) |
| [ApplyAtCenterOfMass](#ApplyAtCenterOfMass):[boolean](/docs/luau/booleans) |
| [Axis](#Axis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [DragFrame](#DragFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [DragStyle](#DragStyle):[Enum.DragDetectorDragStyle](/docs/reference/engine/enums/DragDetectorDragStyle) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [GamepadModeSwitchKeyCode](#GamepadModeSwitchKeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [KeyboardModeSwitchKeyCode](#KeyboardModeSwitchKeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [MaxDragAngle](#MaxDragAngle):[number](/docs/luau/numbers) |
| [MaxDragTranslation](#MaxDragTranslation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [MaxForce](#MaxForce):[number](/docs/luau/numbers) |
| [MaxTorque](#MaxTorque):[number](/docs/luau/numbers) |
| [MinDragAngle](#MinDragAngle):[number](/docs/luau/numbers) |
| [MinDragTranslation](#MinDragTranslation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Orientation](#Orientation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [PermissionPolicy](#PermissionPolicy):[Enum.DragDetectorPermissionPolicy](/docs/reference/engine/enums/DragDetectorPermissionPolicy) |
| [ReferenceInstance](#ReferenceInstance):[Instance](/docs/reference/engine/datatypes/Instance) |
| [ResponseStyle](#ResponseStyle):[Enum.DragDetectorResponseStyle](/docs/reference/engine/enums/DragDetectorResponseStyle) |
| [Responsiveness](#Responsiveness):[number](/docs/luau/numbers) |
| [RunLocally](#RunLocally):[boolean](/docs/luau/booleans) |
| [SecondaryAxis](#SecondaryAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [TrackballRadialPullFactor](#TrackballRadialPullFactor):[number](/docs/luau/numbers) |
| [TrackballRollFactor](#TrackballRollFactor):[number](/docs/luau/numbers) |
| [VRSwitchKeyCode](#VRSwitchKeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [WorldAxis](#WorldAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [WorldSecondaryAxis](#WorldSecondaryAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [AddConstraintFunction](#AddConstraintFunction)(priority: [number](/docs/luau/numbers),function: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection) |
| [GetReferenceFrame](#GetReferenceFrame)():[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [RestartDrag](#RestartDrag)():() |
| [SetDragStyleFunction](#SetDragStyleFunction)(function: [function](/docs/luau/functions)):() |
| [SetPermissionPolicyFunction](#SetPermissionPolicyFunction)(function: [function](/docs/luau/functions)):() |

Events

|  |
| --- |
| [DragContinue](#DragContinue)(playerWhoDragged: [Player](/docs/reference/engine/classes/Player),cursorRay: [Ray](/docs/reference/engine/datatypes/Ray),viewFrame: [CFrame](/docs/reference/engine/datatypes/CFrame),vrInputFrame: OptionalCoordinateFrame,isModeSwitchKeyDown: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DragEnd](#DragEnd)(playerWhoDragged: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [DragStart](#DragStart)(playerWhoDragged: [Player](/docs/reference/engine/classes/Player),cursorRay: [Ray](/docs/reference/engine/datatypes/Ray),viewFrame: [CFrame](/docs/reference/engine/datatypes/CFrame),hitFrame: [CFrame](/docs/reference/engine/datatypes/CFrame),clickedPart: [BasePart](/docs/reference/engine/classes/BasePart),vrInputFrame: OptionalCoordinateFrame,isModeSwitchKeyDown: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

8 inherited from [ClickDetector](/docs/reference/engine/classes/ClickDetector)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [DragDetector](/docs/reference/engine/classes/DragDetector) instance facilitates and encourages interaction with
3D objects in an experience, such as opening doors and drawers, sliding a part
around, and much more. Key features include:

* Place a [DragDetector](/docs/reference/engine/classes/DragDetector) under any [BasePart](/docs/reference/engine/classes/BasePart) or [Model](/docs/reference/engine/classes/Model) to
  make it draggable via all inputs (mouse, touch, gamepad, and VR), all
  without a single line of code.
* Choose from several [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) options, define
  how the object responds to motion via
  [ResponseStyle](/docs/reference/engine/classes/DragDetector#ResponseStyle), and optionally apply axis
  or movement limits.
* Scripts can respond to manipulation of dragged objects to drive UI or make
  logical decisions, such as adjusting the light level in a room based on a
  sliding wall switch dimmer.
* Players can manipulate anchored parts or models and they'll stay exactly
  where you put them upon release.
* [DragDetectors](/docs/reference/engine/classes/DragDetector) work in Studio as long as you're not
  using the Select, Move, Scale, or Rotate tools, making it
  easier to test and adjust draggable objects while editing.

See the [3D Drag Detectors](/docs/ui/3D-drag-detectors) guide for
details and usage examples.

---

API Reference

Properties

ActivatedCursorIcon

Read Parallel

Sets the cursor icon to display when the mouse is activated over the
parent of this [DragDetector](/docs/reference/engine/classes/DragDetector).

DragDetector.ActivatedCursorIcon:ContentId

Sets the cursor icon to display when the mouse is activated over the
parent of this [DragDetector](/docs/reference/engine/classes/DragDetector). If this property is left blank, the
detector will use the default icon.

To change the activated cursor icon, set this property to the asset ID of
the image you'd like to use.

Provide feedback

---

ActivatedCursorIconContent

Read Parallel

Sets the cursor icon to display when the mouse is activated over the
parent of this [DragDetector](/docs/reference/engine/classes/DragDetector). Only supports asset URIs

DragDetector.ActivatedCursorIconContent:[Content](/docs/reference/engine/datatypes/Content)

Sets the cursor icon to display when the mouse is activated over the
parent of this [DragDetector](/docs/reference/engine/classes/DragDetector). If this property is left blank, the
detector will use the default icon.

To change the activated cursor icon, set this property to the asset ID of
the image you'd like to use. Only asset URIs are supported for this
property.

Provide feedback

---

ApplyAtCenterOfMass

Read Parallel

Whether constraint force is applied to the object's center of mass.

DragDetector.ApplyAtCenterOfMass:[boolean](/docs/luau/booleans)

When false (default), constraint force is applied at the point the user
clicks on. When true, force is applied at the object's center of mass.
Only relevant if [ResponseStyle](/docs/reference/engine/classes/DragDetector#ResponseStyle) is
[Enum.DragDetectorResponseStyle.Physical](/docs/reference/engine/enums/DragDetectorResponseStyle#Physical) and the parent object is
unanchored.

Provide feedback

---

Axis

Not Replicated

Read Parallel

The primary axis of motion, expressed relative to the reference frame.

DragDetector.Axis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The primary axis of motion, expressed relative to the reference frame. For
a [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) of
[Enum.DragDetectorDragStyle.TranslateLine](/docs/reference/engine/enums/DragDetectorDragStyle#TranslateLine), the direction of translation;
for [Enum.DragDetectorDragStyle.TranslatePlane](/docs/reference/engine/enums/DragDetectorDragStyle#TranslatePlane), the normal to the plane
of motion; for [Enum.DragDetectorDragStyle.RotateAxis](/docs/reference/engine/enums/DragDetectorDragStyle#RotateAxis), the axis of 1D
rotation. Changing this value automatically updates
[Orientation](/docs/reference/engine/classes/DragDetector#Orientation) and vice versa.

Provide feedback

---

DragFrame

Read Parallel

The [CFrame](/docs/reference/engine/datatypes/CFrame) of the pivot, dependent on the drag detector's
[ReferenceInstance](/docs/reference/engine/classes/DragDetector#ReferenceInstance).

DragDetector.DragFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

If [ReferenceInstance](/docs/reference/engine/classes/DragDetector#ReferenceInstance) is set, the
[CFrame](/docs/reference/engine/datatypes/CFrame) of the pivot relative to the reference frame; otherwise,
the [CFrame](/docs/reference/engine/datatypes/CFrame) of the pivot relative to its frame at the beginning
of the drag.

Provide feedback

---

DragStyle

Read Parallel

The paradigm used to generate proposed motion.

DragDetector.DragStyle:[Enum.DragDetectorDragStyle](/docs/reference/engine/enums/DragDetectorDragStyle)

The paradigm used to generate proposed motion, given a stream of cursor
rays. See [Enum.DragDetectorDragStyle](/docs/reference/engine/enums/DragDetectorDragStyle) for options.

Provide feedback

---

Enabled

Read Parallel

Whether the [DragDetector](/docs/reference/engine/classes/DragDetector) responds to user input.

DragDetector.Enabled:[boolean](/docs/luau/booleans)

If true, the [DragDetector](/docs/reference/engine/classes/DragDetector) responds to user input; if false, it
does not.

Provide feedback

---

GamepadModeSwitchKeyCode

Read Parallel

During gamepad input, the modifier [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for the secondary mode
of motion.

DragDetector.GamepadModeSwitchKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

During gamepad input, the [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for toggling the secondary mode
of motion. Only applies if the drag detector's
[DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) has both primary and secondary
modes of motion.

Provide feedback

---

KeyboardModeSwitchKeyCode

Read Parallel

During keyboard input, the modifier [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for the secondary mode
of motion.

DragDetector.KeyboardModeSwitchKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

During keyboard input, the [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for toggling the secondary mode
of motion. Only applies if the drag detector's
[DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) has both primary and secondary
modes of motion.

Provide feedback

---

MaxDragAngle

Read Parallel

Along with [MinDragAngle](/docs/reference/engine/classes/DragDetector#MinDragAngle), impedes the
drag detector's attempts to generate motion.

DragDetector.MaxDragAngle:[number](/docs/luau/numbers)

If this is greater than [MinDragAngle](/docs/reference/engine/classes/DragDetector#MinDragAngle),
translation will be clamped within that range.

This is not a constraint; it merely impedes the drag detector's attempts
to generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/DragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Only relevant if [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is
[Enum.DragDetectorDragStyle.RotateAxis](/docs/reference/engine/enums/DragDetectorDragStyle#RotateAxis).

Provide feedback

---

MaxDragTranslation

Read Parallel

Along with [MinDragTranslation](/docs/reference/engine/classes/DragDetector#MinDragTranslation),
impedes the drag detector's attempts to generate motion.

DragDetector.MaxDragTranslation:[Vector3](/docs/reference/engine/datatypes/Vector3)

In any dimension, if this is greater than
[MinDragTranslation](/docs/reference/engine/classes/DragDetector#MinDragTranslation), translation
will be clamped within that range.

This is not a constraint; it merely impedes the drag detector's attempts
to generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/DragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Provide feedback

---

MaxForce

Read Parallel

Maximum force applied for the object to reach its goal.

DragDetector.MaxForce:[number](/docs/luau/numbers)

Maximum force applied for the object to reach its goal. Only relevant if
[ResponseStyle](/docs/reference/engine/classes/DragDetector#ResponseStyle) is
[Enum.DragDetectorResponseStyle.Physical](/docs/reference/engine/enums/DragDetectorResponseStyle#Physical) and the parent object is
unanchored.

Provide feedback

---

MaxTorque

Read Parallel

Maximum torque applied for the object to reach its goal.

DragDetector.MaxTorque:[number](/docs/luau/numbers)

Maximum torque applied for the object to reach its goal. Only relevant if
[ResponseStyle](/docs/reference/engine/classes/DragDetector#ResponseStyle) is
[Enum.DragDetectorResponseStyle.Physical](/docs/reference/engine/enums/DragDetectorResponseStyle#Physical) and the parent object is
unanchored.

Provide feedback

---

MinDragAngle

Read Parallel

Along with [MaxDragAngle](/docs/reference/engine/classes/DragDetector#MaxDragAngle), impedes the
drag detector's attempts to generate motion.

DragDetector.MinDragAngle:[number](/docs/luau/numbers)

If this is less than [MaxDragAngle](/docs/reference/engine/classes/DragDetector#MaxDragAngle),
translation will be clamped within that range.

This is not a constraint; it merely impedes the drag detector's attempts
to generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/DragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Only relevant if [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is
[Enum.DragDetectorDragStyle.RotateAxis](/docs/reference/engine/enums/DragDetectorDragStyle#RotateAxis).

Provide feedback

---

MinDragTranslation

Read Parallel

Along with [MaxDragTranslation](/docs/reference/engine/classes/DragDetector#MaxDragTranslation),
impedes the drag detector's attempts to generate motion.

DragDetector.MinDragTranslation:[Vector3](/docs/reference/engine/datatypes/Vector3)

In any dimension, if this is less than
[MaxDragTranslation](/docs/reference/engine/classes/DragDetector#MaxDragTranslation), translation
will be clamped within that range.

This is not a constraint; it merely impedes the drag detector's attempts
to generate motion in order to remain within limits. See
[AddConstraintFunction()](/docs/reference/engine/classes/DragDetector#AddConstraintFunction) to
add custom constraint to a drag.

Provide feedback

---

Orientation

Read Parallel

Specifies the YXZ rotation of axes of motion relative to the reference
frame.

DragDetector.Orientation:[Vector3](/docs/reference/engine/datatypes/Vector3)

Specifies the YXZ rotation of axes of motion relative to the reference
frame (does not change the orientation of the reference frame itself).
Linear translation and axial rotation will be on this reoriented Y
axis, and planar translation in the XZ plane. Changing this value
automatically updates [Axis](/docs/reference/engine/classes/DragDetector#Axis) and vice versa.

Provide feedback

---

PermissionPolicy

Read Parallel

Controls the permission level for which players can interact with the
[DragDetector](/docs/reference/engine/classes/DragDetector).

DragDetector.PermissionPolicy:[Enum.DragDetectorPermissionPolicy](/docs/reference/engine/enums/DragDetectorPermissionPolicy)

Controls the permission level for which players can interact with the
[DragDetector](/docs/reference/engine/classes/DragDetector). Default is
[Enum.DragDetectorPermissionPolicy.Everybody](/docs/reference/engine/enums/DragDetectorPermissionPolicy#Everybody).

Provide feedback

---

ReferenceInstance

Read Parallel

An instance whose [CFrame](/docs/reference/engine/datatypes/CFrame) is the reference frame for the drag
detector.

DragDetector.ReferenceInstance:[Instance](/docs/reference/engine/datatypes/Instance)

An instance whose [CFrame](/docs/reference/engine/datatypes/CFrame) is the reference frame for the drag
detector. The [DragFrame](/docs/reference/engine/classes/DragDetector#DragFrame) is expressed
relative to this [CFrame](/docs/reference/engine/datatypes/CFrame) which may be retrieved via the
[GetReferenceFrame()](/docs/reference/engine/classes/DragDetector#GetReferenceFrame) method.

If this instance is a [PVInstance](/docs/reference/engine/classes/PVInstance), the reference frame will be its
pivot; if an [Attachment](/docs/reference/engine/classes/Attachment), then its world [CFrame](/docs/reference/engine/datatypes/CFrame). If it
is nil or neither of the former, the reference frame will be based on
the pivot of the drag detector's parent [BasePart](/docs/reference/engine/classes/BasePart) or [Model](/docs/reference/engine/classes/Model).

Provide feedback

---

ResponseStyle

Read Parallel

The paradigm used to move, or not move, the objects affected by the drag
detector.

DragDetector.ResponseStyle:[Enum.DragDetectorResponseStyle](/docs/reference/engine/enums/DragDetectorResponseStyle)

Once the proposed motion has been computed and potentially constrained,
this is the paradigm used to move, or not move, the objects affected by
the [DragDetector](/docs/reference/engine/classes/DragDetector). See [Enum.DragDetectorResponseStyle](/docs/reference/engine/enums/DragDetectorResponseStyle) for
options.

Provide feedback

---

Responsiveness

Read Parallel

Higher values cause the object to reach its goal more rapidly.

DragDetector.Responsiveness:[number](/docs/luau/numbers)

Higher values cause the object to reach its goal more rapidly. Only
relevant if [ResponseStyle](/docs/reference/engine/classes/DragDetector#ResponseStyle) is
[Enum.DragDetectorResponseStyle.Physical](/docs/reference/engine/enums/DragDetectorResponseStyle#Physical) and the parent object is
unanchored.

Provide feedback

---

RunLocally

Read Parallel

Whether user input on a [DragDetector](/docs/reference/engine/classes/DragDetector) replicates to the server or
remains local to the specific client.

DragDetector.RunLocally:[boolean](/docs/luau/booleans)

If false (default), the client sends replicated signals
([DragStart](/docs/reference/engine/classes/DragDetector#DragStart),
[DragContinue](/docs/reference/engine/classes/DragDetector#DragContinue),
[DragEnd](/docs/reference/engine/classes/DragDetector#DragEnd)) to the server which processes cursor
rays, makes changes to the data model, and replicates them onwards to
clients.

If true, the client processes those signals itself and does not replicate
them to the server. Client [LocalScripts](/docs/reference/engine/classes/LocalScript) may be used to
respond to these events and [RemoteEvents](/docs/reference/engine/classes/RemoteEvent) may be used
to send any resulting changes that should be replicated to the server.

Provide feedback

---

SecondaryAxis

Not Replicated

Read Parallel

The secondary axis of the motion.

DragDetector.SecondaryAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The secondary axis of the motion. Relates to orientation using the same
paradigm as [Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

TrackballRadialPullFactor

Read Parallel

If [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is
[Enum.DragDetectorDragStyle.RotateTrackball](/docs/reference/engine/enums/DragDetectorDragStyle#RotateTrackball), multiplier for adding a
radial pull rotation as a contribution to the total.

DragDetector.TrackballRadialPullFactor:[number](/docs/luau/numbers)

When the cursor is outside the trackball, the [DragDetector](/docs/reference/engine/classes/DragDetector) can
apply a radial pull rotation that turns the ball as if it were trying to
roll out toward the cursor. This property is a 0 to 1 multiplier for
adding that rotation as a contribution to the total. Only relevant if
[DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is
[Enum.DragDetectorDragStyle.RotateTrackball](/docs/reference/engine/enums/DragDetectorDragStyle#RotateTrackball).

Provide feedback

---

TrackballRollFactor

Read Parallel

If [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is
[Enum.DragDetectorDragStyle.RotateTrackball](/docs/reference/engine/enums/DragDetectorDragStyle#RotateTrackball), multiplier for adding roll
rotation to the total.

DragDetector.TrackballRollFactor:[number](/docs/luau/numbers)

When the cursor is outside the trackball, the [DragDetector](/docs/reference/engine/classes/DragDetector) can
apply a roll rotation that turns the ball as if it were mounted on a vinyl
record facing the viewer. This property is a 0 to 1 multiplier for adding
that roll rotation to the total. Only relevant if
[DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is
[Enum.DragDetectorDragStyle.RotateTrackball](/docs/reference/engine/enums/DragDetectorDragStyle#RotateTrackball).

Provide feedback

---

VRSwitchKeyCode

Read Parallel

During VR input, the modifier [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for the secondary mode of
motion.

DragDetector.VRSwitchKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

During VR input, the [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) for toggling the secondary mode of
motion. Only applies if the drag detector's
[DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) has both primary and secondary
modes of motion.

Provide feedback

---

WorldAxis

Not Replicated

Read Parallel

The [Axis](/docs/reference/engine/classes/DragDetector#Axis) expressed in world space.

DragDetector.WorldAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The [Axis](/docs/reference/engine/classes/DragDetector#Axis) expressed in world space. Relates to
orientation using the same paradigm as [Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

WorldSecondaryAxis

Not Replicated

Read Parallel

The [SecondaryAxis](/docs/reference/engine/classes/DragDetector#SecondaryAxis) expressed in world
space.

DragDetector.WorldSecondaryAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

The [SecondaryAxis](/docs/reference/engine/classes/DragDetector#SecondaryAxis) expressed in world
space. Relates to orientation using the same paradigm as
[Attachments](/docs/reference/engine/classes/Attachment).

Provide feedback

---

Methods

AddConstraintFunction

Adds a function to modify or constrain proposed motion.

DragDetector:AddConstraintFunction(

priority:[number](/docs/luau/numbers), function:[function](/docs/luau/functions)

):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Parameters

|  |
| --- |
| priority:[number](/docs/luau/numbers)  The order of priority for functions added via this method. Higher values take precedence over lower values. |
| function:[function](/docs/luau/functions)  Function for modifying or constraining proposed motion. This function takes an input [CFrame](/docs/reference/engine/datatypes/CFrame) of proposed motion and returns a [CFrame](/docs/reference/engine/datatypes/CFrame) of modified or unmodified motion, both relative to the reference frame. |

Returns

[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)

Use this connection object to remove the constraint function.

Adds a function to modify or constrain proposed motion. The function takes
an input [CFrame](/docs/reference/engine/datatypes/CFrame) of proposed motion and returns a
[CFrame](/docs/reference/engine/datatypes/CFrame) of modified or unmodified motion. Both the input and
output are expressed relative to the reference frame. You can add multiple
functions which will be called in order by priority, passing the results
along in a chain.

To remove an added constraint function, call
[Disconnect()](/docs/reference/engine/datatypes/RBXScriptConnection#Disconnect) on the returned
connection object.

Provide feedback

---

GetReferenceFrame

Returns the reference [CFrame](/docs/reference/engine/datatypes/CFrame) in which motion is expressed.

DragDetector:GetReferenceFrame():[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

The reference [CFrame](/docs/reference/engine/datatypes/CFrame) in which motion is expressed.

Returns the reference [CFrame](/docs/reference/engine/datatypes/CFrame) in which motion is expressed; see
the [ReferenceInstance](/docs/reference/engine/classes/DragDetector#ReferenceInstance) property for
more details.

Provide feedback

---

RestartDrag

May be invoked from a script to restart the drag using new parameters.

DragDetector:RestartDrag():()

Returns

()

May be invoked from a script to restart the drag using new parameters, if
parameters such as [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle),
[Axis](/docs/reference/engine/classes/DragDetector#Axis), or
[SecondaryAxis](/docs/reference/engine/classes/DragDetector#SecondaryAxis) change.

Provide feedback

---

SetDragStyleFunction

Passes a function to be used if and only if
[DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is set to
[Enum.DragDetectorDragStyle.Scriptable](/docs/reference/engine/enums/DragDetectorDragStyle#Scriptable).

DragDetector:SetDragStyleFunction(function:[function](/docs/luau/functions)):()

Parameters

|  |
| --- |
| function:[function](/docs/luau/functions)  Function for monitoring [DragContinue](/docs/reference/engine/classes/DragDetector#DragContinue) signals. This function receives the signal's world space cursor ray and it returns a [CFrame](/docs/reference/engine/datatypes/CFrame) containing the desired location and orientation of the pivot in world space. If this function returns nil, the object will not be moved. |

Returns

()

Passes a function to be used if and only if
[DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) is set to
[Enum.DragDetectorDragStyle.Scriptable](/docs/reference/engine/enums/DragDetectorDragStyle#Scriptable). The given function is called when
responding to a [DragContinue](/docs/reference/engine/classes/DragDetector#DragContinue) signal, it
receives the signal's world space cursor ray with type [Ray](/docs/reference/engine/datatypes/Ray), and
it returns a [CFrame](/docs/reference/engine/datatypes/CFrame) containing the desired location and
orientation of the pivot in world space.

If the function returns nil, the object will not be moved. This is
useful if the script has not yet collected all the information it needs to
give the correct answer, or in temporary cases where you want the object
to stay where it is.

Provide feedback

---

SetPermissionPolicyFunction

Passes a function to be used if and only if
[PermissionPolicy](/docs/reference/engine/classes/DragDetector#PermissionPolicy) is set to
[Enum.DragDetectorPermissionPolicy.Scriptable](/docs/reference/engine/enums/DragDetectorPermissionPolicy#Scriptable).

DragDetector:SetPermissionPolicyFunction(function:[function](/docs/luau/functions)):()

Parameters

|  |
| --- |
| function:[function](/docs/luau/functions)  Function for setting the detector's interactivity. This function accepts a [Player](/docs/reference/engine/classes/Player) parameter for enabling/disabling the detector for a specific player. It also receives a part parameter indicating which specific [BasePart](/docs/reference/engine/classes/BasePart) was clicked, such as one part within a draggable [Model](/docs/reference/engine/classes/Model); this is useful for enabling/disabling the detector based on that part's [Name](/docs/reference/engine/classes/Instance#Name), [Color](/docs/reference/engine/classes/BasePart#Color), [HasTag()](/docs/reference/engine/classes/Instance#HasTag) value, or other details. |

Returns

()

Passes a function to be used if and only if
[PermissionPolicy](/docs/reference/engine/classes/DragDetector#PermissionPolicy) is set to
[Enum.DragDetectorPermissionPolicy.Scriptable](/docs/reference/engine/enums/DragDetectorPermissionPolicy#Scriptable). The given function accepts
a [Player](/docs/reference/engine/classes/Player) parameter for enabling/disabling the detector for a
specific player. It also receives a part parameter indicating which
specific [BasePart](/docs/reference/engine/classes/BasePart) was clicked, such as one part within a draggable
[Model](/docs/reference/engine/classes/Model); this is useful for enabling/disabling the detector based on
that part's [Name](/docs/reference/engine/classes/Instance#Name), [Color](/docs/reference/engine/classes/BasePart#Color),
[HasTag()](/docs/reference/engine/classes/Instance#HasTag) value, or other details.

```
local dragDetector = script.Parent.DragDetector



dragDetector.PermissionPolicy = Enum.DragDetectorPermissionPolicy.Scriptable



dragDetector:SetPermissionPolicyFunction(function(player, part)



if player and player:GetAttribute("IsInTurn") then



return true



elseif part and not part:GetAttribute("IsDraggable") then



return false



else



return true



end



end)
```

Provide feedback

---

Events

DragContinue

Fires when a user continues dragging the object after
[DragStart](/docs/reference/engine/classes/DragDetector#DragStart) has been initiated.

DragDetector.DragContinue(

playerWhoDragged:[Player](/docs/reference/engine/classes/Player), cursorRay:[Ray](/docs/reference/engine/datatypes/Ray), viewFrame:[CFrame](/docs/reference/engine/datatypes/CFrame), vrInputFrame:OptionalCoordinateFrame, isModeSwitchKeyDown:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoDragged:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who initiated the drag through [DragStart](/docs/reference/engine/classes/DragDetector#DragStart) and is now continuing the drag. |
| cursorRay:[Ray](/docs/reference/engine/datatypes/Ray)  [Ray](/docs/reference/engine/datatypes/Ray) emanating from the cursor, aimed into the scene. |
| viewFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)  [CFrame](/docs/reference/engine/datatypes/CFrame) of the user's [Camera](/docs/reference/engine/classes/Camera). |
| vrInputFrame:OptionalCoordinateFrame  If using a VR input device, the [CFrame](/docs/reference/engine/datatypes/CFrame) of the hand holding the cursor/pointer/controller. |
| isModeSwitchKeyDown:[boolean](/docs/luau/booleans)  If the drag detector's [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) has both primary and secondary modes of motion, this parameter indicates whether the user is pressing the modifier input defined through [KeyboardModeSwitchKeyCode](/docs/reference/engine/classes/DragDetector#KeyboardModeSwitchKeyCode), [GamepadModeSwitchKeyCode](/docs/reference/engine/classes/DragDetector#GamepadModeSwitchKeyCode), or [VRSwitchKeyCode](/docs/reference/engine/classes/DragDetector#VRSwitchKeyCode). |

Fires when a user continues dragging the object after
[DragStart](/docs/reference/engine/classes/DragDetector#DragStart) has been initiated.

Provide feedback

---

DragEnd

Fires when a user stops dragging the object.

DragDetector.DragEnd(playerWhoDragged:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoDragged:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who initiated the drag through [DragStart](/docs/reference/engine/classes/DragDetector#DragStart) and has now ended (released) the drag. |

Fires when a user stops dragging the object.

Provide feedback

---

DragStart

Fires when a user starts dragging the object.

DragDetector.DragStart(

playerWhoDragged:[Player](/docs/reference/engine/classes/Player), cursorRay:[Ray](/docs/reference/engine/datatypes/Ray), viewFrame:[CFrame](/docs/reference/engine/datatypes/CFrame), hitFrame:[CFrame](/docs/reference/engine/datatypes/CFrame), clickedPart:[BasePart](/docs/reference/engine/classes/BasePart), vrInputFrame:OptionalCoordinateFrame, isModeSwitchKeyDown:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoDragged:[Player](/docs/reference/engine/classes/Player)  [Player](/docs/reference/engine/classes/Player) who initiated the drag. |
| cursorRay:[Ray](/docs/reference/engine/datatypes/Ray)  [Ray](/docs/reference/engine/datatypes/Ray) emanating from the cursor, aimed into the scene. |
| viewFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)  [CFrame](/docs/reference/engine/datatypes/CFrame) of the user's [Camera](/docs/reference/engine/classes/Camera). |
| hitFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)  The hit frame of the cursor raycast that initiated the drag. |
| clickedPart:[BasePart](/docs/reference/engine/classes/BasePart)  The part that was hit by the cursor raycast that initiated the drag. |
| vrInputFrame:OptionalCoordinateFrame  If using a VR input device, the [CFrame](/docs/reference/engine/datatypes/CFrame) of the hand holding the cursor/pointer/controller. |
| isModeSwitchKeyDown:[boolean](/docs/luau/booleans)  If the drag detector's [DragStyle](/docs/reference/engine/classes/DragDetector#DragStyle) has both primary and secondary modes of motion, this parameter indicates whether the user is pressing the modifier input defined through [KeyboardModeSwitchKeyCode](/docs/reference/engine/classes/DragDetector#KeyboardModeSwitchKeyCode), [GamepadModeSwitchKeyCode](/docs/reference/engine/classes/DragDetector#GamepadModeSwitchKeyCode), or [VRSwitchKeyCode](/docs/reference/engine/classes/DragDetector#VRSwitchKeyCode). |

Fires when a user starts dragging the object.

Provide feedback

---