# RecommendationService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RecommendationService
Scraped: 2026-01-11T02:34:23.109565Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- RecommendationService
- RecommendationPages
- Player
- Object
- LogImpressionEvent
- LogActionEvent
- GenerateItemListAsync
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [RecommendationService](/docs/reference/engine/classes/RecommendationService)

English

Feedback

Engine Class

RecommendationService

A service that provides an interface for you to manage and display
personalized content recommendations.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [GenerateItemListAsync](#GenerateItemListAsync)(generateRecommendationItemListRequest: [Dictionary](/docs/luau/tables#dictionaries)):[RecommendationPages](/docs/reference/engine/classes/RecommendationPages) |
| [GetRecommendationItemAsync](#GetRecommendationItemAsync)(itemId: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries) |
| [LogActionEvent](#LogActionEvent)(actionType: [Enum.RecommendationActionType](/docs/reference/engine/enums/RecommendationActionType),itemId: [string](/docs/luau/strings),tracingId: [string](/docs/luau/strings),actionEventDetails: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [LogImpressionEvent](#LogImpressionEvent)(impressionType: [Enum.RecommendationImpressionType](/docs/reference/engine/enums/RecommendationImpressionType),itemId: [string](/docs/luau/strings),tracingId: [string](/docs/luau/strings),impressionEventDetails: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [RegisterItemAsync](#RegisterItemAsync)(player: [Player](/docs/reference/engine/classes/Player),registerRecommendationItemsRequest: [Dictionary](/docs/luau/tables#dictionaries)):[Dictionary](/docs/luau/tables#dictionaries) |
| [RemoveItemAsync](#RemoveItemAsync)(itemId: [string](/docs/luau/strings)):() |
| [UpdateItemAsync](#UpdateItemAsync)(updateRecommendationItemRequest: [Dictionary](/docs/luau/tables#dictionaries)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

RecommendationService provides an interface for you to manage and display
personalized content recommendations. It supports creating, retrieving,
updating, and deleting recommendation items, as well as generating lists of
recommended content for users. Additionally, it includes functionality for
logging user interactions, such as views and actions, to help refine and
improve recommendation quality. Once set up, you can monitor analytics in the
Creator Dashboard under the Engagement section for an experience.

---

API Reference

Methods

GenerateItemListAsync

Yields

RecommendationService:GenerateItemListAsync(generateRecommendationItemListRequest:[Dictionary](/docs/luau/tables#dictionaries)):[RecommendationPages](/docs/reference/engine/classes/RecommendationPages)

Parameters

|  |
| --- |
| generateRecommendationItemListRequest:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary containing the following fields:   * ConfigName — A unique ID for the specific configuration.   This determines how the candidates are ranked. * LocationId — A developer-defined string that specifies the   location where the recommendation is used, such as "For\_you" or   "Lobby". This parameter will not affect the items returned, and it   can help you track the performance of multiple recommendation   features within your experience. Recommendation metrics for each   individual location will be displayed in the Creator Hub.   LocationId must be a string and cannot be "Other" or   "other" as these values are reserved by the Creator Hub. * PageSize — The number of items returned for each page. * BoostCustomTags — A list of string tags. Any item with this   tag will be boosted in ranking. Note: only supports boosting one tag   now. * CustomContexts — A table of key-value pairs used to pass in   additional context data for ranking. For example, UserId for a   Server script. |

Returns

[RecommendationPages](/docs/reference/engine/classes/RecommendationPages)

This function returns a paginated list of recommended items based on a
given request. The request can specify criteria such as configuration
name, location, and page size to tailor the recommendations. It returns a
[RecommendationPages](/docs/reference/engine/classes/RecommendationPages) object that can be used to iterate through the
list of items.

The ConfigName parameter determines how the recommendation engine ranks
and returns items. For example, you can have configurations that optimize
for views, likes, or purchases. For the ranking to be effective, you must
ensure that you are logging the corresponding user interactions using
[LogImpressionEvent](/docs/reference/engine/classes/RecommendationService#LogImpressionEvent) and
[LogActionEvent](/docs/reference/engine/classes/RecommendationService#LogActionEvent).

Supported ConfigName are:

* MaximizeTimespent: Optimizes recommendations to prioritize content
  that engages users for longer periods.
* MaximizeReactions: Optimizes recommendations to highlight content that
  generates the most user reactions, such as likes and favorites.
* MaximizePlays: Optimizes recommendations to prioritize content that
  generates the most Play actions. To use this configuration
  effectively, you must log both impressions and Play actions. It's
  recommended to filter for "quality" plays (for example play duration
  greater than 60 seconds) before logging to reduce noise and improve the
  system's learning accuracy.
* MaximizeEngagement: Optimizes recommendations through a balanced
  approach that considers multiple engagement signals, including quality
  views and reactions. This config is designed to highlight content that
  performs well across different engagement areas.
* PlayerSpecific: Returns public items created by the player specified
  in the request and sorted by the most recent creation time. To use this
  config, you must pass the UserId in the CustomContexts.
* RecentlyAdded: Returns items sorted by how recent they are, and
  displays the most recently added public content first.
* MaximizeJoins: (Coming soon) Optimizes recommendations to prioritize
  game joins. This configuration is currently exclusive to Roblox Moments
  and focuses on maximizing interactions leading to a teleport. In
  contrast, MaximizePlays is purely optimizing Play actions.
* PlayerOwnedItems: Displays the user's own creations sorted by creation
  time. This config requires user authentication because it displays
  private items. This config is only available on the client.

This function can be called from both the server and the client.
When called from the server, you must pass the UserId in the
CustomContexts.

Code Samples

Generate a list of recommended items

This code snippet demonstrates how to generate a list of recommended items using RecommendationService.

```
local RecommendationService = game:GetService("RecommendationService")



-- Define the request for generating a recommendation list



local request: GenerateRecommendationItemListRequest = {



ConfigName = "MaximizeEngagement",



LocationId = "Lobby",



PageSize = 10



-- NOTE: Uncomment and set CustomContexts.UserId for Server script.



-- No need to set for Local script.



-- CustomContexts = {



--     ["UserId"] = tostring(player.UserId),



-- }



}



-- Call GenerateItemListAsync to get the recommendation pages



local success, recommendationPages = pcall(function()



return RecommendationService:GenerateItemListAsync(request)



end)
```

Provide feedback

---

GetRecommendationItemAsync

Yields

RecommendationService:GetRecommendationItemAsync(itemId:[string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| itemId:[string](/docs/luau/strings)  The ID of the item to retrieve. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary representing the recommendation item with the following
fields:

* ItemId — The unique ID for the item.
* ReferenceId — The developer-provided ID for the item.
* TracingId — An ID for tracking recommendation sessions. This
  will be empty when fetching a single item directly.
* Creator — A table containing the CreatorId and
  CreatorType.
* Attributes — A list of content attributes associated with
  the item.
* CustomTags — A list of custom string tags.
* Visibility — An enum of type
  [RecommendationItemVisibility](/docs/reference/engine/enums/RecommendationItemVisibility).

This function returns a single recommendation item by its ItemId. This
is useful for getting the details of a specific item without having to
fetch a whole list.

This function can be called only from the server.

Code Samples

Get a single recommendation item

This code snippet demonstrates how to retrieve a single recommendation item by its ID.

```
local RecommendationService = game:GetService("RecommendationService")



local function getItem(itemId)



local success, item = pcall(function()



return RecommendationService:GetRecommendationItemAsync(itemId)



end)



if success and item then



print("Successfully retrieved item: " .. item.ItemId)



print("  ReferenceId: " .. item.ReferenceId)



-- The TracingId will be empty when fetching a single item directly



if item.Creator then



print("  CreatorId: " .. tostring(item.Creator.CreatorId))



end



if item.CustomTags then



print("  CustomTags: ")



for _, customTag in ipairs(item.CustomTags) do



print("    " .. customTag)



end



end



else



warn("Failed to retrieve item: " .. itemId .. ". Error: " .. tostring(item))



end



end



-- Example usage (requires a valid itemId)



-- getItem("some-item-id")
```

Provide feedback

---

LogActionEvent

RecommendationService:LogActionEvent(

actionType:[Enum.RecommendationActionType](/docs/reference/engine/enums/RecommendationActionType), itemId:[string](/docs/luau/strings), tracingId:[string](/docs/luau/strings), actionEventDetails:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| actionType:[Enum.RecommendationActionType](/docs/reference/engine/enums/RecommendationActionType)  The enum for the type of action. |
| itemId:[string](/docs/luau/strings)  The item ID returned from registration and [GenerateItemListAsync](/docs/reference/engine/classes/RecommendationService#GenerateItemListAsync). |
| tracingId:[string](/docs/luau/strings)  The tracing ID returned from the [GenerateItemListAsync](/docs/reference/engine/classes/RecommendationService#GenerateItemListAsync) response. Each item has a TracingId. |
| actionEventDetails:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" A dictionary containing the following fields:   * Weight — A number representing the weight of the action.   Default is 1. * DestinationPlaceId — The ID of the place the user was sent   to after the action. Used for   [Play](/docs/reference/engine/enums/RecommendationActionType#Play). * CommentText — Any text associated with the action, such as a   comment. Used for [Comment](/docs/reference/engine/enums/RecommendationActionType#Comment). * ReactionType — A string describing the type of reaction, for   example, "like" or "dislike". Used for   [AddReaction](/docs/reference/engine/enums/RecommendationActionType#AddReaction) or   [RemoveReaction](/docs/reference/engine/enums/RecommendationActionType#RemoveReaction). |

Returns

()

This function logs a user action on a recommended item, such as a "like,"
"share," or "purchase." It requires the itemId of the item and a
tracingId from the GenerateItemListAsync response to link the action to
a specific recommendation context. Additional details about the action can
be provided in the actionEventDetails dictionary.

Logging actions is essential for recommendation configurations that rank
items based on user engagement such as number of likes or purchases.

This function can only be called from the client.

Note: Only LogActionEvent calls in production actually log actions.
Calling this function in Studio doesn't have any effect; you can call it
as many times as you want when testing.

Code Samples

Logging a user action

This code snippet demonstrates how to log a user action on a recommended item.

```
local RecommendationService = game:GetService("RecommendationService")



local function logLike(itemId, tracingId)



local detail: RecommendationActionEventDetails = {



ReactionType = "Like",



Weight = 1.0



}



RecommendationService:LogActionEvent(Enum.RecommendationActionType.AddReaction, itemId, tracingId, detail)



print("Logged 'Like' action for item: " .. itemId)



end



-- Example usage (requires a valid itemId and tracingId from GenerateItemListAsync)



-- logLike("item-id", "tracing-id")
```

Provide feedback

---

LogImpressionEvent

RecommendationService:LogImpressionEvent(

impressionType:[Enum.RecommendationImpressionType](/docs/reference/engine/enums/RecommendationImpressionType), itemId:[string](/docs/luau/strings), tracingId:[string](/docs/luau/strings), impressionEventDetails:[Dictionary](/docs/luau/tables#dictionaries)

):()

Parameters

|  |
| --- |
| impressionType:[Enum.RecommendationImpressionType](/docs/reference/engine/enums/RecommendationImpressionType)  The enum for the type of the impression. |
| itemId:[string](/docs/luau/strings)  The item ID returned from registration and [GenerateItemListAsync](/docs/reference/engine/classes/RecommendationService#GenerateItemListAsync). |
| tracingId:[string](/docs/luau/strings)  The tracing ID returned from the [GenerateItemListAsync](/docs/reference/engine/classes/RecommendationService#GenerateItemListAsync) response. Each item has a TracingId. |
| impressionEventDetails:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" A dictionary containing the following fields:   * Duration — The duration of the impression in seconds. * Weight — A number representing the weight of the impression.   Default is 1. * ItemPosition — The position of the item in the   recommendation list. * DepartureIntent — The [Enum.RecommendationDepartureIntent](/docs/reference/engine/enums/RecommendationDepartureIntent)   indicating the user's intent when leaving a view. For example,   Positive if the view is considered good. |

Returns

()

This function logs an impression event, such as a user viewing a
recommended item. It requires the itemId and a tracingId to associate
the impression with the recommendation context. Details like view duration
and position can be passed in the impressionEventDetails dictionary to
provide more context for the recommendation engine.

Logging impressions, especially Duration, is critical for recommendation
configurations that rank items based on view time.

This function can only be called from the client.

Note: Only LogImpressionEvent calls in production actually log
impressions. Calling this function in Studio doesn't have any effect; you
can call it as many times as you want when testing.

Code Samples

Log a user impression

This code snippet demonstrates how to log a user impression, such as viewing an item.

```
local RecommendationService = game:GetService("RecommendationService")



local function logView(itemId, tracingId)



local detail: RecommendationImpressionEventDetails = {



Duration = 5, -- User viewed for 5 seconds



ItemPosition = 1,



DepartureIntent = Enum.RecommendationDepartureIntent.Neutral



}



RecommendationService:LogImpressionEvent(Enum.RecommendationImpressionType.View, itemId, tracingId, detail)



print("Logged 'View' impression for item: " .. itemId)



end



-- Example usage (requires a valid itemId and tracingId from GenerateItemListAsync)



-- logView("some-item-id", "some-tracing-id")
```

Provide feedback

---

RegisterItemAsync

Yields

RecommendationService:RegisterItemAsync(

player:[Player](/docs/reference/engine/classes/Player), registerRecommendationItemsRequest:[Dictionary](/docs/luau/tables#dictionaries)

):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| player:[Player](/docs/reference/engine/classes/Player)  The player who created the item. |
| registerRecommendationItemsRequest:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary containing the following fields:   * ContentType — The [Enum.RecommendationItemContentType](/docs/reference/engine/enums/RecommendationItemContentType)   specifying the type of content. Type is defined in a generic way.   For example, you can use Static for images, Dynamic for videos,   and Interactive for 3D models that support interaction. * ReferenceId — The developer-defined string that uniquely   identifies the item. * Duration — The duration of the content in seconds. * Attributes — The table of attributes for the item, such as   AssetId or Description. * CustomTags — The list of string tags for filtering and   boosting. * Visibility — The   [RecommendationItemVisibility](/docs/reference/engine/enums/RecommendationItemVisibility)   enum that controls the item's visibility, such as Public or   Private. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A table with only two fields: ItemId and ReferenceId.

This function registers a new item to be included in recommendations. It
requires a player object and a registerRecommendationItemsRequest
dictionary containing details about the item, such as its content type,
reference ID, and custom tags. It returns a dictionary with the ItemId
and the ReferenceId of the newly registered item.

When selecting a ContentType, choose the type that best represents your
item. Note that different content types are not ranked against each other
directly. Instead, they are mixed into the final recommendation list based
on a configured ratio. For example, a configuration might display one
Static item for every ten items. If your experience only features a
single type of content, ensure that all registered items share the same
ContentType.

The ItemId is a unique ID returned by the RecommendationService. All
functions in the RecommendationService use the ItemId as input and
output.

The ReferenceId is a developer-provided identifier for an item. To make
sure that this reference ID is unique, we recommend that you use a UUID.
You can use this reference ID as a key to store rendering-specific
metadata in a data store.

When you register an item, you should only provide information that is
relevant for ranking and recommendations. All other data needed for
rendering should be stored separately in, for example, a data store. This
approach decouples the recommendation logic from the rendering process,
and results in a system that is more modular and easier to maintain.

Attributes is a list of content attributes associated with the item.
Each attribute in the list can contain the following fields:

* AssetId — The ID of an asset, such as an image or video.
* Text — A short text string, like a title.
* Description — A longer text description for the attribute.
* SeekStartTime / SeekEndTime — The start and end times for
  seeking within video content.
* TrimStartTime / TrimEndTime — The start and end times for
  trimming video content.

Common Error Codes:

* HTTP 403 (Forbidden) — This error can occur when you call
  RegisterItemAsync from Studio. Even if you run it as a server script
  in Studio, the request is not issued from a Roblox server. To resolve
  this, publish your experience and run it in the Roblox client.
* HTTP 400 (Bad Request) — This error indicates that a parameter
  is malformed. A common cause is the Attributes table exceeding its
  size limit. If you encounter a 400 error and have a large Attributes
  table, try reducing its size. Remember to only include attributes that
  are relevant for ranking.

This function can only be called from the server.

Code Samples

Register a new item

This code snippet demonstrates how to register a new item for recommendations.

```
local RecommendationService = game:GetService("RecommendationService")



local storage = game:GetService("ReplicatedStorage")



-- Assume a RemoteFunction named 'RegisterItemRemote' exists in ReplicatedStorage



local registerItemRemote = storage.RegisterItemRemote



registerItemRemote.OnServerInvoke = function(player, refId)



local request: RegisterRecommendationItemRequest = {



ContentType = Enum.RecommendationItemContentType.Dynamic,



ReferenceId = refId,



Duration = 60,



Visibility = Enum.RecommendationItemVisibility.Public,



CustomTags = {"locale:en-us", "seasonal:summer"},



Attributes = {



{



AssetId = 123,



Description = "test video",



TrimStartTime = 0,



TrimEndTime = 10.5



}



}



}



local success, response = pcall(function()



return RecommendationService:RegisterItemAsync(player, request)



end)



if success and response then



print("Successfully registered item. ItemId: " .. response.ItemId)



return response.ItemId



else



warn("Failed to register item. Error: " .. tostring(response))



return nil



end



end
```

Provide feedback

---

RemoveItemAsync

Yields

RecommendationService:RemoveItemAsync(itemId:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| itemId:[string](/docs/luau/strings)  The itemId to remove. |

Returns

()

No return value.

This function removes an item from the recommendation system. It takes the
itemId of the item to be deleted as a parameter.

This function can be called from both the server and the client,
with the following limitations:

* When called from the server, it can only remove items registered under
  the same universeId.
* When called from the client, it can only remove items registered by the
  current player.

Code Samples

Remove an item

This code snippet demonstrates how to remove an item from the recommendation system.

```
local RecommendationService = game:GetService("RecommendationService")



local function removeItem(itemId)



local success, err = pcall(function()



return RecommendationService:RemoveItemAsync(itemId)



end)



if success then



print("Successfully removed item: " .. itemId)



else



warn("Failed to remove item: " .. itemId .. ". Error: " .. tostring(err))



end



end
```

Provide feedback

---

UpdateItemAsync

Yields

RecommendationService:UpdateItemAsync(updateRecommendationItemRequest:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| updateRecommendationItemRequest:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary containing the following fields:   * ItemId — The ID of the item to update. * ReferenceId — The new developer-defined string to identify   the item. * Creator — The new creator for the item. Creator is a table   containing two fields: CreatorId: number and   CreatorType: Enum.CreatorType. * Duration — The new duration for the content in seconds. * Visibility — The new visibility setting for the item. * Attributes — The new table of attributes for the item. * CustomTags — The new list of string tags. |

Returns

()

No return value.

This function updates the attributes of an existing recommendation item.
It takes an updateRecommendationItemRequest dictionary containing the
itemId and the fields to be updated. Any fields not included in the
request will remain unchanged.

Items with their
[RecommendationItemVisibility](/docs/reference/engine/enums/RecommendationItemVisibility) set to
Private are not recommended to other users, but they can still be
returned when a user requests their own creations by using the
ConfigName of PlayerOwnedItems.

In Roblox Moments, moderated items are set to Private. While this
prevents other users from seeing them, the item creator can still see
these moderated items and check their moderation status in their My
Moments tab.

This function can only be called from the server.

Code Samples

Update an item

This code snippet demonstrates how to update an existing recommendation item.

```
local RecommendationService = game:GetService("RecommendationService")



local function updateItem(itemId)



-- Only include the fields you want to update



local request: UpdateRecommendationItemRequest = {



ItemId = itemId,



Visibility = Enum.RecommendationItemVisibility.Private,



-- NOTE: the whole CustomTags list will be replaced with this new list



CustomTags = {"updated-tag"}



}



local success, err = pcall(function()



return RecommendationService:UpdateItemAsync(request)



end)



if success then



print("Successfully updated item: " .. itemId)



else



warn("Failed to update item: " .. itemId .. ". Error: " .. tostring(err))



end



end



-- Example usage



-- updateItem("some-item-id-to-update")
```

Provide feedback

---