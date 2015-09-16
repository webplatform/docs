---
title: unsigned right shift assignment
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/2ked96yw(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Right shifts the value of a variable by the number of bits specified in the value of an expression, without maintaining sign, and assigns the result to the variable.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/unsigned right shift assignment'

---
## Summary

Right shifts the value of a variable by the number of bits specified in the value of an expression, without maintaining sign, and assigns the result to the variable.

## Syntax

    result >>>= expression

**result**
:   Any variable.

**expression**
:   Any expression.

## Examples

See Remarks.

``` js
var temp;
temp = -14;
temp >>>= 2;
//result: temp = 1073741820
```

## Remarks

Using the \>\>\>= operator is exactly the same as doing the following:

    result = result >>> expression

The **\>\>\>=** operator shifts the bits of result right by the number of bits specified in expression. Zeroes are filled in from the left. Digits shifted off the right are discarded.

The variable temp has an initial value of -14 (11111111 11111111 11111111 11110010 in two's complement binary). When shifted right two bits, the value equals 1073741820 (00111111 11111111 11111111 11111100 in binary).

## See also

### Other articles

-   [Unsigned Right Shift Operator (\>\>\>)](/javascript/operators/unsigned_right_shift)
-   [Bitwise Left Shift Operator (\<\<)](/javascript/operators/bitwise_left_shift)
-   [Bitwise Right Shift Operator (\>\>)](/javascript/operators/bitwise_right_shift)

