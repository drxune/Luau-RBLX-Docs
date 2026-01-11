# buffer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/buffer
Scraped: 2026-01-11T02:50:05.076552Z

## Inherits
- Actor
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [buffer](/docs/reference/engine/libraries/buffer)

English

Feedback

Engine Library

buffer

A library of buffer functions.

---

Summary

Functions

|  |
| --- |
| [create](#create)(size: [number](/docs/luau/numbers)):[buffer](/docs/reference/engine/libraries/buffer) |
| [fromstring](#fromstring)(str: [string](/docs/luau/strings)):[buffer](/docs/reference/engine/libraries/buffer) |
| [tostring](#tostring)(b: [buffer](/docs/reference/engine/libraries/buffer)):[string](/docs/luau/strings) |
| [len](#len)(b: [buffer](/docs/reference/engine/libraries/buffer)):[number](/docs/luau/numbers) |
| [readbits](#readbits)(b: [buffer](/docs/reference/engine/libraries/buffer),bitOffset: [number](/docs/luau/numbers),bitCount: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readi8](#readi8)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readu8](#readu8)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readi16](#readi16)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readu16](#readu16)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readi32](#readi32)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readu32](#readu32)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readf32](#readf32)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [readf64](#readf64)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [writebits](#writebits)(b: [buffer](/docs/reference/engine/libraries/buffer),bitOffset: [number](/docs/luau/numbers),bitCount: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writei8](#writei8)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writeu8](#writeu8)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writei16](#writei16)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writeu16](#writeu16)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writei32](#writei32)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writeu32](#writeu32)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writef32](#writef32)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [writef64](#writef64)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)):() |
| [readstring](#readstring)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),count: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [writestring](#writestring)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [string](/docs/luau/strings),count: [number](/docs/luau/numbers)?):() |
| [copy](#copy)(target: [buffer](/docs/reference/engine/libraries/buffer),targetOffset: [number](/docs/luau/numbers),source: [buffer](/docs/reference/engine/libraries/buffer),sourceOffset: [number](/docs/luau/numbers)?,count: [number](/docs/luau/numbers)?):() |
| [fill](#fill)(b: [buffer](/docs/reference/engine/libraries/buffer),offset: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers),count: [number](/docs/luau/numbers)?):() |

A buffer is an object that represents a fixed-size mutable block of memory.
The buffer library provides functions for creation and manipulation of buffer
objects, providing all its functions inside the global [buffer](/docs/reference/engine/libraries/buffer)
variable.

Buffer is intended to be used a low-level binary data storage structure,
replacing the uses of [string.pack()](/docs/reference/engine/libraries/string#pack) and [string.unpack()](/docs/reference/engine/libraries/string#unpack).
Use cases include reading and writing existing binary formats, working with
data in a more compact form, serialization to custom binary formats, and
general work with native memory types like fixed-length integers and floats.

When passed through Roblox APIs, including sending a buffer through custom
events, the identity of the buffer object is not preserved and the target will
receive a copy. Similar to other limitations, the same buffer object cannot be
used from multiple [Actor](/docs/reference/engine/classes/Actor) scripts (Parallel Luau).

Many of the functions accept an offset in bytes from the start of the buffer.
Offset of 0 from the start of the buffer memory block accesses the first
byte. All offsets, counts and sizes should be non-negative integer numbers. If
the bytes that are accessed by any read or write operation are outside the
buffer memory, an error is thrown.

The read and write methods that work with integers and floats use
[little-endian](https://en.wikipedia.org/wiki/Endianness) encoding.

---

API Reference

Functions

create

Creates a buffer.

buffer.create(size:[number](/docs/luau/numbers)):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| size:[number](/docs/luau/numbers)  Size of the buffer in bytes. Must be a positive integer. |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

Creates a buffer of the requested size with all bytes initialized to 0.
Size limit is 1 GiB, or 1,073,741,824 bytes. Keep in mind that larger
buffers might fail to allocate if device is running low on memory.

Provide feedback

---

fromstring

Creates a buffer from a string.

buffer.fromstring(str:[string](/docs/luau/strings)):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| str:[string](/docs/luau/strings) |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

Creates a buffer initialized to the contents of the string. The size of
the buffer equals the length of the string.

Provide feedback

---

tostring

Converts a buffer to a string.

buffer.tostring(b:[buffer](/docs/reference/engine/libraries/buffer)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |

Returns

[string](/docs/luau/strings)

Returns the buffer data as a string.

Provide feedback

---

len

Returns the size of the buffer in bytes.

buffer.len(b:[buffer](/docs/reference/engine/libraries/buffer)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |

Returns

[number](/docs/luau/numbers)

Returns the size of the buffer in bytes.

Provide feedback

---

readbits

Reads a range of bits into an unsigned integer from the buffer based on a
specific bitCount integer from 0 to 32, inclusive.

buffer.readbits(

b:[buffer](/docs/reference/engine/libraries/buffer), bitOffset:[number](/docs/luau/numbers), bitCount:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| bitOffset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| bitCount:[number](/docs/luau/numbers)  Integer bit count to read. Error is thrown if this value is not in range of 0 to 32, inclusive. |

Returns

[number](/docs/luau/numbers)

Reads a range of bits into an unsigned integer from the buffer based on a
specific bitCount integer from 0 to 32, inclusive. For example:

* buffer.readbits(b, 0, 8) is equivalent to
  [buffer.readu8(b, 0)](/docs/reference/engine/libraries/buffer#readu8).
* buffer.readbits(b, 0, 16) is equivalent to
  [buffer.readu16(b, 0)](/docs/reference/engine/libraries/buffer#readu16).
* buffer.readbits(b, 0, 32) is equivalent to
  [buffer.readu32(b, 0)](/docs/reference/engine/libraries/buffer#readu32).
* buffer.readbits(b, 0, 24) reads 24 bits from the buffer.

Note that 0 bit width is supported only to not error in generalized
cases where bit count is dynamic, and reading 0 bits returns 0. Also
note that, since the max size of the buffer is 1 GB, bitOffset
cannot be handled as a 32‑bit integer number like byte offset in other
buffer functions.

Provide feedback

---

readi8

Reads an 8-bit signed integer from the buffer.

buffer.readi8(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as an
8-bit signed integer and converting it into a number.

Provide feedback

---

readu8

Reads an 8-bit unsigned integer from the buffer.

buffer.readu8(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as an
8-bit unsigned integer and converting it into a number.

Provide feedback

---

readi16

Reads a 16-bit signed integer from the buffer.

buffer.readi16(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as a
16-bit signed integer and converting it into a number.

Provide feedback

---

readu16

Reads a 16-bit unsigned integer from the buffer.

buffer.readu16(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as a
16-bit unsigned integer and converting it into a number.

Provide feedback

---

readi32

Reads a 32-bit signed integer from the buffer.

buffer.readi32(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as a
32-bit signed integer and converting it into a number.

Provide feedback

---

readu32

Reads a 32-bit unsigned integer from the buffer.

buffer.readu32(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as a
32-bit unsigned integer and converting it into a number.

Provide feedback

---

readf32

Reads a 32-bit floating-point value from the buffer.

buffer.readf32(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as a
32-bit floating-point value and converting it into a number. If the
floating-point value matches any bit patterns that represent NaN (not a
number), the returned value may be converted to a different quiet NaN
representation.

Provide feedback

---

readf64

Reads a 64-bit floating-point value from the buffer.

buffer.readf64(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |

Returns

[number](/docs/luau/numbers)

Reads the data from the buffer by reinterpreting bytes at the offset as a
64-bit floating-point value and converting it into a number. If the
floating-point value matches any bit patterns that represent NaN (not a
number), the returned value may be converted to a different quiet NaN
representation.

Provide feedback

---

writebits

Writes data to the buffer based on a specific bitCount integer from 0
to 32, inclusive.

buffer.writebits(

b:[buffer](/docs/reference/engine/libraries/buffer), bitOffset:[number](/docs/luau/numbers), bitCount:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| bitOffset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| bitCount:[number](/docs/luau/numbers)  Integer bit count to write. Error is thrown if this value is not in range of 0 to 32, inclusive. |
| value:[number](/docs/luau/numbers)  Unsigned 32‑bit number. Only bitCount least significant bits are written. |

Returns

()

Writes data to the buffer based on a specific bitCount integer from 0
to 32, inclusive. value is treated as an unsigned 32‑bit number and
only bitCount least significant bits are written.

Note that 0 bit width is supported only to not error in generalized
cases where bit count is dynamic, and writing 0 bits has no effect. Also
note that, since the max size of the buffer is 1 GB, bitOffset
cannot be handled as a 32‑bit integer number like byte offset in other
buffer functions.

Provide feedback

---

writei8

Writes an 8-bit signed integer to the buffer.

buffer.writei8(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  An integer number in range [-128, 127]. |

Returns

()

Writes data to the buffer by converting the number into an 8-bit signed
integer and writing a single byte.

Provide feedback

---

writeu8

Writes an 8-bit unsigned integer to the buffer.

buffer.writeu8(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  An integer number in range [0, 255]. |

Returns

()

Writes data to the buffer by converting the number into an 8-bit unsigned
integer and writing a single byte.

Provide feedback

---

writei16

Writes a 16-bit signed integer to the buffer.

buffer.writei16(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  An integer number in range [-32,768, 32,767]. |

Returns

()

Writes data to the buffer by converting the number into a 16-bit signed
integer and reinterpreting it as individual bytes.

Provide feedback

---

writeu16

Writes a 16-bit unsigned integer to the buffer.

buffer.writeu16(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  An integer number in range [0, 65,535]. |

Returns

()

Writes data to the buffer by converting the number into a 16-bit unsigned
integer and reinterpreting it as individual bytes.

Provide feedback

---

writei32

Writes a 32-bit signed integer to the buffer.

buffer.writei32(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  An integer number in range [-2,147,483,648, 2,147,483,647]. |

Returns

()

Writes data to the buffer by converting the number into a 32-bit signed
integer and reinterpreting it as individual bytes.

Provide feedback

---

writeu32

Writes a 32-bit unsigned integer to the buffer.

buffer.writeu32(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  An integer number in range [0, 4,294,967,295]. |

Returns

()

Writes data to the buffer by converting the number into a 32-bit unsigned
integer and reinterpreting it as individual bytes.

Provide feedback

---

writef32

Writes a 32-bit floating-point value to the buffer.

buffer.writef32(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  A single-precision floating-point number. |

Returns

()

Writes data to the buffer by converting the number into a 32-bit
floating-point value and reinterpreting it as individual bytes.

Provide feedback

---

writef64

Writes a 64-bit floating-point value to the buffer.

buffer.writef64(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  A double-precision floating-point number. |

Returns

()

Writes data to the buffer by converting the number into a 64-bit
floating-point value and reinterpreting it as individual bytes.

Provide feedback

---

readstring

Reads a string from the buffer.

buffer.readstring(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), count:[number](/docs/luau/numbers)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| count:[number](/docs/luau/numbers)  Length to read. |

Returns

[string](/docs/luau/strings)

Reads a string of length count from the buffer at the specified
offset.

Provide feedback

---

writestring

Writes a string to the buffer.

buffer.writestring(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[string](/docs/luau/strings), count:[number](/docs/luau/numbers)?

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer) |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[string](/docs/luau/strings)  Data to write. |
| count:[number](/docs/luau/numbers)?  Number of bytes to take from the string. This value cannot be larger than the string length. |

Returns

()

Writes data from a string into the buffer at the specified offset. If an
optional count is specified, only count bytes are taken from the
string.

Provide feedback

---

copy

Copies bytes between buffers.

buffer.copy(

target:[buffer](/docs/reference/engine/libraries/buffer), targetOffset:[number](/docs/luau/numbers), source:[buffer](/docs/reference/engine/libraries/buffer), sourceOffset:[number](/docs/luau/numbers)?, count:[number](/docs/luau/numbers)?

):()

Parameters

|  |
| --- |
| target:[buffer](/docs/reference/engine/libraries/buffer)  Buffer to copy data into. |
| targetOffset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| source:[buffer](/docs/reference/engine/libraries/buffer)  Buffer to take the data from. |
| sourceOffset:[number](/docs/luau/numbers)? Default Value: 0 Offset from the beginning of the buffer memory, starting from 0. |
| count:[number](/docs/luau/numbers)?  Number of bytes to copy. If omitted, the whole source data starting from sourceOffset is taken. |

Returns

()

Copies count bytes from source starting at offset sourceOffset into
the target at targetOffset.

It's possible for source and target to be the same. Copying an
overlapping region inside the same buffer acts as if the source region is
copied into a temporary buffer and then that buffer is copied over to the
target.

Provide feedback

---

fill

Sets a region of the buffer memory to some 8-bit unsigned integer value.

buffer.fill(

b:[buffer](/docs/reference/engine/libraries/buffer), offset:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers), count:[number](/docs/luau/numbers)?

):()

Parameters

|  |
| --- |
| b:[buffer](/docs/reference/engine/libraries/buffer)  Buffer to write the data into. |
| offset:[number](/docs/luau/numbers)  Offset from the beginning of the buffer memory, starting from 0. |
| value:[number](/docs/luau/numbers)  An integer number in range [0, 255]. |
| count:[number](/docs/luau/numbers)?  Number of bytes to write. If omitted, all bytes after the specified offset are set. |

Returns

()

Sets count bytes in the buffer starting at the specified offset to
value.

Provide feedback

---