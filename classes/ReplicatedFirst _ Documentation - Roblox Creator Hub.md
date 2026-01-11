# ReplicatedFirst | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ReplicatedFirst
Scraped: 2026-01-11T02:34:45.710619Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- ReplicatedFirst
- LocalScripts
- ReplicatedStorage
- Instance:WaitForChild()
- LocalScript
- ReplicatedFirst:RemoveDefaultLoadingScreen()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst)

English

Feedback

Engine Class

![ReplicatedFirst](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ReplicatedFirst-Dark.webp)ReplicatedFirst

A container whose contents are replicated to all clients (but not back to the
server) first before anything else.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [RemoveDefaultLoadingScreen](#RemoveDefaultLoadingScreen)():() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A container whose contents are replicated to all clients (but not back to the
server) first before anything else.

What is ReplicatedFirst for?
----------------------------

ReplicatedFirst is most commonly used to store
[LocalScripts](/docs/reference/engine/classes/LocalScript) and other objects that are essential for the
game's start. As the contents of ReplicatedFirst replicate to the client
before anything else in the game, it is ideal for creating loading GUIs or
tutorials.

For objects that do not need to be replicated first, developers should use the
[ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage) container instead.

How can I use ReplicatedFirst?
------------------------------

[LocalScripts](/docs/reference/engine/classes/LocalScript) placed within ReplicatedFirst will run. This
means code for custom loading screens or other ReplicatedFirst uses can be ran
at the earliest possible point.

There a number of key considerations developers need to remember when running
[LocalScripts](/docs/reference/engine/classes/LocalScript) in ReplicatedFirst.

* Its contents replicate before anything else in the game, meaning
  [LocalScripts](/docs/reference/engine/classes/LocalScript) running in ReplicatedFirst will need to
  wait for any objects they require to replicate using
  [Instance:WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild)
* Any objects that are to be used by a [LocalScript](/docs/reference/engine/classes/LocalScript) in ReplicatedFirst
  should also be parented to ReplicatedFirst. Otherwise, they may replicate to
  the client late, yielding the script and negating the benefit of
  ReplicatedFirst.

ReplicatedFirst also includes the function
[ReplicatedFirst:RemoveDefaultLoadingScreen()](/docs/reference/engine/classes/ReplicatedFirst#RemoveDefaultLoadingScreen), which can be used to
immediately remove the default Roblox loading screen. Note if any object has
been placed in ReplicatedFirst, the default loading screen will remove after 5
seconds regardless if this function has been called or not.

Code Samples

Custom Loading Screen

This sample demonstrates a custom loading screen with a basic TextLabel. The
code should be placed in a LocalScript within ReplicatedFirst. To expand
on this sample with loading screen animations, see the
[Custom Loading Screens](/docs/ui/customizing-loading-screens)
article.

```
local Players = game:GetService("Players")



local ReplicatedFirst = game:GetService("ReplicatedFirst")



local player = Players.LocalPlayer



local playerGui = player:WaitForChild("PlayerGui")



-- Create a basic loading screen



local screenGui = Instance.new("ScreenGui")



screenGui.IgnoreGuiInset = true



local textLabel = Instance.new("TextLabel")



textLabel.Size = UDim2.new(1, 0, 1, 0)



textLabel.BackgroundColor3 = Color3.fromRGB(0, 20, 40)



textLabel.Font = Enum.Font.GothamMedium



textLabel.TextColor3 = Color3.new(0.8, 0.8, 0.8)



textLabel.Text = "Loading"



textLabel.TextSize = 28



textLabel.Parent = screenGui



-- Parent entire screen GUI to player GUI



screenGui.Parent = playerGui



-- Remove the default loading screen



ReplicatedFirst:RemoveDefaultLoadingScreen()



--task.wait(3)  -- Optionally force screen to appear for a minimum number of seconds



if not game:IsLoaded() then



game.Loaded:Wait()



end



screenGui:Destroy()
```

---

API Reference

Methods

RemoveDefaultLoadingScreen

Immediately removes the default Roblox loading screen. Note if any object
has been placed in [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst), the default loading screen
will remove after 5 seconds regardless if this function has been called or
not.

ReplicatedFirst:RemoveDefaultLoadingScreen():()

Returns

()

Immediately removes the default Roblox loading screen. Note if any object
has been placed in [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst), the default loading screen
will remove after 5 seconds regardless if this function has been called or
not.

Developers should run this function from a [LocalScript](/docs/reference/engine/classes/LocalScript) in
[ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst), as scripts in [ReplicatedFirst](/docs/reference/engine/classes/ReplicatedFirst) will
execute before anything else.

It is advised to not remove the default loading screen unless the
developer wishes to display their own loading screen as an alternative. If
the default screen is removed without replacement users will be able to
see geometry loading in the background.

Code Samples

Custom Loading Screen

This sample demonstrates a custom loading screen with a basic TextLabel. The
code should be placed in a LocalScript within ReplicatedFirst. To expand
on this sample with loading screen animations, see the
[Custom Loading Screens](/docs/ui/customizing-loading-screens)
article.

```
local Players = game:GetService("Players")



local ReplicatedFirst = game:GetService("ReplicatedFirst")



local player = Players.LocalPlayer



local playerGui = player:WaitForChild("PlayerGui")



-- Create a basic loading screen



local screenGui = Instance.new("ScreenGui")



screenGui.IgnoreGuiInset = true



local textLabel = Instance.new("TextLabel")



textLabel.Size = UDim2.new(1, 0, 1, 0)



textLabel.BackgroundColor3 = Color3.fromRGB(0, 20, 40)



textLabel.Font = Enum.Font.GothamMedium



textLabel.TextColor3 = Color3.new(0.8, 0.8, 0.8)



textLabel.Text = "Loading"



textLabel.TextSize = 28



textLabel.Parent = screenGui



-- Parent entire screen GUI to player GUI



screenGui.Parent = playerGui



-- Remove the default loading screen



ReplicatedFirst:RemoveDefaultLoadingScreen()



--task.wait(3)  -- Optionally force screen to appear for a minimum number of seconds



if not game:IsLoaded() then



game.Loaded:Wait()



end



screenGui:Destroy()
```

Provide feedback

---