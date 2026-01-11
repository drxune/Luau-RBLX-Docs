# SharedTable | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/SharedTable
Scraped: 2026-01-11T02:42:33.333386Z

## Inherits
- Actor
- SharedTableRegistry
- Actor:SendMessage()
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [SharedTable](/docs/reference/engine/datatypes/SharedTable)

English

Feedback

Engine Data Type

SharedTable

Provides sharable, table-like storage for key/value pairs.

---

Summary

Constructors

|  |
| --- |
| [new](#new)() |
| [new](#new-t)(t: [table](/docs/luau/tables)) |

Functions

|  |
| --- |
| [clear](#clear)(st: [SharedTable](/docs/reference/engine/datatypes/SharedTable)):() |
| [clone](#clone)(st: [SharedTable](/docs/reference/engine/datatypes/SharedTable),deep: [boolean](/docs/luau/booleans)?):[SharedTable](/docs/reference/engine/datatypes/SharedTable) |
| [cloneAndFreeze](#cloneAndFreeze)(st: [SharedTable](/docs/reference/engine/datatypes/SharedTable),deep: [boolean](/docs/luau/booleans)?):[SharedTable](/docs/reference/engine/datatypes/SharedTable) |
| [increment](#increment)(st: [SharedTable](/docs/reference/engine/datatypes/SharedTable),key: [string](/docs/luau/strings) | [number](/docs/luau/numbers),delta: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [isFrozen](#isFrozen)(st: [SharedTable](/docs/reference/engine/datatypes/SharedTable)):[boolean](/docs/luau/booleans) |
| [size](#size)(st: [SharedTable](/docs/reference/engine/datatypes/SharedTable)):[number](/docs/luau/numbers) |
| [update](#update)(st: [SharedTable](/docs/reference/engine/datatypes/SharedTable),key: [string](/docs/luau/strings) | [number](/docs/luau/numbers),f: [function](/docs/luau/functions)):() |

Represents a table-like data structure that can be shared across execution
contexts. While it can be used for various sorts of general data storage, it
is designed especially for use with
[Parallel Luau](/docs/scripting/multithreading), where it can be used to
share state across scripts parented under different [Actor](/docs/reference/engine/classes/Actor) instances.

There are a couple idiomatic ways to communicate shared tables between
scripts. One method is to store and retrieve [SharedTable](/docs/reference/engine/datatypes/SharedTable) objects in
the [SharedTableRegistry](/docs/reference/engine/classes/SharedTableRegistry). The registry lets any script in the same data
model get or set a [SharedTable](/docs/reference/engine/datatypes/SharedTable) by name. Another method is to use
[Actor:SendMessage()](/docs/reference/engine/classes/Actor#SendMessage) to send a shared table to another [Actor](/docs/reference/engine/classes/Actor)
inside a message.

Like a Luau table, a [SharedTable](/docs/reference/engine/datatypes/SharedTable) object stores a set of key-value
element pairs. Unlike a Luau table, only selected types of objects may be
stored in a SharedTable, similar to other restrictions you'll find elsewhere
in the Roblox Engine.

Keys must either be (1) a string or (2) a nonnegative integer number less than
232. Other kinds of keys are not supported.

Values must have one of the following types: Boolean, Number, Vector, String,
[SharedTable](/docs/reference/engine/datatypes/SharedTable), or a serializable data type. The ability to store a
[SharedTable](/docs/reference/engine/datatypes/SharedTable) as a value in another [SharedTable](/docs/reference/engine/datatypes/SharedTable) permits
the construction of nested and recursive data structures.

[SharedTable](/docs/reference/engine/datatypes/SharedTable) objects are distinct and different
[SharedTable](/docs/reference/engine/datatypes/SharedTable) objects never compare equal, even if they have contents
that would compare equal.

Like a Luau table, a [SharedTable](/docs/reference/engine/datatypes/SharedTable) object may be frozen, in which
case it is read-only. An attempt to modify a frozen [SharedTable](/docs/reference/engine/datatypes/SharedTable)
will raise an error. A frozen [SharedTable](/docs/reference/engine/datatypes/SharedTable) can be created by first
creating a (non-frozen, modifiable) [SharedTable](/docs/reference/engine/datatypes/SharedTable) with the desired
contents, and then calling [SharedTable.cloneAndFreeze()](/docs/reference/engine/datatypes/SharedTable#cloneAndFreeze) to create a
frozen clone of it.

Code Samples

Element Access

Elements in a [SharedTable](/docs/reference/engine/datatypes/SharedTable) are accessed in the same way as
elements of Luau tables, using the st[k] syntax or, for string keys,
st.k.

```
local st = SharedTable.new()



st[1] = "a"



st["x"] = true



st.y = 5



assert(st[1] == "a")



assert(st["x"] == true)



assert(st.x == true)



assert(st["y"] == 5)



assert(st.y == 5)



-- true is not a valid SharedTable key, so attempting to set that key



-- fails:



assert(not pcall(function() st[true] = 100 end))



-- A function is not a valid SharedTable value, so attempting to set a



-- value to a function fails:



assert(not pcall(function() st["f"] = function() end end))
```

Element Iteration

The for loop can be used to iterate over the elements of a
[SharedTable](/docs/reference/engine/datatypes/SharedTable). The elements of the [SharedTable](/docs/reference/engine/datatypes/SharedTable) are not
iterated directly. Instead, a shallow clone is made of the
[SharedTable](/docs/reference/engine/datatypes/SharedTable), and its elements are iterated. This is done to ensure
that a consistent view of the [SharedTable](/docs/reference/engine/datatypes/SharedTable) is maintained throughout
the iteration. Thus, both of the following for loops have the same behavior.

Note that this means that if the [SharedTable](/docs/reference/engine/datatypes/SharedTable) is accessed directly
from within the body of the iteration loop, its state may not be consistent
with the state observed through the iteration.

The iteration order is partially specified. Elements with numeric keys are
iterated before elements with string keys. Elements with numeric keys are
iterated in ascending numeric order. Elements with string keys are iterated
in an unspecified order.

```
local st = SharedTable.new({"a", "b", "c"})



for k, v in SharedTable.clone(st, false) do



print(k, ": ", v)



end



for k, v in st do



print(k, ": ", v)



end
```

---

API Reference

Constructors

new

Returns a new, empty [SharedTable](/docs/reference/engine/datatypes/SharedTable).

SharedTable.new()

Returns a new, empty [SharedTable](/docs/reference/engine/datatypes/SharedTable).

```
local st = SharedTable.new()
```

Provide feedback

---

new

Returns a new [SharedTable](/docs/reference/engine/datatypes/SharedTable) containing elements equivalent to
those in the provided Luau table.

SharedTable.new(t:[table](/docs/luau/tables))

Parameters

|  |
| --- |
| t:[table](/docs/luau/tables)  The Luau table whose elements are to be stored in the new [SharedTable](/docs/reference/engine/datatypes/SharedTable). |

Returns a new [SharedTable](/docs/reference/engine/datatypes/SharedTable) containing elements equivalent to
those in the provided Luau table.

If the provided Luau table contains any keys or values that cannot be
stored in a [SharedTable](/docs/reference/engine/datatypes/SharedTable), construction of the
[SharedTable](/docs/reference/engine/datatypes/SharedTable) fails. See the summary at the top of this page for
a list of types of objects that can be stored in a [SharedTable](/docs/reference/engine/datatypes/SharedTable).
If the Luau table contains any table as a value, that table is converted
into a new [SharedTable](/docs/reference/engine/datatypes/SharedTable).

```
local t = {}



t.x = 1



t.y = 2



t.z = {"a", "b", "c"}



local st = SharedTable.new(t)



assert(st.x == 1)



assert(st.y == 2)



assert(st.z[1] == "a")



assert(st.z[2] == "b")



assert(st.z[3] == "c")
```

Note that in some cases it may be desirable to store a [SharedTable](/docs/reference/engine/datatypes/SharedTable) in the [SharedTableRegistry](/docs/reference/engine/classes/SharedTableRegistry). The Class.ShareTableRegistry:GetSharedTable() method provides a convenient way to accomplish this.

Provide feedback

---

Functions

clear

Removes all of the elements from the [SharedTable](/docs/reference/engine/datatypes/SharedTable).

SharedTable.clear(st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)):()

Parameters

|  |
| --- |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)  The [SharedTable](/docs/reference/engine/datatypes/SharedTable) to clear. |

Returns

()

Atomically removes all of the elements from a [SharedTable](/docs/reference/engine/datatypes/SharedTable).

If the [SharedTable](/docs/reference/engine/datatypes/SharedTable) is frozen, the operation fails and an error
will be raised.

```
local st = SharedTable.new({"a", "b", "c"})



assert(SharedTable.size(st) == 3)



SharedTable.clear(st)



assert(SharedTable.size(st) == 0)
```

Provide feedback

---

clone

Creates and returns a clone of the provided [SharedTable](/docs/reference/engine/datatypes/SharedTable).

SharedTable.clone(

st:[SharedTable](/docs/reference/engine/datatypes/SharedTable), deep:[boolean](/docs/luau/booleans)?

):[SharedTable](/docs/reference/engine/datatypes/SharedTable)

Parameters

|  |
| --- |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)  The [SharedTable](/docs/reference/engine/datatypes/SharedTable) object to clone. |
| deep:[boolean](/docs/luau/booleans)? Default Value: false Whether to create a deep clone (true) or a shallow clone (false). |

Returns

[SharedTable](/docs/reference/engine/datatypes/SharedTable)

Creates a clone of a [SharedTable](/docs/reference/engine/datatypes/SharedTable) and returns the clone.

If the optional deep argument is not present, or if it is present and
its value is false, then a shallow clone is created. A shallow clone
copies only the top-level [SharedTable](/docs/reference/engine/datatypes/SharedTable) object. If any value in
the [SharedTable](/docs/reference/engine/datatypes/SharedTable) itself is a [SharedTable](/docs/reference/engine/datatypes/SharedTable), then both
the original [SharedTable](/docs/reference/engine/datatypes/SharedTable) and the clone [SharedTable](/docs/reference/engine/datatypes/SharedTable)
will refer to the same [SharedTable](/docs/reference/engine/datatypes/SharedTable).

The shallow clone operation is atomic, so the clone [SharedTable](/docs/reference/engine/datatypes/SharedTable)
will contain a consistent snapshot of the state in the original
[SharedTable](/docs/reference/engine/datatypes/SharedTable), even if it is being modified concurrently from
other scripts.

If the optional deep argument is present and its value is true, then a
deep clone is created. A deep clone recursively copies a structure of
[SharedTable](/docs/reference/engine/datatypes/SharedTable) objects, such that there is no state shared between
the original [SharedTable](/docs/reference/engine/datatypes/SharedTable) and the clone.

The clone of each [SharedTable](/docs/reference/engine/datatypes/SharedTable) within the graph of
[SharedTable](/docs/reference/engine/datatypes/SharedTable) objects is atomic, but the deep clone as a whole is
not atomic. Thus, the clone of each [SharedTable](/docs/reference/engine/datatypes/SharedTable) within the
graph will contain a consistent snapshot of the state of the original
[SharedTable](/docs/reference/engine/datatypes/SharedTable) object from which it was cloned, but the states of
different [SharedTable](/docs/reference/engine/datatypes/SharedTable) objects may be inconsistent if the graph
is being modified concurrently from other scripts.

The [SharedTable](/docs/reference/engine/datatypes/SharedTable) object(s) being cloned may be frozen
(read-only) or not. Regardless, the newly created clones are *not* frozen
(and are thus modifiable). To create frozen clones, use the
[SharedTable.cloneAndFreeze](/docs/reference/engine/datatypes/SharedTable#cloneAndFreeze) function.

To illustrate the difference between a shallow clone and a deep clone,
consider the following samples. This first sample creates a shallow clone
and the second creates a deep clone.

Provide feedback

---

cloneAndFreeze

Creates and returns a frozen (read-only) clone of the provided
[SharedTable](/docs/reference/engine/datatypes/SharedTable).

SharedTable.cloneAndFreeze(

st:[SharedTable](/docs/reference/engine/datatypes/SharedTable), deep:[boolean](/docs/luau/booleans)?

):[SharedTable](/docs/reference/engine/datatypes/SharedTable)

Parameters

|  |
| --- |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)  The SharedTable object to clone. |
| deep:[boolean](/docs/luau/booleans)? Default Value: false Whether to create a deep clone (true) or a shallow clone (false). |

Returns

[SharedTable](/docs/reference/engine/datatypes/SharedTable)

Creates a frozen (read-only) clone of a [SharedTable](/docs/reference/engine/datatypes/SharedTable) and returns
the clone. The behavior of this function is the same as the behavior of
clone, except that the clone is frozen.

If a deep clone is requested, then all of the cloned
[SharedTable](/docs/reference/engine/datatypes/SharedTable) objects are frozen.

Provide feedback

---

increment

Adds delta to the value with the provided key and returns the original
value.

SharedTable.increment(

st:[SharedTable](/docs/reference/engine/datatypes/SharedTable), key:[string](/docs/luau/strings) | [number](/docs/luau/numbers), delta:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)  The [SharedTable](/docs/reference/engine/datatypes/SharedTable) object to be updated. |
| key:[string](/docs/luau/strings) | [number](/docs/luau/numbers)  The key of the element in the [SharedTable](/docs/reference/engine/datatypes/SharedTable) object to be updated. |
| delta:[number](/docs/luau/numbers)  The value to be added to the element in the [SharedTable](/docs/reference/engine/datatypes/SharedTable). |

Returns

[number](/docs/luau/numbers)

The original value of the element, before delta was added to it.

Atomically increments the value of an element. An element with the
specified key must exist in the [SharedTable](/docs/reference/engine/datatypes/SharedTable), and it must be of
type number. The specified delta is added to the value, and the
original value is returned.

The SharedTable.update function can also be used for this purpose; this
increment function exists for convenience and performance (in general,
increment is much faster than update, so it should be preferred where
possible). The following two function calls have the same effect:

```
local st = SharedTable.new()



st["x"] = 1



local oldValue = SharedTable.increment(st, "x", 1)



SharedTable.update(st, "x", function(v)



oldValue = v



return v + 1



end)
```

If the [SharedTable](/docs/reference/engine/datatypes/SharedTable) is frozen, the operation fails and an error
will be raised.

Provide feedback

---

isFrozen

Returns true if the [SharedTable](/docs/reference/engine/datatypes/SharedTable) is frozen (read-only).

SharedTable.isFrozen(st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)  The [SharedTable](/docs/reference/engine/datatypes/SharedTable) object whose frozen state is to be queried. |

Returns

[boolean](/docs/luau/booleans)

Returns true if the [SharedTable](/docs/reference/engine/datatypes/SharedTable) is frozen (read-only).

```
local st1 = SharedTable.new({"a", "b", "c"})



assert(not SharedTable.isFrozen(st1))



local st2 = SharedTable.cloneAndFreeze(st1)



assert(SharedTable.isFrozen(st2))
```

Provide feedback

---

size

Returns the number of elements stored in the [SharedTable](/docs/reference/engine/datatypes/SharedTable).

SharedTable.size(st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)  The [SharedTable](/docs/reference/engine/datatypes/SharedTable) object whose size is to be queried. |

Returns

[number](/docs/luau/numbers)

Returns the number of elements stored in the SharedTable. Note that if
other scripts are concurrently modifying the SharedTable, the returned
size may no longer be correct after it is returned, since other scripts
may have added or removed elements from the SharedTable.

```
local st = SharedTable.new({"a", "b", "c"})



assert(SharedTable.size(st) == 3)



st[2] = nil



assert(SharedTable.size(st) == 2)
```

Provide feedback

---

update

Updates the value with the provided key via the provided update function.

SharedTable.update(

st:[SharedTable](/docs/reference/engine/datatypes/SharedTable), key:[string](/docs/luau/strings) | [number](/docs/luau/numbers), f:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| st:[SharedTable](/docs/reference/engine/datatypes/SharedTable)  The [SharedTable](/docs/reference/engine/datatypes/SharedTable) object to be updated. |
| key:[string](/docs/luau/strings) | [number](/docs/luau/numbers)  The key of the element in the [SharedTable](/docs/reference/engine/datatypes/SharedTable) object to be updated. |
| f:[function](/docs/luau/functions)  The function that will be called to compute the new value for the element. |

Returns

()

Atomically updates the value of an element.

When a [SharedTable](/docs/reference/engine/datatypes/SharedTable) is accessed concurrently from scripts
running in different execution contexts, it is possible for their accesses
to interleave unpredictably. Because of this, code like the following is
generally incorrect, because the value may have changed between the read
on the first line and the update on the second line:

```
local oldValue = st["x"]



st["x"] = oldValue .. ",x"
```

The update function makes it possible to perform an atomic update to an
element. It takes a function that it will call with the current value of
the element. The function can then compute and return the new value. Note
that the function may be called multiple times if the
[SharedTable](/docs/reference/engine/datatypes/SharedTable) is being concurrently modified from other scripts.

If the [SharedTable](/docs/reference/engine/datatypes/SharedTable) is frozen, the operation fails and an error
will be raised.

Provide feedback

---