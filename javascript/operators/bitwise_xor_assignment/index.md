---
title: bitwise xor assignment
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/06f6ta51(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Performs a bitwise exclusive OR on a variable and an expression and assigns the result to the variable.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/bitwise xor assignment'

---
## <span>Summary</span>

Performs a bitwise exclusive OR on a variable and an expression and assigns the result to the variable.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result ^= expression

**result**
:   Any variable.

**expression**
:   Any expression.

## <span>Examples</span>

See Remarks.

``` js
var x = 5;
x ^= 12;
// result: x = 9
```

## <span>Remarks</span>

Using the **\^=** operator is exactly the same as specifying:

    result = result ^ expression

The **\^=** operator looks at the binary representation of the values of two expressions and does a bitwise exclusive OR operation on them. The result of this operation behaves as follows:

    0101    (result)
    1100    (expression)
    ----
    1001    (result)

When one, and only one, of the expressions has a 1 in a digit, the result has a 1 in that digit. Otherwise, the result has a 0 in that digit.

## <span>See also</span>

### <span>Other articles</span>

-   [Bitwise XOR Operator (\^)](/javascript/operators/bitwise_xor)

