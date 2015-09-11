---
title: modulus assignment
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff3sz136(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Divides the value of a variable by the value of an expression, and assigns the remainder to the variable.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/modulus assignment'

---
## <span>Summary</span>

Divides the value of a variable by the value of an expression, and assigns the remainder to the variable.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result %= expression

**result**
:   Any variable.

**expression**
:   Any numeric expression.

## <span>Examples</span>

``` js
var x = 19;
var y = 6.7;
y %= x; // result: y = 5.6
```

## <span>Remarks</span>

Using the **%=** operator is exactly the same as specifying:

    result = result % expression

## <span>See also</span>

### <span>Other articles</span>

-   [Modulus Operator](/javascript/operators/modulus)

