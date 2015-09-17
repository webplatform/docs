---
title: 'getUTCMonth'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hkd7k0a3(v=vs.94).aspx)'
compatibility:
  feature: getUTCMonth
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the month of a Date object using Universal Coordinated Time (UTC).'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/getUTCMonth

---
## Summary

Gets the month of a Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.getUTCMonth()

## Return Value

Returns an integer between 0 (January) and 11 (December).

## Examples

The following example shows how to use the **getUTCMonth** method.

``` js
var date = new Date("2/2/2002");
 document.write(date.getUTCMonth());

 // Output: 1
```

## Remarks

The required dateObj reference is a **Date** object. To get the month in local time, use the **getMonth** method.

## See also

### Other articles

-   [getMonth Method (Date)](/javascript/Date/getMonth)
-   [setMonth Method (Date)](/javascript/Date/setMonth)
-   [setUTCMonth Method (Date)](/javascript/Date/setUTCMonth)

