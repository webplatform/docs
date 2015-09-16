---
title: 'bitwise left shift'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/t7f48wx9(v=vs.94).aspx)'
compatibility:
  feature: 'bitwise left shift'
  topic: javascript
readiness: 'Ready to Use'
summary: 'Left shifts the bits of an expression.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/bitwise left shift'

---
## Summary

Left shifts the bits of an expression.

## Syntax

    result = expression1 << expression2

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

The **\<\<** operator shifts the bits of expression1 left by the number of bits specified in expression2. For example, the variable *temp* has a value of 56 because 14 (00001110 in binary) shifted left two bits equals 56 (00111000 in binary).

``` js
var temp
temp = 14 << 2
```

## See also

### Other articles

-   [Left Shift Assignment Operator (\<\<=)](/javascript/operators/left_shift_assignment)
-   [Bitwise Right Shift Operator (\>\>)](/javascript/operators/bitwise_right_shift)
-   [Unsigned Right Shift Operator (\>\>\>)](/javascript/operators/unsigned_right_shift)

