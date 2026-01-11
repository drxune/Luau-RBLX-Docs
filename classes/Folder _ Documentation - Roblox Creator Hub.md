# Folder | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Folder
Scraped: 2026-01-11T02:29:18.533143Z

## Inherits
- Object
- Instance
- Folder
- Model
- UILayout
- UIListLayout
- UIGridLayout
- UIPageLayout
- UITableLayout
- Frame
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Folder](/docs/reference/engine/classes/Folder)

English

Feedback

Engine Class

![Folder](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Folder-Dark.webp)Folder

A simple container used to hold and organize Roblox instances.

---

Summary

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A simple container used to hold and organize Roblox instances. Unlike other
container classes like [Model](/docs/reference/engine/classes/Model), a folder generally offers no additional
functionality. Folders behave the same way as folders in a computer file
system, meaning they can also be parented to each other.

#### Usage in UI Hierarchies

Each [Folder](/docs/reference/engine/classes/Folder) in your UI hierarchy can define its own [UILayout](/docs/reference/engine/classes/UILayout)
([UIListLayout](/docs/reference/engine/classes/UIListLayout), [UIGridLayout](/docs/reference/engine/classes/UIGridLayout), [UIPageLayout](/docs/reference/engine/classes/UIPageLayout),
[UITableLayout](/docs/reference/engine/classes/UITableLayout)), or use a default position-based layout. For example,
you can set up a [Frame](/docs/reference/engine/classes/Frame) with multiple [Folder](/docs/reference/engine/classes/Folder) children, each
with a different [UILayout](/docs/reference/engine/classes/UILayout) type. Additionally, [Folder](/docs/reference/engine/classes/Folder) contents
are exempt from the effects of a [UILayout](/docs/reference/engine/classes/UILayout) sibling.