# SocialService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SocialService
Scraped: 2026-01-11T02:38:26.457911Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- SocialService
- Player
- PromptGameInvite()
- PromptPhoneBook()
- LocalScript
- GuiButton
- CanSendCallInviteAsync()
- Activated
- Player.UserId
- CanSendGameInviteAsync()
- PromptRsvpToEventAsync()
- Script
- RunContext
- ProximityPrompts
- DataModel.PlaceId
- DataModel.JobId
- DataModel.PrivateServerId
- TeleportService:TeleportAsync()
- SocialService:GetPartyAsync()
- Player.PartyId
- Players:GetPlayers()
- SocialService:GetPlayersByPartyId()
- Teams
- GetExperienceEventAsync()
- ExperienceInviteOptions
- Player:GetJoinData()
- CallInviteStateChanged
- GetEventRsvpStatusAsync()
- TeleportService:ReserveServer()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [SocialService](/docs/reference/engine/classes/SocialService)

English

Feedback

Engine Class

![SocialService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SocialService-Dark.webp)SocialService

Facilitates social functions that impact relationships made on the Roblox
platform.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [CanSendCallInviteAsync](#CanSendCallInviteAsync)(player: [Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans) |
| [CanSendGameInviteAsync](#CanSendGameInviteAsync)(player: [Instance](/docs/reference/engine/datatypes/Instance),recipientId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [GetEventRsvpStatusAsync](#GetEventRsvpStatusAsync)(eventId: [string](/docs/luau/strings)):[Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus) |
| [GetExperienceEventAsync](#GetExperienceEventAsync)(eventId: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries)? |
| [GetPartyAsync](#GetPartyAsync)(partyId: [string](/docs/luau/strings)):[Array](/docs/luau/tables#arrays) |
| [GetPlayersByPartyId](#GetPlayersByPartyId)(partyId: [string](/docs/luau/strings)):Instances |
| [GetUpcomingExperienceEventsAsync](#GetUpcomingExperienceEventsAsync)():[Array](/docs/luau/tables#arrays) |
| [HideSelfView](#HideSelfView)():() |
| [PromptFeedbackSubmissionAsync](#PromptFeedbackSubmissionAsync)():() |
| [PromptGameInvite](#PromptGameInvite)(player: [Instance](/docs/reference/engine/datatypes/Instance),experienceInviteOptions: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [PromptLinkSharingAsync](#PromptLinkSharingAsync)(player: [Player](/docs/reference/engine/classes/Player),options: [Dictionary](/docs/luau/tables#dictionaries)):[Tuple](/docs/luau/tuples) |
| [PromptLinkSharing](#PromptLinkSharing)(player: [Player](/docs/reference/engine/classes/Player),options: [Dictionary](/docs/luau/tables#dictionaries)):[Tuple](/docs/luau/tuples)  Deprecated |
| [PromptPhoneBook](#PromptPhoneBook)(player: [Instance](/docs/reference/engine/datatypes/Instance),tag: [string](/docs/luau/strings)):() |
| [PromptRsvpToEventAsync](#PromptRsvpToEventAsync)(eventId: [string](/docs/luau/strings)):[Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus) |
| [ShowSelfView](#ShowSelfView)(selfViewPosition: [Enum.SelfViewPosition](/docs/reference/engine/enums/SelfViewPosition)):() |

Events

|  |
| --- |
| [CallInviteStateChanged](#CallInviteStateChanged)(player: [Instance](/docs/reference/engine/datatypes/Instance),inviteState: [Enum.InviteState](/docs/reference/engine/enums/InviteState)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GameInvitePromptClosed](#GameInvitePromptClosed)(player: [Instance](/docs/reference/engine/datatypes/Instance),recipientIds: [Array](/docs/luau/tables#arrays)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PhoneBookPromptClosed](#PhoneBookPromptClosed)(player: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ShareSheetClosed](#ShareSheetClosed)(player: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Callbacks

|  |
| --- |
| [OnCallInviteInvoked](#OnCallInviteInvoked)(tag: [string](/docs/luau/strings),callParticipantIds: [Array](/docs/luau/tables#arrays)):[Instance](/docs/reference/engine/datatypes/Instance) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

SocialService facilitates social functions that impact relationships made
on the Roblox platform. Its primary usage is to show
[invite prompts](/docs/production/promotion/invite-prompts) and the
phone book to players, allowing them to send invitation requests to their
connections through
[PromptGameInvite()](/docs/reference/engine/classes/SocialService#PromptGameInvite) and
[PromptPhoneBook()](/docs/reference/engine/classes/SocialService#PromptPhoneBook) respectively. You
may leverage signals when such requests are made.

---

API Reference

Methods

CanSendCallInviteAsync

Yields

Indicates whether the given [Player](/docs/reference/engine/classes/Player) can invite other players to a
call.

SocialService:CanSendCallInviteAsync(player:[Instance](/docs/reference/engine/datatypes/Instance)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) instance of the player potentially sending a call invite. |

Returns

[boolean](/docs/luau/booleans)

Whether the specified player can send a call invite.

Returns true if the given [Player](/docs/reference/engine/classes/Player) can send a call invite to a
connection. You should always use the result of this method before calling
[PromptPhoneBook()](/docs/reference/engine/classes/SocialService#PromptPhoneBook) since the
ability to open the phone book may vary depending on the player.

See [Roblox Connect](/docs/resources/roblox-connect) for a sample
implementation of this method.

Code Samples

SocialService:PromptPhoneBook()

The following code sample, placed within a child [LocalScript](/docs/reference/engine/classes/LocalScript) of a [GuiButton](/docs/reference/engine/classes/GuiButton), uses [CanSendCallInviteAsync()](/docs/reference/engine/classes/SocialService#CanSendCallInviteAsync) to confirm that the player can make a call. If so, it connects [PromptPhoneBook()](/docs/reference/engine/classes/SocialService#PromptPhoneBook) to the button's [Activated](/docs/reference/engine/classes/GuiButton#Activated) event.

```
local Players = game:GetService("Players")



local SocialService = game:GetService("SocialService")



local player = Players.LocalPlayer



local button = script.Parent



button.Visible = false



-- Function to check whether the player can send a call invite



local function canSendCallingInvite(sendingPlayer)



local success, canSend = pcall(function()



return SocialService:CanSendCallInviteAsync(sendingPlayer)



end)



return success and canSend



end



local canCall = canSendCallingInvite(player)



if canCall then



button.Visible = true



button.Activated:Connect(function()



SocialService:PromptPhoneBook(player, "")



end)



end
```

Provide feedback

---

CanSendGameInviteAsync

Yields

Indicates whether the given [Player](/docs/reference/engine/classes/Player) can invite other players.

SocialService:CanSendGameInviteAsync(

player:[Instance](/docs/reference/engine/datatypes/Instance), recipientId:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) instance of the player potentially sending an invite. |
| recipientId:[number](/docs/luau/numbers) Default Value: 0 Optional [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the potential recipient, used to check whether the sender can invite that specific recipient. |

Returns

[boolean](/docs/luau/booleans)

Whether the specified player can send an invite.

[CanSendGameInviteAsync()](/docs/reference/engine/classes/SocialService#CanSendGameInviteAsync)
returns true if the given [Player](/docs/reference/engine/classes/Player) can invite other players to the
current experience. You should always use the result of this method before
calling [PromptGameInvite()](/docs/reference/engine/classes/SocialService#PromptGameInvite) since
the ability to invite players may vary depending on the platform or
player.

See
[Player Invite Prompts](/docs/production/promotion/invite-prompts)
for more details on implementing player invite prompts, customizing
prompts and notifications, and using launch data.

Code Samples

Sending an Invite

The following code sample uses
[CanSendGameInviteAsync()](/docs/reference/engine/classes/SocialService#CanSendGameInviteAsync) to
confirm whether the local [Player](/docs/reference/engine/classes/Player) can send an invite. If true, it
then prompts the invite using
[PromptGameInvite()](/docs/reference/engine/classes/SocialService#PromptGameInvite).

```
local SocialService = game:GetService("SocialService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



-- Function to check whether the player can send an invite



local function canSendGameInvite(sendingPlayer)



local success, canSend = pcall(function()



return SocialService:CanSendGameInviteAsync(sendingPlayer)



end)



return success and canSend



end



local canInvite = canSendGameInvite(player)



if canInvite then



SocialService:PromptGameInvite(player)



end
```

Provide feedback

---

GetEventRsvpStatusAsync

Yields

Returns the local player's RSVP status for the given event.

SocialService:GetEventRsvpStatusAsync(eventId:[string](/docs/luau/strings)):[Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus)

Parameters

|  |
| --- |
| eventId:[string](/docs/luau/strings)  The event ID of the event to prompt the player to change their RSVP status for. This must be a valid event ID that exists in the current experience, represented as a string (not a number). |

Returns

[Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus)

Returns an [Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus) indicating the player's current RSVP
status for the event. If the player has not RSVP'd to the event, this
will return [Enum.RsvpStatus.None](/docs/reference/engine/enums/RsvpStatus#None).

Returns the local player's RSVP status for the given event. Events must be
in the current experience and must not have already started. If the event
has already started, this method will return an error.

Note that you can use
[PromptRsvpToEventAsync()](/docs/reference/engine/classes/SocialService#PromptRsvpToEventAsync) to
prompt the player to change their RSVP status for the event.

Code Samples

SocialService:PromptRsvpToEventAsync()

The following example checks if a player is RSVP'd to an event; if not, it gives them the option to RSVP. If the player is already RSVP'd, it gives them the option to cancel their RSVP.

The following [Script](/docs/reference/engine/classes/Script) assumes that [RunContext](/docs/reference/engine/classes/BaseScript#RunContext) is set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client) and that two sibling [ProximityPrompts](/docs/reference/engine/classes/ProximityPrompt) are in place: one for following the event and one for unfollowing the event. The prompts are enabled or disabled based on the player's RSVP status.

```
local SocialService = game:GetService("SocialService")



local EVENT_ID = "YOUR_EVENT_ID"



local followPrompt: ProximityPrompt = script.Parent.FollowProximityPrompt



local unFollowPrompt: ProximityPrompt = script.Parent.UnfollowProximityPrompt



local function updatePrompt(rsvpStatus: Enum.RsvpStatus)



if rsvpStatus == Enum.RsvpStatus.Going then



unFollowPrompt.Enabled = true



followPrompt.Enabled = false



else



unFollowPrompt.Enabled = false



followPrompt.Enabled = true



end



end



local success, currentRsvpStatus = pcall(function()



return SocialService:GetEventRsvpStatusAsync(EVENT_ID)



end)



if not success then



-- Could not retrieve RSVP status; don't enable either proximity prompt



warn("Failed to get RSVP status:", currentRsvpStatus)



return



end



print("CurrentRsvpStatus:", currentRsvpStatus)



updatePrompt(currentRsvpStatus)



unFollowPrompt.Triggered:Connect(function(player)



local rsvpStatus = SocialService:PromptRsvpToEventAsync(EVENT_ID)



updatePrompt(rsvpStatus)



end)



followPrompt.Triggered:Connect(function(player)



local rsvpStatus = SocialService:PromptRsvpToEventAsync(EVENT_ID)



updatePrompt(rsvpStatus)



end)
```

Provide feedback

---

GetExperienceEventAsync

Yields

Returns details for the specified experience event or nil if it is
unavailable.

SocialService:GetExperienceEventAsync(eventId:[string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries)?

Parameters

|  |
| --- |
| eventId:[string](/docs/luau/strings)  The string identifier of the event to retrieve. Must correspond to an event in the current experience. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)?

A dictionary describing the event, or nil if the event does not
exist, belongs to another experience, or is otherwise unavailable.

GetExperienceEventAsync() yields until the request completes and then
returns a dictionary describing the requested event. The dictionary
contains the following fields:

* Id (string)
* Title (string)
* Description (string)
* StartTime (dictionary)
  + Day (number)
  + Year (number)
  + Month (number)
  + Minute (number)
  + Millisecond (number)
  + Hour (number)
  + Second (number)
* EndTime (dictionary)
  + Day (number)
  + Year (number)
  + Month (number)
  + Minute (number)
  + Millisecond (number)
  + Hour (number)
  + Second (number)
* HasStarted (boolean)
* HasEnded (boolean)
* Status ([Enum.ExperienceEventStatus](/docs/reference/engine/enums/ExperienceEventStatus))
* UserRsvpStatus ([Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus) or nil)

If the event cannot be found, belongs to a different experience, or the
response is malformed, this method returns nil. Requests may also fail
with a HttpError <status> message if the service returns an unexpected
error code.

Code Samples

SocialService:GetUpcomingExperienceEventsAsync()

Finds the next event that has not started and prompts the player to RSVP. This avoids hardcoded IDs by discovering events at runtime.

```
local SocialService = game:GetService("SocialService")



-- Discover the next upcoming/active event and prompt the player to RSVP



local function promptNextUpcomingEvent()



local success, eventsOrError = pcall(function()



return SocialService:GetUpcomingExperienceEventsAsync()



end)



if not success then



warn("Failed to load upcoming events:", eventsOrError)



return



end



local upcomingEvents = eventsOrError



local selectedEvent



for _, event in ipairs(upcomingEvents) do



if not event.HasStarted and not event.HasEnded then



selectedEvent = event



break



end



end



if selectedEvent then



local success, result = pcall(function()



return SocialService:PromptRsvpToEventAsync(selectedEvent.Id)



end)



if not success then



warn("RSVP prompt failed:", result)



end



else



warn("No future events available to prompt.")



return



end



end



promptNextUpcomingEvent()
```

Provide feedback

---

GetPartyAsync

Yields

Returns an array of dictionaries containing data for all members of the
specified party who are currently in the experience.

SocialService:GetPartyAsync(partyId:[string](/docs/luau/strings)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| partyId:[string](/docs/luau/strings) |

Returns

[Array](/docs/luau/tables#arrays)

An array of dictionaries representing the members of the specified
party who are currently in the experience.

Returns an array of dictionaries containing data for all members
associated with the given partyId. The returned array reflects the
current state of the party across all active server instances within the
experience and it is ordered by the time each party member accepted the
party invite. This means the first element in the array is the earliest to
accept and the last is the most recent.

This method is useful for retrieving up-to-date information about all
party members currently in the experience and across different servers,
enabling coordinated group behavior such as teleportation, matchmaking, or
party-based gameplay logic.

Each dictionary in the returned array contains the following fields:

| Key | Value Type | Description |
| --- | --- | --- |
| UserId | number | The player's [Player.UserId](/docs/reference/engine/classes/Player#UserId) property. |
| PlaceId | number | The [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the place the party member is currently in. |
| JobId | string | The [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of the server instance the user currently resides in. |
| PrivateServerId | string | If applicable, the [DataModel.PrivateServerId](/docs/reference/engine/classes/DataModel#PrivateServerId) when the party member is in a private or reserved server. |
| ReservedServerAccessCode | string | If applicable, the access code for the reserved server that the user currently resides in. Useful for teleporting party members to each other using [TeleportService:TeleportAsync()](/docs/reference/engine/classes/TeleportService#TeleportAsync). |

To test this service in your experience, use the
[Party Simulator](/docs/studio/testing-modes#party-simulation) in
Roblox Studio or publish the experience and play it in the Roblox
application.

Code Samples

SocialService:GetPartyAsync()

The following example checks if a player is in a party when they join. If so, it retrieves the latest party data using [SocialService:GetPartyAsync()](/docs/reference/engine/classes/SocialService#GetPartyAsync) and outputs the details of each party member.

```
local SocialService = game:GetService("SocialService")



local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



local partyId = player.PartyId



if partyId == "" then



warn("Player is not in a party")



return



end



local success, partyData = pcall(function()



return SocialService:GetPartyAsync(partyId)



end)



if success and partyData then



for _, partyMemberData in partyData do



print(



partyMemberData.UserId,



partyMemberData.PlaceId,



partyMemberData.JobId,



partyMemberData.PrivateServerId,



partyMemberData.ReservedServerAccessCode



)



end



else



warn("Failed to retrieve party data")



end



end)
```

Provide feedback

---

GetPlayersByPartyId

Returns a table of all presently connected [Player](/docs/reference/engine/classes/Player) objects whose
[Player.PartyId](/docs/reference/engine/classes/Player#PartyId) property matches the passed partyId.

SocialService:GetPlayersByPartyId(partyId:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| partyId:[string](/docs/luau/strings) |

Returns

Instances

A table of [Player](/docs/reference/engine/classes/Player) objects whose [Player.PartyId](/docs/reference/engine/classes/Player#PartyId)
property matches the passed partyId.

Returns a table of all presently connected [Player](/docs/reference/engine/classes/Player) objects whose
[Player.PartyId](/docs/reference/engine/classes/Player#PartyId) property matches the provided partyId. This
method behaves similarly to [Players:GetPlayers()](/docs/reference/engine/classes/Players#GetPlayers) but filters the
results to include only those players belonging to the specified party.

To test this service in your experience, use the
[Party Simulator](/docs/studio/testing-modes#party-simulation) in
Roblox Studio or publish the experience and play it in the Roblox
application.

Code Samples

SocialService:GetPlayersByPartyId()

The following example listens for when a player joins the experience. If the player is part of a party, it uses [SocialService:GetPlayersByPartyId()](/docs/reference/engine/classes/SocialService#GetPlayersByPartyId) to retrieve all players in the same party who are currently connected to the server. It then outputs the name of each party member.

```
local SocialService = game:GetService("SocialService")



local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



local partyId = player.PartyId



if partyId ~= "" then



local partyPlayers: { Player } = SocialService:GetPlayersByPartyId(partyId)



for _, partyMember in partyPlayers do



print("Party Member: " .. partyMember.Name)



end



else



warn("Player is not in a party")



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

Provide feedback

---

GetUpcomingExperienceEventsAsync

Yields

Returns active and upcoming experience events for the current experience.

SocialService:GetUpcomingExperienceEventsAsync():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of dictionaries describing each active or upcoming event in
the current experience, ordered by soonest start time first.

GetUpcomingExperienceEventsAsync() yields while the client requests data
for the current experience and then returns an array of dictionaries, each
with the same structure described in
[GetExperienceEventAsync()](/docs/reference/engine/classes/SocialService#GetExperienceEventAsync).
The array includes only events that are currently active or have not yet
ended, excluding cancelled, moderated, or unpublished events. Results are
sorted so the soonest start time appears first.

If the service indicates there are no matching events, this method returns
an empty array. Requests may raise a HttpError <status> message if the
service returns an unexpected error code.

Code Samples

SocialService:GetUpcomingExperienceEventsAsync()

Finds the next event that has not started and prompts the player to RSVP. This avoids hardcoded IDs by discovering events at runtime.

```
local SocialService = game:GetService("SocialService")



-- Discover the next upcoming/active event and prompt the player to RSVP



local function promptNextUpcomingEvent()



local success, eventsOrError = pcall(function()



return SocialService:GetUpcomingExperienceEventsAsync()



end)



if not success then



warn("Failed to load upcoming events:", eventsOrError)



return



end



local upcomingEvents = eventsOrError



local selectedEvent



for _, event in ipairs(upcomingEvents) do



if not event.HasStarted and not event.HasEnded then



selectedEvent = event



break



end



end



if selectedEvent then



local success, result = pcall(function()



return SocialService:PromptRsvpToEventAsync(selectedEvent.Id)



end)



if not success then



warn("RSVP prompt failed:", result)



end



else



warn("No future events available to prompt.")



return



end



end



promptNextUpcomingEvent()
```

Provide feedback

---

HideSelfView

Hides the calling player's self view.

SocialService:HideSelfView():()

Returns

()

Hides the calling player's self view. If this method is called while the
self view is already hidden, it does nothing.

Provide feedback

---

PromptFeedbackSubmissionAsync

Yields

Prompts the player to submit feedback about the current experience.

SocialService:PromptFeedbackSubmissionAsync():()

Returns

()

Displays a feedback submission dialog to the player, allowing them to
provide feedback about their experience. The submitted feedback becomes
available to developers in the Creator Dashboard under the Audience >
Feedback section.

Players can submit feedback once per day per experience. Experience owners
cannot submit feedback for their own experiences. If the player has
already submitted feedback for the day, owns the experience, or is
otherwise ineligible, the prompt will display a message indicating that
feedback is unavailable.

This method yields until the player either submits feedback or dismisses
the dialog. As an asynchronous operation, it should be called using
task.spawn() or within a coroutine.

Note that this service does not work during playtesting in Roblox Studio.
To test the feedback prompt, you must publish the experience and play it
in the Roblox application.

Code Samples

SocialService:PromptFeedbackSubmissionAsync()

The following example shows how to prompt players for feedback at appropriate moments in your experience, such as after reaching a milestone or completing a level.

```
local SocialService = game:GetService("SocialService")



-- Function to prompt for feedback



local function promptForFeedback()



local success, errorMessage = pcall(function()



SocialService:PromptFeedbackSubmissionAsync()



end)



if success then



print("Feedback prompt completed")



else



warn("Failed to prompt for feedback:", errorMessage)



end



end



-- Prompt for feedback when player reaches a milestone



local function onMilestoneReached()



promptForFeedback()



end



-- Example usage: Connect to a game event



game.ReplicatedStorage.MilestoneReached.OnClientEvent:Connect(onMilestoneReached)
```

Provide feedback

---

PromptGameInvite

Prompts the given [Player](/docs/reference/engine/classes/Player) with the invite screen.

SocialService:PromptGameInvite(

player:[Instance](/docs/reference/engine/datatypes/Instance), experienceInviteOptions:[Instance](/docs/reference/engine/datatypes/Instance)

):()

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) to prompt with the invite popup. |
| experienceInviteOptions:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" Optional [ExperienceInviteOptions](/docs/reference/engine/classes/ExperienceInviteOptions) object for customizing the prompt. |

Returns

()

[PromptGameInvite()](/docs/reference/engine/classes/SocialService#PromptGameInvite) displays an
invite prompt to the local player through which they may invite their
connections to the current experience. Before calling this method, you
should use
[CanSendGameInviteAsync()](/docs/reference/engine/classes/SocialService#CanSendGameInviteAsync) to
determine whether the player can send an invite, as this ability may vary
depending on the platform or player.

See
[Player Invite Prompts](/docs/production/promotion/invite-prompts)
for more details on implementing invite prompts, customizing prompts and
notifications, and using launch data.

Code Samples

Sending an Invite

The following code sample uses
[CanSendGameInviteAsync()](/docs/reference/engine/classes/SocialService#CanSendGameInviteAsync) to
confirm whether the local [Player](/docs/reference/engine/classes/Player) can send an invite. If true, it
then prompts the invite using
[PromptGameInvite()](/docs/reference/engine/classes/SocialService#PromptGameInvite).

```
local SocialService = game:GetService("SocialService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



-- Function to check whether the player can send an invite



local function canSendGameInvite(sendingPlayer)



local success, canSend = pcall(function()



return SocialService:CanSendGameInviteAsync(sendingPlayer)



end)



return success and canSend



end



local canInvite = canSendGameInvite(player)



if canInvite then



SocialService:PromptGameInvite(player)



end
```

Provide feedback

---

PromptLinkSharingAsync

Yields

SocialService:PromptLinkSharingAsync(

player:[Player](/docs/reference/engine/classes/Player), options:[Dictionary](/docs/luau/tables#dictionaries)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  Prompts the given [Player](/docs/reference/engine/classes/Player) with a Roblox platform-level share sheet with a generated share link. |
| options:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Dictionary that specifies the configuration for the generated link. It includes the following optional key-value pairs:   * FallbackLinkId (string). Determines how this share link will   direct player to once expired. Default to experience join link. * ExpirationSeconds (number). Determines time to expiration once the   share link is created. Truncates to nearest integer. Defaults to   86,400. * PreviewTitle (string) Preview title of the share link. * PreviewDescription (string) Preview description of the share link. * PreviewAssetId (number) Image asset ID used for share link   preview. * LaunchData (string). Used to set a parameter in   [Player:GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData) when a player joined using the   generated share link. |

Returns

[Tuple](/docs/luau/tuples)

A tuple containing an Enum.PromptLinkSharingResult indicating the
result of the link sharing prompt.

This call is restricted to server scripts. After a link is successfully
generated, the target player will either be prompted to open a share sheet
with the generated link, or the link will be copied directly to the
clipboard if share sheet functionality is not available to the player.

```
local HttpService = game:GetService("HttpService")



local SocialService = game:GetService("SocialService")



local success, result  = pcall(function()



local data = {



promoCode = "j7du67"



}



local launchData = HttpService:JSONEncode(data)



local LinkSharingOptions = {



ExpirationSeconds = 20000,



PreviewTitle = "Awesome Game",



PreviewDescription = "Lets play together",



LaunchData = launchData,



}



return SocialService:PromptLinkSharing(player, LinkSharingOptions)



end)



if not success or result ~= Enum.PromptLinkSharingResult.Success then



warn("PromptLinkSharing failed:", tostring(result))



end
```

Provide feedback

---

PromptLinkSharing

Deprecated

Show details

---

PromptPhoneBook

Prompts the given [Player](/docs/reference/engine/classes/Player) with the phone book.

SocialService:PromptPhoneBook(

player:[Instance](/docs/reference/engine/datatypes/Instance), tag:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The player to prompt with the phone book. |
| tag:[string](/docs/luau/strings)  String to help differentiate between various phone book "entry points" or similar. For example, you can pass a string defining what region of an experience the calling player's character is currently in. |

Returns

()

Prompts the given [Player](/docs/reference/engine/classes/Player) with the phone book. If the player
chooses to call someone, the
[CallInviteStateChanged](/docs/reference/engine/classes/SocialService#CallInviteStateChanged) event
fires. You should use
[CanSendCallInviteAsync()](/docs/reference/engine/classes/SocialService#CanSendCallInviteAsync)
prior to calling [PromptPhoneBook()](/docs/reference/engine/classes/SocialService#PromptPhoneBook)
since the ability to see the phone book may vary depending on the player.

If a player is not eligible to open the phone book, an error dialog is
shown.

See [Roblox Connect](/docs/resources/roblox-connect) for a sample
implementation of this method.

Code Samples

SocialService:PromptPhoneBook()

The following code sample, placed within a child [LocalScript](/docs/reference/engine/classes/LocalScript) of a [GuiButton](/docs/reference/engine/classes/GuiButton), uses [CanSendCallInviteAsync()](/docs/reference/engine/classes/SocialService#CanSendCallInviteAsync) to confirm that the player can make a call. If so, it connects [PromptPhoneBook()](/docs/reference/engine/classes/SocialService#PromptPhoneBook) to the button's [Activated](/docs/reference/engine/classes/GuiButton#Activated) event.

```
local Players = game:GetService("Players")



local SocialService = game:GetService("SocialService")



local player = Players.LocalPlayer



local button = script.Parent



button.Visible = false



-- Function to check whether the player can send a call invite



local function canSendCallingInvite(sendingPlayer)



local success, canSend = pcall(function()



return SocialService:CanSendCallInviteAsync(sendingPlayer)



end)



return success and canSend



end



local canCall = canSendCallingInvite(player)



if canCall then



button.Visible = true



button.Activated:Connect(function()



SocialService:PromptPhoneBook(player, "")



end)



end
```

Provide feedback

---

PromptRsvpToEventAsync

Yields

Prompts the local [Player](/docs/reference/engine/classes/Player) with a prompt to change their RSVP status
to the given event.

SocialService:PromptRsvpToEventAsync(eventId:[string](/docs/luau/strings)):[Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus)

Parameters

|  |
| --- |
| eventId:[string](/docs/luau/strings)  The event ID of the event to prompt the player to change their RSVP status for. This must be a valid event ID that exists in the current experience, represented as a string (not a number). |

Returns

[Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus)

Returns a [Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus) indicating the player's new RSVP status
after the prompt is closed. If the player closes the prompt without
changing their RSVP status, this will return [Enum.RsvpStatus.None](/docs/reference/engine/enums/RsvpStatus#None) or
their old [Enum.RsvpStatus](/docs/reference/engine/enums/RsvpStatus) if they had already selected a status.

PromptRsvpToEventAsync() displays a prompt to the local player through
which they may change their RSVP status to the given event.

Events must be in the current experience and must not have already
started. If the event has already started, this method will return an
error.

Note that you can use
[GetEventRsvpStatusAsync()](/docs/reference/engine/classes/SocialService#GetEventRsvpStatusAsync)
to check the player's current RSVP status before calling this method.

Code Samples

SocialService:PromptRsvpToEventAsync()

The following example checks if a player is RSVP'd to an event; if not, it gives them the option to RSVP. If the player is already RSVP'd, it gives them the option to cancel their RSVP.

The following [Script](/docs/reference/engine/classes/Script) assumes that [RunContext](/docs/reference/engine/classes/BaseScript#RunContext) is set to [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client) and that two sibling [ProximityPrompts](/docs/reference/engine/classes/ProximityPrompt) are in place: one for following the event and one for unfollowing the event. The prompts are enabled or disabled based on the player's RSVP status.

```
local SocialService = game:GetService("SocialService")



local EVENT_ID = "YOUR_EVENT_ID"



local followPrompt: ProximityPrompt = script.Parent.FollowProximityPrompt



local unFollowPrompt: ProximityPrompt = script.Parent.UnfollowProximityPrompt



local function updatePrompt(rsvpStatus: Enum.RsvpStatus)



if rsvpStatus == Enum.RsvpStatus.Going then



unFollowPrompt.Enabled = true



followPrompt.Enabled = false



else



unFollowPrompt.Enabled = false



followPrompt.Enabled = true



end



end



local success, currentRsvpStatus = pcall(function()



return SocialService:GetEventRsvpStatusAsync(EVENT_ID)



end)



if not success then



-- Could not retrieve RSVP status; don't enable either proximity prompt



warn("Failed to get RSVP status:", currentRsvpStatus)



return



end



print("CurrentRsvpStatus:", currentRsvpStatus)



updatePrompt(currentRsvpStatus)



unFollowPrompt.Triggered:Connect(function(player)



local rsvpStatus = SocialService:PromptRsvpToEventAsync(EVENT_ID)



updatePrompt(rsvpStatus)



end)



followPrompt.Triggered:Connect(function(player)



local rsvpStatus = SocialService:PromptRsvpToEventAsync(EVENT_ID)



updatePrompt(rsvpStatus)



end)
```

Provide feedback

---

ShowSelfView

Shows the calling player's self view.

SocialService:ShowSelfView(selfViewPosition:[Enum.SelfViewPosition](/docs/reference/engine/enums/SelfViewPosition)):()

Parameters

|  |
| --- |
| selfViewPosition:[Enum.SelfViewPosition](/docs/reference/engine/enums/SelfViewPosition) Default Value: "LastPosition" The position to place the self view . |

Returns

()

Shows the calling player's self view. If this method is called while the
self view is already visible, it does nothing.

Provide feedback

---

Events

CallInviteStateChanged

Fires when a player's call invite state changes.

SocialService.CallInviteStateChanged(

player:[Instance](/docs/reference/engine/datatypes/Instance), inviteState:[Enum.InviteState](/docs/reference/engine/enums/InviteState)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) instance of the player who had a call invite state change. |
| inviteState:[Enum.InviteState](/docs/reference/engine/enums/InviteState)  The new call invite state. |

This event fires when a player's call invite state changes.

Code Samples

SocialService.CallInviteStateChanged

```
local SocialService = game:GetService("SocialService")



local button = script.Parent



local isPhonebookOpen = false



SocialService.CallInviteStateChanged:Connect(function(_, inviteState)



local isCalling = inviteState == Enum.InviteState.Placed



if isCalling or isPhonebookOpen then



button.Visible = false



else



button.Visible = true



end



end)
```

Provide feedback

---

GameInvitePromptClosed

Fires when a player closes an invite prompt.

SocialService.GameInvitePromptClosed(

player:[Instance](/docs/reference/engine/datatypes/Instance), recipientIds:[Array](/docs/luau/tables#arrays)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) instance of the player who closed the prompt. |
| recipientIds:[Array](/docs/luau/tables#arrays)  No longer populated; an empty array. |

This event fires when a player closes an invite prompt.

Provide feedback

---

PhoneBookPromptClosed

Fires when a player closes the phone book prompt.

SocialService.PhoneBookPromptClosed(player:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) instance of the player who closed the phone book. |

Fires when a player closes the phone book prompt.

Provide feedback

---

ShareSheetClosed

SocialService.ShareSheetClosed(player:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player) |

Provide feedback

---

Callbacks

OnCallInviteInvoked

Callback for when a call is placed from the phone book.

SocialService.OnCallInviteInvoked(

tag:[string](/docs/luau/strings), callParticipantIds:[Array](/docs/luau/tables#arrays)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| tag:[string](/docs/luau/strings)  String to help differentiate between various phone book entry points. |
| callParticipantIds:[Array](/docs/luau/tables#arrays)  Array containing all of the players involved in the call. The caller will always be the first player in the array. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Table including the PlaceId and ReservedServerAccessCode keys
whose values are the [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) and the server access
code returned by [TeleportService:ReserveServer()](/docs/reference/engine/classes/TeleportService#ReserveServer),
respectively.

A callback to process when a call is placed from the phone book. The tag
parameter can be used to differentiate between different "entry points" or
similar, as described in
[PromptPhoneBook()](/docs/reference/engine/classes/SocialService#PromptPhoneBook). Only one
callback can be set.

Code Samples

SocialService.OnCallInviteInvoked

```
local SocialService = game:GetService("SocialService")



local TeleportService = game:GetService("TeleportService")



SocialService.OnCallInviteInvoked = function()



local placeId = 0123456789 -- This is the place ID of the desired place to drop call participants into



local accessCode = TeleportService:ReserveServer(placeId)



return { ReservedServerAccessCode = accessCode, PlaceId = placeId }



end
```

Provide feedback

---