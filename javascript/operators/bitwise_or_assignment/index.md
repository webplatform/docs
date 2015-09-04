---
title: bitwise or assignment
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Performs a bitwise OR on the value of a variable and the value of an expression and assigns the result to the variable.'
uri: 'javascript/operators/bitwise or assignment'

---
# bitwise or assignment

## Summary

Performs a bitwise OR on the value of a variable and the value of an expression and assigns the result to the variable.

## Syntax

    result |= expression

**result**
:   Any variable.

**expression**
:   Any expression.

## Examples

See Remarks.

``` {.js}
var x = 5;
x |= 12;
// result: x = 13
```

## Remarks

Using this operator is exactly the same as specifying:

    result = result | expression

The **|=** operator looks at the binary representation of the values of result and expression and does a bitwise OR operation on them. The result of this operation behaves like this:

    0101    (result)
    1100    (expression)
    ----
    1101    (output)

Any time either of the expressions has a 1 in a digit, the result has a 1 in that digit. Otherwise, the result has a 0 in that digit.

## See also

### Other articles

-   [Bitwise OR Operator (|)](/javascript/operators/bitwise_or)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/81bads72(v=vs.94).aspx)

