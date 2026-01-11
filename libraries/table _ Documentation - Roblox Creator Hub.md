# table | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/table
Scraped: 2026-01-11T02:49:58.234336Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [table](/docs/reference/engine/libraries/table)

English

Feedback

Engine Library

table

A library of table functions.

---

Summary

Functions

|  |
| --- |
| [clear](#clear)(table: [table](/docs/luau/tables)):() |
| [clone](#clone)(t: [table](/docs/luau/tables)):[table](/docs/luau/tables) |
| [concat](#concat)(t: [Array](/docs/luau/tables#arrays),sep: [string](/docs/luau/strings),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [create](#create)(count: [number](/docs/luau/numbers),value: Variant):[table](/docs/luau/tables) |
| [find](#find)(haystack: [table](/docs/luau/tables),needle: Variant,init: [number](/docs/luau/numbers)):Variant |
| [foreach](#foreach)(t: [table](/docs/luau/tables),f: [function](/docs/luau/functions)):()  Deprecated |
| [foreachi](#foreachi)(t: [Array](/docs/luau/tables#arrays),f: [function](/docs/luau/functions)):()  Deprecated |
| [freeze](#freeze)(t: [table](/docs/luau/tables)):[table](/docs/luau/tables) |
| [getn](#getn)(t: [Array](/docs/luau/tables#arrays)):[number](/docs/luau/numbers)  Deprecated |
| [insert](#insert)(t: [Array](/docs/luau/tables#arrays),pos: [number](/docs/luau/numbers),value: Variant):() |
| [insert](#insert-t-value)(t: [Array](/docs/luau/tables#arrays),value: Variant):() |
| [isfrozen](#isfrozen)(t: [table](/docs/luau/tables)):[boolean](/docs/luau/booleans) |
| [maxn](#maxn)(t: [table](/docs/luau/tables)):[number](/docs/luau/numbers) |
| [move](#move)(src: [table](/docs/luau/tables),a: [number](/docs/luau/numbers),b: [number](/docs/luau/numbers),t: [number](/docs/luau/numbers),dst: [table](/docs/luau/tables)):[table](/docs/luau/tables) |
| [pack](#pack)(values...: Variant):Variant |
| [remove](#remove)(t: [Array](/docs/luau/tables#arrays),pos: [number](/docs/luau/numbers)):Variant |
| [sort](#sort)(t: [Array](/docs/luau/tables#arrays),comp: [function](/docs/luau/functions)):() |
| [unpack](#unpack)(list: [table](/docs/luau/tables),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |

This library provides generic functions for table/array manipulation,
providing all its functions inside the global [table](/docs/reference/engine/libraries/table) variable. Most
functions in the [table](/docs/reference/engine/libraries/table) library assume that the table represents an
array or a list. For these functions, the "length" of a table means the result
of the length operator.

---

API Reference

Functions

clear

Sets all keys in the given table to nil.

table.clear(table:[table](/docs/luau/tables)):()

Parameters

|  |
| --- |
| table:[table](/docs/luau/tables)  The table whose keys will be cleared. |

Returns

()

Sets the value for all keys within the given table to nil. This causes
the # operator to return 0 for the given table. The allocated capacity
of the table's array portion is maintained, which allows for efficient
re-use of the space.

```
local grades = {95, 82, 71, 92, 100, 60}



print(grades[4], #grades) --> 92, 6



table.clear(grades)



print(grades[4], #grades) --> nil, 0



-- If grades is filled again with the same number of entries,



-- no potentially expensive array resizing will occur



-- because the capacity was maintained by table.clear.
```

This function does not delete/destroy the table provided to it. This
function is meant to be used specifically for tables that are to be
re-used.

Provide feedback

---

clone

Returns a shallow copy of the provided table.

table.clone(t:[table](/docs/luau/tables)):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The table to be cloned. |

Returns

[table](/docs/luau/tables)

The clone of the provided table.

Returns an unfrozen shallow copy of the provided table.

Provide feedback

---

concat

Returns the given range of table elements as a string where each element
is separated by the given separator.

table.concat(

t:[Array](/docs/luau/tables#arrays), sep:[string](/docs/luau/strings), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| t:[Array](/docs/luau/tables#arrays)  The table that will be converted into a string. |
| sep:[string](/docs/luau/strings)  The string that will be concatenated between each entry in the table. |
| i:[number](/docs/luau/numbers) Default Value: 1 The starting index of the table concatenation. |
| j:[number](/docs/luau/numbers)  The ending index of the table concatenation. |

Returns

[string](/docs/luau/strings)

Given an array where all elements are strings or numbers, returns the
string t[i] ... sep ... t[i+1] ... sep ... t[j]. The default value for
sep is an empty string, the default for i is 1, and the default for j
is #t. If i is greater than j, returns the empty string.

Provide feedback

---

create

Returns a new table populated with many instances of the specified value.

table.create(

count:[number](/docs/luau/numbers), value:Variant

):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| count:[number](/docs/luau/numbers) |
| value:Variant |

Returns

[table](/docs/luau/tables)

Creates a table with the array portion allocated to the given number of
elements, optionally filled with the given value.

```
local t = table.create(3, "Roblox")



print(table.concat(t)) --> RobloxRobloxRoblox
```

If you are inserting into large array-like tables and are certain of a
reasonable upper limit to the number of elements, it's recommended to use
this function to initialize the table. This ensures the table's array
portion of its memory is sufficiently sized, as resizing it can be
expensive. For small quantities this is typically not noticeable.

Provide feedback

---

find

Returns the index of the first occurrence of needle within haystack
starting from init.

table.find(

haystack:[table](/docs/luau/tables), needle:Variant, init:[number](/docs/luau/numbers)

):Variant

Parameters

|  |
| --- |
| haystack:[table](/docs/luau/tables) |
| needle:Variant |
| init:[number](/docs/luau/numbers) |

Returns

Variant

Within the given array-like table haystack, find the first occurrence of
value needle, starting from index init or the beginning if not
provided. If the value is not found, nil is returned.

A [linear search](https://en.wikipedia.org/wiki/Linear_search) algorithm
is performed.

```
local t = {"a", "b", "c", "d", "e"}



print(table.find(t, "d")) --> 4



print(table.find(t, "z")) --> nil, because z is not in the table



print(table.find(t, "b", 3)) --> nil, because b appears before index 3
```

Provide feedback

---

foreach

Deprecated

Show details

---

foreachi

Deprecated

Show details

---

freeze

Makes the given table read-only.

table.freeze(t:[table](/docs/luau/tables)):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The table to be frozen. |

Returns

[table](/docs/luau/tables)

The frozen table.

This function makes the given table read-only, effectively "freezing" it
in its current state. Attempting to modify a frozen table throws an error.

This freezing effect is shallow, which means that you can write to a table
within a frozen table. To deep freeze a table, call this function
recursively on all of the descending tables.

Provide feedback

---

getn

Deprecated

Show details

---

insert

Inserts the provided value to the target position of the array.

table.insert(

t:[Array](/docs/luau/tables#arrays), pos:[number](/docs/luau/numbers), value:Variant

):()

Parameters

|  |
| --- |
| t:[Array](/docs/luau/tables#arrays)  The table that is being appended to. |
| pos:[number](/docs/luau/numbers)  The position at which the value will be inserted. |
| value:Variant  The value that will be appended to the table. |

Returns

()

Inserts the provided value to the target position of the array.

Provide feedback

---

insert

Appends the provided value to the end of the array.

table.insert(

t:[Array](/docs/luau/tables#arrays), value:Variant

):()

Parameters

|  |
| --- |
| t:[Array](/docs/luau/tables#arrays)  The table that is being appended to. |
| value:Variant  The value that will be appended to the table. |

Returns

()

Appends the provided value to the end of the array.

Provide feedback

---

isfrozen

Returns true if the given table is frozen and false if it isn't
frozen.

table.isfrozen(t:[table](/docs/luau/tables)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The table to check. |

Returns

[boolean](/docs/luau/booleans)

Whether the table is frozen from [table.freeze()](/docs/reference/engine/libraries/table#freeze).

This function returns true if the given table is frozen and false if
it isn't frozen. You can freeze tables using [table.freeze()](/docs/reference/engine/libraries/table#freeze).

Provide feedback

---

maxn

Returns the maximum numeric key of the provided table, or zero if the
table has no numeric keys.

table.maxn(t:[table](/docs/luau/tables)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables) |

Returns

[number](/docs/luau/numbers)

Returns the maximum numeric key of the provided table, or zero if the
table has no numeric keys. Gaps in the table are ignored.

Provide feedback

---

move

Copies the specified range of elements from one table to another.

table.move(

src:[table](/docs/luau/tables), a:[number](/docs/luau/numbers), b:[number](/docs/luau/numbers), t:[number](/docs/luau/numbers), dst:[table](/docs/luau/tables)

):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| src:[table](/docs/luau/tables)  Source table. |
| a:[number](/docs/luau/numbers)  Start copying at src[a]. |
| b:[number](/docs/luau/numbers)  Copy up to and including src[b]. |
| t:[number](/docs/luau/numbers)  Copy into dst[t], .... |
| dst:[table](/docs/luau/tables) Default Value: src Destination table. |

Returns

[table](/docs/luau/tables)

dst, for convenience.

Copies elements in table src from src[a] up to src[b] into table
dst starting at index t. Equivalent to the assignment statement
dst[t], ..., dst[t + (b - a)] = src[a], ..., src[b].

The default for dst is src. The destination range may overlap with the
source range.

Returns dst for convenience.

Provide feedback

---

pack

Returns a new table containing the provided values.

table.pack(values...:Variant):Variant

Parameters

|  |
| --- |
| values...:Variant |

Returns

Variant

Returns a new table with all arguments stored into keys 1, 2, etc. and
with a field "n" with the total number of arguments. Note that the
resulting table may not be a sequence.

```
local t = table.pack(1, 2, 3)



print(table.concat(t, ", ")) --> 1, 2, 3
```

Provide feedback

---

remove

Removes the specified element from the array, shifting later elements down
to fill in the empty space if possible.

table.remove(

t:[Array](/docs/luau/tables#arrays), pos:[number](/docs/luau/numbers)

):Variant

Parameters

|  |
| --- |
| t:[Array](/docs/luau/tables#arrays)  The table that is having an element removed. |
| pos:[number](/docs/luau/numbers)  The index of the element being removed. |

Returns

Variant

Removes from array t the element at position pos, returning the value of
the removed element. When pos is an integer between 1 and #t, it
shifts down the elements t[pos+1], t[pos+2], ..., t[#t] and erases
element t[#t]. If the pos parameter is not provided, pos defaults to the
length of the table removing the last element.

Provide feedback

---

sort

Sorts table elements using the provided comparison function or the <
operator.

table.sort(

t:[Array](/docs/luau/tables#arrays), comp:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| t:[Array](/docs/luau/tables#arrays) |
| comp:[function](/docs/luau/functions) Default Value: nil An optional comparison function to be used when comparing elements in the table. This function receives two elements, and should return true if the first element should be sorted before the second in the final order. |

Returns

()

Sorts elements of array t in a given order, from t[1] to t[#t]. If
comp is given, then it must be a function that receives two elements and
returns true when the first element must come before the second in the
final order.

The error invalid order function for sorting is thrown if both
comp(a, b) and comp(b, a) return true.

If comp is not given, then the standard Luau operator < is used
instead.

Provide feedback

---

unpack

Returns all elements from the given list as a tuple.

table.unpack(

list:[table](/docs/luau/tables), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| list:[table](/docs/luau/tables)  The list of elements to be unpacked. |
| i:[number](/docs/luau/numbers) Default Value: 1 The index of the first element to unpack. |
| j:[number](/docs/luau/numbers) Default Value: #list The index of the last element to unpack. |

Returns

[Tuple](/docs/luau/tuples)

Returns the elements from the given list. By default, i is 1 and j is
the length of list.

Note that this same functionality is also provided by the global
[unpack()](/docs/reference/engine/globals/LuaGlobals#unpack) function.

Provide feedback

---