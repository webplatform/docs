---
title: 'modulus'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9f59bza0(v=vs.94).aspx)'
compatibility:
  feature: modulus
  topic: javascript
readiness: 'Ready to Use'
summary: 'Divides the value of one expression by the value of another, and returns the remainder.'
tags:
  - JS
  - Basic
uri: javascript/operators/modulus

---
## Summary

Divides the value of one expression by the value of another, and returns the remainder.

## Syntax

    result = number1 % number2

**result**
:   Any variable.

**number1**
:   Any numeric expression.

**number2**
:   Any numeric expression.

## Examples

The following code shows how to use the modulus operator.

``` js
var modResult = 19 % 6.7;
document.write(modResult);
// Output: 5.6
```

## Remarks

The modulus, or remainder, operator divides number1 by number2 and returns only the remainder as result. The sign of result is the same as the sign of number1. The value of result is between 0 and the absolute value of number2.

