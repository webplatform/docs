---
title: 'getTime'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7hcawkw2(v=vs.94).aspx)'
compatibility:
  feature: getTime
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the time value in milliseconds.'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/getTime

---
## Summary

Gets the time value in milliseconds.

## Syntax

    dateObj.getTime()

## Return Value

Returns the number of milliseconds between midnight, January 1, 1970 and the time value in the Date object. The range of dates is approximately 285,616 years from either side of midnight, January 1, 1970. Negative numbers indicate dates prior to 1970.

## Examples

The following example shows how to use the **getTime** method.

``` js
var minute = 1000 * 60;
 var hour = minute * 60;
 var day = hour * 24;

 date = new Date("1/1/2001");
 var time = date.getTime();

 document.write(Math.round(time / day) + " days from 1/1/1970 to 1/1/2001");

 // Output: 11323 days from 1/1/1970 to 1/1/2001
```

## Remarks

The required dateObj reference is a **Date** object.

When doing multiple date and time calculations, you may want to define variables equal to the number of milliseconds in a day, hour, or minute. For example:

    var minute = 1000 * 60;
    var hour = minute * 60;
    var day = hour * 24;

See Date and Time Calculations (Windows Scripting - JScript) for more information about how to use the **getTime** method.

## See also

### Other articles

-   [setTime Method (Date)](/javascript/Date/setTime)

