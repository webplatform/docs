---
title: bitwise xor
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ece515h6(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Performs a bitwise exclusive OR on two expressions.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/bitwise xor'

---
## Summary

Performs a bitwise exclusive OR on two expressions.

## Syntax

<span class="language">JavaScript</span>

    result = expression1 ^ expression2

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

See Remarks.

``` js
var x;
x = 5 ^ 12;
// result: x = 9
```

## Remarks

The **\^** operator looks at the binary representation of the values of two expressions and does a bitwise exclusive OR operation on them. The result of this operation behaves as follows:

    0101   (expression1)
    1100   (expression2)
    ----
    1001   (result)

When one, and only one, of the expressions has a 1 in a digit, the result has a 1 in that digit. Otherwise, the result has a 0 in that digit.

## See also

### Other articles

-   [Bitwise XOR Assignment Operator (\^=)](/javascript/operators/bitwise_xor_assignment)

