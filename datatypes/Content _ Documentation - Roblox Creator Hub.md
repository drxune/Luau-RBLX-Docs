# Content | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Content
Scraped: 2026-01-11T02:42:08.740706Z

## Inherits
- Object
- Instance
- EditableImage
- EditableMesh
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Content](/docs/reference/engine/datatypes/Content)

English

Feedback

Engine Data Type

Content

Represents a reference to asset content stored externally or as an object
within the place.

---

Summary

Constructors

|  |
| --- |
| [fromUri](#fromUri)(uri: [string](/docs/luau/strings)) |
| [fromObject](#fromObject)(object: [Object](/docs/reference/engine/classes/Object)) |

Properties

|  |
| --- |
| [none](#none):[Content](/docs/reference/engine/datatypes/Content) |
| [SourceType](#SourceType):[Enum.ContentSourceType](/docs/reference/engine/enums/ContentSourceType) |
| [Uri](#Uri):[string](/docs/luau/strings)? |
| [Object](#Object):[Object](/docs/reference/engine/classes/Object)? |
| [Opaque](#Opaque):Opaque? |

The Content data type represents a reference to asset content stored
externally or as an object within the place, wrapping a single value of one of
the supported [Enum.ContentSourceType](/docs/reference/engine/enums/ContentSourceType) values.

##### Warning

Replication is not yet supported for [Object](/docs/reference/engine/datatypes/Content#Object) values.
When an [Instance](/docs/reference/engine/classes/Instance) with a [Content](/docs/reference/engine/datatypes/Content) property containing a
[Object](/docs/reference/engine/datatypes/Content#Object) value is replicated, an unusable placeholder
[Object](/docs/reference/engine/classes/Object) of the same type will be used instead of the [Object](/docs/reference/engine/classes/Object)
itself, and any attempt to read or write the contents of that placeholder
object will throw. These placeholder objects will render as a cyan and magenta
checkerboard pattern.

This will be replaced with standard replication behavior in the future. For
now, do not use [EditableImage](/docs/reference/engine/classes/EditableImage) or [EditableMesh](/docs/reference/engine/classes/EditableMesh) as
[Content](/docs/reference/engine/datatypes/Content) on the server on an [Instance](/docs/reference/engine/classes/Instance) that can replicate to
clients.

---

API Reference

Constructors

fromUri

Returns a new Content with an [asset URI](/docs/projects/assets#asset-uris) string value referencing content external to the place.

Content.fromUri(uri:[string](/docs/luau/strings))

Parameters

|  |
| --- |
| uri:[string](/docs/luau/strings)  The [asset URI](/docs/projects/assets#asset-uris) string. |

Returns a new Content with an [asset URI](/docs/projects/assets#asset-uris) string value referencing content external to the place.

[Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) will be [Uri](/docs/reference/engine/enums/ContentSourceType), and [Content.Uri](/docs/reference/engine/datatypes/Content#Uri) will contain a non‑nil string value.

If uri is empty, [Content.none](/docs/reference/engine/datatypes/Content#none) will be returned instead.

Provide feedback

---

fromObject

Returns a new Content with a strong reference to an [Object](/docs/reference/engine/classes/Object).

Content.fromObject(object:[Object](/docs/reference/engine/classes/Object))

Parameters

|  |
| --- |
| object:[Object](/docs/reference/engine/classes/Object)  The [Object](/docs/reference/engine/classes/Object) to reference. |

Returns a new Content with a strong reference to an [Object](/docs/reference/engine/classes/Object).

[Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) will be [Object](/docs/reference/engine/enums/ContentSourceType), and [Content.Object](/docs/reference/engine/datatypes/Content#Object) will contain a non‑nil [Object](/docs/reference/engine/classes/Object) reference.

[Content.Object](/docs/reference/engine/datatypes/Content#Object) references are strong references that hold shared ownership of the [Object](/docs/reference/engine/classes/Object). Any [Content.Object](/docs/reference/engine/datatypes/Content#Object) reference will extend the lifetime of that [Object](/docs/reference/engine/classes/Object) and prevent it from being garbage collected.

Throws if object is nil.

Provide feedback

---

Properties

none

An empty Content value with [Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) of
[None](/docs/reference/engine/enums/ContentSourceType).

Content.none:[Content](/docs/reference/engine/datatypes/Content)

An empty Content value with [Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) of
[None](/docs/reference/engine/enums/ContentSourceType).

Provide feedback

---

SourceType

The source type of the contained value.

Content.SourceType:[Enum.ContentSourceType](/docs/reference/engine/enums/ContentSourceType)

The source type of the contained value. Indicates which property contains
a non‑nil value.

Provide feedback

---

Uri

A URI string if [Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) is
[Uri](/docs/reference/engine/enums/ContentSourceType), otherwise nil.

Content.Uri:[string](/docs/luau/strings)?

A URI string if [Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) is
[Uri](/docs/reference/engine/enums/ContentSourceType), otherwise nil.

Provide feedback

---

Object

A reference to a non-nil [Object](/docs/reference/engine/classes/Object) if [Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType)
is [Object](/docs/reference/engine/enums/ContentSourceType), otherwise nil.

Content.Object:[Object](/docs/reference/engine/classes/Object)?

A reference to a non-nil [Object](/docs/reference/engine/classes/Object) if [Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType)
is [Object](/docs/reference/engine/enums/ContentSourceType), otherwise nil.

Provide feedback

---

Opaque

A reference to a non-nil Opaque content if
[Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) is [Opaque](/docs/reference/engine/enums/ContentSourceType),
otherwise nil.

Content.Opaque:Opaque?

A reference to a non-nil Opaque content if
[Content.SourceType](/docs/reference/engine/datatypes/Content#SourceType) is [Opaque](/docs/reference/engine/enums/ContentSourceType),
otherwise nil.

Provide feedback

---