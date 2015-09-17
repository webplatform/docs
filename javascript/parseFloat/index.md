---
title: 'parseFloat'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/d5hbbd4z(v=vs.94).aspx)'
compatibility:
  feature: parseFloat
  topic: javascript
readiness: 'Ready to Use'
summary: 'Converts a string to a floating-point number.'
tags:
  - JS_Basic
uri: javascript/parseFloat

---
## Summary

Converts a string to a floating-point number.

## Syntax

    parseFloat( numString )

## Examples

``` js
parseFloat("123.45")  // returns 123.45
parseFloat("abc")  // returns NaN
parseFloat("1.2abc")  // returns 1.2
```

## Remarks

The required numString argument is a string that contains a floating-point number.

The **parseFloat** function returns a numerical value equal to the number contained in numString. If no prefix of numString can be successfully parsed into a floating-point number, **NaN** (not a number) is returned.

You can test for **NaN** using the **isNaN** function.

## See also

### Other articles

-   [isNaN Function](/javascript/isNaN)
-   [parseInt Function](/javascript/parseInt)
-   [String Object](/javascript/String)

