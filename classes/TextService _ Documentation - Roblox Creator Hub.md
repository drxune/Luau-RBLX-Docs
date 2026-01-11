# TextService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextService
Scraped: 2026-01-11T02:41:59.459134Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- TextService
- TextFilterTranslatedResult
- TextFilterResult
- GetTextBoundsParams
- TextService:GetTextSize()
- TextService:FilterStringAsync()
- Chat
- TextChatService
- ContentProvider:PreloadAsync()
- TextLabel.FontFace
- TextService:GetFamilyInfoAsync()
- GetTextBoundsParams.Font
- TextService:GetTextBoundsAsync()
- TextLabel.AbsoluteSize
- TextLabel.TextBounds
- TextLabel
- TextButton
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextService](/docs/reference/engine/classes/TextService)

English

Feedback

Engine Class

TextService

The TextService is a service internally responsible for handling the display
of text in the game.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [FilterAndTranslateStringAsync](#FilterAndTranslateStringAsync)(stringToFilter: [string](/docs/luau/strings),fromUserId: [number](/docs/luau/numbers),targetLocales: [Array](/docs/luau/tables#arrays),textContext: [Enum.TextFilterContext](/docs/reference/engine/enums/TextFilterContext)):[TextFilterTranslatedResult](/docs/reference/engine/classes/TextFilterTranslatedResult) |
| [FilterStringAsync](#FilterStringAsync)(stringToFilter: [string](/docs/luau/strings),fromUserId: [number](/docs/luau/numbers),textContext: [Enum.TextFilterContext](/docs/reference/engine/enums/TextFilterContext)):[TextFilterResult](/docs/reference/engine/classes/TextFilterResult) |
| [GetFamilyInfoAsync](#GetFamilyInfoAsync)(assetId: ContentId):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetTextBoundsAsync](#GetTextBoundsAsync)(params: [GetTextBoundsParams](/docs/reference/engine/classes/GetTextBoundsParams)):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [GetTextSize](#GetTextSize)(string: [string](/docs/luau/strings),fontSize: [number](/docs/luau/numbers),font: [Enum.Font](/docs/reference/engine/enums/Font),frameSize: [Vector2](/docs/reference/engine/datatypes/Vector2)):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [GetTextSizeOffsetAsync](#GetTextSizeOffsetAsync)(fontSize: [number](/docs/luau/numbers),font: [Font](/docs/reference/engine/datatypes/Font)):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The TextService is a service internally responsible for handling the display
of text in the game.

This class has two member functions:

The [TextService:GetTextSize()](/docs/reference/engine/classes/TextService#GetTextSize) function gives developers the ability to
calculate the space required for a specific text string with specified
formatting, returning a [Vector2](/docs/reference/engine/datatypes/Vector2) pixel size.

The [TextService:FilterStringAsync()](/docs/reference/engine/classes/TextService#FilterStringAsync) function is required to properly
filter user specified text (such as chat messages or other inputs) in the
interests of user safety. Developers not using the Roblox default
[Chat](/docs/reference/engine/classes/Chat), or allowing users to otherwise input text must use this
function.

---

API Reference

Methods

FilterAndTranslateStringAsync

Yields

Chat translation is not supported in legacy chat. This method is no longer
supported and should not be used.

TextService:FilterAndTranslateStringAsync(

stringToFilter:[string](/docs/luau/strings), fromUserId:[number](/docs/luau/numbers), targetLocales:[Array](/docs/luau/tables#arrays), textContext:[Enum.TextFilterContext](/docs/reference/engine/enums/TextFilterContext)

):[TextFilterTranslatedResult](/docs/reference/engine/classes/TextFilterTranslatedResult)

Parameters

|  |
| --- |
| stringToFilter:[string](/docs/luau/strings) |
| fromUserId:[number](/docs/luau/numbers) |
| targetLocales:[Array](/docs/luau/tables#arrays) |
| textContext:[Enum.TextFilterContext](/docs/reference/engine/enums/TextFilterContext) Default Value: "PrivateChat" |

Returns

[TextFilterTranslatedResult](/docs/reference/engine/classes/TextFilterTranslatedResult)

Chat translation is not supported in legacy chat. This method is no longer
supported and should not be used. All calls return an empty object.
Translating chat messages is only available via [TextChatService](/docs/reference/engine/classes/TextChatService).

Provide feedback

---

FilterStringAsync

Yields

Filters a string being received from a user, and returns a
[TextFilterResult](/docs/reference/engine/classes/TextFilterResult) which can be used to distribute the correctly
filtered text accordingly.

TextService:FilterStringAsync(

stringToFilter:[string](/docs/luau/strings), fromUserId:[number](/docs/luau/numbers), textContext:[Enum.TextFilterContext](/docs/reference/engine/enums/TextFilterContext)

):[TextFilterResult](/docs/reference/engine/classes/TextFilterResult)

Parameters

|  |
| --- |
| stringToFilter:[string](/docs/luau/strings)  The text to be filtered. |
| fromUserId:[number](/docs/luau/numbers)  The userId of the player filtering the text. |
| textContext:[Enum.TextFilterContext](/docs/reference/engine/enums/TextFilterContext) Default Value: "PrivateChat" The context that the filtered message will be used in. |

Returns

[TextFilterResult](/docs/reference/engine/classes/TextFilterResult)

The FilterStringAsync function filters a string being received from a
user, using the [TextService](/docs/reference/engine/classes/TextService), and returns a
[TextFilterResult](/docs/reference/engine/classes/TextFilterResult) which can be used to distribute the correctly
filtered text accordingly.

#### Usage

This method should be called once each time a user submits a message. Do
not cache the results of this function and re-use them for separate
messages. If a user submits the same text multiple times this method must
be called again each time the message is sent. If the results are cached
and reused spam detection and many forms of context-aware filtering will
be broken and potentially put user safety at risk. Games that improperly
use cached results may face moderation.

However, it is encouraged to keep these result objects to display the same
message to users who join the server later. For example: this can be used
to safely and efficiently implement a server chat log that always uses the
least restrictive filtering for users who join later, or for efficiently
displaying text like a pet name to a user who joins the game after the pet
was first spawned and name filtered.

The optional [Enum.TextFilterContext](/docs/reference/engine/enums/TextFilterContext) parameter will not impact the
filtered result of the query. This value will be used to improve Roblox's
text filtering.

Private text is anything that is seen only by specific players, rather
than every player. For example, if the chat is seen by a single player, or
by a selected group of players, then the chat is considered private. Chat
for teams or chat that is potentially visible to a wider group, such as
the server, is considered public. If you are unsure what your text
qualifies as, leave the optional field blank.

Note:

* This method always yields to make a text filtering service call
* This method may throw if there is a service error that can not be
  resolved. If this function throws an error please do not retry the
  request; this method implements its own retry logic internally. If this
  method fails do not display the text to any user.
* This method currently throws if *fromUserId* is not online on the
  current server. We plan to support users who are offline or on a
  different server in the future.

Code Samples

Pet Name Filter Example

This code sample includes a simple demonstration of how
[TextService:FilterStringAsync()](/docs/reference/engine/classes/TextService#FilterStringAsync) should be implemented in a system
where players are allowed to name their pets.

Note, this code sample includes the server-side implementation only (to be
placed in a Script). Examples of how to implement the client-side of this
system are included under the RemoteEvent and RemoteFunction examples.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local TextService = game:GetService("TextService")



local Players = game:GetService("Players")



local Remotes = Instance.new("Folder")



Remotes.Name = "PetNamingRemotes"



Remotes.Parent = ReplicatedStorage



local UserNamedPet = Instance.new("RemoteEvent")



UserNamedPet.Name = "UserNamedPet"



UserNamedPet.Parent = Remotes



local SendPetName = Instance.new("RemoteEvent")



SendPetName.Name = "SendPetName"



SendPetName.Parent = Remotes



local RequestAllPetNames = Instance.new("RemoteFunction")



RequestAllPetNames.Name = "RequestAllPetNames"



RequestAllPetNames.Parent = Remotes



local filterResults = {}



local function broadcastPetName(userId)



local filterResult = filterResults[userId]



if filterResult then



for _, player in pairs(Players:GetPlayers()) do



if player then



-- spawn a new thread so as to not yield the update



task.spawn(function()



-- grab the filtered string for this user



local toUserId = player.UserId



local filteredString = filterResult:GetNonChatStringForUserAsync(toUserId)



filteredString = filteredString or ""



SendPetName:FireClient(player, userId, filteredString)



end)



end



end



end



end



UserNamedPet.OnServerEvent:Connect(function(player, petName)



local fromUserId = player.UserId



-- pcall to catch errors



local success, result = pcall(function()



return TextService:FilterStringAsync(petName, fromUserId)



end)



if success then



filterResults[fromUserId] = result



broadcastPetName(fromUserId)



else



print("Could not filter pet name")



end



end)



RequestAllPetNames.OnServerInvoke = function(player)



local toUserId = player.UserId



local petNames = {}



-- go through filter results and filter the pet name to be sent



for fromUserId, filterResult in pairs(filterResults) do



local filteredString = filterResult:GetNonChatStringForUserAsync(toUserId)



filteredString = filteredString or ""



-- need to convert userId to string so it can't be sent via a remote function



petNames[tostring(fromUserId)] = filteredString



end



return petNames



end



Players.PlayerRemoving:Connect(function(oldPlayer)



local userId = oldPlayer.UserId



filterResults[userId] = nil



end)
```

Provide feedback

---

GetFamilyInfoAsync

Yields

Returns a table containing the name and faces of a font family.

TextService:GetFamilyInfoAsync(assetId:ContentId):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| assetId:ContentId  Asset ID of the font family to look up. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

The information about the font family.

Returns a table containing the name and faces of a font family.

The returned table is structured like this:

```
type FaceInfo = {



Name: string, -- Examples: "Regular", "Book", "Italic", "Thin Italic"



Weight: Enum.FontWeight,



Style: Enum.FontStyle, -- Either Normal or Italic



}



type FamilyInfo = {



Name: string, -- Examples: "Source Sans Pro", "Grenze Gotisch"



Faces: {FaceInfo} -- There's always at least 1 but there can be up to 18.



}
```

If the font family has already been loaded by a previous call to
GetFamilyInfoAsync, [ContentProvider:PreloadAsync()](/docs/reference/engine/classes/ContentProvider#PreloadAsync), or a text
object with the [TextLabel.FontFace](/docs/reference/engine/classes/TextLabel#FontFace) property set, then the method
returns without yielding.

#### Errors

This method can fail because of network errors. You should always wrap it
in a pcall for error handling.

Throws an error in these scenarios:

* The passed family is an empty string.
* Downloading the family failed.
* The asset ID is invalid or points to an asset that doesn't exist.

Code Samples

TextService: Getting font family information

This example showcases a possible usage of the
[TextService:GetFamilyInfoAsync()](/docs/reference/engine/classes/TextService#GetFamilyInfoAsync) method.

It prints out information about a font family to the output window.

```
local TextService = game:GetService("TextService")



local familyToCheck = "rbxasset://fonts/families/Arial.json"



-- This is a yield function which may take up to a few seconds to download the font.



local info = TextService:GetFamilyInfoAsync(familyToCheck)



print("Name of the font:", info.Name)



print("Faces:")



for _, face in info.Faces do



print("--------")



print("Name:", face.Name)



print("Weight:", face.Weight.Name)



print("Style:", face.Style.Name)



end
```

Provide feedback

---

GetTextBoundsAsync

Yields

Calculates the width and height of text given parameters.

TextService:GetTextBoundsAsync(params:[GetTextBoundsParams](/docs/reference/engine/classes/GetTextBoundsParams)):[Vector2](/docs/reference/engine/datatypes/Vector2)

Parameters

|  |
| --- |
| params:[GetTextBoundsParams](/docs/reference/engine/classes/GetTextBoundsParams)  A reference to a [GetTextBoundsParams](/docs/reference/engine/classes/GetTextBoundsParams) object. |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

The size of the text as a [Vector2](/docs/reference/engine/datatypes/Vector2).

This method is similar to [TextService:GetTextSize()](/docs/reference/engine/classes/TextService#GetTextSize), but uses the
[Font](/docs/reference/engine/datatypes/Font) object instead of [Enum.Font](/docs/reference/engine/enums/Font), which has access to more
fonts.

Used to measure how big some text will be given a set of properties like
the string, size, and font.

This is a yield function because some fonts may need to be loaded in order
to measure them. If the font is already loaded, then it will not yield.
[ContentProvider:PreloadAsync()](/docs/reference/engine/classes/ContentProvider#PreloadAsync) can be used to make sure a font is
loaded.

#### Errors

This method can fail because of network errors. You should always wrap it
in a pcall for error handling.

Throws an error in these scenarios:

* The [GetTextBoundsParams.Font](/docs/reference/engine/classes/GetTextBoundsParams#Font) has a blank family.
* The params argument was nil.
* The font family or font face failed to download.

Code Samples

TextService: Measuring text size

This example shows how you can use [TextService:GetTextBoundsAsync()](/docs/reference/engine/classes/TextService#GetTextBoundsAsync).

It measures the size of some text in a specific font, then prints the result.

```
local TextService = game:GetService("TextService")



local params = Instance.new("GetTextBoundsParams")



params.Text = "hello world!"



params.Font = Font.new("rbxasset://fonts/families/GrenzeGotisch.json", Enum.FontWeight.Thin)



params.Size = 20



params.Width = 200



local size = TextService:GetTextBoundsAsync(params)



print("The size of the text is:", size)
```

Provide feedback

---

GetTextSize

Computes the [Vector2](/docs/reference/engine/datatypes/Vector2) dimensions (in pixels) that will be taken
up with text when using the specified formatting parameters and size
constraints.

TextService:GetTextSize(

string:[string](/docs/luau/strings), fontSize:[number](/docs/luau/numbers), font:[Enum.Font](/docs/reference/engine/enums/Font), frameSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

):[Vector2](/docs/reference/engine/datatypes/Vector2)

Parameters

|  |
| --- |
| string:[string](/docs/luau/strings)  The string for which the text size is to be calculated. |
| fontSize:[number](/docs/luau/numbers)  The integer representing the font size used. |
| font:[Enum.Font](/docs/reference/engine/enums/Font)  The font used. |
| frameSize:[Vector2](/docs/reference/engine/datatypes/Vector2)  The [TextLabel.AbsoluteSize](/docs/reference/engine/classes/TextLabel#AbsoluteSize) of the text object to be used. Required to compute how the text will wrap. |

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

The size of the space required, in pixels, by the string with the
specified formatting.

Computes the [Vector2](/docs/reference/engine/datatypes/Vector2) dimensions (in pixels) that will be taken
up with text when using the specified formatting parameters and size
constraints.

Note, the fontSize parameter will not accept the [Enum.FontSize](/docs/reference/engine/enums/FontSize) Enum.
Instead the integer size corresponding with the [Enum.FontSize](/docs/reference/engine/enums/FontSize) Enum
should be used. This is not equal to the value of the [Enum.FontSize](/docs/reference/engine/enums/FontSize)
Enum. For example, for *Size11* font, the integer *11* should be used.

This function is a useful alternative to the [TextLabel.TextBounds](/docs/reference/engine/classes/TextLabel#TextBounds)
property of the [TextLabel](/docs/reference/engine/classes/TextLabel) and [TextButton](/docs/reference/engine/classes/TextButton) objects. Using
the [TextLabel.TextBounds](/docs/reference/engine/classes/TextLabel#TextBounds) property to calculate the dimensions text
requires is often impractical as it requires a [TextLabel](/docs/reference/engine/classes/TextLabel) object to
be created.

With GetTextSize, the dimensions required by a particular text string in a
particular [TextLabel](/docs/reference/engine/classes/TextLabel) or [TextButton](/docs/reference/engine/classes/TextButton) can be calculated
before any object is created or text property set.

Developers are recommended to add a pixel of padding to the result to
ensure no text is cut off.

This method is limited to only fonts that are listed in [Enum.Font](/docs/reference/engine/enums/Font). To
get access to more fonts, you can use
[TextService:GetTextBoundsAsync()](/docs/reference/engine/classes/TextService#GetTextBoundsAsync) instead.

Code Samples

TextService: Getting the Text Size

This example showcases a possible usage of the GetTextSize function.

It computes the possible [Vector2](/docs/reference/engine/datatypes/Vector2) dimensions (in pixels) of the
string *"Hello World"* when the font size is *12*, the font size *SourceSans*
and the frame size is *(1,1)*.

The expected return of this function is the Vector2 value *9, 13*.

```
local TextService = game:GetService("TextService")



local function getTextBounds()



local message = "Hello World"



local size = Vector2.new(1, 1)



local bounds = TextService:GetTextSize(message, 12, "SourceSans", size)



return bounds + Vector2.new(1, 1)



end



print(getTextBounds())
```

Provide feedback

---

GetTextSizeOffsetAsync

Yields

TextService:GetTextSizeOffsetAsync(

fontSize:[number](/docs/luau/numbers), font:[Font](/docs/reference/engine/datatypes/Font)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| fontSize:[number](/docs/luau/numbers) |
| font:[Font](/docs/reference/engine/datatypes/Font) |

Returns

[number](/docs/luau/numbers)

Provide feedback

---