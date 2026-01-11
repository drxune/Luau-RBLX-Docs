# VideoService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VideoService
Scraped: 2026-01-11T02:31:15.707453Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- VideoService
- VideoSampler
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [VideoService](/docs/reference/engine/classes/VideoService)

English

Feedback

Engine Class

VideoService

An internal service that offers no functionality to developers.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [CreateVideoSamplerAsync](#CreateVideoSamplerAsync)(content: [Content](/docs/reference/engine/datatypes/Content),options: [Dictionary](/docs/luau/tables#dictionaries)?):[VideoSampler](/docs/reference/engine/classes/VideoSampler) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Methods

CreateVideoSamplerAsync

Yields

Creates a [VideoSampler](/docs/reference/engine/classes/VideoSampler) that samples frames from the provided video
content.

VideoService:CreateVideoSamplerAsync(

content:[Content](/docs/reference/engine/datatypes/Content), options:[Dictionary](/docs/luau/tables#dictionaries)?

):[VideoSampler](/docs/reference/engine/classes/VideoSampler)

Parameters

|  |
| --- |
| content:[Content](/docs/reference/engine/datatypes/Content)  The video content to sample from. |
| options:[Dictionary](/docs/luau/tables#dictionaries)?  Options table for creating the [VideoSampler](/docs/reference/engine/classes/VideoSampler):   * Size – A [Enum.VideoSampleSize](/docs/reference/engine/enums/VideoSampleSize) value that determines the   resolution of textures produced by the [VideoSampler](/docs/reference/engine/classes/VideoSampler).   Defaults to [Enum.VideoSampleSize.Small](/docs/reference/engine/enums/VideoSampleSize#Small). Use the smallest   resolution that meets your needs to minimize memory usage and   improve sampling performance. |

Returns

[VideoSampler](/docs/reference/engine/classes/VideoSampler)

The created [VideoSampler](/docs/reference/engine/classes/VideoSampler).

Creates a [VideoSampler](/docs/reference/engine/classes/VideoSampler) that samples frames from the provided video
content.

Provide feedback

---