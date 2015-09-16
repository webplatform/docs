---
title: 'left shift assignment'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/2027xe5w(v=vs.94).aspx)'
compatibility:
  feature: 'left shift assignment'
  topic: javascript
readiness: 'Ready to Use'
summary: 'Moves the specified number of bits to the left and assigns the result to result. The bits vacated by the operation are filled with 0.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/left shift assignment'

---
## Summary

Moves the specified number of bits to the left and assigns the result to result. The bits vacated by the operation are filled with 0.

## Syntax

    result <<= expression

**result**
:   Any variable.

**expression**
:   The number of bits to move.

## Examples

Using the **\<\<=** operator is the same as specifying `result = result << expression`

``` js
// 14 is 00000000000000000000000000001110
var temp = 14;
temp <<= 2;
document.write(temp);
// 56 is 00000000000000000000000000111000
Output: 56
```

## See also

### Other articles

-   [Bitwise Left Shift Operator (\<\<)](/javascript/operators/bitwise_left_shift)
-   [Bitwise Right Shift Operator (\>\>)](/javascript/operators/bitwise_right_shift)
-   [Unsigned Right Shift Operator (\>\>\>)](/javascript/operators/unsigned_right_shift)

