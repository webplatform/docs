---
title: round
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns a supplied numeric expression rounded to the nearest integer.'
uri: javascript/Math/round

---
# round

## Summary

Returns a supplied numeric expression rounded to the nearest integer.

## Syntax

    Math.round( number )

## Examples

``` {.js}
Math.round(0.8);  // 1
Math.round(2.2);  // 2
Math.round(2.5);  // 3
Math.round(4);    // 4
Math.round(-1.5); // -1
```

## Remarks

The required number argument is the value to be rounded to the nearest integer.

For positive numbers, if the decimal portion of number is 0.5 or greater, the return value is equal to the smallest integer greater than number. If the decimal portion is less than 0.5, the return value is the largest integer less than or equal to number.

For negative numbers, if the decimal portion is exactly -0.5, the return value is the smallest integer that is greater than the number.

For example, `Math.round(8.5)` returns 9, but `Math.round(-8.5)` returns -8.

## See also

### Other articles

-   [Math.ceil Function](/javascript/Math/ceil)
-   [Math.floor Function](/javascript/Math/floor)
-   [Math Object](/javascript/Math)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)

