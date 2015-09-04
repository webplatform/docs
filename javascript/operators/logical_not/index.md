---
title: logical not
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Performs logical negation on an expression.'
uri: 'javascript/operators/logical not'

---
# logical not

## Summary

Performs logical negation on an expression.

## Syntax

    result = ! expression

**result**
:   Any variable.

**expression**
:   Any expression.

## Examples

``` {.js}
var x = 5;
var y = 7;
var z;
z = ! (x = y); // result: z = true
z = ! (y > x); // result: z = false
```

## Remarks

The following table illustrates how result is determined.

If `expression` is
:   Then `result` is
True
:   False
False
:   True

All unary operators, such as the **!** operator, evaluate expressions as follows:

-   If applied to undefined or null expressions, a run-time error is raised.
-   Objects are converted to strings.
-   Strings are converted to numbers if possible. If not, a run-time error is raised.
-   Boolean values are treated as numbers (0 if false, 1 if true).

The operator is applied to the resulting number.

For the **!** operator, if expression is nonzero, result is zero. If expression is zero, result is 1.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/zz722703(v=vs.94).aspx)

