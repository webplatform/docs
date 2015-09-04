---
title: getHours
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
summary: 'Gets the hours in a date, using local time.'
uri: javascript/Date/getHours

---
# getHours

## Summary

Gets the hours in a date, using local time.

## Syntax

    dateObj.getHours()

## Return Value

An integer between 0 and 23, indicating the number of hours since midnight. Zero is returned if the time is before 1:00:00 am. If a **Date** object was created without specifying the time, by default the hour is 0.

## Examples

The following example shows how to use the **getHours** method.

``` {.js}
var date = new Date("1/1/2001");
 document.write(date.getHours());
 document.write("<br/>");

 date.setTime(50000000);
 document.write(date.getHours());

 // Output:
 // 0
 // 5
```

## Remarks

The required dateObj reference is a **Date** object. To get the hours value using Universal Coordinated Time (UTC), use the **getUTCHours** method.

## See also

### Other articles

-   [getUTCHours Method (Date)](/javascript/Date/getUTCHours)
-   [setHours Method (Date)](/javascript/Date/setHours)
-   [setUTCHours Method (Date)](/javascript/Date/setUTCHours)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/815z9tc9(v=vs.94).aspx)

