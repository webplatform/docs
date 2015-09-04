---
title: modulus assignment
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Divides the value of a variable by the value of an expression, and assigns the remainder to the variable.'
uri: 'javascript/operators/modulus assignment'

---
# modulus assignment

## Summary

Divides the value of a variable by the value of an expression, and assigns the remainder to the variable.

## Syntax

    result %= expression

**result**
:   Any variable.

**expression**
:   Any numeric expression.

## Examples

``` {.js}
var x = 19;
var y = 6.7;
y %= x; // result: y = 5.6
```

## Remarks

Using the **%=** operator is exactly the same as specifying:

    result = result % expression

## See also

### Other articles

-   [Modulus Operator](/javascript/operators/modulus)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff3sz136(v=vs.94).aspx)

