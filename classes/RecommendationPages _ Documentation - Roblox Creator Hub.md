# RecommendationPages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RecommendationPages
Scraped: 2026-01-11T02:33:59.534822Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Pages
- RecommendationPages
- GenerateItemListAsync
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Pages](/docs/reference/engine/classes/Pages)
6. /
7. [RecommendationPages](/docs/reference/engine/classes/RecommendationPages)

English

Feedback

Engine Class

RecommendationPages

A special version of the [Pages](/docs/reference/engine/classes/Pages) class returned by
[GenerateItemListAsync](/docs/reference/engine/classes/RecommendationService#GenerateItemListAsync).

Not Creatable

Not Replicated

---

Summary

Inherited Members

3 inherited from [Pages](/docs/reference/engine/classes/Pages)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A special version of the [Pages](/docs/reference/engine/classes/Pages) class returned by
[GenerateItemListAsync](/docs/reference/engine/classes/RecommendationService#GenerateItemListAsync). See
the following code sample for reference on the returned data format.

Code Samples

Generate a list of recommended items

This code snippet demonstrates how to generate a list of recommended items and print their details using the RecommendationService.

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



if success then



-- Get the current page of recommended items



local currentPage = recommendationPages:GetCurrentPage()



for _, item in ipairs(currentPage) do



print("ItemId: " .. item.ItemId)



print("  ReferenceId: " .. item.ReferenceId)



print("  TracingId: " .. item.TracingId)



end



else



warn("RecommendationService error: " .. tostring(recommendationPages))



end



--[[ Returned data format for each item in the page



{



"ItemId": string,



"ReferenceId": string,



"TracingId": string,



"Creator": {



"CreatorId": number,



"CreatorType": Enum.CreatorType,



}?,



"Attributes": {



{



"AssetId": number?,



"Text": string?,



"Description": string?,



"SeekStartTime": number?,



"SeekEndTime": number?,



"TrimStartTime": number?,



"TrimEndTime": number?



}



}?,



"CustomTags": { string }?



}



--]]
```