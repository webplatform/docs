---
title: 'valueOf'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155184(v=vs.94).aspx)'
compatibility:
  feature: valueOf
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the stored time value in milliseconds since midnight, January 1, 1970 UTC.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/valueOf

---
## Summary

Returns the stored time value in milliseconds since midnight, January 1, 1970 UTC.

## Syntax

    date.valueOf()

## Return Value

The stored time value in milliseconds since midnight, January 1, 1970 UTC. This is the same value as **getTime**. The date object is any instance of a Date.

## Examples

The following example illustrates the use of the **valueOf** method with a date.

``` js
var myDate = new Date();
 myDate.setFullYear(2100, 5, 5);
 if (myDate.getTime() == myDate.valueOf())
     document.write("values are the same");
 else
     document.write("values are different");

 // Output: values are the same
```

