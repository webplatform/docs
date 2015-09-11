---
title: right shift assignment
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7fd7s4a7(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Right shifts the value of a variable by the number of bits specified in the value of an expression, maintaining the sign, and assigns the result to the variable.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/right shift assignment'

---
## <span>Summary</span>

Right shifts the value of a variable by the number of bits specified in the value of an expression, maintaining the sign, and assigns the result to the variable.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result >>= expression

**result**
:   Any variable.

**expression**
:   Any expression.

## <span>Examples</span>

``` js
// 14 is 00000000000000000000000000001110
var temp = 14;
temp >>= 2;
document.write(temp);
// 3 is 00000000000000000000000000000011
//Output: 3
```

## <span>Remarks</span>

Using the **\>\>=** operator is exactly the same as specifying:

    result = result >> expression

The **\>\>=** operator shifts the bits of result right by the number of bits specified in expression. The sign bit of result is used to fill the digits from the left. Digits shifted off the right are discarded. For example, after the following code is evaluated, temp has a value of -4: 14 (11110010 in binary) shifted right two bits equals -4 (11111100 in binary).

    var temp
    temp = -14
    temp >>= 2

## <span>See also</span>

### <span>Other articles</span>

-   [Bitwise Left Shift Operator (\<\<)](/javascript/operators/bitwise_left_shift)
-   [Bitwise Right Shift Operator (\>\>)](/javascript/operators/bitwise_right_shift)
-   [Unsigned Right Shift Operator (\>\>\>)](/javascript/operators/unsigned_right_shift)

