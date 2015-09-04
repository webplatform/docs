---
title: bitwise or
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Performs a bitwise OR on two expressions.'
uri: 'javascript/operators/bitwise or'

---
# bitwise or

## Summary

Performs a bitwise OR on two expressions.

## Syntax

    result = expression1 | expression2

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

See Remarks.

``` {.js}
var x;
x = 5 | 12;
// result: x = 13
```

## Remarks

The **|** operator looks at the binary representation of the values of two expressions and does a bitwise OR operation on them. The result of this operation behaves as follows:

    0101   (expression1)
    1100   (expression2)
    ----
    1101   (result)

Any time either of the expressions has a 1 in a digit, the result will have a 1 in that digit. Otherwise, the result will have a 0 in that digit.

## See also

### Other articles

-   [Bitwise OR Assignment Operator (|=)](/javascript/operators/bitwise_or_assignment)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/066h456z(v=vs.94).aspx)

