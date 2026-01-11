# Tween | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Tween
Scraped: 2026-01-11T02:27:39.069558Z

## Tags
- Not Replicated

## Inherits
- TweenBase
- Tween
- Instance
- Object
- TweenService:Create()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TweenBase](/docs/reference/engine/classes/TweenBase)
6. /
7. [Tween](/docs/reference/engine/classes/Tween)

English

Feedback

Engine Class

Tween

The [Tween](/docs/reference/engine/classes/Tween) object controls the playback of an interpolation.

---

Summary

Properties

|  |
| --- |
| [Instance](#Instance):[Instance](/docs/reference/engine/datatypes/Instance) |
| [TweenInfo](#TweenInfo):[TweenInfo](/docs/reference/engine/datatypes/TweenInfo) |

Inherited Members

5 inherited from [TweenBase](/docs/reference/engine/classes/TweenBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [Tween](/docs/reference/engine/classes/Tween) object controls the playback of an interpolation. Creating
and configuring a [Tween](/docs/reference/engine/classes/Tween) is done with the [TweenService:Create()](/docs/reference/engine/classes/TweenService#Create)
function; [Instance.new()](/docs/reference/engine/datatypes/Instance#new) cannot be used for this particular object.

Note that while the configuration of a tween can be accessed after a tween has
been created, it can not be modified. If new goals are needed for an
interpolation, a new [Tween](/docs/reference/engine/classes/Tween) must be created.

Also note that multiple tweens can be played on the same object at the same
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

---

API Reference

Properties

Instance

Read Only

Not Replicated

Read Parallel

Read-only property that points to the [Instance](/docs/reference/engine/classes/Instance) whose properties
are being interpolated by the tween.

Tween.Instance:[Instance](/docs/reference/engine/datatypes/Instance)

This property of a [Tween](/docs/reference/engine/classes/Tween) (read-only) points to the
[Instance](/docs/reference/engine/classes/Instance) whose properties are being interpolated.

Code Samples

Tween Instance

This code sample includes a simple function that will return true if the
instance of a tween is a Part.

```
local TweenService = game:GetService("TweenService")



local function isInstanceAPart(tween)



local instance = tween.Instance



return instance:IsA("BasePart")



end



local tweenInfo = TweenInfo.new()



local instance = Instance.new("Part")



local tween = TweenService:Create(instance, tweenInfo, {



Transparency = 1,



})



print(isInstanceAPart(tween))
```

Provide feedback

---

TweenInfo

Read Only

Not Replicated

Read Parallel

Read-only property that includes information on how the interpolation of
the [Tween](/docs/reference/engine/classes/Tween) is to be carried out.

Tween.TweenInfo:[TweenInfo](/docs/reference/engine/datatypes/TweenInfo)

Read-only property that includes information on how the interpolation of
the [Tween](/docs/reference/engine/classes/Tween) is to be carried out, using the [TweenInfo](/docs/reference/engine/datatypes/TweenInfo)
data type.

Code Samples

TweenInfo Examples

An example of the range of different interpolation effects that can be used in
Tweens.

```
-- A TweenInfo with all default parameters



TweenInfo.new()



-- A TweenInfo with its time set to 0.5 seconds.



TweenInfo.new(0.5)



-- A TweenInfo with its easing style set to Back.



TweenInfo.new(0.5, Enum.EasingStyle.Back)



-- A TweenInfo with its easing direction set to In.



TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In)



-- A TweenInfo that repeats itself 4 times.



TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In, 4)



-- A TweenInfo that reverses its interpolation after reaching its goal.



TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In, 4, true)



-- A TweenInfo that loops indefinitely.



TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In, -1, true)



-- A TweenInfo with a delay of 1 second between each interpolation.



TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.In, 4, true, 1)
```

Provide feedback

---