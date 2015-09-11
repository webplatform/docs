---
title: unsigned right shift
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/342xfs5s(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Right shifts the bits of an expression, without maintaining sign.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/unsigned right shift'

---
## <span>Summary</span>

Right shifts the bits of an expression, without maintaining sign.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result = expression1 >>> expression2

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## <span>Examples</span>

See Remarks.

``` js
var temp;
temp = -14 >>> 2;
// result: temp = 1073741820
```

## <span>Remarks</span>

The **\>\>\>** operator shifts the bits of expression1 right by the number of bits specified in expression2. Zeroes are filled in from the left. Digits shifted off the right are discarded.

The variable temp has an initial value -14 (11111111 11111111 11111111 11110010 in two's complement binary). When it is shifted right two bits, the value equals 1073741820 (00111111 11111111 11111111 11111100 in binary).

## <span>See also</span>

### <span>Other articles</span>

-   [Unsigned Right Shift Assignment Operator (\>\>\>=)](/javascript/operators/unsigned_right_shift_assignment)
-   [Bitwise Left Shift Operator (\<\<)](/javascript/operators/bitwise_left_shift)
-   [Bitwise Right Shift Operator (\>\>)](/javascript/operators/bitwise_right_shift)

