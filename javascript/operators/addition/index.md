---
title: 'addition'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/wwfws59w(v=vs.94).aspx)'
compatibility:
  feature: addition
  topic: javascript
readiness: 'Ready to Use'
summary: 'Adds the value of one numeric expression to another, or concatenates two strings.'
tags:
  - JS_Basic
uri: javascript/operators/addition

---
## Summary

Adds the value of one numeric expression to another, or concatenates two strings.

## Syntax

    result = expression1 + expression2;

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

``` js
console.log(1 + 1); // 2
console.log('hello' + ' world'); // 'hello world'
console.log(1 + '1'); // '11'
console.log('1' + 1); // '11'
```

## Remarks

The types of the two expressions determine the behavior of the `+` operator.

|If|Then|
|:--|:---|
|Both expressions are numeric or Boolean|Add|
|Both expressions are strings|Concatenate|
|One expression is numeric and the other is a string|Concatenate|

## See also

### Other articles

-   [Addition Assignment Operator (`+=`)](/javascript/operators/addition_assignment)

