---
title: 'abs'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/09bx9f48(v=vs.94).aspx)'
compatibility:
  feature: abs
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the absolute value of a number (the value without regard to whether it is positive or negative). For example, the absolute value of -5 is the same as the absolute value of 5.'
tags:
  - JS
  - Basic
uri: javascript/Math/abs

---
## Summary

Returns the absolute value of a number (the value without regard to whether it is positive or negative). For example, the absolute value of -5 is the same as the absolute value of 5.

## Syntax

    Math.abs( number )

**number**
:   Required. The required number argument is a numeric expression for which the absolute value is needed.

## Return Value

The absolute value of the number argument.

## Examples

The following example illustrates the use of the **abs** function.

``` js
var s;
 var v1 = Math.abs(6);
 var v2 = Math.abs(-6);
 if (v1 == v2) {
     document.write("Absolute values are the same.");
 }
 else {
 document.write("Absolute values are different.");
 }

 // Output: Absolute values are the same.
```

## See also

### Other articles

-   [Math Object](/javascript/Math)

