# Debris | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Debris
Scraped: 2026-01-11T02:35:35.800739Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- Debris
- Instance:Destroy()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Debris](/docs/reference/engine/classes/Debris)

English

Feedback

Engine Class

Debris

Allows scheduling the guaranteed destruction of an object without yielding.  
.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [MaxItems](#MaxItems):[number](/docs/luau/numbers)  Deprecated |

Methods

|  |
| --- |
| [AddItem](#AddItem)(item: [Instance](/docs/reference/engine/datatypes/Instance),lifetime: [number](/docs/luau/numbers)):() |
| [addItem](#addItem)(item: [Instance](/docs/reference/engine/datatypes/Instance),lifetime: [number](/docs/luau/numbers)):()  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Debris service allows scheduling guaranteed destruction of an object
without yielding.

#### Advantages

Besides creating a bit of a mess, objects that are no longer required can use
up system memory and cause an experience to run slower over time. For this
reason, it's always advised to call [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy) on objects you
no longer need. In some cases, however, an object may have a specific period
of utility before it can be destroyed.

Consider a wall being smashed into individual bricks. If you want a brick to
linger for 3 seconds before being destroyed, you can use the following code:

```
task.wait(3)



brick:Destroy()
```

However, waiting causes the thread to yield which may be undesired. To avoid
yielding, a callback function can be scheduled to run on a new thread after 3
seconds:

```
task.delay(3, function()



brick:Destroy()



end)
```

Or in one line:

```
task.delay(3, brick.Destroy, brick)
```

While this now avoids yielding, it has a potential drawback in that the
scheduled callback will never run if the script is disabled or destroyed
before the callback runs.

This is where [Debris](/docs/reference/engine/classes/Debris) has a specific advantage, as it does not yield
the current thread and runs outside the context of the script, guaranteeing
the instance is eventually destroyed even if the script is disabled or
destroyed. The following code does not yield and guarantees the instance will
be destroyed:

```
Debris:AddItem(brick, 3)
```

Note that [Debris](/docs/reference/engine/classes/Debris) has a hardcoded maximum of 1,000 objects, so if more
than 1,000 items are added, the oldest debris will be destroyed instantly to
make room for new debris.

Code Samples

Debris AddItem

Creates parts on a loop and parents them to the Workspace, then uses
Debris.AddItem to clean them up.

```
local Debris = game:GetService("Debris")



local ball = Instance.new("Part")



ball.Anchored = false



ball.Shape = Enum.PartType.Ball



ball.TopSurface = Enum.SurfaceType.Smooth



ball.BottomSurface = Enum.SurfaceType.Smooth



ball.Size = Vector3.new(1, 1, 1)



local RNG = Random.new()



local MAX_VELOCITY = 10



while true do



local newBall = ball:Clone()



newBall.BrickColor = BrickColor.random()



newBall.CFrame = CFrame.new(0, 30, 0)



newBall.Velocity =



Vector3.new(RNG:NextNumber(-MAX_VELOCITY, MAX_VELOCITY), 0, RNG:NextNumber(-MAX_VELOCITY, MAX_VELOCITY))



newBall.Parent = game.Workspace



Debris:AddItem(newBall, 2)



task.wait(0.1)



end
```

---

API Reference

Properties

MaxItems

Deprecated

Show details

---

Methods

AddItem

Schedules a given [Instance](/docs/reference/engine/classes/Instance) for destruction within the specified
lifetime.

Debris:AddItem(

item:[Instance](/docs/reference/engine/datatypes/Instance), lifetime:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| item:[Instance](/docs/reference/engine/datatypes/Instance)  The [Instance](/docs/reference/engine/classes/Instance) to add to [Debris](/docs/reference/engine/classes/Debris). |
| lifetime:[number](/docs/luau/numbers) Default Value: 10 Number of seconds before the [Instance](/docs/reference/engine/classes/Instance) should be destroyed. |

Returns

()

Schedules a given [Instance](/docs/reference/engine/classes/Instance) for destruction within the specified
lifetime. After the lifetime argument has elapsed, the object is
destroyed in the same manner as [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy). Note that the
lifetime argument is optional and defaults to 10 seconds.

Note that [Debris](/docs/reference/engine/classes/Debris) has a hardcoded maximum of 1,000 objects, so if
more than 1,000 items are added, the oldest debris will be destroyed
instantly to make room for new debris. This means you should treat the
lifetime parameter as a maximum lifetime, not an exact lifetime.

Code Samples

Debris AddItem

Creates parts on a loop and parents them to the Workspace, then uses
Debris.AddItem to clean them up.

```
local Debris = game:GetService("Debris")



local ball = Instance.new("Part")



ball.Anchored = false



ball.Shape = Enum.PartType.Ball



ball.TopSurface = Enum.SurfaceType.Smooth



ball.BottomSurface = Enum.SurfaceType.Smooth



ball.Size = Vector3.new(1, 1, 1)



local RNG = Random.new()



local MAX_VELOCITY = 10



while true do



local newBall = ball:Clone()



newBall.BrickColor = BrickColor.random()



newBall.CFrame = CFrame.new(0, 30, 0)



newBall.Velocity =



Vector3.new(RNG:NextNumber(-MAX_VELOCITY, MAX_VELOCITY), 0, RNG:NextNumber(-MAX_VELOCITY, MAX_VELOCITY))



newBall.Parent = game.Workspace



Debris:AddItem(newBall, 2)



task.wait(0.1)



end
```

Provide feedback

---

addItem

Deprecated

Show details

---