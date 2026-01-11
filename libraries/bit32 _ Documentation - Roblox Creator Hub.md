# bit32 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/libraries/bit32
Scraped: 2026-01-11T02:49:40.894442Z
1. [Libraries](/docs/reference/engine/libraries)
2. /
3. [bit32](/docs/reference/engine/libraries/bit32)

English

Feedback

Engine Library

bit32

A library of functions to perform bitwise operations.

---

Summary

Functions

|  |
| --- |
| [arshift](#arshift)(x: [number](/docs/luau/numbers),disp: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [band](#band)(numbers: [Tuple](/docs/luau/tuples)):[number](/docs/luau/numbers) |
| [bnot](#bnot)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [bor](#bor)(numbers: [Tuple](/docs/luau/tuples)):[number](/docs/luau/numbers) |
| [btest](#btest)(numbers: [Tuple](/docs/luau/tuples)):[boolean](/docs/luau/booleans) |
| [bxor](#bxor)(numbers: [Tuple](/docs/luau/tuples)):[number](/docs/luau/numbers) |
| [byteswap](#byteswap)(x: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [countlz](#countlz)(n: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [countrz](#countrz)(n: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [extract](#extract)(n: [number](/docs/luau/numbers),field: [number](/docs/luau/numbers),width: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [replace](#replace)(n: [number](/docs/luau/numbers),v: [number](/docs/luau/numbers),field: [number](/docs/luau/numbers),width: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [lrotate](#lrotate)(x: [number](/docs/luau/numbers),disp: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [lshift](#lshift)(x: [number](/docs/luau/numbers),disp: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [rrotate](#rrotate)(x: [number](/docs/luau/numbers),disp: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [rshift](#rshift)(x: [number](/docs/luau/numbers),disp: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |

This library provides functions to perform bitwise operations.

#### Number Limitations

This library treats numbers as unsigned 32-bit integers; numbers will be
converted to this before being used (see image below). Numbers with decimal
numbers are rounded to the nearest whole number.

![32-bit integer conversion (in hexadecimal)](https://prod.docsiteassets.roblox.com/assets/engine-api/libraries/bit32/32-Bit-Restriction.png)

---

API Reference

Functions

arshift

Returns a number after its bits have been arithmetically shifted to the
right by a given displacement.

bit32.arshift(

x:[number](/docs/luau/numbers), disp:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The number whose bits shall be shifted. |
| disp:[number](/docs/luau/numbers)  The integer number of bits to shift by. |

Returns

[number](/docs/luau/numbers)

Returns the number x shifted disp bits to the right. The number disp
may be any representable integer. Negative displacements shift to the
left.

This shift operation is what is called arithmetic shift. Vacant bits on
the left are filled with copies of the higher bit of x; vacant bits on
the right are filled with zeros. In particular, displacements with
absolute values higher than 31 result in zero or 0xFFFFFFFF (all original
bits are shifted out).

Provide feedback

---

band

Returns the bitwise AND of all provided numbers.

bit32.band(numbers:[Tuple](/docs/luau/tuples)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| numbers:[Tuple](/docs/luau/tuples) |

Returns

[number](/docs/luau/numbers)

Returns the bitwise AND of all provided numbers.

Each bit is tested against the following truth table:

| A | B | Output |
| --- | --- | --- |
| 0 | 0 | 0 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 1 | 1 |

![Bitwise AND of 3 numbers](https://prod.docsiteassets.roblox.com/assets/engine-api/libraries/bit32/AND.png)

Provide feedback

---

bnot

Returns the bitwise negation of a given number.

bit32.bnot(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the bitwise negation of x.

![Negation of a provided number](https://prod.docsiteassets.roblox.com/assets/engine-api/libraries/bit32/NOT.png)

For any integer x, the following identity holds:

```
assert(bit32.bnot(x) == (-1 - x) % 2^32)
```

Provide feedback

---

bor

Returns the bitwise OR of all provided numbers.

bit32.bor(numbers:[Tuple](/docs/luau/tuples)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| numbers:[Tuple](/docs/luau/tuples) |

Returns

[number](/docs/luau/numbers)

Returns the bitwise OR of all provided numbers.

Each bit is tested against the following truth table:

| A | B | Output |
| --- | --- | --- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 1 |

![Bitwise OR of 3 numbers](https://prod.docsiteassets.roblox.com/assets/engine-api/libraries/bit32/OR.png)

Provide feedback

---

btest

Returns a boolean describing whether the bitwise and of its operands is
different from zero.

bit32.btest(numbers:[Tuple](/docs/luau/tuples)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| numbers:[Tuple](/docs/luau/tuples) |

Returns

[boolean](/docs/luau/booleans)

Returns a boolean signalling whether the bitwise *and* of its operands is
different from zero.

Provide feedback

---

bxor

Returns the bitwise XOR of all provided numbers.

bit32.bxor(numbers:[Tuple](/docs/luau/tuples)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| numbers:[Tuple](/docs/luau/tuples) |

Returns

[number](/docs/luau/numbers)

Returns the bitwise XOR of all provided numbers.

Each bit is tested against the following truth table:

| A | B | Output |
| --- | --- | --- |
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 0 |

![Bitwise XOR of 3 numbers](https://prod.docsiteassets.roblox.com/assets/engine-api/libraries/bit32/XOR.png)

Provide feedback

---

byteswap

Returns the given number with the order of the bytes swapped.

bit32.byteswap(x:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the given number with the order of the bytes swapped.

Provide feedback

---

countlz

Returns the number of consecutive zero bits in the 32-bit representation
of the provided number starting from the left-most (most significant) bit.

bit32.countlz(n:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| n:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the number of consecutive zero bits in the 32-bit representation
of the provided number starting from the left-most (most significant) bit.
Returns 32 if the provided number is zero.

Provide feedback

---

countrz

Returns the number of consecutive zero bits in the 32-bit representation
of the provided number starting from the right-most (least significant)
bit.

bit32.countrz(n:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| n:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the number of consecutive zero bits in the 32-bit representation
of the provided number starting from the right-most (least significant)
bit. Returns 32 if the provided number is zero.

Provide feedback

---

extract

Extract a range of bits from a number and return them as an unsigned
number.

bit32.extract(

n:[number](/docs/luau/numbers), field:[number](/docs/luau/numbers), width:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| n:[number](/docs/luau/numbers) |
| field:[number](/docs/luau/numbers) |
| width:[number](/docs/luau/numbers) Default Value: 1 |

Returns

[number](/docs/luau/numbers)

Returns the unsigned number formed by the bits field to
field + width - 1 from n. Bits are numbered from 0 (least significant)
to 31 (most significant). All accessed bits must be in the range [0, 31].
The default for width is 1.

Provide feedback

---

replace

Return a copy of a number with a range of bits replaced by a given value.

bit32.replace(

n:[number](/docs/luau/numbers), v:[number](/docs/luau/numbers), field:[number](/docs/luau/numbers), width:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| n:[number](/docs/luau/numbers) |
| v:[number](/docs/luau/numbers) |
| field:[number](/docs/luau/numbers) |
| width:[number](/docs/luau/numbers) Default Value: 1 |

Returns

[number](/docs/luau/numbers)

Returns a copy of n with the bits field to field + width - 1
replaced by the value v. See [bit32.extract()](/docs/reference/engine/libraries/bit32#extract) for details about
field and width.

Provide feedback

---

lrotate

Returns a number after its bits have been rotated to the left by a given
number of times.

bit32.lrotate(

x:[number](/docs/luau/numbers), disp:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| disp:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the number x rotated disp bits to the left. The number disp
may be any representable integer. For any valid displacement, the
following identity holds:

```
assert(bit32.lrotate(x, disp) == bit32.lrotate(x, disp % 32))
```

In particular, negative displacements rotate to the right.

Provide feedback

---

lshift

Returns a number whose bits have been logically shifted to the left by a
given displacement.

bit32.lshift(

x:[number](/docs/luau/numbers), disp:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| disp:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the number x shifted disp bits to the left. The number disp
may be any representable integer. Negative displacements shift to the
right. In any direction, vacant bits are filled with zeros. In particular,
displacements with absolute values higher than 31 result in zero (all bits
are shifted out).

![Number shifted 3 to the left](https://prod.docsiteassets.roblox.com/assets/engine-api/libraries/bit32/LSHIFT.png)

For positive displacements, the following equality holds:

```
assert(bit32.lshift(b, disp) == (b * 2^disp) % 2^32)
```

Provide feedback

---

rrotate

Returns a number after its bits have been rotated to the right by a given
number of times.

bit32.rrotate(

x:[number](/docs/luau/numbers), disp:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| disp:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the number x rotated disp bits to the right. The number disp
may be any representable integer.

For any valid displacement, the following identity holds:

```
assert(bit32.rrotate(x, disp) == bit32.rrotate(x , disp % 32))
```

In particular, negative displacements rotate to the left.

Provide feedback

---

rshift

Returns a number whose bits have been logically shifted to the right by a
given displacement.

bit32.rshift(

x:[number](/docs/luau/numbers), disp:[number](/docs/luau/numbers)

):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers) |
| disp:[number](/docs/luau/numbers) |

Returns

[number](/docs/luau/numbers)

Returns the number x shifted disp bits to the right. The number disp
may be any representable integer. Negative displacements shift to the
left. In any direction, vacant bits are filled with zeros. In particular,
displacements with absolute values higher than 31 result in zero (all bits
are shifted out).

![Number shifted 3 to the right](https://prod.docsiteassets.roblox.com/assets/engine-api/libraries/bit32/RSHIFT.png)

For positive displacements, the following equality holds:

```
assert(bit32.rshift(b, disp) == (b % 2^32 / 2^disp) // 1)
```

This shift operation is what is called logical shift.

Provide feedback

---