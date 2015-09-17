---
title: 'bitwise right shift'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/5s9e947e(v=vs.94).aspx)'
compatibility:
  feature: 'bitwise right shift'
  topic: javascript
readiness: 'Ready to Use'
summary: 'Right shifts the bits of an expression, maintaining sign.'
tags:
  - JS_Basic
uri: 'javascript/operators/bitwise right shift'

---
## Summary

Right shifts the bits of an expression, maintaining sign.

## Syntax

    result = expression1 >> expression2

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

The \>\> operator shifts the bits of expression1 right by the number of bits specified in expression2. The sign bit of expression1 is used to fill the digits from the left. Digits shifted off the right are discarded. For example, after the following code is evaluated, temp has a value of -4: -14 (11110010 in two's complement binary) shifted right two bits equals -4 (11111100 in two's complement binary).

``` js
var temp
temp = -14 >> 2
```

## See also

### Other articles

-   [Bitwise Left Shift Operator (\<\<)](/javascript/operators/bitwise_left_shift)
-   [Right Shift Assignment Operator (\>\>=)](/javascript/operators/right_shift_assignment)
-   [Unsigned Right Shift Operator (\>\>\>)](/javascript/operators/unsigned_right_shift)

