# Team | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Team
Scraped: 2026-01-11T02:39:27.517521Z

## Inherits
- Object
- Instance
- Team
- Teams
- Player
- Model
- Team.TeamColor
- Player.TeamColor
- Player.Team
- Player.Neutral
- Team.AutoAssignable
- SpawnLocation.Neutral
- SpawnLocation.TeamColor
- SpawnLocation
- SpawnLocation.AllowTeamChangeOnTouch
- Player.PartyId
- SocialService:GetPlayersByPartyId()
- Players
- SpawnLocations
- Tool
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Team](/docs/reference/engine/classes/Team)

English

Feedback

Engine Class

![Team](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Team-Dark.webp)Team

The [Team](/docs/reference/engine/classes/Team) class represents a faction in a Roblox place. The only valid
parent for a Team is in the [Teams](/docs/reference/engine/classes/Teams) service.

---

Summary

Properties

|  |
| --- |
| [AutoAssignable](#AutoAssignable):[boolean](/docs/luau/booleans) |
| [AutoColorCharacters](#AutoColorCharacters):[boolean](/docs/luau/booleans)  Deprecated |
| [Score](#Score):[number](/docs/luau/numbers)  Deprecated |
| [TeamColor](#TeamColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor) |

Methods

|  |
| --- |
| [GetPlayers](#GetPlayers)():Instances |

Events

|  |
| --- |
| [PlayerAdded](#PlayerAdded)(player: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PlayerRemoved](#PlayerRemoved)(player: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [Team](/docs/reference/engine/classes/Team) class represents a faction in a Roblox place. The only valid
parent for a Team is in the [Teams](/docs/reference/engine/classes/Teams) service. Teams offer a range of
features that are useful to developers that can be divided into two rough
groups:

* Features that work 'out of the box'
* Features developers can program into their game.

Built-in Team Behavior

The following functionality of Teams exists by default and does not require
the developer to program any custom behavior.

* When part of a Team, the name above a player's character [Model](/docs/reference/engine/classes/Model) will
  be colored to the [Team.TeamColor](/docs/reference/engine/classes/Team#TeamColor)
* Changing [Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) will cause [Player.Team](/docs/reference/engine/classes/Player#Team) to switch
  to the Team with the corresponding [Team.TeamColor](/docs/reference/engine/classes/Team#TeamColor)
* When using the default player list users will be grouped and displayed
  together as a team
* Setting [Player.Neutral](/docs/reference/engine/classes/Player#Neutral) to true will cause the [Player](/docs/reference/engine/classes/Player) to be
  disassociated with the team, but it will not change [Player.Team](/docs/reference/engine/classes/Player#Team) or
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

Optional Extended Team Behaviors

Many developers chose to add the following features to teams in their own
code.

* Implement checks in weapon code to prevent friendly fire.
* Implement checks in doors or other features that allow only certain teams to
  use them
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

Team Rebalance with Party Integration

This code sample demonstrates how to assign players to [Teams](/docs/reference/engine/classes/Team) based on their [Player.PartyId](/docs/reference/engine/classes/Player#PartyId) using the [SocialService:GetPlayersByPartyId()](/docs/reference/engine/classes/SocialService#GetPlayersByPartyId) method. When a player joins the experience, the script checks whether they're part of a party. If so, it attempts to assign them to the same team as other party members. If no match is found or the player isn't in a party, they're placed on the team with fewer members to maintain balance.

```
local Teams = game:GetService("Teams")



local Players = game:GetService("Players")



local SocialService = game:GetService("SocialService")



local redTeam = Instance.new("Team")



redTeam.Name = "Red Team"



redTeam.TeamColor = BrickColor.Red()



redTeam.AutoAssignable = false



redTeam.Parent = Teams



local blueTeam = Instance.new("Team")



blueTeam.Name = "Blue Team"



blueTeam.TeamColor = BrickColor.Blue()



blueTeam.AutoAssignable = false



blueTeam.Parent = Teams



local function assignPlayerToTeam(player)



local partyId = player.PartyId



if partyId == "" then



assignBalancedTeam(player)



return



end



local teams = { redTeam, blueTeam }



local matchingTeam = nil



local partyPlayers = SocialService:GetPlayersByPartyId(partyId)



for _, partyPlayer in partyPlayers do



if partyPlayer ~= player and table.find(teams, partyPlayer.Team) then



matchingTeam = partyPlayer.Team



break



end



end



if matchingTeam then



player.Team = matchingTeam



player.TeamColor = matchingTeam.TeamColor



else



assignBalancedTeam(player)



end



end



function assignBalancedTeam(player)



local redCount = #redTeam:GetPlayers()



local blueCount = #blueTeam:GetPlayers()



local chosenTeam = redCount <= blueCount and redTeam or blueTeam



player.Team = chosenTeam



player.TeamColor = chosenTeam.TeamColor



end



local function groupPlayersByParty()



local seenPartyIds = {}



local groupedPlayers = {}



for _, player in Players:GetPlayers() do



if player.PartyId == "" then



table.insert(groupedPlayers, { player })



elseif not table.find(seenPartyIds, player.PartyId) then



table.insert(seenPartyIds, player.PartyId)



local partyPlayers = SocialService:GetPlayersByPartyId(player.PartyId)



table.insert(groupedPlayers, partyPlayers)



end



end



return groupedPlayers



end



-- Call this function to rebalance teams



local function rebalanceTeams()



local groups = groupPlayersByParty()



table.sort(groups, function(a, b)



return #a > #b



end)



for _, player in Players:GetPlayers() do



player.Team = nil



end



for _, group in groups do



local redCount = #redTeam:GetPlayers()



local blueCount = #blueTeam:GetPlayers()



local bestTeam



if redCount <= blueCount then



bestTeam = redTeam



else



bestTeam = blueTeam



end



for _, player in group do



player.Team = bestTeam



player.TeamColor = bestTeam.TeamColor



end



end



for _, player in Players:GetPlayers() do



player:LoadCharacter()



end



end



Players.PlayerAdded:Connect(function(player)



assignPlayerToTeam(player)



player:LoadCharacter()



player:GetPropertyChangedSignal("PartyId"):Connect(function()



if player.PartyId ~= "" then



assignPlayerToTeam(player)



end



end)



end)
```

---

API Reference

Properties

AutoAssignable

Read Parallel

This property determines whether [Players](/docs/reference/engine/classes/Player) will be
automatically placed onto the [Team](/docs/reference/engine/classes/Team) when joining. If multiple teams
have this property set to true, Roblox will attempt to even the teams out
when [Players](/docs/reference/engine/classes/Player) are added.

Team.AutoAssignable:[boolean](/docs/luau/booleans)

This property determines whether [Players](/docs/reference/engine/classes/Player) will be
automatically placed onto the [Team](/docs/reference/engine/classes/Team) when joining. If multiple teams
have this property set to true, Roblox will attempt to even the teams out
when [Players](/docs/reference/engine/classes/Player) are added.

When a [Player](/docs/reference/engine/classes/Player) joins a game they will be assigned to the
[Team](/docs/reference/engine/classes/Team) with [Team.AutoAssignable](/docs/reference/engine/classes/Team#AutoAssignable) set to true that has the
fewest players. If no such team is available, [Player.Neutral](/docs/reference/engine/classes/Player#Neutral) will
be set to true.

Note while using this property will help even out teams when players are
added, it will not do anything when players are removed. For this reason
developers may wish to implement their own team balancing system.

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

Provide feedback

---

AutoColorCharacters

Deprecated

Show details

---

Score

Deprecated

Show details

---

TeamColor

Read Parallel

This property sets the color of the [Team](/docs/reference/engine/classes/Team). Determines the
[Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) property of players who are a member of the team.
Also determines the color displayed on the player list and above player's
heads.

Team.TeamColor:[BrickColor](/docs/reference/engine/datatypes/BrickColor)

This property sets the color of the [Team](/docs/reference/engine/classes/Team). Determines the
[Player.TeamColor](/docs/reference/engine/classes/Player#TeamColor) property of players who are a member of the team.

A lot of Roblox's default team functionality is based on the team color,
rather than the name or object. For example,
[SpawnLocations](/docs/reference/engine/classes/SpawnLocation) can be assigned to a team via
[SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor). For this reason it is recommended that
developers ensure each [Team](/docs/reference/engine/classes/Team) has a unique TeamColor.

Any player which is a part of a team will have their name color changed to
the team's TeamColor property. They will also be put underneath the team
heading on the player list.

Code Samples

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

Provide feedback

---

Methods

GetPlayers

Write Parallel

Returns a list of [Players](/docs/reference/engine/classes/Player) who are assigned to the
[Team](/docs/reference/engine/classes/Team). A [Player](/docs/reference/engine/classes/Player) is considered assigned if their
[Player.Team](/docs/reference/engine/classes/Player#Team) property is equal to the [Team](/docs/reference/engine/classes/Team) and
[Player.Neutral](/docs/reference/engine/classes/Player#Neutral) is false.

Team:GetPlayers():Instances

Returns

Instances

An array of [Players](/docs/reference/engine/classes/Player) in the [Team](/docs/reference/engine/classes/Team).

Returns a list of [Players](/docs/reference/engine/classes/Player) who are assigned to the
[Team](/docs/reference/engine/classes/Team). A [Player](/docs/reference/engine/classes/Player) is considered assigned if their
[Player.Team](/docs/reference/engine/classes/Player#Team) property is equal to the [Team](/docs/reference/engine/classes/Team) and
[Player.Neutral](/docs/reference/engine/classes/Player#Neutral) is false.

This function has a number of potential uses, including counting the
number of players on a [Team](/docs/reference/engine/classes/Team) or giving every [Player](/docs/reference/engine/classes/Player) on a
[Team](/docs/reference/engine/classes/Team) a [Tool](/docs/reference/engine/classes/Tool).

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

Events

PlayerAdded

Fires whenever a [Player](/docs/reference/engine/classes/Player) is assigned to the [Team](/docs/reference/engine/classes/Team). A player
is considered assigned if their [Player.Team](/docs/reference/engine/classes/Player#Team) property is equal to
the [Team](/docs/reference/engine/classes/Team) and [Player.Neutral](/docs/reference/engine/classes/Player#Neutral) is false.

Team.PlayerAdded(player:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) that was added. |

Fires whenever a [Player](/docs/reference/engine/classes/Player) is assigned to the [Team](/docs/reference/engine/classes/Team). A player
is considered assigned if their [Player.Team](/docs/reference/engine/classes/Player#Team) property is equal to
the [Team](/docs/reference/engine/classes/Team) and [Player.Neutral](/docs/reference/engine/classes/Player#Neutral) is false.

This event is team specific and will only fire when a [Player](/docs/reference/engine/classes/Player)
joints the specific [Team](/docs/reference/engine/classes/Team). Any function connected to this event
will be passed the [Player](/docs/reference/engine/classes/Player) object of the player who joined the
team. For example:

```
Team.PlayerAdded:Connect(function(player)



print(player.Name.." has joined the team")



end)
```

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

Provide feedback

---

PlayerRemoved

Fires whenever a [Player](/docs/reference/engine/classes/Player) is removed from a [Team](/docs/reference/engine/classes/Team). This can
be due to the [Player](/docs/reference/engine/classes/Player) leaving the game, [Player.Neutral](/docs/reference/engine/classes/Player#Neutral)
being set to true or the [Player](/docs/reference/engine/classes/Player) joining a different team.

Team.PlayerRemoved(player:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) removed. |

Fires whenever a [Player](/docs/reference/engine/classes/Player) is removed from a [Team](/docs/reference/engine/classes/Team). This can
be due to the [Player](/docs/reference/engine/classes/Player) leaving the game, [Player.Neutral](/docs/reference/engine/classes/Player#Neutral)
being set to true or the [Player](/docs/reference/engine/classes/Player) joining a different team.

This event is team specific and will only fire when a [Player](/docs/reference/engine/classes/Player)
leaves the specific [Team](/docs/reference/engine/classes/Team). Any function connected to this event
will be passed the [Player](/docs/reference/engine/classes/Player) object of the player who left the team.
For example:

```
Team.PlayerRemoved:Connect(function(player)



print(player.Name.." has left the team")



end)
```

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

Provide feedback

---