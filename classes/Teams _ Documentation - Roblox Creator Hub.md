# Teams | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Teams
Scraped: 2026-01-11T02:27:58.189160Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- Teams
- Team
- Model
- Team.TeamColor
- Player.TeamColor
- Player.Team
- Player.Neutral
- Player
- Team.AutoAssignable
- SpawnLocation.Neutral
- SpawnLocation.TeamColor
- SpawnLocation
- SpawnLocation.AllowTeamChangeOnTouch
- Instances
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Teams](/docs/reference/engine/classes/Teams)

English

Feedback

Engine Class

![Teams](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Teams-Dark.webp)Teams

The Teams service holds a game's [Team](/docs/reference/engine/classes/Team) objects. [Team](/docs/reference/engine/classes/Team) objects
must be parented to the Teams service.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [GetTeams](#GetTeams)():Instances |
| [RebalanceTeams](#RebalanceTeams)():()  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Teams service holds a game's [Team](/docs/reference/engine/classes/Team) objects. [Team](/docs/reference/engine/classes/Team) objects
must be parented to the Teams service.

Teams offer a range of features that are useful to developers. These can
broadly be divided into features that work out-of-the-box and features
developers can program into their game.

Built-in team behavior The following functionality of Teams exists by
default and does not require the developer to program any custom behavior.

* When part of a Team, the name above a player's character [Model](/docs/reference/engine/classes/Model) will
  be colored to the [Team.TeamColor](/docs/reference/engine/classes/Team#TeamColor)
* Changing [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) will cause [Player.Team](/docs/reference/engine/classes/Player#Team) switch to
  the Team with the corresponding [Team.TeamColor](/docs/reference/engine/classes/Team#TeamColor)
* When using the default player list users will be grouped and displayed by
  team
* Setting [Player.Neutral](/docs/reference/engine/classes/Player#Neutral) to true will cause the [Player](/docs/reference/engine/classes/Player) to be
  dis-associated with the team, but will not change [Player.Team](/docs/reference/engine/classes/Player#Team) or
  [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor)
* When a [Player](/docs/reference/engine/classes/Player) joins a game, they will be allocated to the team with
  [Team.AutoAssignable](/docs/reference/engine/classes/Team#AutoAssignable) set to true that has the fewest players. If no
  auto assignable team is available, [Player.Neutral](/docs/reference/engine/classes/Player#Neutral) will be set to
  true
* When [SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral) is set to false, only players whose
  [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) matches [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor) can spawn
  on that [SpawnLocation](/docs/reference/engine/classes/SpawnLocation)
* When [SpawnLocation.AllowTeamChangeOnTouch](/docs/reference/engine/classes/SpawnLocation#AllowTeamChangeOnTouch) is set to true, a player's
  [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) will change to [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor) when
  their character touches the [SpawnLocation](/docs/reference/engine/classes/SpawnLocation)

Optional extended team behavior Many developers chose to add the following
features to teams in their own code.

* Implement checks for team in weapon code to prevent team killing
* Implement doors or other features that only certain teams can use
* Periodically reassign teams to maintain team balance

Code Samples

Simple Team Rebalance

This code sample includes a simple example of how to re-balance teams. When
Team.AutoAssignable is set to true players will be added to Teams in a
balanced fashion. However as Players leave the game this can lead to
unbalanced teams as players are not reallocated. This code keeps track of the
number of players in each team and, when players leave will check to see if
the teams need re-balancing.

```
local Teams = game:GetService("Teams")



-- create two teams



local redTeam = Instance.new("Team")



redTeam.TeamColor = BrickColor.new("Bright red")



redTeam.AutoAssignable = true



redTeam.Name = "Red Team"



redTeam.Parent = Teams



local blueTeam = Instance.new("Team")



blueTeam.TeamColor = BrickColor.new("Bright blue")



blueTeam.AutoAssignable = true



blueTeam.Name = "Blue Team"



blueTeam.Parent = Teams



-- start counting the number of players on each team



local numberRed, numberBlue = 0, 0



local function playerAdded(team)



-- increase the team's count by 1



if team == redTeam then



numberRed = numberRed + 1



elseif team == blueTeam then



numberBlue = numberBlue + 1



end



end



local function playerRemoved(team)



-- decrease the team's count by 1



if team == redTeam then



numberRed = numberRed - 1



elseif team == blueTeam then



numberBlue = numberBlue - 1



end



-- check if the teams are unbalanced



local bigTeam, smallTeam = nil, nil



if (numberRed - numberBlue) > 2 then



bigTeam = redTeam



smallTeam = blueTeam



elseif (numberBlue - numberRed) > 2 then



bigTeam = blueTeam



smallTeam = redTeam



end



if bigTeam then



-- pick a random player



local playerList = bigTeam:GetPlayers()



local player = playerList[math.random(1, #playerList)]



-- check the player exists



if player then



-- change the player's team



player.TeamColor = smallTeam.TeamColor



-- respawn the player



player:LoadCharacter()



end



end



end



-- listen for players being added / removed



blueTeam.PlayerAdded:Connect(function(_player)



playerAdded(blueTeam)



end)



blueTeam.PlayerRemoved:Connect(function(_player)



playerRemoved(blueTeam)



end)



redTeam.PlayerAdded:Connect(function(_player)



playerAdded(redTeam)



end)



redTeam.PlayerRemoved:Connect(function(_player)



playerRemoved(redTeam)



end)
```

Team Only Door

The following code sample will create a door in the Workspace that can only be
walked through by Players on the Bright red team.

```
local Players = game:GetService("Players")



local door = Instance.new("Part")



door.Anchored = true



door.Size = Vector3.new(7, 10, 1)



door.Position = Vector3.new(0, 5, 0)



door.Parent = workspace



local debounce = false



door.Touched:Connect(function(hit)



if not debounce then



debounce = true



if hit then



local player = Players:GetPlayerFromCharacter(hit.Parent)



if player and player.TeamColor == BrickColor.new("Bright red") then



door.Transparency = 0.5



door.CanCollide = false



task.wait(3)



door.Transparency = 0



door.CanCollide = true



end



end



task.wait(0.5)



debounce = false



end



end)
```

Team Kill Check

This code sample includes a quick function that can be added to weapons in a
place to prevent them from team killing. It will return false when the two
players are on different teams or if either of them is neutral.

```
local Players = game:GetService("Players")



function checkTeamKill(playerAttack, playerVictim)



if playerAttack.Team ~= playerVictim.Team or playerAttack.Neutral or playerVictim.Neutral then



return false



end



return true



end



local players = Players:GetPlayers()



checkTeamKill(players[1], players[2])
```

---

API Reference

Methods

GetTeams

Returns a table containing the game's [Team](/docs/reference/engine/classes/Team) objects. Will only
return [Team](/docs/reference/engine/classes/Team) objects that are parented to the [Teams](/docs/reference/engine/classes/Teams)
service.

Teams:GetTeams():Instances

Returns

Instances

An array of [Teams](/docs/reference/engine/classes/Team) in the game.

The GetTeam function returns a table containing the game's [Team](/docs/reference/engine/classes/Team)
objects.

Note this will only return Team objects that are directly parented to the
[Teams](/docs/reference/engine/classes/Teams) service. For this reason it is recommended developers only
parent [Team](/docs/reference/engine/classes/Team) objects to the [Teams](/docs/reference/engine/classes/Teams) service and not to other
[Instances](/docs/reference/engine/classes/Instance) (or to each other).

Code Samples

Teams GetTeams

The example below prints the number of players on each Team.

```
local Teams = game:GetService("Teams")



local teams = Teams:GetTeams()



for _, team in pairs(teams) do



local players = team:GetPlayers()



print("Team", team.Name, "has", #players, "players")



end
```

Provide feedback

---

RebalanceTeams

Deprecated

Show details

---