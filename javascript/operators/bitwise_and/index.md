---
title: bitwise and
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dazfy1f3(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Performs a bitwise AND operation on two 32-bit expressions.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/bitwise and'

---
## <span>Summary</span>

Performs a bitwise AND operation on two 32-bit expressions.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result = expression1 & expression2

**result**
:   The result of the operation.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## <span>Examples</span>

The following examples show how to use the & operator. See Remarks for more information.

``` js
// 9 is 00000000000000000000000000001001
var expr1 = 9;

// 5 is 00000000000000000000000000000101
var expr2 = 5;

// 1 is 00000000000000000000000000000001
var result = expr1 & expr2;

document.write(result);
// Output: 1
```

## <span>Remarks</span>

The & does a bitwise AND operation on the each of the bits of two 32-bit expressions. If both of the bits are 1, the result is 1. Otherwise, the result is 0.

|Bit1|Bit2|ANDed Value|
|:---|:---|:----------|
|0|0|0|
|1|1|1|
|1|0|0|
|0|1|0|

## <span>See also</span>

### <span>Other articles</span>

-   [Bitwise AND Assignment Operator (&=)](/javascript/operators/bitwise_and_assignment)

