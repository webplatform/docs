---
title: min
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
readiness: 'Ready to Use'
summary: 'Returns the smaller of a set of numeric expressions.'
tags:
  - JS
  - Basic
uri: javascript/Math/min

---
## Summary

Returns the smaller of a set of numeric expressions.

## Syntax

    Math.min([ number1 [, number2 [... [, numberN ]]]])

## Examples

The following code shows how to get the smaller of two expressions.

``` js
var x = Math.min(107 - 3, 48 * 90);
 document.write(x);

 // Output:
 // 104
```

## Remarks

The optional number1, number2, ..., numberN arguments are numeric expressions to be evaluated.

If no arguments are provided, the return value is equal to [Number.POSITIVE\_INFINITY](/javascript/Number/constants). If any argument is **NaN** , the return value is also **NaN**.

## See also

### Other articles

-   [Math.max Function](/javascript/Math/max)

