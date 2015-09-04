---
title: bitwise and
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Performs a bitwise AND operation on two 32-bit expressions.'
uri: 'javascript/operators/bitwise and'

---
# bitwise and

## Summary

Performs a bitwise AND operation on two 32-bit expressions.

## Syntax

    result = expression1 & expression2

**result**
:   The result of the operation.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

The following examples show how to use the & operator. See Remarks for more information.

``` {.js}
// 9 is 00000000000000000000000000001001
var expr1 = 9;

// 5 is 00000000000000000000000000000101
var expr2 = 5;

// 1 is 00000000000000000000000000000001
var result = expr1 & expr2;

document.write(result);
// Output: 1
```

## Remarks

The & does a bitwise AND operation on the each of the bits of two 32-bit expressions. If both of the bits are 1, the result is 1. Otherwise, the result is 0.

Bit1
:   Bit2
0
:   0
1
:   1
1
:   0
0
:   1

## See also

### Other articles

-   [Bitwise AND Assignment Operator (&=)](/javascript/operators/bitwise_and_assignment)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dazfy1f3(v=vs.94).aspx)

