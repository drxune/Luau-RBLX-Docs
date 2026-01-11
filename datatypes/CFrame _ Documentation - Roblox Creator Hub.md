# CFrame | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/CFrame
Scraped: 2026-01-11T02:44:41.987773Z

## Inherits
- Instances
- Camera
- Attachments
- BasePart.CFrame
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [CFrame](/docs/reference/engine/datatypes/CFrame)

English

Feedback

Engine Data Type

CFrame

A data type that represents both a 3D position and orientation.

---

Summary

Constructors

|  |
| --- |
| [new](#new)() |
| [new](#new-pos)(pos: [Vector3](/docs/reference/engine/datatypes/Vector3)) |
| [new](#new-pos-lookAt)(pos: [Vector3](/docs/reference/engine/datatypes/Vector3),lookAt: [Vector3](/docs/reference/engine/datatypes/Vector3)) |
| [new](#new-x-y-z)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers)) |
| [new](#new-x-y-z-qX-q)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers),qX: [number](/docs/luau/numbers),qY: [number](/docs/luau/numbers),qZ: [number](/docs/luau/numbers),qW: [number](/docs/luau/numbers)) |
| [new](#new-x-y-z-R00)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers),z: [number](/docs/luau/numbers),R00: [number](/docs/luau/numbers),R01: [number](/docs/luau/numbers),R02: [number](/docs/luau/numbers),R10: [number](/docs/luau/numbers),R11: [number](/docs/luau/numbers),R12: [number](/docs/luau/numbers),R20: [number](/docs/luau/numbers),R21: [number](/docs/luau/numbers),R22: [number](/docs/luau/numbers)) |
| [lookAt](#lookAt)(at: [Vector3](/docs/reference/engine/datatypes/Vector3),lookAt: [Vector3](/docs/reference/engine/datatypes/Vector3),up: [Vector3](/docs/reference/engine/datatypes/Vector3)) |
| [lookAlong](#lookAlong)(at: [Vector3](/docs/reference/engine/datatypes/Vector3),direction: [Vector3](/docs/reference/engine/datatypes/Vector3),up: [Vector3](/docs/reference/engine/datatypes/Vector3)) |
| [fromRotationBetweenVectors](#fromRotationBetweenVectors)(from: [Vector3](/docs/reference/engine/datatypes/Vector3),to: [Vector3](/docs/reference/engine/datatypes/Vector3)) |
| [fromEulerAngles](#fromEulerAngles)(rx: [number](/docs/luau/numbers),ry: [number](/docs/luau/numbers),rz: [number](/docs/luau/numbers),order: [Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder)) |
| [fromEulerAnglesXYZ](#fromEulerAnglesXYZ)(rx: [number](/docs/luau/numbers),ry: [number](/docs/luau/numbers),rz: [number](/docs/luau/numbers)) |
| [fromEulerAnglesYXZ](#fromEulerAnglesYXZ)(rx: [number](/docs/luau/numbers),ry: [number](/docs/luau/numbers),rz: [number](/docs/luau/numbers)) |
| [Angles](#Angles)(rx: [number](/docs/luau/numbers),ry: [number](/docs/luau/numbers),rz: [number](/docs/luau/numbers)) |
| [fromOrientation](#fromOrientation)(rx: [number](/docs/luau/numbers),ry: [number](/docs/luau/numbers),rz: [number](/docs/luau/numbers)) |
| [fromAxisAngle](#fromAxisAngle)(v: [Vector3](/docs/reference/engine/datatypes/Vector3),r: [number](/docs/luau/numbers)) |
| [fromMatrix](#fromMatrix)(pos: [Vector3](/docs/reference/engine/datatypes/Vector3),vX: [Vector3](/docs/reference/engine/datatypes/Vector3),vY: [Vector3](/docs/reference/engine/datatypes/Vector3),vZ: [Vector3](/docs/reference/engine/datatypes/Vector3)) |

Properties

|  |
| --- |
| [identity](#identity):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Rotation](#Rotation):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [X](#X):[number](/docs/luau/numbers) |
| [Y](#Y):[number](/docs/luau/numbers) |
| [Z](#Z):[number](/docs/luau/numbers) |
| [LookVector](#LookVector):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [RightVector](#RightVector):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [UpVector](#UpVector):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [XVector](#XVector):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [YVector](#YVector):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ZVector](#ZVector):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [Inverse](#Inverse)():[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Lerp](#Lerp)(goal: [CFrame](/docs/reference/engine/datatypes/CFrame),alpha: [number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Orthonormalize](#Orthonormalize)():[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [ToWorldSpace](#ToWorldSpace)(...: [Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>):[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)> |
| [ToObjectSpace](#ToObjectSpace)(...: [Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>):[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)> |
| [PointToWorldSpace](#PointToWorldSpace)(...: [Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |
| [PointToObjectSpace](#PointToObjectSpace)(...: [Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |
| [VectorToWorldSpace](#VectorToWorldSpace)(...: [Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |
| [VectorToObjectSpace](#VectorToObjectSpace)(...: [Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |
| [GetComponents](#GetComponents)():[Tuple](/docs/luau/tuples) |
| [ToEulerAngles](#ToEulerAngles)(order: [Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder)):[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [ToEulerAnglesXYZ](#ToEulerAnglesXYZ)():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [ToEulerAnglesYXZ](#ToEulerAnglesYXZ)():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [ToOrientation](#ToOrientation)():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [ToAxisAngle](#ToAxisAngle)():[Vector3](/docs/reference/engine/datatypes/Vector3),[number](/docs/luau/numbers) |
| [components](#components)():[Tuple](/docs/luau/tuples) |
| [FuzzyEq](#FuzzyEq)(other: [CFrame](/docs/reference/engine/datatypes/CFrame),epsilon: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [AngleBetween](#AngleBetween)(other: [CFrame](/docs/reference/engine/datatypes/CFrame)):[number](/docs/luau/numbers) |

Math Operations

|  |
| --- |
| [`CFrame * CFrame`](#CFrame-*-CFrame) |
| [`CFrame * Vector3`](#CFrame-*-Vector3) |
| [`CFrame + Vector3`](#CFrame-+-Vector3) |
| [`CFrame - Vector3`](#CFrame---Vector3) |

The [CFrame](/docs/reference/engine/datatypes/CFrame) data type, short for coordinate frame, describes a
3D position and orientation. It is made up of a positional component and a
rotational component and includes essential arithmetic operations for
working with 3D data on Roblox.

```
-- Create a CFrame at a certain position and Euler rotation



local cf = CFrame.new(0, 5, 0) * CFrame.fromEulerAngles(math.rad(45), 0, 0)
```

For an introduction to the [CFrame](/docs/reference/engine/datatypes/CFrame) data type, see
[CFrames](/docs/workspace/cframes).

#### Positional Component

The positional component is available as a [Vector3](/docs/reference/engine/datatypes/Vector3). In addition,
the components of a [CFrame](/docs/reference/engine/datatypes/CFrame) object's position are also available in
the [X](/docs/reference/engine/datatypes/CFrame#X), [Y](/docs/reference/engine/datatypes/CFrame#Y) and [Z](/docs/reference/engine/datatypes/CFrame#Z)
properties like a [Vector3](/docs/reference/engine/datatypes/Vector3).

#### Rotational Component

[CFrame](/docs/reference/engine/datatypes/CFrame) stores 3D rotation data in a 3×3 rotation matrix.
These values are returned by the [CFrame:GetComponents()](/docs/reference/engine/datatypes/CFrame#GetComponents) function
after the x, y and z positional values. This matrix is used internally
when doing calculations involving rotations, using radians as their unit
(for conversion from one to the other, use [math.rad()](/docs/reference/engine/libraries/math#rad) or
[math.deg()](/docs/reference/engine/libraries/math#deg)). For more information on how the Roblox Engine performs
rotations, see [Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder).

The table below represents the components of a [CFrame](/docs/reference/engine/datatypes/CFrame) object's
rotation matrix and their relationship with the available vector properties
such as [LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) and
[RightVector](/docs/reference/engine/datatypes/CFrame#RightVector). Although the individual components
of the rotation matrix are rarely useful by themselves, the vector properties
which derive from them are much more useful.

| XVector, RightVector | YVector, UpVector | ZVector, -LookVector† |
| --- | --- | --- |
| R00 | R01 | R02 |
| R10 | R11 | R12 |
| R20 | R21 | R22 |

† Unlike the others,
[LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) represents the negated
column components. The [LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) is
useful because many [Instances](/docs/reference/engine/classes/Instance) such as the
[Camera](/docs/reference/engine/classes/Camera) and [Attachments](/docs/reference/engine/classes/Attachment)
treat that vector as the direction the instance is pointing.

---

API Reference

Constructors

new

Returns a blank identity [CFrame](/docs/reference/engine/datatypes/CFrame).

CFrame.new()

Creates a blank identity [CFrame](/docs/reference/engine/datatypes/CFrame).

Provide feedback

---

new

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) with no rotation with the position of the
provided [Vector3](/docs/reference/engine/datatypes/Vector3).

CFrame.new(pos:[Vector3](/docs/reference/engine/datatypes/Vector3))

Parameters

|  |
| --- |
| pos:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) with no rotation with the position of the
provided [Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

new

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) with the position of the first
[Vector3](/docs/reference/engine/datatypes/Vector3) and an orientation pointed toward the second.

CFrame.new(

pos:[Vector3](/docs/reference/engine/datatypes/Vector3), lookAt:[Vector3](/docs/reference/engine/datatypes/Vector3) )

Parameters

|  |
| --- |
| pos:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| lookAt:[Vector3](/docs/reference/engine/datatypes/Vector3) |

Returns a new [CFrame](/docs/reference/engine/datatypes/CFrame) located at pos and facing towards
lookAt, assuming that (0, 1, 0) is considered "up" in world space.

This constructor overload has been replaced by [CFrame.lookAt()](/docs/reference/engine/datatypes/CFrame#lookAt),
which accomplishes a similar goal. It remains for the sake of backward
compatibility.

At high pitch angles (around 82 degrees), you may experience numerical
instability. If this is an issue, or if you require a different "up"
vector, use [CFrame.fromMatrix()](/docs/reference/engine/datatypes/CFrame#fromMatrix) to more accurately construct
the [CFrame](/docs/reference/engine/datatypes/CFrame). Additionally, if lookAt is directly above pos
(pitch angle of 90 degrees), the "up" vector switches to the X axis.

Provide feedback

---

new

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) with a position comprised of the provided x, y, and z components.

CFrame.new(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |
| z:[number](/docs/luau/numbers) |

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) with a position comprised of the provided x, y, and z components.

Provide feedback

---

new

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) from position (x, y, z) and
quaternion (qX, qY, qZ, qW).

CFrame.new(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers), qX:[number](/docs/luau/numbers), qY:[number](/docs/luau/numbers), qZ:[number](/docs/luau/numbers), qW:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |
| z:[number](/docs/luau/numbers) |
| qX:[number](/docs/luau/numbers) |
| qY:[number](/docs/luau/numbers) |
| qZ:[number](/docs/luau/numbers) |
| qW:[number](/docs/luau/numbers) |

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) from position (x, y, z) and
quaternion (qX, qY, qZ, qW). The quaternion is expected
to be of unit length to represent a valid rotation.
If this isn't the case, the quaternion will be normalized.

Provide feedback

---

new

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) from position (x, y, z) with an
orientation specified by the rotation matrix.

CFrame.new(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers), z:[number](/docs/luau/numbers), R00:[number](/docs/luau/numbers), R01:[number](/docs/luau/numbers), R02:[number](/docs/luau/numbers), R10:[number](/docs/luau/numbers), R11:[number](/docs/luau/numbers), R12:[number](/docs/luau/numbers), R20:[number](/docs/luau/numbers), R21:[number](/docs/luau/numbers), R22:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| y:[number](/docs/luau/numbers) |
| z:[number](/docs/luau/numbers) |
| R00:[number](/docs/luau/numbers) |
| R01:[number](/docs/luau/numbers) |
| R02:[number](/docs/luau/numbers) |
| R10:[number](/docs/luau/numbers) |
| R11:[number](/docs/luau/numbers) |
| R12:[number](/docs/luau/numbers) |
| R20:[number](/docs/luau/numbers) |
| R21:[number](/docs/luau/numbers) |
| R22:[number](/docs/luau/numbers) |

Creates a [CFrame](/docs/reference/engine/datatypes/CFrame) from position (x, y, z) with an
orientation specified by the rotation matrix.

[[R00 R01 R02] [R10 R11 R12] [R20 R21 R22]]

Provide feedback

---

lookAt

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) with the position of the first
[Vector3](/docs/reference/engine/datatypes/Vector3) and an orientation pointed toward the second.

CFrame.lookAt(

at:[Vector3](/docs/reference/engine/datatypes/Vector3), lookAt:[Vector3](/docs/reference/engine/datatypes/Vector3), up:[Vector3](/docs/reference/engine/datatypes/Vector3) )

Parameters

|  |
| --- |
| at:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| lookAt:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| up:[Vector3](/docs/reference/engine/datatypes/Vector3) Default Value: Vector3.yAxis |

Returns a new [CFrame](/docs/reference/engine/datatypes/CFrame) with the position of at and facing
towards lookAt, optionally specifying the upward direction (up) with a
default of (0, 1, 0).

Provide feedback

---

lookAlong

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) with the position of the first
[Vector3](/docs/reference/engine/datatypes/Vector3) and an orientation directed along the second.

CFrame.lookAlong(

at:[Vector3](/docs/reference/engine/datatypes/Vector3), direction:[Vector3](/docs/reference/engine/datatypes/Vector3), up:[Vector3](/docs/reference/engine/datatypes/Vector3) )

Parameters

|  |
| --- |
| at:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| direction:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| up:[Vector3](/docs/reference/engine/datatypes/Vector3) Default Value: Vector3.yAxis |

Returns a new [CFrame](/docs/reference/engine/datatypes/CFrame) with the position of at and facing
along direction, optionally specifying the upward direction (up)
with a default of (0, 1, 0).

This constructor is equivalent to CFrame.lookAt(at, at + direction).

Provide feedback

---

fromRotationBetweenVectors

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) representing the orientation needed to rotate
from the first [Vector3](/docs/reference/engine/datatypes/Vector3) to the second, with the position set to zero.

CFrame.fromRotationBetweenVectors(

from:[Vector3](/docs/reference/engine/datatypes/Vector3), to:[Vector3](/docs/reference/engine/datatypes/Vector3) )

Parameters

|  |
| --- |
| from:[Vector3](/docs/reference/engine/datatypes/Vector3)  Vector representing the "from" direction. |
| to:[Vector3](/docs/reference/engine/datatypes/Vector3)  Vector representing the "to" direction. |

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) representing the orientation needed to rotate
from the first [Vector3](/docs/reference/engine/datatypes/Vector3) to the second, with the position set to zero.

Provide feedback

---

fromEulerAngles

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from angles rx, ry, and rz in
radians. Rotations are applied in the optional [Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder) with a
default of XYZ.

CFrame.fromEulerAngles(

rx:[number](/docs/luau/numbers), ry:[number](/docs/luau/numbers), rz:[number](/docs/luau/numbers), order:[Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder) )

Parameters

|  |
| --- |
| rx:[number](/docs/luau/numbers) |
| ry:[number](/docs/luau/numbers) |
| rz:[number](/docs/luau/numbers) |
| order:[Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder) Default Value: Enum.RotationOrder.XYZ |

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from angles rx, ry, and rz in
radians. Rotations are applied in the optional [Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder) with a
default of XYZ, equivalent to:

```
CFrame.fromEulerAngles(rx, 0, 0) *  -- X



CFrame.fromEulerAngles(0, ry, 0) *  -- Y



CFrame.fromEulerAngles(0, 0, rz)    -- Z
```

Provide feedback

---

fromEulerAnglesXYZ

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from angles rx, ry, and rz in
radians using [Enum.RotationOrder.XYZ](/docs/reference/engine/enums/RotationOrder#XYZ).

CFrame.fromEulerAnglesXYZ(

rx:[number](/docs/luau/numbers), ry:[number](/docs/luau/numbers), rz:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| rx:[number](/docs/luau/numbers) |
| ry:[number](/docs/luau/numbers) |
| rz:[number](/docs/luau/numbers) |

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from angles rx, ry, and rz in
radians using [Enum.RotationOrder.XYZ](/docs/reference/engine/enums/RotationOrder#XYZ), equivalent to:

```
CFrame.fromEulerAngles(rx, 0, 0) *  -- X



CFrame.fromEulerAngles(0, ry, 0) *  -- Y



CFrame.fromEulerAngles(0, 0, rz)    -- Z
```

Provide feedback

---

fromEulerAnglesYXZ

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from angles rx, ry, and rz in
radians using [Enum.RotationOrder.YXZ](/docs/reference/engine/enums/RotationOrder#YXZ).

CFrame.fromEulerAnglesYXZ(

rx:[number](/docs/luau/numbers), ry:[number](/docs/luau/numbers), rz:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| rx:[number](/docs/luau/numbers) |
| ry:[number](/docs/luau/numbers) |
| rz:[number](/docs/luau/numbers) |

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from angles rx, ry, and rz in
radians using [Enum.RotationOrder.YXZ](/docs/reference/engine/enums/RotationOrder#YXZ), equivalent to:

```
CFrame.fromEulerAngles(0, ry, 0) *  -- Y



CFrame.fromEulerAngles(rx, 0, 0) *  -- X



CFrame.fromEulerAngles(0, 0, rz)    -- Z
```

Provide feedback

---

Angles

Equivalent to [fromEulerAnglesXYZ()](/docs/reference/engine/datatypes/CFrame#fromEulerAnglesXYZ).

CFrame.Angles(

rx:[number](/docs/luau/numbers), ry:[number](/docs/luau/numbers), rz:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| rx:[number](/docs/luau/numbers) |
| ry:[number](/docs/luau/numbers) |
| rz:[number](/docs/luau/numbers) |

Equivalent to [fromEulerAnglesXYZ()](/docs/reference/engine/datatypes/CFrame#fromEulerAnglesXYZ).

Provide feedback

---

fromOrientation

Equivalent to [fromEulerAnglesYXZ()](/docs/reference/engine/datatypes/CFrame#fromEulerAnglesYXZ).

CFrame.fromOrientation(

rx:[number](/docs/luau/numbers), ry:[number](/docs/luau/numbers), rz:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| rx:[number](/docs/luau/numbers) |
| ry:[number](/docs/luau/numbers) |
| rz:[number](/docs/luau/numbers) |

Equivalent to [fromEulerAnglesYXZ()](/docs/reference/engine/datatypes/CFrame#fromEulerAnglesYXZ).

Provide feedback

---

fromAxisAngle

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from a unit [Vector3](/docs/reference/engine/datatypes/Vector3) and a rotation in radians.

CFrame.fromAxisAngle(

v:[Vector3](/docs/reference/engine/datatypes/Vector3), r:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| v:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| r:[number](/docs/luau/numbers) |

Returns a rotated [CFrame](/docs/reference/engine/datatypes/CFrame) from a unit [Vector3](/docs/reference/engine/datatypes/Vector3) and a rotation in radians.

Provide feedback

---

fromMatrix

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) from a translation and the columns of a rotation matrix.

CFrame.fromMatrix(

pos:[Vector3](/docs/reference/engine/datatypes/Vector3), vX:[Vector3](/docs/reference/engine/datatypes/Vector3), vY:[Vector3](/docs/reference/engine/datatypes/Vector3), vZ:[Vector3](/docs/reference/engine/datatypes/Vector3) )

Parameters

|  |
| --- |
| pos:[Vector3](/docs/reference/engine/datatypes/Vector3)  The 3D position of the [CFrame](/docs/reference/engine/datatypes/CFrame). |
| vX:[Vector3](/docs/reference/engine/datatypes/Vector3)  Equivalent to [RightVector](/docs/reference/engine/datatypes/CFrame#RightVector). |
| vY:[Vector3](/docs/reference/engine/datatypes/Vector3)  Equivalent to [UpVector](/docs/reference/engine/datatypes/CFrame#UpVector). |
| vZ:[Vector3](/docs/reference/engine/datatypes/Vector3)  Equivalent to -[LookVector](/docs/reference/engine/datatypes/CFrame#LookVector). |

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) from a translation and the columns of a rotation
matrix. If vZ is excluded, the third column is calculated as
vX:Cross(vY).Unit.

Provide feedback

---

Properties

identity

An identity [CFrame](/docs/reference/engine/datatypes/CFrame) with no translation or rotation.

CFrame.identity:[CFrame](/docs/reference/engine/datatypes/CFrame)

An identity [CFrame](/docs/reference/engine/datatypes/CFrame) with no translation or rotation. This
property is a constant and must be accessed globally as opposed to
through an individual [CFrame](/docs/reference/engine/datatypes/CFrame) object.

Provide feedback

---

Position

The 3D position of the [CFrame](/docs/reference/engine/datatypes/CFrame).

CFrame.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

The 3D position of the [CFrame](/docs/reference/engine/datatypes/CFrame).

Provide feedback

---

Rotation

A copy of the [CFrame](/docs/reference/engine/datatypes/CFrame) with no translation.

CFrame.Rotation:[CFrame](/docs/reference/engine/datatypes/CFrame)

A copy of the [CFrame](/docs/reference/engine/datatypes/CFrame) with no translation.

Provide feedback

---

X

The X coordinate of the position.

CFrame.X:[number](/docs/luau/numbers)

The X coordinate of the position.

Provide feedback

---

Y

The Y coordinate of the position.

CFrame.Y:[number](/docs/luau/numbers)

The Y coordinate of the position.

Provide feedback

---

Z

The Z coordinate of the position.

CFrame.Z:[number](/docs/luau/numbers)

The Z coordinate of the position.

Provide feedback

---

LookVector

The forward-direction component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's
orientation, equivalent to the negated form of
[ZVector](/docs/reference/engine/datatypes/CFrame#ZVector).

CFrame.LookVector:[Vector3](/docs/reference/engine/datatypes/Vector3)

The forward-direction component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's
orientation, equivalent to the negated [ZVector](/docs/reference/engine/datatypes/CFrame#ZVector)
or the negated third column of the rotation matrix.

```
local cf = CFrame.new(0, 0, 0)



local x, y, z, R00, R01, R02, R10, R11, R12, R20, R21, R22 = cf:GetComponents()



print(cf.LookVector)     --> (-0, -0, -1)



print(-cf.ZVector)       --> (-0, -0, -1)



print(-R02, -R12, -R22)  --> (-0 -0 -1)
```

Adding a [CFrame](/docs/reference/engine/datatypes/CFrame) object's
[LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) to itself produces a
[CFrame](/docs/reference/engine/datatypes/CFrame) moved forward in whichever direction it's facing by 1
unit.

Provide feedback

---

RightVector

The right-direction component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's
orientation.

CFrame.RightVector:[Vector3](/docs/reference/engine/datatypes/Vector3)

The right-direction component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's
orientation. Equivalent to [XVector](/docs/reference/engine/datatypes/CFrame#XVector) or the first
column of the rotation matrix.

```
local cf = CFrame.new(0, 0, 0)



local x, y, z, R00, R01, R02, R10, R11, R12, R20, R21, R22 = cf:GetComponents()



print(cf.RightVector)  --> (1, 0, 0)



print(cf.XVector)      --> (1, 0, 0)



print(R00, R10, R20)   --> (1 0 0)
```

Provide feedback

---

UpVector

The up-direction component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's orientation.

CFrame.UpVector:[Vector3](/docs/reference/engine/datatypes/Vector3)

The up-direction component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's orientation.
Equivalent to [YVector](/docs/reference/engine/datatypes/CFrame#YVector) or the second column of
the rotation matrix.

```
local cf = CFrame.new(0, 0, 0)



local x, y, z, R00, R01, R02, R10, R11, R12, R20, R21, R22 = cf:GetComponents()



print(cf.UpVector)    --> (0, 1, 0)



print(cf.YVector)     --> (0, 1, 0)



print(R01, R11, R21)  --> (0 1 0)
```

Provide feedback

---

XVector

Equivalent to [RightVector](/docs/reference/engine/datatypes/CFrame#RightVector).

CFrame.XVector:[Vector3](/docs/reference/engine/datatypes/Vector3)

The X component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's orientation. Equivalent
to [RightVector](/docs/reference/engine/datatypes/CFrame#RightVector) or the first column of the
rotation matrix.

```
local cf = CFrame.new(0, 0, 0)



local x, y, z, R00, R01, R02, R10, R11, R12, R20, R21, R22 = cf:GetComponents()



print(cf.XVector)      --> (1, 0, 0)



print(cf.RightVector)  --> (1, 0, 0)



print(R00, R10, R20)   --> (1 0 0)
```

Provide feedback

---

YVector

Equivalent to [UpVector](/docs/reference/engine/datatypes/CFrame#UpVector).

CFrame.YVector:[Vector3](/docs/reference/engine/datatypes/Vector3)

The Y component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's orientation. Equivalent
to [UpVector](/docs/reference/engine/datatypes/CFrame#UpVector) or the second column of the
rotation matrix.

```
local cf = CFrame.new(0, 0, 0)



local x, y, z, R00, R01, R02, R10, R11, R12, R20, R21, R22 = cf:GetComponents()



print(cf.YVector)     --> (0, 1, 0)



print(cf.UpVector)    --> (0, 1, 0)



print(R01, R11, R21)  --> (0 1 0)
```

Provide feedback

---

ZVector

The Z component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's orientation. Equivalent
to the third column of the rotation matrix.

CFrame.ZVector:[Vector3](/docs/reference/engine/datatypes/Vector3)

The Z component of the [CFrame](/docs/reference/engine/datatypes/CFrame) object's orientation. Equivalent
to the negated [LookVector](/docs/reference/engine/datatypes/CFrame#LookVector) or the third column
of the rotation matrix.

```
local cf = CFrame.new(0, 0, 0)



local x, y, z, R00, R01, R02, R10, R11, R12, R20, R21, R22 = cf:GetComponents()



print(cf.ZVector)      --> (0, 0, 1)



print(-cf.LookVector)  --> (0, 0, 1)



print(R02, R12, R22)   --> (0 0 1)
```

Provide feedback

---

Methods

Inverse

Returns the inverse of the [CFrame](/docs/reference/engine/datatypes/CFrame).

CFrame:Inverse():[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns the inverse of the [CFrame](/docs/reference/engine/datatypes/CFrame).

Provide feedback

---

Lerp

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) interpolated between itself and goal by the
fraction alpha.

CFrame:Lerp(

goal:[CFrame](/docs/reference/engine/datatypes/CFrame), alpha:[number](/docs/luau/numbers)

):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| goal:[CFrame](/docs/reference/engine/datatypes/CFrame) |
| alpha:[number](/docs/luau/numbers) |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns a [CFrame](/docs/reference/engine/datatypes/CFrame) interpolated between itself and goal by the
fraction alpha.

Provide feedback

---

Orthonormalize

Returns an orthonormalized copy of the [CFrame](/docs/reference/engine/datatypes/CFrame).

CFrame:Orthonormalize():[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns an orthonormalized copy of the [CFrame](/docs/reference/engine/datatypes/CFrame). The
[BasePart.CFrame](/docs/reference/engine/classes/BasePart#CFrame) property automatically applies orthonormalization,
but other APIs which take [CFrames](/docs/reference/engine/datatypes/CFrame) do not, so this method
is occasionally necessary when incrementally updating a [CFrame](/docs/reference/engine/datatypes/CFrame)
and using it with them.

Provide feedback

---

ToWorldSpace

Receives one or more [CFrame](/docs/reference/engine/datatypes/CFrame) objects and returns them
transformed from object to world space.

CFrame:ToWorldSpace(...:[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>):[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>

Parameters

|  |
| --- |
| ...:[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)> |

Returns

[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>

Receives one or more [CFrame](/docs/reference/engine/datatypes/CFrame) objects and returns them
transformed from object to world space. Equivalent to:

CFrame \* cf

Provide feedback

---

ToObjectSpace

Receives one or more [CFrame](/docs/reference/engine/datatypes/CFrame) objects and returns them
transformed from world to object space.

CFrame:ToObjectSpace(...:[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>):[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>

Parameters

|  |
| --- |
| ...:[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)> |

Returns

[Tuple](/docs/luau/tuples)<[CFrame](/docs/reference/engine/datatypes/CFrame)>

Receives one or more [CFrame](/docs/reference/engine/datatypes/CFrame) objects and returns them
transformed from world to object space. Equivalent to:

CFrame:Inverse() \* cf

Provide feedback

---

PointToWorldSpace

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them
transformed from object to world space.

CFrame:PointToWorldSpace(...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Parameters

|  |
| --- |
| ...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |

Returns

[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them
transformed from object to world space. Equivalent to:

CFrame \* v3

Provide feedback

---

PointToObjectSpace

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them
transformed from world to object space.

CFrame:PointToObjectSpace(...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Parameters

|  |
| --- |
| ...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |

Returns

[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them
transformed from world to object space. Equivalent to:

CFrame:Inverse() \* v3

Provide feedback

---

VectorToWorldSpace

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them rotated
from object to world space.

CFrame:VectorToWorldSpace(...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Parameters

|  |
| --- |
| ...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |

Returns

[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them rotated
from object to world space. Equivalent to:

(CFrame - CFrame.Position) \* v3

Provide feedback

---

VectorToObjectSpace

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them rotated
from world to object space.

CFrame:VectorToObjectSpace(...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>):[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Parameters

|  |
| --- |
| ...:[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)> |

Returns

[Tuple](/docs/luau/tuples)<[Vector3](/docs/reference/engine/datatypes/Vector3)>

Receives one or more [Vector3](/docs/reference/engine/datatypes/Vector3) objects and returns them rotated
from world to object space. Equivalent to:

(CFrame:Inverse() - CFrame:Inverse().Position) \* v3

Provide feedback

---

GetComponents

Returns the values x, y, z, R00, R01, R02, R10, R11,
R12, R20, R21, and R22, where x y z represent the position
of the [CFrame](/docs/reference/engine/datatypes/CFrame) and R00‑R22 represent its 3×3 rotation
matrix.

CFrame:GetComponents():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Returns the values x, y, z, R00, R01, R02, R10, R11,
R12, R20, R21, and R22, where x y z represent the position
of the [CFrame](/docs/reference/engine/datatypes/CFrame) and R00‑R22 represent its 3×3 rotation
matrix.

Provide feedback

---

ToEulerAngles

Returns approximate angles that could be used to generate the
[CFrame](/docs/reference/engine/datatypes/CFrame) using the optional [Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder).

CFrame:ToEulerAngles(order:[Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder)):[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| order:[Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder) Default Value: Enum.RotationOrder.XYZ |

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers), [number](/docs/luau/numbers)

Returns approximate angles that could be used to generate the
[CFrame](/docs/reference/engine/datatypes/CFrame) using the optional [Enum.RotationOrder](/docs/reference/engine/enums/RotationOrder). If you don't
provide order, the method uses [Enum.RotationOrder.XYZ](/docs/reference/engine/enums/RotationOrder#XYZ).

Provide feedback

---

ToEulerAnglesXYZ

Returns approximate angles that could be used to generate the
[CFrame](/docs/reference/engine/datatypes/CFrame) using [Enum.RotationOrder.XYZ](/docs/reference/engine/enums/RotationOrder#XYZ).

CFrame:ToEulerAnglesXYZ():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers), [number](/docs/luau/numbers)

Returns approximate angles that could be used to generate the
[CFrame](/docs/reference/engine/datatypes/CFrame) using [Enum.RotationOrder.XYZ](/docs/reference/engine/enums/RotationOrder#XYZ).

Provide feedback

---

ToEulerAnglesYXZ

Returns approximate angles that could be used to generate the
[CFrame](/docs/reference/engine/datatypes/CFrame) using [Enum.RotationOrder.YXZ](/docs/reference/engine/enums/RotationOrder#YXZ).

CFrame:ToEulerAnglesYXZ():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers), [number](/docs/luau/numbers)

Returns approximate angles that could be used to generate the
[CFrame](/docs/reference/engine/datatypes/CFrame) using [Enum.RotationOrder.YXZ](/docs/reference/engine/enums/RotationOrder#YXZ).

Provide feedback

---

ToOrientation

Equivalent to [CFrame:ToEulerAnglesYXZ()](/docs/reference/engine/datatypes/CFrame#ToEulerAnglesYXZ).

CFrame:ToOrientation():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers), [number](/docs/luau/numbers)

Equivalent to [CFrame:ToEulerAnglesYXZ()](/docs/reference/engine/datatypes/CFrame#ToEulerAnglesYXZ).

Provide feedback

---

ToAxisAngle

Returns a tuple of a [Vector3](/docs/reference/engine/datatypes/Vector3) and a number which represent the
rotation of the [CFrame](/docs/reference/engine/datatypes/CFrame) in the axis-angle representation.

CFrame:ToAxisAngle():[Vector3](/docs/reference/engine/datatypes/Vector3),[number](/docs/luau/numbers)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3), [number](/docs/luau/numbers)

Returns a tuple of a [Vector3](/docs/reference/engine/datatypes/Vector3) and a number which represent the
rotation of the [CFrame](/docs/reference/engine/datatypes/CFrame) in the axis-angle representation.

Provide feedback

---

components

Equivalent to [CFrame:GetComponents()](/docs/reference/engine/datatypes/CFrame#GetComponents).

CFrame:components():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Equivalent to [CFrame:GetComponents()](/docs/reference/engine/datatypes/CFrame#GetComponents).

Provide feedback

---

FuzzyEq

Returns true if the other [CFrame](/docs/reference/engine/datatypes/CFrame) is sufficiently close to
this [CFrame](/docs/reference/engine/datatypes/CFrame) in both position and rotation.

CFrame:FuzzyEq(

other:[CFrame](/docs/reference/engine/datatypes/CFrame), epsilon:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| other:[CFrame](/docs/reference/engine/datatypes/CFrame) |
| epsilon:[number](/docs/luau/numbers) Default Value: 0.00001 (1e-5) |

Returns

[boolean](/docs/luau/booleans)

Returns true if the other [CFrame](/docs/reference/engine/datatypes/CFrame) is sufficiently close to
this [CFrame](/docs/reference/engine/datatypes/CFrame) in both position and rotation. The epsilon value
is used to control the tolerance for this similarity; this value is
optional and should be a small positive value if provided. The similarity
for position is component-wise while rotation uses a fast approximation of
the angle difference.

Provide feedback

---

AngleBetween

Returns the angle, in radians, between the orientation of one
[CFrame](/docs/reference/engine/datatypes/CFrame) and another.

CFrame:AngleBetween(other:[CFrame](/docs/reference/engine/datatypes/CFrame)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| other:[CFrame](/docs/reference/engine/datatypes/CFrame) |

Returns

[number](/docs/luau/numbers)

Returns the angle, in radians, between the orientation of one
[CFrame](/docs/reference/engine/datatypes/CFrame) and another. This function does not take the position of
either [CFrame](/docs/reference/engine/datatypes/CFrame) into account and only looks at the relative
orientation.

Provide feedback

---

Math Operations

`CFrame` \* `CFrame`

Produces a new [CFrame](/docs/reference/engine/datatypes/CFrame) representing the composition of the two
[CFrames](/docs/reference/engine/datatypes/CFrame).

[CFrame](/docs/reference/engine/datatypes/CFrame) \* [CFrame](/docs/reference/engine/datatypes/CFrame) : [CFrame](/docs/reference/engine/datatypes/CFrame)

Produces a new [CFrame](/docs/reference/engine/datatypes/CFrame) representing the composition of the two
[CFrames](/docs/reference/engine/datatypes/CFrame).

Provide feedback

---

`CFrame` \* `Vector3`

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) transformed from object to world
coordinates.

[CFrame](/docs/reference/engine/datatypes/CFrame) \* [Vector3](/docs/reference/engine/datatypes/Vector3) : [Vector3](/docs/reference/engine/datatypes/Vector3)

Produces a [Vector3](/docs/reference/engine/datatypes/Vector3) transformed from object to world
coordinates.

Provide feedback

---

`CFrame` + `Vector3`

Produces a [CFrame](/docs/reference/engine/datatypes/CFrame) translated in world space by the
[Vector3](/docs/reference/engine/datatypes/Vector3).

[CFrame](/docs/reference/engine/datatypes/CFrame) + [Vector3](/docs/reference/engine/datatypes/Vector3) : [CFrame](/docs/reference/engine/datatypes/CFrame)

Produces a [CFrame](/docs/reference/engine/datatypes/CFrame) translated in world space by the
[Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

`CFrame` - `Vector3`

Produces a [CFrame](/docs/reference/engine/datatypes/CFrame) translated in world space by the negative
[Vector3](/docs/reference/engine/datatypes/Vector3).

[CFrame](/docs/reference/engine/datatypes/CFrame) - [Vector3](/docs/reference/engine/datatypes/Vector3) : [CFrame](/docs/reference/engine/datatypes/CFrame)

Produces a [CFrame](/docs/reference/engine/datatypes/CFrame) translated in world space by the negative
[Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---