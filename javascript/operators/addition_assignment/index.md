---
title: addition assignment
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/w2xk8y0c(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Adds the value of an expression to the value of a variable and assigns the result to the variable.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/addition assignment'

---
## Summary

Adds the value of an expression to the value of a variable and assigns the result to the variable.

## Syntax

    result += expression

**result**
:   Any variable.

**expression**
:   Any expression.

## Examples

``` js
var x = 5;
x += 2;
// result: x = 7
```

## Remarks

Using this operator is exactly the same as specifying: `result = result + expression`.

The types of the two expressions determine the behavior of the += operator.

|If|Then|
|:--|:---|
|Both expressions are numeric or Boolean|Add|
|Both expressions are strings|Concatenate|
|One expression is numeric and the other is a string|Concatenate|

## See also

### Other articles

-   [Addition Operator (+)](/javascript/operators/addition)

