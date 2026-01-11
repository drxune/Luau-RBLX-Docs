# PackageLink | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PackageLink
Scraped: 2026-01-11T02:36:09.738936Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- PackageLink
- DataModel
- PackageLinks
- Scripts
- Instances
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PackageLink](/docs/reference/engine/classes/PackageLink)

English

Feedback

Engine Class

![PackageLink](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/PackageLink-Dark.webp)PackageLink

Links a [DataModel](/docs/reference/engine/classes/DataModel) instance to a corresponding asset in the cloud.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [AutoUpdate](#AutoUpdate):[boolean](/docs/luau/booleans) |
| [Creator](#Creator):[string](/docs/luau/strings) |
| [DefaultName](#DefaultName):[string](/docs/luau/strings) |
| [PackageAssetName](#PackageAssetName):[string](/docs/luau/strings) |
| [PackageId](#PackageId):ContentId |
| [PermissionLevel](#PermissionLevel):[Enum.PackagePermission](/docs/reference/engine/enums/PackagePermission) |
| [SerializedDefaultAttributes](#SerializedDefaultAttributes):BinaryString |
| [Status](#Status):[string](/docs/luau/strings) |
| [VersionNumber](#VersionNumber):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The purpose of the [PackageLink](/docs/reference/engine/classes/PackageLink) object is to link a [DataModel](/docs/reference/engine/classes/DataModel)
instance to a corresponding asset in the cloud. This improves flows for
collaboration, version control, and sharing for models. The
[PackageLink](/docs/reference/engine/classes/PackageLink) instance will be a child of the root of the entire package
hierarchy.

[PackageLinks](/docs/reference/engine/classes/PackageLink) are not creatable through
[Scripts](/docs/reference/engine/classes/Script). They can only be added through interaction with Studio
and can only be parented to [Instances](/docs/reference/engine/classes/Instance) that can be published
independently of [DataModel](/docs/reference/engine/classes/DataModel) publish. The [PackageLink](/docs/reference/engine/classes/PackageLink) instance
will always be the first child shown in the tree view, regardless of sorting.

---

API Reference

Properties

AutoUpdate

Roblox Script Security

Read Parallel

When this property is set to true, the package associated with the given
[PackageLink](/docs/reference/engine/classes/PackageLink) automatically updates to the latest version.

PackageLink.AutoUpdate:[boolean](/docs/luau/booleans)

When this property is set to true, the package associated with the given
[PackageLink](/docs/reference/engine/classes/PackageLink) will be automatically updated to the latest version.
By default, this property is false upon creation of a package.

This property lets you decide if a given package should be automatically
updated to the latest version when entering a given place. The game
periodically checks for new updates while a place is open.

Provide feedback

---

Creator

Read Only

Not Replicated

Not Scriptable

Read Parallel

The creator of the package asset.

PackageLink.Creator:[string](/docs/luau/strings)

The creator of the package asset.

Provide feedback

---

DefaultName

Not Accessible Security

Read Parallel

PackageLink.DefaultName:[string](/docs/luau/strings)

Provide feedback

---

PackageAssetName

Read Only

Not Replicated

Not Scriptable

Read Parallel

The asset name of the package.

PackageLink.PackageAssetName:[string](/docs/luau/strings)

The asset name of the package.

Provide feedback

---

PackageId

Read Only

Not Replicated

Read Parallel

The ID of the asset this package corresponds to.

PackageLink.PackageId:ContentId

The ID of the asset this package corresponds to.

Provide feedback

---

PermissionLevel

Read Only

Not Replicated

Not Scriptable

Read Parallel

The package permission for the current Studio user.

PackageLink.PermissionLevel:[Enum.PackagePermission](/docs/reference/engine/enums/PackagePermission)

The package permission for the current Studio user.

Provide feedback

---

SerializedDefaultAttributes

Not Accessible Security

Read Parallel

PackageLink.SerializedDefaultAttributes:BinaryString

Provide feedback

---

Status

Read Only

Not Replicated

Roblox Script Security

Read Parallel

The status of the package.

PackageLink.Status:[string](/docs/luau/strings)

The status of the package. It can be one of the following statuses: Up To
Date, Changed, New Version Available, Changed + New Version Available.

Provide feedback

---

VersionNumber

Not Replicated

Not Accessible Security

Read Parallel

Refers to a revision of a specific package.

PackageLink.VersionNumber:[number](/docs/luau/numbers)

This property refers to a revision of a specific package

Provide feedback

---