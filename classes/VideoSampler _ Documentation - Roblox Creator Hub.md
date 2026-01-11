# VideoSampler | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/VideoSampler
Scraped: 2026-01-11T02:36:47.144687Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- VideoSampler
- VideoService:CreateVideoSamplerAsync()
- VideoContent
- TimeLength
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [VideoSampler](/docs/reference/engine/classes/VideoSampler)

English

Feedback

Engine Class

VideoSampler

An object for sampling frames from video content.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [TimeLength](#TimeLength):[number](/docs/luau/numbers) |
| [VideoContent](#VideoContent):[Content](/docs/reference/engine/datatypes/Content) |

Methods

|  |
| --- |
| [GetSamplesAtTimesAsync](#GetSamplesAtTimesAsync)(times: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |

Inherited Members

6 inherited from [Object](/docs/reference/engine/classes/Object)

This object lets you get image frames from selected timestamps of a video. To
create a [VideoSampler](/docs/reference/engine/classes/VideoSampler), call
[VideoService:CreateVideoSamplerAsync()](/docs/reference/engine/classes/VideoService#CreateVideoSamplerAsync).

---

API Reference

Properties

TimeLength

Read Only

Not Replicated

Read Parallel

The length of the [VideoContent](/docs/reference/engine/classes/VideoSampler#VideoContent) in
seconds.

VideoSampler.TimeLength:[number](/docs/luau/numbers)

The length of the [VideoContent](/docs/reference/engine/classes/VideoSampler#VideoContent) in
seconds.

Provide feedback

---

VideoContent

Read Only

Not Replicated

Read Parallel

The asset loaded into the [VideoSampler](/docs/reference/engine/classes/VideoSampler).

VideoSampler.VideoContent:[Content](/docs/reference/engine/datatypes/Content)

The asset loaded into the [VideoSampler](/docs/reference/engine/classes/VideoSampler).

Provide feedback

---

Methods

GetSamplesAtTimesAsync

Yields

Gets image frames at the specified timestamps.

VideoSampler:GetSamplesAtTimesAsync(times:[Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| times:[Array](/docs/luau/tables#arrays)  An array of requested timestamps in seconds for which to retrieve image frames. Each timestamp should be a number between 0 and [TimeLength](/docs/reference/engine/classes/VideoSampler#TimeLength). |

Returns

[Array](/docs/luau/tables#arrays)

An array of dictionary or nil values for each requested timestamp. If
a requested timestamp is out of range or the [VideoSampler](/docs/reference/engine/classes/VideoSampler) was
unable to produce a sample, the corresponding entry in the returned
array will be nil.

Each dictionary contains the following keys:

* Time (number): The timestamp of the returned image frame in
  seconds. This value may differ slightly from the requested
  timestamp.
* Image ([Content](/docs/reference/engine/datatypes/Content)): A [Content](/docs/reference/engine/datatypes/Content) with a
  [SourceType](/docs/reference/engine/datatypes/Content#SourceType) of
  [Enum.ContentSourceType.Opaque](/docs/reference/engine/enums/ContentSourceType#Opaque) containing the image frame at the
  corresponding timestamp.

This method allows you to get a set of image frames from a video at
specified timestamps as image [Content](/docs/reference/engine/datatypes/Content) objects.

Provide feedback

---