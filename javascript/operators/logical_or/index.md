---
title: logical or
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/xxxekd04(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Performs a logical disjunction on two expressions.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/logical or'

---
## Summary

Performs a logical disjunction on two expressions.

## Syntax

<span class="language">JavaScript</span>

    result = expression1 || expression2

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## Examples

``` js
var x = 5;
var y = 7;
var z;
z = (x < y) || (x <= y); // result: z = true
z = (x < y) || (x > y); // result: z = true
z = (x > y) || (x <= y); // result: z = true
z = (x > y) || (x >= y); // result: z = false
```

## Remarks

If either or both expressions evaluate to **True** , result is **True**. The following table illustrates how result is determined:

|If `expression1` is|And `expression2` is|The `result` is|
|:------------------|:-------------------|:--------------|
|True|True|True|
|True|False|True|
|False|True|True|
|False|False|False|

JavaScript uses the following rules for converting non-Boolean values to Boolean values:

-   All objects are considered true.
-   Strings are considered false if and only if they are empty.
-   null and undefined are considered false.
-   Numbers are false if, and only if, they are 0.

