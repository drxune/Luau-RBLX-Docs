# AudioPages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioPages
Scraped: 2026-01-11T02:33:09.082601Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Pages
- AudioPages
- AssetService:SearchAudio()
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Pages](/docs/reference/engine/classes/Pages)
6. /
7. [AudioPages](/docs/reference/engine/classes/AudioPages)

English

Feedback

Engine Class

AudioPages

A special version of the [Pages](/docs/reference/engine/classes/Pages) class returned by
[AssetService:SearchAudio()](/docs/reference/engine/classes/AssetService#SearchAudio).

Not Creatable

Not Replicated

---

Summary

Inherited Members

3 inherited from [Pages](/docs/reference/engine/classes/Pages)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A special version of the [Pages](/docs/reference/engine/classes/Pages) class returned by
[AssetService:SearchAudio()](/docs/reference/engine/classes/AssetService#SearchAudio). See the following code sample for
reference on the returned data format.

Code Samples

Getting Music Search Titles

This code gets the music assets returned by the keyword "happy" and prints out their titles.

```
local AssetService = game:GetService("AssetService")



local audioSearchParams = Instance.new("AudioSearchParams")



audioSearchParams.SearchKeyword = "happy"



local success, result = pcall(function()



return AssetService:SearchAudio(audioSearchParams)



end)



if success then



local currentPage = result:GetCurrentPage()



for _, audio in currentPage do



print(audio.Title)



end



else



warn("AssetService error: " .. result)



end



--[[ Returned data format



{



"AudioType": string,



"Artist": string,



"Title": string,



"Tags": {



"string"



},



"Id": number,



"IsEndorsed": boolean,



"Description": string,



"Duration": number,



"CreateTime": string,



"UpdateTime": string,



"Creator": {



"Id": number,



"Name": string,



"Type": number,



"IsVerifiedCreator": boolean



}



}



--]]
```