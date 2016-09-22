<!-- Note: This file is automatically generated from source code comments. Changes made in this file will be overridden. -->

# Function chain

Wrap any value in a chain, allowing to perform chained operations on
the value.

All methods available in the js library can be called upon the chain,
and then will be evaluated with the value itself as first argument.
The chain can be closed by executing `chain.done()`, which returns
the final value.

The chain has a number of special functions:

- `done()`     Finalize the chain and return the chain's value.
- `valueOf()`  The same as `done()`
- `toString()` Executes `format()` onto the chain's value, returning
               a string representation of the value.


## Syntax

```js
chain(value)
```

### Parameters

Parameter | Type | Description
--------- | ---- | -----------
`value` | * | A value of any type on which to start a chained operation.

### Returns

Type | Description
---- | -----------
type.Chain | The created chain


## Examples

```js
chain(3)
    .add(4)
    .subtract(2)
    .done();     // 5

chain( [[1, 2], [3, 4]] )
    .subset(index(0, 0), 8)
    .multiply(3)
    .done();     // [[24, 6], [9, 12]]
```

