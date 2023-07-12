[Вопросы для собеседования](README.md)

# Computer Science(Eng)

## Why are floating point numbers inaccurate?
Floating point numbers in most programming languages are represented very similar to _scientific notation_:
with an exponent and mantissa(significant) and both of them must be integers, so we can't represent _some_ decimals
in that way. 

For example, we want to store `9.2` decimal number, then it will be presented in memory as 
 > 5179139571476070 * 2<sup>-49</sup>
 
Here exponent is `-49` and mantissa `5179139571476070` 

### Interpreting the Data
Usually programming languages have 2 types of floating point numbers:
_single precision(32 bits) & double precision(64 bits)_. In java type for single-precision floating point
number called `float` and `double` for double precision numbers.

#### Sign
The Sign stored in the first component as single bit. `0` means positive number, `1` means negative

#### Exponent
Stored in the middle asa 11 bits. To get true exponent you must subtract number **2<sup>(# of bits) - 1</sup> - 1**
to be able to have negative values.
#### Mantissa
Stored as third component as 52 bits. In scientific notation using decimal numbers mantissa always startswith non-zero
decimal number. it is also true for binary but as we only have `1` and `0` so mantissa always starts with 1.

We don't store this `1` to save space, we add it later. 
To get our mantissa we divide our `double` by 2<sup># of bits</sup> we do this because we're storing only fractional part of 
mantissa.
Then we add 1 to get true mantissa. And we're getting only approximate value because we represent our number as fraction of binary numbers 
 one of them is always power of 2.