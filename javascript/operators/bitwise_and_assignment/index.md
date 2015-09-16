---
title: bitwise and assignment
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/a9h8y72a(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the result of a bitwise AND operation on the value of a variable and the value of an expression. The variable and the expression are treated as 32-bit integers.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/bitwise and assignment'

---
## Summary

Sets the result of a bitwise AND operation on the value of a variable and the value of an expression. The variable and the expression are treated as 32-bit integers.

## Syntax

    result &= expression

**result**
:   Any variable.

**expression**
:   Any expression.

## Examples

Using this operator is the same as specifying `result = result & expression`

The [Bitwise AND Operator (&)](/javascript/operators/bitwise_and) looks at the binary representation of the values of result and expression and does a bitwise AND operation on them. The output of this operation behaves such that any time both of the expressions have a 1 in a digit, the result has a 1 in that digit; otherwise, the result has a 0 in that digit.

``` js
// 9 is 00000000000000000000000000001001
var expr1 = 9;

// 5 is 00000000000000000000000000000101
var expr2 = 5;

// 1 is 00000000000000000000000000000001
expr1 &= expr2;

document.write(expr1);
// result: 1
```

## See also

### Other articles

-   [Bitwise AND Operator (&)](/javascript/operators/bitwise_and)

