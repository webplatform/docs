---
title: getMonth
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/z284z68x(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the month, using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getMonth

---
## Summary

Gets the month, using local time.

## Syntax

    dateObj.getMonth()

## Return Value

The **getMonth** method returns an integer between 0 (January) and 11 (December). For a **Date** constructed with "Jan 5, 1996", **getMonth** returns 0.

## Examples

The following example shows how to use the **getMonth** method.

``` js
var date = new Date("1/1/2001");
 document.write(date.getMonth());

 // Output: 0
```

## Remarks

The required dateObj reference is a **Date** object. To get the month value using Universal Coordinated Time (UTC), use the **getUTCMonth** method.

## See also

### Other articles

-   [getUTCMonth Method (Date)](/javascript/Date/getUTCMonth)
-   [setMonth Method (Date)](/javascript/Date/setMonth)
-   [setUTCMonth Method (Date)](/javascript/Date/setUTCMonth)

