# AudioSearchParams | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioSearchParams
Scraped: 2026-01-11T02:28:39.069966Z

## Tags
- Not Replicated

## Inherits
- Instance
- AudioSearchParams
- AssetService:SearchAudio()
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioSearchParams](/docs/reference/engine/classes/AudioSearchParams)

English

Feedback

Engine Class

AudioSearchParams

Instance to be passed to [AssetService:SearchAudio()](/docs/reference/engine/classes/AssetService#SearchAudio) to search for
audio assets.

Not Replicated

---

Summary

Properties

|  |
| --- |
| [Album](#Album):[string](/docs/luau/strings) |
| [Artist](#Artist):[string](/docs/luau/strings) |
| [AudioSubType](#AudioSubType):[Enum.AudioSubType](/docs/reference/engine/enums/AudioSubType) |
| [AudioSubtype](#AudioSubtype):[Enum.AudioSubType](/docs/reference/engine/enums/AudioSubType)  Deprecated |
| [MaxDuration](#MaxDuration):[number](/docs/luau/numbers) |
| [MinDuration](#MinDuration):[number](/docs/luau/numbers) |
| [SearchKeyword](#SearchKeyword):[string](/docs/luau/strings) |
| [Tag](#Tag):[string](/docs/luau/strings) |
| [Title](#Title):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Instance to be passed to [AssetService:SearchAudio()](/docs/reference/engine/classes/AssetService#SearchAudio) to search for
audio assets.

---

API Reference

Properties

Album

Read Parallel

The album the audio asset belongs to.

AudioSearchParams.Album:[string](/docs/luau/strings)

Searches for audio which belongs to this album. Needs to be an exact
match.

Provide feedback

---

Artist

Read Parallel

The artist that created the audio asset.

AudioSearchParams.Artist:[string](/docs/luau/strings)

Searches for audio which was created by this artist. Needs to be an exact
match.

Provide feedback

---

AudioSubType

Read Parallel

AudioSearchParams.AudioSubType:[Enum.AudioSubType](/docs/reference/engine/enums/AudioSubType)

Provide feedback

---

AudioSubtype

Deprecated

Show details

---

MaxDuration

Read Parallel

The maximum duration of the audio asset.

AudioSearchParams.MaxDuration:[number](/docs/luau/numbers)

Searches for audio with a duration less than or equal to this value.

Provide feedback

---

MinDuration

Read Parallel

The minimum duration of the audio asset.

AudioSearchParams.MinDuration:[number](/docs/luau/numbers)

Searches for audio with a duration greater than or equal to this value.

Provide feedback

---

SearchKeyword

Read Parallel

The keyword to search for.

AudioSearchParams.SearchKeyword:[string](/docs/luau/strings)

Searches for audio relevant to this keyword.

Provide feedback

---

Tag

Read Parallel

The tag of the audio asset.

AudioSearchParams.Tag:[string](/docs/luau/strings)

Searches for audio which has this tag. Needs to be an exact match.

Provide feedback

---

Title

Read Parallel

The title of the audio asset.

AudioSearchParams.Title:[string](/docs/luau/strings)

Searches for audio with this title. Needs to be an exact match.

Provide feedback

---