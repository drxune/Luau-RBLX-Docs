# string | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/string
Scraped: 2026-01-11T02:50:04.616630Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [string](/docs/reference/engine/libraries/string)

English

Feedback

Engine Library

string

Provides generic functions to manipulate strings.

---

Summary

Functions

|  |
| --- |
| [byte](#byte)(s: [string](/docs/luau/strings),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [char](#char)(...: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [find](#find)(s: [string](/docs/luau/strings),pattern: [string](/docs/luau/strings),init: [number](/docs/luau/numbers),plain: [boolean](/docs/luau/booleans)):[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [format](#format)(formatstring: [string](/docs/luau/strings),...: [string](/docs/luau/strings)):[string](/docs/luau/strings) |
| [gmatch](#gmatch)(s: [string](/docs/luau/strings),pattern: [string](/docs/luau/strings)):[function](/docs/luau/functions) |
| [gsub](#gsub)(s: [string](/docs/luau/strings),pattern: [string](/docs/luau/strings),replacement: Variant,replacements: [number](/docs/luau/numbers)):[string](/docs/luau/strings),[number](/docs/luau/numbers) |
| [len](#len)(s: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [lower](#lower)(s: [string](/docs/luau/strings)):[string](/docs/luau/strings) |
| [match](#match)(s: [string](/docs/luau/strings),pattern: [string](/docs/luau/strings),init: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [pack](#pack)(format: [string](/docs/luau/strings),...: Variant):[string](/docs/luau/strings) |
| [packsize](#packsize)(format: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [rep](#rep)(s: [string](/docs/luau/strings),n: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [reverse](#reverse)(s: [string](/docs/luau/strings)):[string](/docs/luau/strings) |
| [split](#split)(s: [string](/docs/luau/strings),separator: [string](/docs/luau/strings)):[table](/docs/luau/tables) |
| [sub](#sub)(s: [string](/docs/luau/strings),i: [number](/docs/luau/numbers),j: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [unpack](#unpack)(format: [string](/docs/luau/strings),data: [string](/docs/luau/strings),readStart: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [upper](#upper)(s: [string](/docs/luau/strings)):[string](/docs/luau/strings) |

The string library provides generic functions to manipulate strings, such as
to extract substrings or match patterns. You can access the string library by
the global [string](/docs/reference/engine/libraries/string) library.

See
[String pattern reference](/docs/luau/strings#string-pattern-reference)
for details on using [string.match()](/docs/reference/engine/libraries/string#match), [string.gmatch()](/docs/reference/engine/libraries/string#gmatch), and
[string.gsub()](/docs/reference/engine/libraries/string#gsub) to find (and replace) substrings.

---

API Reference

Functions

byte

Returns the internal numerical codes of the characters
s[i], s[i+1], ..., s[j]. The default value for i is 1; the default
value for j is i. These indices are corrected following the same rules
of function string.sub.

string.byte(

s:[string](/docs/luau/strings), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |
| i:[number](/docs/luau/numbers) Default Value: 1 |
| j:[number](/docs/luau/numbers) Default Value: i |

Returns

[number](/docs/luau/numbers)

Returns the internal numerical codes of the characters
s[i], s[i+1], ..., s[j]. The default value for i is 1; the default
value for j is i. These indices are corrected following the same rules
of function [string.sub()](/docs/reference/engine/libraries/string#sub).

Provide feedback

---

char

Receives zero or more integers and returns a string with length equal to
the number of arguments, in which each character has the internal
numerical code equal to its corresponding argument.

string.char(...:[number](/docs/luau/numbers)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| ...:[number](/docs/luau/numbers) |

Returns

[string](/docs/luau/strings)

Receives zero or more integers and returns a string with length equal to
the number of arguments, in which each character has the internal
numerical code equal to its corresponding argument.

Provide feedback

---

find

Looks for the first match of pattern in the string s and returns the
indices of s where the occurrence starts and ends.

string.find(

s:[string](/docs/luau/strings), pattern:[string](/docs/luau/strings), init:[number](/docs/luau/numbers), plain:[boolean](/docs/luau/booleans)

):[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings)  The string to search within. |
| pattern:[string](/docs/luau/strings)  The pattern to search for in given string. |
| init:[number](/docs/luau/numbers) Default Value: 1 The starting index for the search. |
| plain:[boolean](/docs/luau/booleans) Default Value: false |

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers)

The starting index of the match.

The ending index of the match.

Searches for the first occurrence of a pattern in a string and returns the
start and end indices of the match. If no match is found, it returns
nil. You can specify where to start the search using the optional init
parameter which defaults to 1 and can be negative. An optional plain
parameter turns off pattern matching, so the function performs a plain
substring search; note that if you use plain, you must also provide
init.

```
-- Example 1: Basic usage



local s = "Hello, world!"



local pattern = "world"



local start_index, end_index = string.find(s, pattern)



print(start_index, end_index)  -- Output: 8 12
```

```
-- Example 2: Using init parameter



local s = "Hello, world! Hello, Roblox!"



local pattern = "Hello"



local start_index, end_index = string.find(s, pattern, 10)



print(start_index, end_index)  -- Output: 15 19
```

```
-- Example 3: Using plain parameter



local s = "Hello, world! (Hello)"



local pattern = "(Hello)"



local start_index, end_index = string.find(s, pattern, 1, true)



print(start_index, end_index)  -- Output: 14 20
```

```
-- Example 4: No Pattern found



local s = "Hello, world!"



local pattern = "Roblox"



local start_index, end_index = string.find(s, pattern)



print(start_index, end_index)  -- Output: nil
```

Provide feedback

---

format

Returns a formatted version of its variable number of arguments following
the description given in its first argument, which must be a string.

string.format(

formatstring:[string](/docs/luau/strings), ...:[string](/docs/luau/strings)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| formatstring:[string](/docs/luau/strings) |
| ...:[string](/docs/luau/strings) |

Returns

[string](/docs/luau/strings)

Returns a formatted version of its variable number of arguments following
the description given in its first argument, which must be a string.

You can convert variables into user-friendly strings of text using the
[string.format()](/docs/reference/engine/libraries/string#format) function. The function requires the following
format:

%[flags][width].[precision][specifier].

#### Specifiers

The most important part of string formatting is the specifiers.

| Specifier | Accepts | Outputs | Example Output |
| --- | --- | --- | --- |
| c | integer |  | 3 |
| d or i | integer | Decimal representation. | 321 |
| e or E | float | Scientific notation using e or E. | 3.296e2 3.296E2 |
| f | float |  | 3231.1231 |
| g or G | float | The shorter of e/E and f. | 3E14 3e14 |
| o | integer | Octal representation. | 610 |
| q | string | String in a form suitable to be safely read back by the Luau interpreter. The string is written between double quotes and all double quotes, new lines, embedded zeros, and backslashes are correctly escaped. | "print(\"Hi\")" |
| s | string |  | Hello world! |
| u | integer | Decimal representation. | 3131 |
| x or X | integer | Hexadecimal representation. | 7fa 7FA |
| \* | any | Equivalent to s but accepts any variable by converting it to a string using [tostring()](/docs/reference/engine/globals/LuaGlobals#tostring). | table: 0x0123456789abcdef |
| % |  | % followed by another % will return the % sign itself. | % |

```
local str = "The magic word is %s"



print(string.format(str, "Roblox"))



-- The magic word is Roblox



local str = "The magic word is %q"



print(string.format(str, "Roblox"))



-- The magic word is "Roblox"



local str = "Skip to \na new line and \nanother new line!"



print(string.format(str, "%q"))



--[[ Output:



Skip to



a new line and



another new line!



]]
```

#### Flags

| Flag | Description |
| --- | --- |
| - | Left-justify the given field width (see Width below). Right justification is the default. |
| + | Forces a "+" sign to precede a number. Has no effect on negative numbers. |
| (space) | One blank space is inserted before a positive number, while negative numbers are unaffected. This is useful for making positive and negative numbers vertically align in a visual stacked list. |
| # | When used with o and x/X, writes a 0 (octal) or 0x/0X (hex) before values other than zero. When used with e/E and f, forces the output to contain a decimal point, even if no digits would follow (by default, no decimal point is written if no digits follow). When used with g or G, the result is the same as with e or E but trailing zeros are not removed. |
| 0 | Left-pads the number with zeros instead of empty spaces (see Width below). |

```
local str = "%-10d"



print(string.format(str, 300) .. "]")



-- 300       ]



-- There are 7 spaces between '300' and ']'



local str = "%+i versus %+i"



print(string.format(str, 300, -300)) -- +300 versus -300



local str = "There is a% i%% chance of rain in Seattle today."



print(string.format(str, 100))



-- There is a 100% chance of rain in Seattle today.
```

#### Width

| Width | Description |
| --- | --- |
| (number) | Minimum number of characters to return. If the number of characters to be formatted is less than this number, the result is padded with blank spaces. |

```
local str = "%012i"



print("Score: " .. string.format(str, 15000))



-- Output: Score: 000000015000



-- The output has 12 digits total, left-padded with zeros
```

#### Precision

The default precision is 1. If you give a period without a value, the
default is 0.

| Precision | Description |
| --- | --- |
| .(number) | For integer specifiers (d, i, o, u, x/X), precision specifies the minimum number of digits to be returned. If the value to be formatted is shorter than this number, the result is padded with leading zeros. A precision of 0 means that no character is written for the value 0. For e/E and f specifiers, this is the number of digits to be printed after the decimal point. For g/G specifiers, this is the maximum number of digits (before the e/E, if present). For s, this is the maximum number of characters to be returned. For c and q, this has no effect. |

```
-- Add decimal with precision of 2 for a currency output



local str = "$%.2f"



print(string.format(str, 300)) -- Output: $300.00



-- Return first 6 letters of a string



local str = "%.6s"



print(string.format(str, "Robloxian")) -- Output: Roblox



local str = "Once upon a time, there was a dragon named %s and it had %.8f horns."



print(string.format(str, "Pi", math.pi))



-- Output: Once upon a time, there was a dragon named Pi and it had 3.14159265 horns.
```

Provide feedback

---

gmatch

Returns an iterator function that returns the next captures from pattern
over the string s each time it's called.

string.gmatch(

s:[string](/docs/luau/strings), pattern:[string](/docs/luau/strings)

):[function](/docs/luau/functions)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |
| pattern:[string](/docs/luau/strings) |

Returns

[function](/docs/luau/functions)

Returns an iterator function that returns the next captures from pattern
over the string s each time it's called.

Provide feedback

---

gsub

Returns a copy of s in which all or the first n occurrences of the
pattern are replaced with the given replacement. The second value returned
is the total number of substitutions made.

string.gsub(

s:[string](/docs/luau/strings), pattern:[string](/docs/luau/strings), replacement:Variant, replacements:[number](/docs/luau/numbers)

):[string](/docs/luau/strings),[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings)  The string whose occurrences of the given pattern shall be replaced. |
| pattern:[string](/docs/luau/strings)  The pattern to be matched and replaced. |
| replacement:Variant  Determines what should replace the occurrence(s) of the given pattern. |
| replacements:[number](/docs/luau/numbers)  The maximum number of substitutions to make. |

Returns

[string](/docs/luau/strings), [number](/docs/luau/numbers)

Short for global substitution. Returns a copy of s in which all (or the
first n, if given) occurrences of the pattern are substituted (replaced)
with the given replacement. The second value returned is the total
number of substitutions made.

The replacement can be one of several types, each used differently to
determine the actual string:

* string: The pattern is replaced with the string directly
* table: The string that matched the pattern is looked up in the table as
  a key, and the value (string) is what replaces it, if it exists.
* function: Called with the string that matched the pattern, should return
  the string to replace the matched pattern.

An optional final argument can be provided which specifies the maximum
number of substitutions to make (for example, stop after 2 replacements)

#### Various Examples

```
-- Basic replacement



string.gsub("I love tacos!", "tacos", "Roblox") --> I love Roblox! 1



-- Replacement with a pattern



string.gsub("I like red!", "%w+", "word") --> word word word! 3



-- Replacement table



string.gsub("I play Roblox.", "%w+", {I="Je", play="joue à"}) --> Je joue à Roblox. 3



-- Replacement function



string.gsub("I have 2 cats.", "%d+", function(n) return tonumber(n) * 12 end) --> I have 24 cats. 1



-- Replace only twice



string.gsub("aaa", "a", "b", 2) --> bba 2



-- Replacement with capture groups (maximum of nine)



string.gsub("love2play Roblox", "(%w+)(%d+)(%w+)%s+(%w+)", "I %1 %2 %3 %4!") --> I love 2 play Roblox! 1
```

Provide feedback

---

len

Returns the length of a string.

string.len(s:[string](/docs/luau/strings)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |

Returns

[number](/docs/luau/numbers)

Returns the length of a string.

Provide feedback

---

lower

Returns a copy of a string with all uppercase letters changed to
lowercase.

string.lower(s:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |

Returns

[string](/docs/luau/strings)

Returns a copy of a string with all uppercase letters changed to
lowercase.

Provide feedback

---

match

Looks for the first match of pattern in the string s. If a match is
found, it is returned; otherwise, it returns nil. A third, optional
numerical argument, init, specifies where to start the search.

string.match(

s:[string](/docs/luau/strings), pattern:[string](/docs/luau/strings), init:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |
| pattern:[string](/docs/luau/strings) |
| init:[number](/docs/luau/numbers) Default Value: 1 |

Returns

[string](/docs/luau/strings)

Looks for the first match of pattern in the string s. If a match is
found, it is returned; otherwise, it returns nil. A third, optional
numerical argument, init, specifies where to start the search; its default
value is 1 and can be negative.

Provide feedback

---

pack

Returns a binary string containing the provided arguments.

string.pack(

format:[string](/docs/luau/strings), ...:Variant

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| format:[string](/docs/luau/strings) |
| ...:Variant |

Returns

[string](/docs/luau/strings)

Returns a binary string containing the provided arguments. The first
argument, format, determines the way the remaining arguments are packed;
see [here](https://www.lua.org/manual/5.3/manual.html#6.4.2) for options.

Provide feedback

---

packsize

Returns the size in bytes of any string packed with a given description.

string.packsize(format:[string](/docs/luau/strings)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| format:[string](/docs/luau/strings) |

Returns

[number](/docs/luau/numbers)

Returns the size in bytes of any string packed with a given description.
The sole argument, format, determines the way the remaining arguments
are packed, but you cannot use s and z because they have variable
lengths. See [here](https://www.lua.org/manual/5.3/manual.html#6.4.2) for
options.

Provide feedback

---

rep

Returns a string that is the concatenation of n copies of the string
s.

string.rep(

s:[string](/docs/luau/strings), n:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |
| n:[number](/docs/luau/numbers) |

Returns

[string](/docs/luau/strings)

Returns a string that is the concatenation of n copies of the string
s.

Provide feedback

---

reverse

Returns a string that is the string s reversed.

string.reverse(s:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |

Returns

[string](/docs/luau/strings)

Returns a string that is the string s reversed.

Provide feedback

---

split

Splits a string into parts based on the defined separator character(s),
returning a table of ordered results.

string.split(

s:[string](/docs/luau/strings), separator:[string](/docs/luau/strings)

):[table](/docs/luau/tables)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings)  The string to split. |
| separator:[string](/docs/luau/strings) Default Value: , The separator character(s) to be used for splitting the string. |

Returns

[table](/docs/luau/tables)

Splits a string into parts based on the defined separator character(s),
returning a table of ordered results.

If an empty "slice" is located, that part will be returned as an empty
string. For instance string.split("abc||def", "|") will return a table
with three strings: "abc", "", and "def".

```
local values = input:split(",")



print(values[1], values[2], values[3])
```

Also note that whitespace from the original string will be preserved, for
example string.split("abc \_ def", "\_") will honor the whitespace on both
sides of the \_ separator. By default, the separator character is , but
you can specify an alternative character or series of characters.

Corner Cases

#### Empty String

```
"" --> ""
```

#### Empty Slices

```
"foo,,bar" --> "foo", "", "bar"



",foo" --> "", "foo"



"foo," --> "foo", ""



"," --> "", ""



",," --> "", "", ""
```

#### Whitespace Preserved

```
"   whitespace   " --> "   whitespace   "



"foo , bar" --> "foo ", " bar"
```

#### Invalid UTF-8

```
"\xFF" --> "\xFF"



"\xFD,\xFE" --> "\xFD", "\xFE"
```

#### Unicode

```
"，" --> U+FF0C FULLWIDTH COMMA



"我很高兴，你呢？" --> "我很高兴", "你呢？"



"•" --> U+2022 BULLET



"hello•world" --> "hello", "world"
```

Provide feedback

---

sub

Returns the substring of s that starts at i and continues until and
including j. i and j can be negative. i defaults to 1 and j
defaults to -1.

string.sub(

s:[string](/docs/luau/strings), i:[number](/docs/luau/numbers), j:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |
| i:[number](/docs/luau/numbers) Default Value: 1 |
| j:[number](/docs/luau/numbers) Default Value: -1 |

Returns

[string](/docs/luau/strings)

Returns the substring of s that starts at i and continues until and
including j. i and j can be negative. i defaults to 1 and j
defaults to -1.

Provide feedback

---

unpack

Extracts the values packed in the provided binary string.

string.unpack(

format:[string](/docs/luau/strings), data:[string](/docs/luau/strings), readStart:[string](/docs/luau/strings)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| format:[string](/docs/luau/strings) |
| data:[string](/docs/luau/strings) |
| readStart:[string](/docs/luau/strings) Default Value: 1 |

Returns

[Tuple](/docs/luau/tuples)

The values packed into the provided binary string, plus the index of
the first unread byte.

Extracts the values packed in the provided binary string based on the
first argument, format, which should match the one originally used to
[pack()](/docs/reference/engine/libraries/string#pack) the string; see
[here](https://www.lua.org/manual/5.3/manual.html#6.4.2) for options. The
optional third parameter determines the byte at which the reading starts.

Provide feedback

---

upper

Returns a copy of a string with all lowercase letters changed to
uppercase.

string.upper(s:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| s:[string](/docs/luau/strings) |

Returns

[string](/docs/luau/strings)

Returns a copy of a string with all lowercase letters changed to
uppercase.

Provide feedback

---