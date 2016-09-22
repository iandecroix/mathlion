<!-- Note: This file is automatically generated from source code comments. Changes made in this file will be overridden. -->

# Function complex

Create a complex value or convert a value to a complex value.


## Syntax

```js
complex()                           // creates a complex value with zero
                                         // as real and imaginary part.
complex(re : number, im : string)   // creates a complex value with provided
                                         // values for real and imaginary part.
complex(re : number)                // creates a complex value with provided
                                         // real value and zero imaginary part.
complex(complex : Complex)          // clones the provided complex value.
complex(arg : string)               // parses a string into a complex value.
complex(array : Array)              // converts the elements of the array
                                         // or matrix element wise into a
                                         // complex value.
complex({re: number, im: number})   // creates a complex value with provided
                                         // values for real an imaginary part.
complex({r: number, phi: number})   // creates a complex value with provided
                                         // polar coordinates
```

### Parameters

Parameter | Type | Description
--------- | ---- | -----------
`args` | * &#124; Array &#124; Matrix |  Arguments specifying the real and imaginary part of the complex number

### Returns

Type | Description
---- | -----------
Complex &#124; Array &#124; Matrix | Returns a complex value


## Examples

```js
var a = complex(3, -4);     // a = Complex 3 - 4i
a.re = 5;                        // a = Complex 5 - 4i
var i = a.im;                    // Number -4;
var b = complex('2 + 6i');  // Complex 2 + 6i
var c = complex();          // Complex 0 + 0i
var d = add(a, b);          // Complex 5 + 2i
```


## See also

[bignumber](bignumber.md),
[boolean](boolean.md),
[index](index.md),
[matrix](matrix.md),
[number](number.md),
[string](string.md),
[unit](unit.md)