# utf8 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/utf8
Scraped: 2026-01-11T02:49:47.609859Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [utf8](/docs/reference/engine/libraries/utf8)

English

Feedback

Engine Library

utf8

This library provides basic support for UTF-8 encoding.

---

Summary

Functions

|  |
| --- |
| [char](#char)(codepoints: [Tuple](/docs/luau/tuples)<[number](/docs/luau/numbers)>):[string](/docs/luau/strings) |
| [codes](#codes)(str: [string](/docs/luau/strings)):[function](/docs/luau/functions),[string](/docs/luau/strings),[number](/docs/luau/numbers) |
| [codepoint](#codepoint)(str: [string](/docs/luau/strings),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples)<[number](/docs/luau/numbers)> |
| [len](#len)(s: [string](/docs/luau/strings),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [offset](#offset)(s: [string](/docs/luau/strings),n: [number](/docs/luau/numbers),i: [number](/docs/luau/numbers)):[number](/docs/luau/numbers)? |
| [graphemes](#graphemes)(str: [string](/docs/luau/strings),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):[function](/docs/luau/functions) |
| [nfcnormalize](#nfcnormalize)(str: [string](/docs/luau/strings)):[string](/docs/luau/strings) |
| [nfdnormalize](#nfdnormalize)(str: [string](/docs/luau/strings)):[string](/docs/luau/strings) |

Properties

|  |
| --- |
| [charpattern](#charpattern):[string](/docs/luau/strings) |

This library provides basic support for UTF-8 encoding. This library does
not provide any support for Unicode other than the handling of the encoding.
Any operation that needs the meaning of a character, such as character
classification, is outside its scope.

Unless stated otherwise, all functions that expect a byte position as a
parameter assume that the given position is either the start of a byte
sequence or one plus the length of the subject string. As in the string
library, negative indices count from the end of the string.

You can find a large catalog of usable UTF-8 characters
[here](https://www.w3schools.com/charsets/ref_html_utf8.asp).

---

API Reference

Functions

char

Converts zero or more codepoints to UTF-8 byte sequences.

utf8.char(codepoints:[Tuple](/docs/luau/tuples)<[number](/docs/luau/numbers)>):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| codepoints:[Tuple](/docs/luau/tuples)<[number](/docs/luau/numbers)> |

Returns

[string](/docs/luau/strings)

Receives zero or more codepoints as integers, converts each one to its
corresponding UTF-8 byte sequence and returns a string with the
concatenation of all these sequences.

Provide feedback

---

codes

Returns an iterator function that iterates over all codepoints in a given
string.

utf8.codes(str:[string](/docs/luau/strings)):[function](/docs/luau/functions),[string](/docs/luau/strings),[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| str:[string](/docs/luau/strings)  The string to iterate over. |

Returns

[function](/docs/luau/functions), [string](/docs/luau/strings), [number](/docs/luau/numbers)

Returns an iterator function so that the construction:

```
for position, codepoint in utf8.codes(str) do



-- body



end
```

will iterate over all codepoints in string str. It raises an error if it
meets any invalid byte sequence.

Provide feedback

---

codepoint

Returns the codepoints (as integers) from all codepoints in a given
string.

utf8.codepoint(

str:[string](/docs/luau/strings), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):[Tuple](/docs/luau/tuples)<[number](/docs/luau/numbers)>

Parameters

|  |
| --- |
| str:[string](/docs/luau/strings) |
| i:[number](/docs/luau/numbers) Default Value: 1 The index of the codepoint that should be fetched from this string. |
| j:[number](/docs/luau/numbers) Default Value: i The index of the last codepoint between i and j that will be returned. If excluded, this will default to the value of i. |

Returns

[Tuple](/docs/luau/tuples)<[number](/docs/luau/numbers)>

Returns the codepoints (as integers) from all codepoints in the provided
string (str) that start between byte positions i and j (both
included). The default for i is 1 and for j is i. It raises an
error if it meets any invalid byte sequence.

Provide feedback

---

len

Returns the number of UTF-8 codepoints in a given string.

utf8.len(

s:[string](/docs/luau/strings), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |
| i:[number](/docs/luau/numbers) Default Value: 1 The starting position. |
| j:[number](/docs/luau/numbers) Default Value: -1 The ending position. |

Returns

[number](/docs/luau/numbers)

Returns the number of UTF-8 codepoints in the string *str* that start
between positions i and j (both inclusive). The default for i is 1
and for j is -1. If it finds any invalid byte sequence, returns a nil
value plus the position of the first invalid byte.

Provide feedback

---

offset

Returns the position (in bytes) where the encoding of the n‑th codepoint
of s (counting from byte position i) starts.

utf8.offset(

s:[string](/docs/luau/strings), n:[number](/docs/luau/numbers), i:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)?

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |
| n:[number](/docs/luau/numbers) |
| i:[number](/docs/luau/numbers) Default Value: 1 |

Returns

[number](/docs/luau/numbers)?

Returns the position (in bytes) where the encoding of the n‑th codepoint
of s (counting from byte position i) starts. A negative n gets
characters before position i. The default for i is 1 when n is
non-negative and #s + 1 otherwise, so that utf8.offset(s, -n) gets the
offset of the n‑th character from the end of the string. If the
specified character is neither in the subject nor right after its end, the
function returns nil.

Provide feedback

---

graphemes

Returns an iterator function that iterates over the grapheme clusters of a
given string.

utf8.graphemes(

str:[string](/docs/luau/strings), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):[function](/docs/luau/functions)

Parameters

|  |
| --- |
| str:[string](/docs/luau/strings) |
| i:[number](/docs/luau/numbers) |
| j:[number](/docs/luau/numbers) |

Returns

[function](/docs/luau/functions)

Returns an iterator function so that

```
for first, last in utf8.graphemes(str) do



local grapheme = s:sub(first, last)



-- body



end
```

will iterate the grapheme clusters of the string.

Provide feedback

---

nfcnormalize

Converts the input string to Normal Form C.

utf8.nfcnormalize(str:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| str:[string](/docs/luau/strings) |

Returns

[string](/docs/luau/strings)

Converts the input string to Normal Form C, which tries to convert
decomposed characters into composed characters.

Provide feedback

---

nfdnormalize

Converts the input string to Normal Form D.

utf8.nfdnormalize(str:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| str:[string](/docs/luau/strings)  The string to convert. |

Returns

[string](/docs/luau/strings)

Converts the input string to Normal Form D, which tries to break up
composed characters into decomposed characters.

Provide feedback

---

Properties

charpattern

The pattern "[%z\x01-\x7F\xC2-\xF4][\x80-\xBF]\*", which matches exactly
zero or more UTF-8 byte sequences, assuming that the subject is a valid
UTF-8 string.

utf8.charpattern:[string](/docs/luau/strings)

The pattern "[%z\x01-\x7F\xC2-\xF4][\x80-\xBF]\*", which matches exactly
zero or more UTF-8 byte sequence, assuming that the subject is a valid
UTF-8 string.

Provide feedback

---