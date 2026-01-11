# TweenService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TweenService
Scraped: 2026-01-11T02:33:41.630825Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- TweenService
- Tweens
- Tween
- TweenService:Create()
- Workspace
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TweenService](/docs/reference/engine/classes/TweenService)

English

Feedback

Engine Class

TweenService

Used to create [Tweens](/docs/reference/engine/classes/Tween) which interpolate, or tween, the
properties of instances.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [Create](#Create)(instance: [Instance](/docs/reference/engine/datatypes/Instance),tweenInfo: [TweenInfo](/docs/reference/engine/datatypes/TweenInfo),propertyTable: [Dictionary](/docs/luau/tables#dictionaries)):[Tween](/docs/reference/engine/classes/Tween) |
| [GetValue](#GetValue)(alpha: [number](/docs/luau/numbers),easingStyle: [Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle),easingDirection: [Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection)):[number](/docs/luau/numbers) |
| [SmoothDamp](#SmoothDamp)(current: Variant,target: Variant,velocity: Variant,smoothTime: [number](/docs/luau/numbers),maxSpeed: [number](/docs/luau/numbers)?,dt: [number](/docs/luau/numbers)?):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[TweenService](/docs/reference/engine/classes/TweenService) is used to create [Tweens](/docs/reference/engine/classes/Tween) which interpolate,
or tween, the properties of instances. [Tweens](/docs/reference/engine/classes/Tween) can be used on any
object with compatible property types, including:

* [number](/docs/luau/numbers)
* [boolean](/docs/luau/booleans)
* [CFrame](/docs/reference/engine/datatypes/CFrame)
* [Rect](/docs/reference/engine/datatypes/Rect)
* [Color3](/docs/reference/engine/datatypes/Color3)
* [UDim](/docs/reference/engine/datatypes/UDim)
* [UDim2](/docs/reference/engine/datatypes/UDim2)
* [Vector2](/docs/reference/engine/datatypes/Vector2)
* [Vector2int16](/docs/reference/engine/datatypes/Vector2int16)
* [Vector3](/docs/reference/engine/datatypes/Vector3)
* [EnumItem](/docs/reference/engine/datatypes/EnumItem)

[TweenService:Create()](/docs/reference/engine/classes/TweenService#Create), the primary constructor function, takes
[TweenInfo](/docs/reference/engine/datatypes/TweenInfo) specifications about the tween and generates the
[Tween](/docs/reference/engine/classes/Tween) object which can then be used to play the tween.

Note that [Tweens](/docs/reference/engine/classes/Tween) can interpolate multiple properties at the same
time, but they must not be interpolating the same property. If two tweens
attempt to modify the same property, the initial tween will be cancelled and
overwritten by the most recent tween.

Code Samples

Tween Creation

In this example a Tween is created to animate the position and color of a
Part. Because the position and color are part of the same tween, they will
change at the exact same rate and will reach their goal at the same time.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Color = Color3.new(1, 0, 0)



part.Anchored = true



part.Parent = game.Workspace



local goal = {}



goal.Position = Vector3.new(10, 10, 0)



goal.Color = Color3.new(0, 1, 0)



local tweenInfo = TweenInfo.new(5)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()
```

Looping a Tween

This code sample includes an example of how a looped tween can be created. A
part is instanced in the [Workspace](/docs/reference/engine/classes/Workspace) and a [Tween](/docs/reference/engine/classes/Tween) is created
using [TweenService:Create()](/docs/reference/engine/classes/TweenService#Create) that is set to animate its position along
the Y axis.

The looped effect is achieved by modifying the [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) used in
[TweenService:Create()](/docs/reference/engine/classes/TweenService#Create). Specifically, when RepeatCount is set to less
than 0, the tween will play indefinitely. Also, setting Reverses to true
will cause the tween to play in reverse once it has reached its destination.
In combination this creates a looped effect.

The correct way to make a tween play indefinitely is to set RepeatCount to
-1. You should avoid using large numbers or [math.huge](/docs/reference/engine/libraries/math#huge) as a
substitute as this is unstable and may stop working at any point.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.Parent = workspace



local tweenInfo = TweenInfo.new(



2, -- Time



Enum.EasingStyle.Linear, -- EasingStyle



Enum.EasingDirection.Out, -- EasingDirection



-1, -- RepeatCount (when less than zero the tween will loop indefinitely)



true, -- Reverses (tween will reverse once reaching its goal)



0 -- DelayTime



)



local tween = TweenService:Create(part, tweenInfo, { Position = Vector3.new(0, 30, 0) })



tween:Play()



task.wait(10)



tween:Cancel() -- cancel the animation after 10 seconds
```

Pausing a Tween

This sample demonstrates how the playback of a tween can be paused and
resumed.

A part is instanced in the Workspace and a tween is setup that will move it 50
studs along the X axis. However during playback the tween is briefly paused,
then resumed. To further illustrate this the BrickColor of the part changes
from red to green while it is paused.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.BrickColor = BrickColor.new("Bright green")



part.Parent = workspace



local goal = {}



goal.Position = Vector3.new(50, 10, 0)



local tweenInfo = TweenInfo.new(10, Enum.EasingStyle.Linear)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()



task.wait(3)



part.BrickColor = BrickColor.new("Bright red")



tween:Pause()



task.wait(2)



part.BrickColor = BrickColor.new("Bright green")



tween:Play()
```

---

API Reference

Methods

Create

Creates a new [Tween](/docs/reference/engine/classes/Tween) given the object whose properties are to be
tweened, a [TweenInfo](/docs/reference/engine/datatypes/TweenInfo), and a dictionary of goal property values.

TweenService:Create(

instance:[Instance](/docs/reference/engine/datatypes/Instance), tweenInfo:[TweenInfo](/docs/reference/engine/datatypes/TweenInfo), propertyTable:[Dictionary](/docs/luau/tables#dictionaries)

):[Tween](/docs/reference/engine/classes/Tween)

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) whose properties are to be tweened. |
| tweenInfo:[TweenInfo](/docs/reference/engine/datatypes/TweenInfo)  The [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) to be used. |
| propertyTable:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary of properties, and their target values, to be tweened. |

Returns

[Tween](/docs/reference/engine/classes/Tween)

This constructor creates a new [Tween](/docs/reference/engine/classes/Tween) from three arguments: the
object to tween, the [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) specifications, and a table
containing the properties to tween and values to tween to.

The propertyTable parameter needs to be a dictionary where the keys are
the string names of the property (for example Position, Transparency,
or Color), and the values are the property targets at the end of the
tween.

The [Tween](/docs/reference/engine/classes/Tween) created using this function is unique to the object
given as the instance parameter. To apply the same tween to another
object, call this function again with the new object.

Code Samples

Tween Creation

In this example a Tween is created to animate the position and color of a
Part. Because the position and color are part of the same tween, they will
change at the exact same rate and will reach their goal at the same time.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Color = Color3.new(1, 0, 0)



part.Anchored = true



part.Parent = game.Workspace



local goal = {}



goal.Position = Vector3.new(10, 10, 0)



goal.Color = Color3.new(0, 1, 0)



local tweenInfo = TweenInfo.new(5)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()
```

Looping a Tween

This code sample includes an example of how a looped tween can be created. A
part is instanced in the [Workspace](/docs/reference/engine/classes/Workspace) and a [Tween](/docs/reference/engine/classes/Tween) is created
using [TweenService:Create()](/docs/reference/engine/classes/TweenService#Create) that is set to animate its position along
the Y axis.

The looped effect is achieved by modifying the [TweenInfo](/docs/reference/engine/datatypes/TweenInfo) used in
[TweenService:Create()](/docs/reference/engine/classes/TweenService#Create). Specifically, when RepeatCount is set to less
than 0, the tween will play indefinitely. Also, setting Reverses to true
will cause the tween to play in reverse once it has reached its destination.
In combination this creates a looped effect.

The correct way to make a tween play indefinitely is to set RepeatCount to
-1. You should avoid using large numbers or [math.huge](/docs/reference/engine/libraries/math#huge) as a
substitute as this is unstable and may stop working at any point.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Position = Vector3.new(0, 10, 0)



part.Anchored = true



part.Parent = workspace



local tweenInfo = TweenInfo.new(



2, -- Time



Enum.EasingStyle.Linear, -- EasingStyle



Enum.EasingDirection.Out, -- EasingDirection



-1, -- RepeatCount (when less than zero the tween will loop indefinitely)



true, -- Reverses (tween will reverse once reaching its goal)



0 -- DelayTime



)



local tween = TweenService:Create(part, tweenInfo, { Position = Vector3.new(0, 30, 0) })



tween:Play()



task.wait(10)



tween:Cancel() -- cancel the animation after 10 seconds
```

Provide feedback

---

GetValue

Calculates a new alpha given an [Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle) and
[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection).

TweenService:GetValue(

alpha:[number](/docs/luau/numbers), easingStyle:[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle), easingDirection:[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| alpha:[number](/docs/luau/numbers)  An interpolation value between 0 and 1. |
| easingStyle:[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle)  The easing style to use. |
| easingDirection:[Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection)  The easing direction to use. |

Returns

[number](/docs/luau/numbers)

A new alpha value generated from the given easing style and direction.

Returns a new alpha value for interpolating using the given alpha value,
[Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle), and [Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection). The provided alpha value
will be clamped between 0 and 1.

Provide feedback

---

SmoothDamp

Write Parallel

Smoothly interpolates a value towards a target, simulating a critically
damped spring.

TweenService:SmoothDamp(

current:Variant, target:Variant, velocity:Variant, smoothTime:[number](/docs/luau/numbers), maxSpeed:[number](/docs/luau/numbers)?, dt:[number](/docs/luau/numbers)?

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| current:Variant  The current value to smooth. |
| target:Variant  The target value to reach. |
| velocity:Variant  The current velocity with which the current value should approach the target value. You shouldn't modify this value between calls yourself, it's used to store the stateful velocity. In most cases, initialize this with 0, Vector2.zero, Vector3.zero, or CFrame.identity depending on the type, or if needed, with your initial velocity. |
| smoothTime:[number](/docs/luau/numbers)  The duration over which the total smoothing operation should take place. Note that since this is a damped spring, there's no guarantee current will be exactly target after this time, but it will be close. Smaller values result in quicker smoothing. |
| maxSpeed:[number](/docs/luau/numbers)?  The maximum speed at which the current value should approach the target value. Leaving this nil defaults to math.huge, meaning the velocity isn't clamped. |
| dt:[number](/docs/luau/numbers)?  The rate at which the smoothing operation should be applied. If left nil, the current engine delta time will be used. |

Returns

[Tuple](/docs/luau/tuples)

The new value and new velocity calculated from the smoothing
operation.

Smoothly interpolates a value towards a target, simulating a critically
damped spring. Returns a tuple with (newValue, newVelocity).
newVelocity needs to be fed to the next call of SmoothDamp to ensure
smooth results. Supports Datatype.number, [Vector2](/docs/reference/engine/datatypes/Vector2),
[Vector3](/docs/reference/engine/datatypes/Vector3), and [CFrame](/docs/reference/engine/datatypes/CFrame).

Provide feedback

---