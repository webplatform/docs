---
title: 'getUTCSeconds'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/4y0y6x01(v=vs.94).aspx)'
compatibility:
  feature: getUTCSeconds
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the seconds of a Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCSeconds

---
## Summary

Gets the seconds of a Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.getUTCSeconds()

## Return Value

Returns an integer between 0 and 59. Zero is returned when the time is less than one second into the current minute. If a **Date** object was created without specifying the time, by default the UTC seconds value is 0.

## Examples

The following example shows how to use the **getUTCSeconds** method.

``` js
var date = new Date("1/1/2001");
 document.write(date. getUTCSeconds());

 // Output: 0
```

## Remarks

The required dateObj reference is a **Date** object. To get the number of seconds in local time, use the **getSeconds** method.

## See also

### Other articles

-   [getSeconds Method (Date)](/javascript/Date/getSeconds)
-   [setSeconds Method (Date)](/javascript/Date/setSeconds)
-   [setUTCSeconds Method (Date)](/javascript/Date/setUTCSeconds)

