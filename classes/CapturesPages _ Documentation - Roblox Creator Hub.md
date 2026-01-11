# CapturesPages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CapturesPages
Scraped: 2026-01-11T02:41:04.608685Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Pages
- CapturesPages
- CaptureService.ReadCapturesFromGalleryAsync
- Instance
- Object
- CaptureService:ReadCapturesFromGalleryAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Pages](/docs/reference/engine/classes/Pages)
6. /
7. [CapturesPages](/docs/reference/engine/classes/CapturesPages)

English

Feedback

Engine Class

CapturesPages

A special version of the [Pages](/docs/reference/engine/classes/Pages) class returned by
[CaptureService.ReadCapturesFromGalleryAsync](/docs/reference/engine/classes/CaptureService#ReadCapturesFromGalleryAsync).

Not Creatable

Not Replicated

---

Summary

Inherited Members

3 inherited from [Pages](/docs/reference/engine/classes/Pages)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A special version of the [Pages](/docs/reference/engine/classes/Pages) class returned by
[CaptureService:ReadCapturesFromGalleryAsync()](/docs/reference/engine/classes/CaptureService#ReadCapturesFromGalleryAsync). See the following code
sample for reference on the returned data format.

Code Samples

Read captures from gallery and iterate over pages

This code snippet demonstrates how to fetch captures from a user gallery, iterate over the result pages, and return all captures.

```
local CaptureService = game:GetService("CaptureService")



local function readCapturesFromGallery()



local allCaptures = {}



local capturesPages



local success, result = pcall(function()



local readResult, pages = CaptureService:ReadCapturesFromGalleryAsync()



if readResult == Enum.ReadCapturesFromGalleryResult.Success then



capturesPages = pages



end



return readResult



end)



if not success or result ~= Enum.ReadCapturesFromGalleryResult.Success then



-- Likely a permissions error, see CaptureService:PromptCaptureGalleryPermissionAsync()



warn("Failed to fetch initial captures: " .. result.Name)



return



end



-- Iterate through current page



local currentPage = capturesPages:GetCurrentPage()



for _, capture in currentPage do



table.insert(allCaptures, capture)



end



-- Advance to next page until finished



while not capturesPages.IsFinished do



local advanceToNextPageSuccess, _ = pcall(function()



capturesPages:AdvanceToNextPageAsync()



end)



if not advanceToNextPageSuccess then



return



end



currentPage = capturesPages:GetCurrentPage()



for _, capture in currentPage do



table.insert(allCaptures, capture)



end



end



return allCaptures



end
```