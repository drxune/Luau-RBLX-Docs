# SpawnLocation | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SpawnLocation
Scraped: 2026-01-11T02:35:23.364775Z

## Inherits
- Part
- SpawnLocation
- SpawnLocations
- Player
- Teams
- ForceFields
- FormFactorPart
- BasePart
- PVInstance
- Instance
- Object
- SpawnLocation.AllowTeamChangeOnTouch
- Team
- Team.AutoAssignable
- Workspace
- SpawnLocation.Neutral
- SpawnLocation.TeamColor
- Script
- Players
- Player.TeamColor
- RespawnTime
- Player.Neutral
- SpawnLocation.Enabled
- ForceField
- Instance.DescendantAdded
- Instance.ChildAdded
- Explosions
- Humanoid:TakeDamage()
- BasePart.Touched
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Part](/docs/reference/engine/classes/Part)
6. /
7. [SpawnLocation](/docs/reference/engine/classes/SpawnLocation)

English

Feedback

Engine Class

![SpawnLocation](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SpawnLocation-Dark.webp)SpawnLocation

[SpawnLocations](/docs/reference/engine/classes/SpawnLocation), or "spawns" determine where a
[Player](/docs/reference/engine/classes/Player) respawns when they die. They can be configured to allow only
certain players to use each spawn, using [Teams](/docs/reference/engine/classes/Team). They also control
how [ForceFields](/docs/reference/engine/classes/ForceField) are set up for newly-spawned players.

---

Summary

Properties

|  |
| --- |
| [AllowTeamChangeOnTouch](#AllowTeamChangeOnTouch):[boolean](/docs/luau/booleans) |
| [Duration](#Duration):[number](/docs/luau/numbers) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Neutral](#Neutral):[boolean](/docs/luau/booleans) |
| [TeamColor](#TeamColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor) |

Inherited Members

1 inherited from [Part](/docs/reference/engine/classes/Part)

2 inherited from [FormFactorPart](/docs/reference/engine/classes/FormFactorPart)

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

SpawnLocations, or "spawns" determine where a [Player](/docs/reference/engine/classes/Player) respawns when
they die. They can be configured to allow only certain players to use each
spawn, using [Teams](/docs/reference/engine/classes/Team). They also control how
[ForceFields](/docs/reference/engine/classes/ForceField) are set up for newly-spawned players.

SpawnLocations can be used as checkpoints, such as in an obstacle course,
using the [SpawnLocation.AllowTeamChangeOnTouch](/docs/reference/engine/classes/SpawnLocation#AllowTeamChangeOnTouch) property, so that when
a player touches it, they will change teams to the SpawnLocation's team. In
this case, only the first [Team](/docs/reference/engine/classes/Team) should have [Team.AutoAssignable](/docs/reference/engine/classes/Team#AutoAssignable)
set to true, else players will not start at the first checkpoint.

Note if a SpawnLocation is added to the [Workspace](/docs/reference/engine/classes/Workspace) in Studio with
[SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral) set to false a Team will be created
corresponding to [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor) if it does not already exist.
This behavior does not occur when spawns are created in-game using a
[Script](/docs/reference/engine/classes/Script) or if the properties of the SpawnLocation are changed after
already being added. It is recommended that developers always set up their
teams manually and not rely on this behavior.

Spawning Rules
--------------

There are several rules that come into play for a given SpawnLocation when a
player respawns:

* When [SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral) is set to false only
  [Players](/docs/reference/engine/classes/Player) with [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) matching
  [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor) will respawn above it
* When [SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral) is set to true any Player can spawn above
  it regardless of [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor)
* If multiple eligible spawns are available to a [Player](/docs/reference/engine/classes/Player), a random one
  will be chosen
* Players will spawn at different points on top of a SpawnLocation, but
  currently, they may still spawn on top of each other if they spawn right
  after one and other

See also:

* If you'd like to configure how long it takes for a player to respawn, take a
  look at the [RespawnTime](/docs/reference/engine/classes/Players#RespawnTime) property

Code Samples

SpawnLocation Checkpoints

This sample demonstrates how SpawnLocations can be used to make a checkpoint
system. Typically this would be done Studio and not in Lua, but this example
serves as a comprehensive example of what Team and SpawnLocation properties
need to be used to achieve this setup.

```
local Teams = game:GetService("Teams")



-- create start team (AutoAssignable = true)



local startTeam = Instance.new("Team")



startTeam.Name = "Start"



startTeam.AutoAssignable = true



startTeam.TeamColor = BrickColor.new("White")



startTeam.Parent = Teams



-- create checkpoint teams (Autoassignable = false), ensuring all TeamColors are unique



local team1 = Instance.new("Team")



team1.Name = "Checkpoint 1"



team1.AutoAssignable = false



team1.TeamColor = BrickColor.new("Bright blue")



team1.Parent = Teams



local team2 = Instance.new("Team")



team2.Name = "Checkpoint 2"



team2.AutoAssignable = false



team2.TeamColor = BrickColor.new("Bright green")



team2.Parent = Teams



local team3 = Instance.new("Team")



team3.Name = "Checkpoint 2"



team3.AutoAssignable = false



team3.TeamColor = BrickColor.new("Bright red")



team3.Parent = Teams



-- create spawns



local startSpawn = Instance.new("SpawnLocation")



startSpawn.Anchored = true



startSpawn.Size = Vector3.new(5, 1, 5)



startSpawn.Neutral = false



startSpawn.AllowTeamChangeOnTouch = false



startSpawn.TeamColor = startTeam.TeamColor



startSpawn.BrickColor = startTeam.TeamColor



startSpawn.Parent = game.Workspace



local team1Spawn = Instance.new("SpawnLocation")



team1Spawn.Anchored = true



team1Spawn.Size = Vector3.new(5, 1, 5)



team1Spawn.Neutral = false



team1Spawn.AllowTeamChangeOnTouch = true



team1Spawn.TeamColor = team1.TeamColor



team1Spawn.BrickColor = team1.TeamColor



team1Spawn.Parent = game.Workspace



local team2Spawn = Instance.new("SpawnLocation")



team2Spawn.Anchored = true



team2Spawn.Size = Vector3.new(5, 1, 5)



team2Spawn.Neutral = false



team2Spawn.AllowTeamChangeOnTouch = true



team2Spawn.TeamColor = team2.TeamColor



team2Spawn.BrickColor = team2.TeamColor



team2Spawn.Parent = game.Workspace



local team3Spawn = Instance.new("SpawnLocation")



team3Spawn.Anchored = true



team3Spawn.Size = Vector3.new(5, 1, 5)



team3Spawn.Neutral = false



team3Spawn.AllowTeamChangeOnTouch = true



team3Spawn.TeamColor = team3.TeamColor



team3Spawn.BrickColor = team3.TeamColor



team3Spawn.Parent = game.Workspace



-- position spawns



startSpawn.CFrame = CFrame.new(0, 0.5, 0)



team1Spawn.CFrame = CFrame.new(10, 0.5, 0)



team2Spawn.CFrame = CFrame.new(20, 0.5, 0)



team3Spawn.CFrame = CFrame.new(30, 0.5, 0)
```

---

API Reference

Properties

AllowTeamChangeOnTouch

Read Parallel

Allows a [Player](/docs/reference/engine/classes/Player) to join the team by touching the
[SpawnLocation](/docs/reference/engine/classes/SpawnLocation). When set to true, if a [Player](/docs/reference/engine/classes/Player) character
comes into contact with the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation), the player's
[Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) will be set to [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor).

SpawnLocation.AllowTeamChangeOnTouch:[boolean](/docs/luau/booleans)

Allows a [Player](/docs/reference/engine/classes/Player) to join the team by touching the
[SpawnLocation](/docs/reference/engine/classes/SpawnLocation). When set to true, if a [Player](/docs/reference/engine/classes/Player) character
comes into contact with the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation), the player's
[Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) will be set to [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor).
[Player.Neutral](/docs/reference/engine/classes/Player#Neutral) will also be set to [SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral)
upon contact, meaning a player can also become neutral by touching a spawn
location.

This will not function when [SpawnLocation.Enabled](/docs/reference/engine/classes/SpawnLocation#Enabled) is set to false.

#### Making Checkpoints

This feature is often used to make checkpoints in obstacle courses or
similar games.

Code Samples

SpawnLocation Checkpoints

This sample demonstrates how SpawnLocations can be used to make a checkpoint
system. Typically this would be done Studio and not in Lua, but this example
serves as a comprehensive example of what Team and SpawnLocation properties
need to be used to achieve this setup.

```
local Teams = game:GetService("Teams")



-- create start team (AutoAssignable = true)



local startTeam = Instance.new("Team")



startTeam.Name = "Start"



startTeam.AutoAssignable = true



startTeam.TeamColor = BrickColor.new("White")



startTeam.Parent = Teams



-- create checkpoint teams (Autoassignable = false), ensuring all TeamColors are unique



local team1 = Instance.new("Team")



team1.Name = "Checkpoint 1"



team1.AutoAssignable = false



team1.TeamColor = BrickColor.new("Bright blue")



team1.Parent = Teams



local team2 = Instance.new("Team")



team2.Name = "Checkpoint 2"



team2.AutoAssignable = false



team2.TeamColor = BrickColor.new("Bright green")



team2.Parent = Teams



local team3 = Instance.new("Team")



team3.Name = "Checkpoint 2"



team3.AutoAssignable = false



team3.TeamColor = BrickColor.new("Bright red")



team3.Parent = Teams



-- create spawns



local startSpawn = Instance.new("SpawnLocation")



startSpawn.Anchored = true



startSpawn.Size = Vector3.new(5, 1, 5)



startSpawn.Neutral = false



startSpawn.AllowTeamChangeOnTouch = false



startSpawn.TeamColor = startTeam.TeamColor



startSpawn.BrickColor = startTeam.TeamColor



startSpawn.Parent = game.Workspace



local team1Spawn = Instance.new("SpawnLocation")



team1Spawn.Anchored = true



team1Spawn.Size = Vector3.new(5, 1, 5)



team1Spawn.Neutral = false



team1Spawn.AllowTeamChangeOnTouch = true



team1Spawn.TeamColor = team1.TeamColor



team1Spawn.BrickColor = team1.TeamColor



team1Spawn.Parent = game.Workspace



local team2Spawn = Instance.new("SpawnLocation")



team2Spawn.Anchored = true



team2Spawn.Size = Vector3.new(5, 1, 5)



team2Spawn.Neutral = false



team2Spawn.AllowTeamChangeOnTouch = true



team2Spawn.TeamColor = team2.TeamColor



team2Spawn.BrickColor = team2.TeamColor



team2Spawn.Parent = game.Workspace



local team3Spawn = Instance.new("SpawnLocation")



team3Spawn.Anchored = true



team3Spawn.Size = Vector3.new(5, 1, 5)



team3Spawn.Neutral = false



team3Spawn.AllowTeamChangeOnTouch = true



team3Spawn.TeamColor = team3.TeamColor



team3Spawn.BrickColor = team3.TeamColor



team3Spawn.Parent = game.Workspace



-- position spawns



startSpawn.CFrame = CFrame.new(0, 0.5, 0)



team1Spawn.CFrame = CFrame.new(10, 0.5, 0)



team2Spawn.CFrame = CFrame.new(20, 0.5, 0)



team3Spawn.CFrame = CFrame.new(30, 0.5, 0)
```

Provide feedback

---

Duration

Read Parallel

The length of time, in seconds, that a [ForceField](/docs/reference/engine/classes/ForceField) will be applied
to a [Player](/docs/reference/engine/classes/Player) character spawning at this [SpawnLocation](/docs/reference/engine/classes/SpawnLocation). If
Duration is zero, the [ForceField](/docs/reference/engine/classes/ForceField) is never created, and it will not
trigger the [Instance.DescendantAdded](/docs/reference/engine/classes/Instance#DescendantAdded) or
[Instance.ChildAdded](/docs/reference/engine/classes/Instance#ChildAdded) events.

SpawnLocation.Duration:[number](/docs/luau/numbers)

The length of time, in seconds, that a [ForceField](/docs/reference/engine/classes/ForceField) will be applied
to a [Player](/docs/reference/engine/classes/Player) character spawning at this [SpawnLocation](/docs/reference/engine/classes/SpawnLocation). If
Duration is zero, the [ForceField](/docs/reference/engine/classes/ForceField) is never created, and it will not
trigger the [Instance.DescendantAdded](/docs/reference/engine/classes/Instance#DescendantAdded) or
[Instance.ChildAdded](/docs/reference/engine/classes/Instance#ChildAdded) events.

This default value of this property is 10 seconds.

The duration feature allows developers to easily give
[Players](/docs/reference/engine/classes/Player) protection from 'spawn killing' which can be a
frustrating experience for players. Note, [ForceFields](/docs/reference/engine/classes/ForceField)
will only protect users from [Explosions](/docs/reference/engine/classes/Explosion) and weapons that
use [Humanoid:TakeDamage()](/docs/reference/engine/classes/Humanoid#TakeDamage) to deal damage or otherwise check for a
[ForceField](/docs/reference/engine/classes/ForceField).

Code Samples

SpawnLocation ForceField

This sample will create a neutral SpawnLocation in the Workspace that'll give
players spawning a ForceField for 20 seconds.

```
local spawnLocation = Instance.new("SpawnLocation")



spawnLocation.Anchored = true



spawnLocation.Size = Vector3.new(5, 1, 5)



spawnLocation.Neutral = true -- anyone can spawn here



spawnLocation.Duration = 20



spawnLocation.Parent = workspace
```

Provide feedback

---

Enabled

Read Parallel

Sets whether or not the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) is enabled. When disabled
players cannot spawn at the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) and the
AllowTeamChangeOnTouch functionality is disabled.

SpawnLocation.Enabled:[boolean](/docs/luau/booleans)

Sets whether or not the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) is enabled. When disabled
players cannot spawn at the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) and the
[SpawnLocation.AllowTeamChangeOnTouch](/docs/reference/engine/classes/SpawnLocation#AllowTeamChangeOnTouch) functionality is disabled.

This property provides the most convenient way of preventing
[Players](/docs/reference/engine/classes/Player) from spawning at a spawn.

Note, although team changing on touch using
[SpawnLocation.AllowTeamChangeOnTouch](/docs/reference/engine/classes/SpawnLocation#AllowTeamChangeOnTouch) is disabled when Enabled is
set to false, other touched events using [BasePart.Touched](/docs/reference/engine/classes/BasePart#Touched) will
still fire.

Code Samples

SpawnLocation Enabled

The following sample will create a SpawnLocation in the Workspace that will
become semi-transparent when it is disabled.

```
local spawnLocation = Instance.new("SpawnLocation")



spawnLocation.Anchored = true



spawnLocation.Size = Vector3.new(5, 1, 5)



spawnLocation.Neutral = true -- anyone can spawn here



spawnLocation.Enabled = true



spawnLocation.Parent = workspace



local function onEnabledChanged()



spawnLocation.Transparency = spawnLocation.Enabled and 0 or 0.5



end



spawnLocation:GetPropertyChangedSignal("Enabled"):Connect(onEnabledChanged)



task.wait(5)



spawnLocation.Enabled = false -- transparency = 0.5
```

Provide feedback

---

Neutral

Read Parallel

Whether or not a [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) is affiliated with a specific team.
This means that any [Player](/docs/reference/engine/classes/Player), of any [Team](/docs/reference/engine/classes/Team), can spawn on it
if this property is set to true.

SpawnLocation.Neutral:[boolean](/docs/luau/booleans)

Whether or not a spawn is affiliated with a specific team. This means that
any [Player](/docs/reference/engine/classes/Player), of any [Team](/docs/reference/engine/classes/Team), can spawn on it if this property
is set to true.

If Neutral is set to false, only players whose [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) is
equal to [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor) can use the
[SpawnLocation](/docs/reference/engine/classes/SpawnLocation).

If [SpawnLocation.AllowTeamChangeOnTouch](/docs/reference/engine/classes/SpawnLocation#AllowTeamChangeOnTouch) is true
[Player.Neutral](/docs/reference/engine/classes/Player#Neutral) will be set to this property upon contact with the
spawn.

Code Samples

SpawnLocation Checkpoints

This sample demonstrates how SpawnLocations can be used to make a checkpoint
system. Typically this would be done Studio and not in Lua, but this example
serves as a comprehensive example of what Team and SpawnLocation properties
need to be used to achieve this setup.

```
local Teams = game:GetService("Teams")



-- create start team (AutoAssignable = true)



local startTeam = Instance.new("Team")



startTeam.Name = "Start"



startTeam.AutoAssignable = true



startTeam.TeamColor = BrickColor.new("White")



startTeam.Parent = Teams



-- create checkpoint teams (Autoassignable = false), ensuring all TeamColors are unique



local team1 = Instance.new("Team")



team1.Name = "Checkpoint 1"



team1.AutoAssignable = false



team1.TeamColor = BrickColor.new("Bright blue")



team1.Parent = Teams



local team2 = Instance.new("Team")



team2.Name = "Checkpoint 2"



team2.AutoAssignable = false



team2.TeamColor = BrickColor.new("Bright green")



team2.Parent = Teams



local team3 = Instance.new("Team")



team3.Name = "Checkpoint 2"



team3.AutoAssignable = false



team3.TeamColor = BrickColor.new("Bright red")



team3.Parent = Teams



-- create spawns



local startSpawn = Instance.new("SpawnLocation")



startSpawn.Anchored = true



startSpawn.Size = Vector3.new(5, 1, 5)



startSpawn.Neutral = false



startSpawn.AllowTeamChangeOnTouch = false



startSpawn.TeamColor = startTeam.TeamColor



startSpawn.BrickColor = startTeam.TeamColor



startSpawn.Parent = game.Workspace



local team1Spawn = Instance.new("SpawnLocation")



team1Spawn.Anchored = true



team1Spawn.Size = Vector3.new(5, 1, 5)



team1Spawn.Neutral = false



team1Spawn.AllowTeamChangeOnTouch = true



team1Spawn.TeamColor = team1.TeamColor



team1Spawn.BrickColor = team1.TeamColor



team1Spawn.Parent = game.Workspace



local team2Spawn = Instance.new("SpawnLocation")



team2Spawn.Anchored = true



team2Spawn.Size = Vector3.new(5, 1, 5)



team2Spawn.Neutral = false



team2Spawn.AllowTeamChangeOnTouch = true



team2Spawn.TeamColor = team2.TeamColor



team2Spawn.BrickColor = team2.TeamColor



team2Spawn.Parent = game.Workspace



local team3Spawn = Instance.new("SpawnLocation")



team3Spawn.Anchored = true



team3Spawn.Size = Vector3.new(5, 1, 5)



team3Spawn.Neutral = false



team3Spawn.AllowTeamChangeOnTouch = true



team3Spawn.TeamColor = team3.TeamColor



team3Spawn.BrickColor = team3.TeamColor



team3Spawn.Parent = game.Workspace



-- position spawns



startSpawn.CFrame = CFrame.new(0, 0.5, 0)



team1Spawn.CFrame = CFrame.new(10, 0.5, 0)



team2Spawn.CFrame = CFrame.new(20, 0.5, 0)



team3Spawn.CFrame = CFrame.new(30, 0.5, 0)
```

Provide feedback

---

TeamColor

Read Parallel

Sets what team the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) is affiliated to. If
[SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral) property is false, only
[Players](/docs/reference/engine/classes/Player) with the same [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) as the
spawn's TeamColor will be able to spawn there.

SpawnLocation.TeamColor:[BrickColor](/docs/reference/engine/datatypes/BrickColor)

The TeamColor property sets what team the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) is
affiliated to. If [SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral) property is false, only
[Players](/docs/reference/engine/classes/Player) with the same [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) as the
spawn's TeamColor will be able to spawn there.

If [SpawnLocation.AllowTeamChangeOnTouch](/docs/reference/engine/classes/SpawnLocation#AllowTeamChangeOnTouch) is true
[Player.Neutral](/docs/reference/engine/classes/Player#Neutral) will be set to this property upon contact with the
spawn.

Code Samples

SpawnLocation Checkpoints

This sample demonstrates how SpawnLocations can be used to make a checkpoint
system. Typically this would be done Studio and not in Lua, but this example
serves as a comprehensive example of what Team and SpawnLocation properties
need to be used to achieve this setup.

```
local Teams = game:GetService("Teams")



-- create start team (AutoAssignable = true)



local startTeam = Instance.new("Team")



startTeam.Name = "Start"



startTeam.AutoAssignable = true



startTeam.TeamColor = BrickColor.new("White")



startTeam.Parent = Teams



-- create checkpoint teams (Autoassignable = false), ensuring all TeamColors are unique



local team1 = Instance.new("Team")



team1.Name = "Checkpoint 1"



team1.AutoAssignable = false



team1.TeamColor = BrickColor.new("Bright blue")



team1.Parent = Teams



local team2 = Instance.new("Team")



team2.Name = "Checkpoint 2"



team2.AutoAssignable = false



team2.TeamColor = BrickColor.new("Bright green")



team2.Parent = Teams



local team3 = Instance.new("Team")



team3.Name = "Checkpoint 2"



team3.AutoAssignable = false



team3.TeamColor = BrickColor.new("Bright red")



team3.Parent = Teams



-- create spawns



local startSpawn = Instance.new("SpawnLocation")



startSpawn.Anchored = true



startSpawn.Size = Vector3.new(5, 1, 5)



startSpawn.Neutral = false



startSpawn.AllowTeamChangeOnTouch = false



startSpawn.TeamColor = startTeam.TeamColor



startSpawn.BrickColor = startTeam.TeamColor



startSpawn.Parent = game.Workspace



local team1Spawn = Instance.new("SpawnLocation")



team1Spawn.Anchored = true



team1Spawn.Size = Vector3.new(5, 1, 5)



team1Spawn.Neutral = false



team1Spawn.AllowTeamChangeOnTouch = true



team1Spawn.TeamColor = team1.TeamColor



team1Spawn.BrickColor = team1.TeamColor



team1Spawn.Parent = game.Workspace



local team2Spawn = Instance.new("SpawnLocation")



team2Spawn.Anchored = true



team2Spawn.Size = Vector3.new(5, 1, 5)



team2Spawn.Neutral = false



team2Spawn.AllowTeamChangeOnTouch = true



team2Spawn.TeamColor = team2.TeamColor



team2Spawn.BrickColor = team2.TeamColor



team2Spawn.Parent = game.Workspace



local team3Spawn = Instance.new("SpawnLocation")



team3Spawn.Anchored = true



team3Spawn.Size = Vector3.new(5, 1, 5)



team3Spawn.Neutral = false



team3Spawn.AllowTeamChangeOnTouch = true



team3Spawn.TeamColor = team3.TeamColor



team3Spawn.BrickColor = team3.TeamColor



team3Spawn.Parent = game.Workspace



-- position spawns



startSpawn.CFrame = CFrame.new(0, 0.5, 0)



team1Spawn.CFrame = CFrame.new(10, 0.5, 0)



team2Spawn.CFrame = CFrame.new(20, 0.5, 0)



team3Spawn.CFrame = CFrame.new(30, 0.5, 0)
```

Provide feedback

---