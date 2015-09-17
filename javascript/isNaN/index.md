---
title: 'isNaN'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/66ztdbe6(v=vs.94).aspx)'
compatibility:
  feature: isNaN
  topic: javascript
readiness: 'Ready to Use'
summary: 'Determines whether a supplied number is NaN (not a number).'
tags:
  - JS_Basic
uri: javascript/isNaN

---
## Summary

Determines whether a supplied number is NaN (not a number).

## Syntax

    isNaN(numValue)

**numValue**
:   Required. the value to be tested against NaN

## Return Value

true if the value, converted to the Number type, is the NaN; otherwise false.

## Examples

``` js
isNaN(100); // false
isNaN("100"); // false
isNaN("ABC"); // true
isNaN("10C"); // true
isNaN("abc123"); // true
isNaN(Math.sqrt(-1)); // true
```

## Remarks

You typically use this method to test return values from the [parseInt](/javascript/parseInt) and [parseFloat](/javascript/parseFloat) functions.

Alternatively, a variable that contains **NaN** or another value could be compared to itself. If it compares as unequal, it is **NaN**. This is because **NaN** is the only value that is not equal to itself.

## See also

### Other articles

-   [isFinite Function](/javascript/isFinite)
-   [NaN Constant](/javascript/NaN)
-   [parseFloat Function](/javascript/parseFloat)
-   [parseInt Function](/javascript/parseInt)

