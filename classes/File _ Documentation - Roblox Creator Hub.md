# File | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/File
Scraped: 2026-01-11T02:27:45.490680Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- File
- Name
- Image
- ImageLabel
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [File](/docs/reference/engine/classes/File)

English

Feedback

Engine Class

![File](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/File-Dark.webp)File

An asset loaded from a file on disk.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [Size](#Size):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetBinaryContents](#GetBinaryContents)():[string](/docs/luau/strings) |
| [GetTemporaryId](#GetTemporaryId)():ContentId |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object that represents an asset loaded from a file on a local disk. Files
generate a temporary asset ID in the form rbxtemp:// which can be used in
Studio without uploading the asset, but will be destroyed when the
[File](/docs/reference/engine/classes/File) is destroyed or when the Studio session ends. Temporary asset IDs
are not shared across [collaborative](/docs/projects/collaboration)
sessions.

The default [Name](/docs/reference/engine/classes/Instance#Name) of a [File](/docs/reference/engine/classes/File) instance will be the
filename on disk, excluding the path but including the extension.

---

API Reference

Properties

Size

Hidden

Read Only

Not Replicated

Plugin Security

Read Parallel

The size of the file on disk, in bytes.

File.Size:[number](/docs/luau/numbers)

The file size (in bytes) of the local file associated with this
[File](/docs/reference/engine/classes/File).

Provide feedback

---

Methods

GetBinaryContents

Plugin Security

Reads the contents of the [File](/docs/reference/engine/classes/File) as a string.

File:GetBinaryContents():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

A raw binary string representation of the [File](/docs/reference/engine/classes/File) contents.

This function is used to read the contents of the [File](/docs/reference/engine/classes/File) as a raw
binary string. This allows the file to be uploaded to web endpoints, or to
be processed by plugins.

Provide feedback

---

GetTemporaryId

Plugin Security

Gets a rbxtemp:// asset ID for this [File](/docs/reference/engine/classes/File).

File:GetTemporaryId():ContentId

Returns

ContentId

The temporary asset ID.

This function is used to retrieve a temporary asset ID associated with the
[File](/docs/reference/engine/classes/File). The ID can be used like rbxassetid://, for example it can
be assigned to the [Image](/docs/reference/engine/classes/ImageLabel#Image) property of an
[ImageLabel](/docs/reference/engine/classes/ImageLabel).

Throws an error if the file does not exist on disk.

Provide feedback

---