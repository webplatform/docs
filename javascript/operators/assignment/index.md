---
title: 'assignment'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/1w2h1k9x(v=vs.94).aspx)'
compatibility:
  feature: assignment
  topic: javascript
notes:
  - 'Needs example'
readiness: 'Almost Ready'
summary: 'The assignment operator takes the value of the right operand and assigns it to the left operand.'
tags:
  - JS_Basic
uri: javascript/operators/assignment

---
## Summary

The assignment operator takes the value of the right operand and assigns it to the left operand.

## Syntax

    result = expression;

**result**
:   Any variable.

**expression**
:   Any expression that returns a value.

## Examples

``` js
var x;
x = 5;
```

## Remarks

The = operator behaves like other operators, so expressions that contain it have a value. This means that you can chain assignment operators as follows: `j = k = l = 0`. In this case `j` , `k` , and `l` equal zero.

