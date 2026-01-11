# CatalogSearchParams | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/CatalogSearchParams
Scraped: 2026-01-11T02:42:09.033651Z

## Inherits
- AvatarEditorService:SearchCatalog()
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [CatalogSearchParams](/docs/reference/engine/datatypes/CatalogSearchParams)

English

Feedback

Engine Data Type

CatalogSearchParams

Stores parameters used in catalog searches via
[AvatarEditorService:SearchCatalog()](/docs/reference/engine/classes/AvatarEditorService#SearchCatalog).

---

Summary

Properties

|  |
| --- |
| [SearchKeyword](#SearchKeyword):[string](/docs/luau/strings) |
| [MinPrice](#MinPrice):[number](/docs/luau/numbers) |
| [MaxPrice](#MaxPrice):[number](/docs/luau/numbers) |
| [SortType](#SortType):[Enum.CatalogSortType](/docs/reference/engine/enums/CatalogSortType) |
| [SortAggregation](#SortAggregation):[Enum.CatalogSortAggregation](/docs/reference/engine/enums/CatalogSortAggregation) |
| [CategoryFilter](#CategoryFilter):[Enum.CatalogCategoryFilter](/docs/reference/engine/enums/CatalogCategoryFilter) |
| [SalesTypeFilter](#SalesTypeFilter):[Enum.SalesTypeFilter](/docs/reference/engine/enums/SalesTypeFilter) |
| [BundleTypes](#BundleTypes):[Array](/docs/luau/tables#arrays)<[Enum.BundleType](/docs/reference/engine/enums/BundleType)> |
| [AssetTypes](#AssetTypes):[Array](/docs/luau/tables#arrays)<[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)> |
| [IncludeOffSale](#IncludeOffSale):[boolean](/docs/luau/booleans) |
| [CreatorName](#CreatorName):[string](/docs/luau/strings) |
| [CreatorType](#CreatorType):[Enum.CreatorTypeFilter](/docs/reference/engine/enums/CreatorTypeFilter) |
| [CreatorId](#CreatorId):[number](/docs/luau/numbers) |
| [Limit](#Limit):[number](/docs/luau/numbers) |

The [CatalogSearchParams](/docs/reference/engine/datatypes/CatalogSearchParams) data type stores the parameters of a
catalog search via [AvatarEditorService:SearchCatalog()](/docs/reference/engine/classes/AvatarEditorService#SearchCatalog).

When accessing the value of the [CatalogSearchParams.BundleTypes](/docs/reference/engine/datatypes/CatalogSearchParams#BundleTypes) or
[CatalogSearchParams.AssetTypes](/docs/reference/engine/datatypes/CatalogSearchParams#AssetTypes) property the returned table will be
read-only to avoid confusion when not directly accessing the
[CatalogSearchParams](/docs/reference/engine/datatypes/CatalogSearchParams) instance.

For example, you can use these properties as follows:

```
local params = CatalogSearchParams.new()



params.SearchKeyword = "Test"



params.MinPrice = 5000



params.MaxPrice = 10000



params.BundleTypes = {Enum.BundleType.Animations, Enum.BundleType.BodyParts}



local types = params.BundleTypes



for _, val in types do



print(val)



end



-- table.insert(types, Enum.BundleType.Animations) -- This would not work because the table is read only
```

---

API Reference

Properties

SearchKeyword

The keyword to search for catalog results with.

CatalogSearchParams.SearchKeyword:[string](/docs/luau/strings)

The keyword to search for catalog results with.

Provide feedback

---

MinPrice

The minimum item price to search for.

CatalogSearchParams.MinPrice:[number](/docs/luau/numbers)

The minimum item price to search for.

Provide feedback

---

MaxPrice

The maximum item price to search for.

CatalogSearchParams.MaxPrice:[number](/docs/luau/numbers)

The maximum item price to search for.

Provide feedback

---

SortType

The order in which to sort the results.

CatalogSearchParams.SortType:[Enum.CatalogSortType](/docs/reference/engine/enums/CatalogSortType)

The order in which to sort the results, represented by a
[Enum.CatalogSortType](/docs/reference/engine/enums/CatalogSortType).

Provide feedback

---

SortAggregation

The time period to use to aggregate the sort results.

CatalogSearchParams.SortAggregation:[Enum.CatalogSortAggregation](/docs/reference/engine/enums/CatalogSortAggregation)

The time period to use to aggregate the sort results by, represented by a
[Enum.CatalogCategoryFilter](/docs/reference/engine/enums/CatalogCategoryFilter). This only applies when the sort type is
[Enum.CatalogSortType.MostFavorited](/docs/reference/engine/enums/CatalogSortType#MostFavorited) or
[Enum.CatalogSortType.BestSelling](/docs/reference/engine/enums/CatalogSortType#BestSelling). It does not apply for other sort
types.

Provide feedback

---

CategoryFilter

The category to filter the search by.

CatalogSearchParams.CategoryFilter:[Enum.CatalogCategoryFilter](/docs/reference/engine/enums/CatalogCategoryFilter)

The category to filter the search by, represented by a
[Enum.CatalogCategoryFilter](/docs/reference/engine/enums/CatalogCategoryFilter).

Provide feedback

---

SalesTypeFilter

The sales type filter the search by.

CatalogSearchParams.SalesTypeFilter:[Enum.SalesTypeFilter](/docs/reference/engine/enums/SalesTypeFilter)

The sales type the search by, represented by a [Enum.SalesTypeFilter](/docs/reference/engine/enums/SalesTypeFilter).

Provide feedback

---

BundleTypes

An array containing [Enum.BundleType](/docs/reference/engine/enums/BundleType) values to filter the search by.

CatalogSearchParams.BundleTypes:[Array](/docs/luau/tables#arrays)<[Enum.BundleType](/docs/reference/engine/enums/BundleType)>

An array containing [Enum.BundleType](/docs/reference/engine/enums/BundleType) values to filter the search by.

Provide feedback

---

AssetTypes

An array containing [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType) values to filter the search by.

CatalogSearchParams.AssetTypes:[Array](/docs/luau/tables#arrays)<[Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType)>

An array containing [Enum.AvatarAssetType](/docs/reference/engine/enums/AvatarAssetType) values to filter the search by.

Provide feedback

---

IncludeOffSale

Whether off sale items should be included in the results.

CatalogSearchParams.IncludeOffSale:[boolean](/docs/luau/booleans)

Whether off sale items should be included in the results.

Provide feedback

---

CreatorName

Search for items with the given creator name.

CatalogSearchParams.CreatorName:[string](/docs/luau/strings)

Search for items with the given creator name. Specify whether to search
users, groups, or both with [CatalogSearchParams.CreatorType](/docs/reference/engine/datatypes/CatalogSearchParams#CreatorType).

Provide feedback

---

CreatorType

Search for items created by the given creator type.

CatalogSearchParams.CreatorType:[Enum.CreatorTypeFilter](/docs/reference/engine/enums/CreatorTypeFilter)

Search for items created by the given creator type. When unspecified, it
defaults to returning creations from both [Enum.CreatorTypeFilter.User](/docs/reference/engine/enums/CreatorTypeFilter#User)
and [Enum.CreatorTypeFilter.Group](/docs/reference/engine/enums/CreatorTypeFilter#Group). Searching by
[CatalogSearchParams.CreatorId](/docs/reference/engine/datatypes/CatalogSearchParams#CreatorId) with [Enum.CreatorTypeFilter.All](/docs/reference/engine/enums/CreatorTypeFilter#All)
results in a HTTP 400 Bad Request error.

Provide feedback

---

CreatorId

Search for items created by the given creator ID.

CatalogSearchParams.CreatorId:[number](/docs/luau/numbers)

Search for items created by the single creator ID. Specify user or group
with [CatalogSearchParams.CreatorType](/docs/reference/engine/datatypes/CatalogSearchParams#CreatorType). Searching by creator ID
and creator name is not supported; specify one, not both.

Provide feedback

---

Limit

Specifies the number of items to return. Accepts 10, 28, 30, 60,
and 120. Defaults to 30.

CatalogSearchParams.Limit:[number](/docs/luau/numbers)

Specifies the number of items to return. Accepts 10, 28, 30, 60,
and 120. Defaults to 30.

Provide feedback

---