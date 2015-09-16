---
title: getUTCHours
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/s12ec8ba(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the hours value in a Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCHours

---
## Summary

Gets the hours value in a Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.getUTCHours()

## Return Value

Returns an integer between 0 and 23 indicating the number of hours since midnight. Zero is returned if the time is before 1:00:00 am. If a **Date** object was created without specifying the time, by default the hour is 0 in UTC time. This time may be non-zero in other time zones.

## Examples

The following example illustrates the use of the **getUTCHours** method.

``` js
var date = new Date("1/1/2001");
 document.write(date.getUTCHours());
 document.write("<br/>");

 var date2 = new Date("1/1/2001 11:22:33");
 document.write(datee.getUTCHours());

 // Output (in the PST time zone):
 // 8
 // 19
```

## Remarks

The required dateObj reference is a **Date** object. To get the number of hours elapsed since midnight using local time, use the **getHours** method.

## See also

### Other articles

-   [getHours Method (Date)](/javascript/Date/getHours)
-   [setHours Method (Date)](/javascript/Date/setHours)
-   [setUTCHours Method (Date)](/javascript/Date/setUTCHours)

