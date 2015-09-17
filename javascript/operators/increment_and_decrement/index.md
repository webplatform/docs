---
title: 'increment and decrement'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/26k41698(v=vs.94).aspx)'
compatibility:
  feature: 'increment and decrement'
  topic: javascript
readiness: 'Ready to Use'
summary: 'The increment operator increments, and the decrement operator decrements, the value of a variable by one.'
tags:
  - JS_Basic
uri: 'javascript/operators/increment and decrement'

---
## Summary

The increment operator increments, and the decrement operator decrements, the value of a variable by one.

## Syntax

    result = ++ variable

    result = -- variable

    result = variable ++

    result = variable --

**result**
:   Any variable.

**variable**
:   Any variable.

## Examples

See Remarks.

``` js
var k = 5;
var j;
j = ++k; //result: j = 6, k = 5
j = k++; //result: j = 5, k = 6
```

## Remarks

If the operator appears before the variable, the value is modified before the expression is evaluated. If the operator appears after the variable, the value is modified after the expression is evaluated. In other words, given `j = ++k;` , the value of `j` is the original value of `k` plus one; given `j = k++;` , the value of `j` is the original value of `k` , which is incremented after its value is assigned to `j`.

