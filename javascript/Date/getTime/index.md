---
title: getTime
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7hcawkw2(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the time value in milliseconds.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getTime

---
## <span>Summary</span>

Gets the time value in milliseconds.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getTime()

## <span>Return Value</span>

Returns the number of milliseconds between midnight, January 1, 1970 and the time value in the Date object. The range of dates is approximately 285,616 years from either side of midnight, January 1, 1970. Negative numbers indicate dates prior to 1970.

## <span>Examples</span>

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

## <span>Remarks</span>

The required dateObj reference is a **Date** object.

When doing multiple date and time calculations, you may want to define variables equal to the number of milliseconds in a day, hour, or minute. For example:

    var minute = 1000 * 60;
    var hour = minute * 60;
    var day = hour * 24;

See Date and Time Calculations (Windows Scripting - JScript) for more information about how to use the **getTime** method.

## <span>See also</span>

### <span>Other articles</span>

-   [setTime Method (Date)](/javascript/Date/setTime)

