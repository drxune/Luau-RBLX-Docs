# Tool | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Tool
Scraped: 2026-01-11T02:30:34.442693Z

## Tags
- Not Replicated

## Inherits
- BackpackItem
- Tool
- Humanoid
- Mouse
- Model
- PVInstance
- Instance
- Object
- Flag
- Backpack
- Player
- Player.Character
- Workspace
- BasePart
- Tool.RequiresHandle
- StarterPack
- Tool:Activate()
- Tool:Deactivate()
- Tool.Activated
- Tool.Deactivated
- JumpPower
- Tool.Enabled
- GripUp
- GripRight
- GripForward
- GripPos
- Tool.GripUp
- Tool.GripRight
- Tool.GripPos
- Tool.Grip
- Tool.GripForward
- ContextActionService:BindActivate()
- WalkSpeed
- Tool.ManualActivationOnly
- LocalScript
- Tool.Unequipped
- Tool.Equipped
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BackpackItem](/docs/reference/engine/classes/BackpackItem)
6. /
7. [Tool](/docs/reference/engine/classes/Tool)

English

Feedback

Engine Class

![Tool](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Tool-Dark.webp)Tool

An object, such as a weapon, that can be equipped by a [Humanoid](/docs/reference/engine/classes/Humanoid).

---

Summary

Properties

|  |
| --- |
| [CanBeDropped](#CanBeDropped):[boolean](/docs/luau/booleans) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Grip](#Grip):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [GripForward](#GripForward):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GripPos](#GripPos):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GripRight](#GripRight):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GripUp](#GripUp):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ManualActivationOnly](#ManualActivationOnly):[boolean](/docs/luau/booleans) |
| [RequiresHandle](#RequiresHandle):[boolean](/docs/luau/booleans) |
| [ToolTip](#ToolTip):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [Activate](#Activate)():() |
| [Deactivate](#Deactivate)():() |

Events

|  |
| --- |
| [Activated](#Activated)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Deactivated](#Deactivated)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Equipped](#Equipped)(mouse: [Mouse](/docs/reference/engine/classes/Mouse)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Unequipped](#Unequipped)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

2 inherited from [BackpackItem](/docs/reference/engine/classes/BackpackItem)

26 inherited from [Model](/docs/reference/engine/classes/Model)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Flag](/docs/reference/engine/classes/Flag)

A Tool is an object that a [Humanoid](/docs/reference/engine/classes/Humanoid) object can equip. For players,
they are stored in a [Backpack](/docs/reference/engine/classes/Backpack) object parented to a [Player](/docs/reference/engine/classes/Player)
object. In-experience, players may have multiple tools which appear as icons
at the bottom of the screen. Equipping a tool moves it from the
[Backpack](/docs/reference/engine/classes/Backpack) and into a [Player.Character](/docs/reference/engine/classes/Player#Character) model in the
[Workspace](/docs/reference/engine/classes/Workspace). By default, tools are held in the right hand and have a
handle in them, which is a [BasePart](/docs/reference/engine/classes/BasePart) named Handle inside (although
one isn't required if [Tool.RequiresHandle](/docs/reference/engine/classes/Tool#RequiresHandle) is false). Tools that are
to be provided to (re)spawning players should be stored in the
[StarterPack](/docs/reference/engine/classes/StarterPack).

Code Samples

Explode Tool Example

This code is meant to be placed in a Script within a Tool. It allows a player
to spawn explosions by equipping the tool and clicking on the ground. It does
so by defining a function, explode, which creates a non-deadly explosion at
a given point. Then, it defines a function, onActivated, that runs when the
tool is activated. Finally, it connects the Activated event of the tool to the
onActivated function.

To test this code out, try creating a Tool and put a Part inside it. Name the
Part "Handle". Put a Script inside the Tool next, and paste the code into it.
Finally, put the Tool in the StarterPack.

```
local tool = script.Parent



local function explode(point)



local e = Instance.new("Explosion")



e.DestroyJointRadiusPercent = 0 -- Make the explosion non-deadly



e.Position = point



e.Parent = workspace



end



local function onActivated()



-- Get the Humanoid that Activated the tool



local human = tool.Parent.Humanoid



-- Call explode with the current point the Humanoid is targetting



explode(human.TargetPoint)



end



tool.Activated:Connect(onActivated)
```

Sword Tool Example

This code sample is for a Tool object with a Part named Handle. It detects
when Humanoids other than the current holder hit the handle, and deals some
damage to them. In addition, when the Tool is activated, it triggers a slash
animation in the default character animation scripts. Try out this script by
creating a Tool object in the StarterPack. Put a Part inside it, and name it
Handle. Paste this code into a Script inside the Tool, then try slashing at
another Humanoid!

```
local tool = script.Parent



local function onTouch(partOther)



-- First, try to see if the part we touched was part of a Humanoid



local humanOther = partOther.Parent:FindFirstChild("Humanoid")



-- Ignore touches by non-humanoids



if not humanOther then



return



end



-- Ignore touches by the Humanoid carrying the sword



if humanOther.Parent == tool.Parent then



return



end



humanOther:TakeDamage(5)



end



-- Trigger a slash animation



local function slash()



-- Default character scripts will listen for a "toolanim" StringValue



local value = Instance.new("StringValue")



value.Name = "toolanim"



value.Value = "Slash" -- try also: Lunge



value.Parent = tool



end



tool.Activated:Connect(slash)



tool.Handle.Touched:Connect(onTouch)
```

---

API Reference

Properties

CanBeDropped

Read Parallel

Controls whether the player can drop the tool.

Tool.CanBeDropped:[boolean](/docs/luau/booleans)

The CanBeDropped property controls whether the player can drop the
[Tool](/docs/reference/engine/classes/Tool).

If true, when the backspace button is pressed, the tool will be parented
to [Workspace](/docs/reference/engine/classes/Workspace) and removed from the player's [Backpack](/docs/reference/engine/classes/Backpack). If
false, nothing will happen when backspace is pressed, and the tool will
remain equipped.

Provide feedback

---

Enabled

Read Parallel

Relates to whether or not the tool can be used.

Tool.Enabled:[boolean](/docs/luau/booleans)

The Enabled property relates to whether or not the [Tool](/docs/reference/engine/classes/Tool) can be
used. This is useful if you want to prevent a player from using a tool,
but don't want to remove it from their [Backpack](/docs/reference/engine/classes/Backpack).

When set to true, the player can use the tool. When set to false, the
tool is disabled and the player cannot use it; this prevents the tool from
being activated or deactivated by the [Tool:Activate()](/docs/reference/engine/classes/Tool#Activate) and
[Tool:Deactivate()](/docs/reference/engine/classes/Tool#Deactivate) methods, and it prevents the
[Tool.Activated](/docs/reference/engine/classes/Tool#Activated) and [Tool.Deactivated](/docs/reference/engine/classes/Tool#Deactivated) events from firing.

Code Samples

Superjump Tool

The code sample below creates [Tool](/docs/reference/engine/classes/Tool) in the local player's
[Backpack](/docs/reference/engine/classes/Backpack) that increases their [JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower)
from 50 to 150 for 5 seconds.

This example uses the tool's [Tool.Enabled](/docs/reference/engine/classes/Tool#Enabled) property as a debounce by
setting the property to true when the player jumps and back to false after
the 5 second duration.

Unequipping the tool also stops the player from super jumping by changing the
[JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower) back to 50.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



local tool = Instance.new("Tool")



tool.Name = "SuperJump"



tool.RequiresHandle = false



tool.Parent = player.Backpack



function toolActivated()



humanoid.JumpPower = 150



tool.Enabled = false



task.wait(5)



tool.Enabled = true



humanoid.JumpPower = 50



end



tool.Activated:Connect(toolActivated)



tool.Unequipped:Connect(function()



humanoid.JumpPower = 50



end)
```

Provide feedback

---

Grip

Read Parallel

Stores the tool's "grip" properties as one [CFrame](/docs/reference/engine/datatypes/CFrame).

Tool.Grip:[CFrame](/docs/reference/engine/datatypes/CFrame)

The Grip property stores the tool's "grip" properties as a single
[CFrame](/docs/reference/engine/datatypes/CFrame). These properties position how the player holds the tool
and include [GripUp](/docs/reference/engine/classes/Tool#GripUp), [GripRight](/docs/reference/engine/classes/Tool#GripRight),
[GripForward](/docs/reference/engine/classes/Tool#GripForward), and [GripPos](/docs/reference/engine/classes/Tool#GripPos).

Code Samples

Grip Stick

The code below insert's a [Tool](/docs/reference/engine/classes/Tool) named Stick into the local player's
Class.BackPack. When the player activates the tool, the code prints the
values of the tool's grip properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local tool = Instance.new("Tool")



tool.Name = "Stick"



tool.Parent = player.Backpack



local handle = Instance.new("Part")



handle.Name = "Handle"



handle.Parent = tool



handle.Size = Vector3.new(0.1, 3, 0.1)



handle.Color = Color3.fromRGB(108, 88, 75) -- Brown



tool.Activated:Connect(function()



print(tool.Grip)



print(tool.GripUp)



print(tool.GripRight)



print(tool.GripForward)



print(tool.GripPos)



end)
```

Provide feedback

---

GripForward

Hidden

Not Replicated

Read Parallel

Represents the R02, R12, and R22 values of the grip
[CFrame](/docs/reference/engine/datatypes/CFrame) rotation matrix.

Tool.GripForward:[Vector3](/docs/reference/engine/datatypes/Vector3)

One of the properties that specifies a tool's orientation in a character's
hand. This represents the R02, R12, and R22 values of the grip
[CFrame](/docs/reference/engine/datatypes/CFrame) rotation matrix.

Other tool properties that control how a character holds a tool include
[Tool.GripUp](/docs/reference/engine/classes/Tool#GripUp), [Tool.GripRight](/docs/reference/engine/classes/Tool#GripRight), and [Tool.GripPos](/docs/reference/engine/classes/Tool#GripPos). All
of these properties are stored in a single [CFrame](/docs/reference/engine/datatypes/CFrame) in the
[Tool.Grip](/docs/reference/engine/classes/Tool#Grip) property.

Code Samples

Grip Stick

The code below insert's a [Tool](/docs/reference/engine/classes/Tool) named Stick into the local player's
Class.BackPack. When the player activates the tool, the code prints the
values of the tool's grip properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local tool = Instance.new("Tool")



tool.Name = "Stick"



tool.Parent = player.Backpack



local handle = Instance.new("Part")



handle.Name = "Handle"



handle.Parent = tool



handle.Size = Vector3.new(0.1, 3, 0.1)



handle.Color = Color3.fromRGB(108, 88, 75) -- Brown



tool.Activated:Connect(function()



print(tool.Grip)



print(tool.GripUp)



print(tool.GripRight)



print(tool.GripForward)



print(tool.GripPos)



end)
```

Provide feedback

---

GripPos

Hidden

Not Replicated

Read Parallel

The positional offset of the tool's weld matrix.

Tool.GripPos:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property controls the positional offset of the tool's weld matrix. It
is one of several properties used to position how the player character
holds the tool.

Other properties that control how a character holds a tool include
[Tool.GripUp](/docs/reference/engine/classes/Tool#GripUp), [Tool.GripRight](/docs/reference/engine/classes/Tool#GripRight), and [Tool.GripForward](/docs/reference/engine/classes/Tool#GripForward).
All of these properties are stored in a single [CFrame](/docs/reference/engine/datatypes/CFrame) in the
[Tool.Grip](/docs/reference/engine/classes/Tool#Grip) property.

Code Samples

Grip Stick

The code below insert's a [Tool](/docs/reference/engine/classes/Tool) named Stick into the local player's
Class.BackPack. When the player activates the tool, the code prints the
values of the tool's grip properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local tool = Instance.new("Tool")



tool.Name = "Stick"



tool.Parent = player.Backpack



local handle = Instance.new("Part")



handle.Name = "Handle"



handle.Parent = tool



handle.Size = Vector3.new(0.1, 3, 0.1)



handle.Color = Color3.fromRGB(108, 88, 75) -- Brown



tool.Activated:Connect(function()



print(tool.Grip)



print(tool.GripUp)



print(tool.GripRight)



print(tool.GripForward)



print(tool.GripPos)



end)
```

Provide feedback

---

GripRight

Hidden

Not Replicated

Read Parallel

Represents the R00, R10, and R20 values of the grip
[CFrame](/docs/reference/engine/datatypes/CFrame) rotation matrix.

Tool.GripRight:[Vector3](/docs/reference/engine/datatypes/Vector3)

One of the properties that specifies a tool's orientation in a character's
hand. This represents the R00, R10, and R20 values of the grip
[CFrame](/docs/reference/engine/datatypes/CFrame) rotation matrix.

Other tool properties that control how a character holds a tool include
[Tool.GripUp](/docs/reference/engine/classes/Tool#GripUp), [Tool.GripForward](/docs/reference/engine/classes/Tool#GripForward), and [Tool.GripPos](/docs/reference/engine/classes/Tool#GripPos).
All of these properties are stored in a single [CFrame](/docs/reference/engine/datatypes/CFrame) in the
[Tool.Grip](/docs/reference/engine/classes/Tool#Grip) property.

Code Samples

Grip Stick

The code below insert's a [Tool](/docs/reference/engine/classes/Tool) named Stick into the local player's
Class.BackPack. When the player activates the tool, the code prints the
values of the tool's grip properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local tool = Instance.new("Tool")



tool.Name = "Stick"



tool.Parent = player.Backpack



local handle = Instance.new("Part")



handle.Name = "Handle"



handle.Parent = tool



handle.Size = Vector3.new(0.1, 3, 0.1)



handle.Color = Color3.fromRGB(108, 88, 75) -- Brown



tool.Activated:Connect(function()



print(tool.Grip)



print(tool.GripUp)



print(tool.GripRight)



print(tool.GripForward)



print(tool.GripPos)



end)
```

Provide feedback

---

GripUp

Hidden

Not Replicated

Read Parallel

Represents the R01, R11, and R21 values of the grip
[CFrame](/docs/reference/engine/datatypes/CFrame) rotation matrix.

Tool.GripUp:[Vector3](/docs/reference/engine/datatypes/Vector3)

One of the properties that specifies a tool's orientation in a character's
hand. This represents the R01, R11, and R21 values of the grip
[CFrame](/docs/reference/engine/datatypes/CFrame) rotation matrix.

Other tool properties that control how a character holds a tool include
[Tool.GripRight](/docs/reference/engine/classes/Tool#GripRight), [Tool.GripForward](/docs/reference/engine/classes/Tool#GripForward), and
[Tool.GripPos](/docs/reference/engine/classes/Tool#GripPos). All of these properties are stored in a single
[CFrame](/docs/reference/engine/datatypes/CFrame) in the [Tool.Grip](/docs/reference/engine/classes/Tool#Grip) property.

Code Samples

Grip Stick

The code below insert's a [Tool](/docs/reference/engine/classes/Tool) named Stick into the local player's
Class.BackPack. When the player activates the tool, the code prints the
values of the tool's grip properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local tool = Instance.new("Tool")



tool.Name = "Stick"



tool.Parent = player.Backpack



local handle = Instance.new("Part")



handle.Name = "Handle"



handle.Parent = tool



handle.Size = Vector3.new(0.1, 3, 0.1)



handle.Color = Color3.fromRGB(108, 88, 75) -- Brown



tool.Activated:Connect(function()



print(tool.Grip)



print(tool.GripUp)



print(tool.GripRight)



print(tool.GripForward)



print(tool.GripPos)



end)
```

Provide feedback

---

ManualActivationOnly

Read Parallel

Controls whether the [Tool](/docs/reference/engine/classes/Tool) can be activated without executing
[Tool:Activate()](/docs/reference/engine/classes/Tool#Activate).

Tool.ManualActivationOnly:[boolean](/docs/luau/booleans)

This property controls whether the [Tool](/docs/reference/engine/classes/Tool) can be activated without
explicitly executing [Tool:Activate()](/docs/reference/engine/classes/Tool#Activate) in a script.

When set to true, the tool will only fire [Tool.Activated](/docs/reference/engine/classes/Tool#Activated) when
[Tool:Activate()](/docs/reference/engine/classes/Tool#Activate) is called. This also suppresses the
[ContextActionService:BindActivate()](/docs/reference/engine/classes/ContextActionService#BindActivate) function.

When set to false, mouse clicks (when the tool is equipped) will also
fire [Tool.Activated](/docs/reference/engine/classes/Tool#Activated).

Code Samples

Sprint Tool

The code sample below creates [Tool](/docs/reference/engine/classes/Tool) in the local player's
[Backpack](/docs/reference/engine/classes/Backpack) that increases their [WalkSpeed](/docs/reference/engine/classes/Humanoid#Walkspeed)
from 16 to 30 for 5 seconds.

This example uses the tool's [Tool.ManualActivationOnly](/docs/reference/engine/classes/Tool#ManualActivationOnly) property as a
debounce by setting the property to true when the player begins sprinting
and to false when the player stops sprinting. As a result, when the player
is sprinting, the tool cannot be re-activated.

Unequipping the tool also stops the player from sprinting by changing the
[WalkSpeed](/docs/reference/engine/classes/Humanoid#Walkspeed) to 16.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



local tool = Instance.new("Tool")



tool.Name = "Sprint"



tool.RequiresHandle = false



tool.Parent = player:WaitForChild("Backpack")



function toolActivated()



humanoid.WalkSpeed = 30



tool.ManualActivationOnly = true



task.wait(5)



tool.ManualActivationOnly = false



humanoid.WalkSpeed = 16



end



tool.Activated:Connect(toolActivated)



tool.Unequipped:Connect(function()



humanoid.WalkSpeed = 16



end)
```

Provide feedback

---

RequiresHandle

Read Parallel

Determines whether a [Tool](/docs/reference/engine/classes/Tool) functions without a handle.

Tool.RequiresHandle:[boolean](/docs/luau/booleans)

This property determines whether a [Tool](/docs/reference/engine/classes/Tool) functions without a
handle.

A tool has a handle when it contains a child part named Handle. Tools
with handles typically require the player equipping them to hold an object
to use them, for instance weapons. Tools without handles typically don't
require the player equipping them to hold anything to use them, for
instance "fly" or "summon" tools.

When set to true, the tool will function only with a handle. When set to
false, the tool will function even without a handle.

Provide feedback

---

ToolTip

Read Parallel

Controls the message displayed when the player's mouse hovers over the
tool in their backpack.

Tool.ToolTip:[string](/docs/luau/strings)

The ToolTip property controls the message that will be displayed when the
player's [Mouse](/docs/reference/engine/classes/Mouse) hovers over the [Tool](/docs/reference/engine/classes/Tool) in their
[Backpack](/docs/reference/engine/classes/Backpack).

Generally, the value of this property should describe the what the tool is
or its use. For instance, for a shovel tool, you may choose to set the
ToolTip to:

```
tool.ToolTip = "Shovel"
```

or

```
tool.ToolTip = "Use to dig"
```

or

```
tool.ToolTip = "Shovel - Use to dig"
```

Provide feedback

---

Methods

Activate

Simulates activation of the [Tool](/docs/reference/engine/classes/Tool).

Tool:Activate():()

Returns

()

This function simulates activation of the [Tool](/docs/reference/engine/classes/Tool). The tool must be
equipped for this function to work.

Code Samples

Invisibility Tool

The code below creates a [Tool](/docs/reference/engine/classes/Tool) in the local player's [Backpack](/docs/reference/engine/classes/Backpack)
that turns the player invisible when activated and visible when deactivated.

When equipped, the script simulates the tool being activated and turns the
player invisible for 3 seconds and then simulates the tool being deactivated.
Holding the left mouse button down turns the player invisible for up to 3
seconds, with a cooldown period of 1 second, or until the player releases
their left mouse button.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character



local tool = Instance.new("Tool")



tool.Name = "Invisibility Tool"



tool.RequiresHandle = false



tool.Parent = player.Backpack



local invisible = false



local function toolActivated()



if invisible then



return



end



invisible = true



for _, bodypart in pairs(character:GetChildren()) do



if bodypart:IsA("MeshPart") or bodypart:IsA("Part") then



bodypart.Transparency = 1



end



end



task.wait(3)



tool:Deactivate()



task.wait(1)



invisible = false



end



local function toolDeactivated()



if not invisible then



return



end



for _, bodypart in pairs(character:GetChildren()) do



if bodypart.Name ~= "HumanoidRootPart" then



if bodypart:IsA("MeshPart") or bodypart:IsA("Part") then



bodypart.Transparency = 0



end



end



end



end



local function toolEquipped()



tool:Activate()



end



tool.Equipped:Connect(toolEquipped)



tool.Activated:Connect(toolActivated)



tool.Deactivated:Connect(toolDeactivated)



tool.Unequipped:Connect(toolDeactivated)
```

Provide feedback

---

Deactivate

Simulates deactivation of the [Tool](/docs/reference/engine/classes/Tool).

Tool:Deactivate():()

Returns

()

This function simulates deactivation of the [Tool](/docs/reference/engine/classes/Tool). The tool must be
equipped for this function to work.

Code Samples

Invisibility Tool

The code below creates a [Tool](/docs/reference/engine/classes/Tool) in the local player's [Backpack](/docs/reference/engine/classes/Backpack)
that turns the player invisible when activated and visible when deactivated.

When equipped, the script simulates the tool being activated and turns the
player invisible for 3 seconds and then simulates the tool being deactivated.
Holding the left mouse button down turns the player invisible for up to 3
seconds, with a cooldown period of 1 second, or until the player releases
their left mouse button.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character



local tool = Instance.new("Tool")



tool.Name = "Invisibility Tool"



tool.RequiresHandle = false



tool.Parent = player.Backpack



local invisible = false



local function toolActivated()



if invisible then



return



end



invisible = true



for _, bodypart in pairs(character:GetChildren()) do



if bodypart:IsA("MeshPart") or bodypart:IsA("Part") then



bodypart.Transparency = 1



end



end



task.wait(3)



tool:Deactivate()



task.wait(1)



invisible = false



end



local function toolDeactivated()



if not invisible then



return



end



for _, bodypart in pairs(character:GetChildren()) do



if bodypart.Name ~= "HumanoidRootPart" then



if bodypart:IsA("MeshPart") or bodypart:IsA("Part") then



bodypart.Transparency = 0



end



end



end



end



local function toolEquipped()



tool:Activate()



end



tool.Equipped:Connect(toolEquipped)



tool.Activated:Connect(toolActivated)



tool.Deactivated:Connect(toolDeactivated)



tool.Unequipped:Connect(toolDeactivated)
```

Provide feedback

---

Events

Activated

Fires when the player clicks while the tool is equipped.

Tool.Activated():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the player clicks while the [Tool](/docs/reference/engine/classes/Tool) is
equipped. It is not fired if the Ctrl key is pressed during
the click.

This event is typically used to perform an action when the player uses the
tool, for instance to launch a rocket from a rocket launcher weapon tool.

The below code, when placed in a [LocalScript](/docs/reference/engine/classes/LocalScript), creates a tool in
the local player's [Backpack](/docs/reference/engine/classes/Backpack) and prints "Tool activated" when the
player clicks while the created tool is equipped.

```
local Players = game:GetService("Players")



local tool = Instance.new("Tool")



tool.RequiresHandle = false



tool.Parent = Players.LocalPlayer.Backpack



function onActivation()



print("Tool activated")



end



tool.Activated:Connect(onActivation)
```

Provide feedback

---

Deactivated

Fires when the player releases their click while the tool is equipped and
activated.

Tool.Deactivated():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the player releases their click while the
[Tool](/docs/reference/engine/classes/Tool) is equipped and activated. It is typically used to perform an
action when the player stops using a tool.

The below code, when placed in a [LocalScript](/docs/reference/engine/classes/LocalScript), creates a tool in
the local player's [Backpack](/docs/reference/engine/classes/Backpack) and prints "Tool deactivated" when the
player releases their click while the tool is equipped and activated.

```
local Players = game:GetService("Players")



local tool = Instance.new("Tool")



tool.RequiresHandle = false



tool.Parent = Players.LocalPlayer.Backpack



function toolDeactivated()



print("Tool deactivated")



end



tool.Deactivated:Connect(toolDeactivated)
```

Provide feedback

---

Equipped

Fires when the tool is equipped.

Tool.Equipped(mouse:[Mouse](/docs/reference/engine/classes/Mouse)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| mouse:[Mouse](/docs/reference/engine/classes/Mouse)  The player's mouse. |

This event fires when a player equips the [Tool](/docs/reference/engine/classes/Tool) (takes it out of
their [Backpack](/docs/reference/engine/classes/Backpack)).

The opposite of this event, [Tool.Unequipped](/docs/reference/engine/classes/Tool#Unequipped), can be used to
determine when the player unequips the tool by putting it in their
backpack.

Note that this event does not fire when [Tool.RequiresHandle](/docs/reference/engine/classes/Tool#RequiresHandle) is
enabled and no handle is present.

Code Samples

Print when a Player Equips a Tool

The example shown below will print "A tool was equipped" each time the tool is
equipped by the player. Please note that the below example assumes that you've
already defined what "Tool" is.

```
local Tool = script.Parent



local function onEquipped(_mouse)



print("The tool was equipped")



end



Tool.Equipped:Connect(onEquipped)
```

Provide feedback

---

Unequipped

Fires when the tool is unequipped.

Tool.Unequipped():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when a player unequips the [Tool](/docs/reference/engine/classes/Tool) (puts it in their
[Backpack](/docs/reference/engine/classes/Backpack)).

The opposite of this event, [Tool.Equipped](/docs/reference/engine/classes/Tool#Equipped), can be used to
determine when the player equips the tool by taking it out of their
backpack.

Note that this event does not fire when [Tool.RequiresHandle](/docs/reference/engine/classes/Tool#RequiresHandle) is
enabled and no handle is present.

Provide feedback

---