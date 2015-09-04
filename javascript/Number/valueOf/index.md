---
title: valueOf
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns the primitive value of the specified number.'
uri: javascript/Number/valueOf

---
# valueOf

## Summary

Returns the primitive value of the specified number.

## Syntax

    number.valueOf()

## Return Value

Returns the number.

## Examples

In the following example, the instantiated number object is the same as the return value of this method.

``` {.js}
var num = 1234;
 var s = num.valueOf();

 if (num === s)
 document.write("same");
 else
 document.write("different");

 // Output:
 // same
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj159595(v=vs.94).aspx)

