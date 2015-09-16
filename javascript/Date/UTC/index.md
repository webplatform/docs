---
title: UTC
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/wz6stk2z(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the number of milliseconds between midnight, January 1, 1970 Universal Coordinated Time (UTC) (or GMT) and the specified date.'
tags:
  - JS
  - Basic
uri: javascript/Date/UTC

---
## Summary

Returns the number of milliseconds between midnight, January 1, 1970 Universal Coordinated Time (UTC) (or GMT) and the specified date.

## Syntax

    Date.UTC( year , month , day [ , hours [, minutes [, seconds [, ms ]]]])

**year**
:   Required. The full year designation is required for cross-century date accuracy. If year is between 0 and 99 is used, then year is assumed to be 1900 + year.

**month**
:   Required. The month as an integer between 0 and 11 (January to December).

**day**
:   Required. The date as an integer between 1 and 31.

**hours**
:   Optional. Must be supplied if minutes is supplied. An integer from 0 to 23 (midnight to 11pm) that specifies the hour.

**minutes**
:   Optional. Must be supplied if seconds is supplied. An integer from 0 to 59 that specifies the minutes.

**seconds**
:   Optional. Must be supplied if milliseconds is supplied. An integer from 0 to 59 that specifies the seconds.

**ms**
:   Optional. An integer from 0 to 999 that specifies the milliseconds.

## Examples

The following example illustrates the use of the **Date.UTC** function.

``` js
// Determine the milliseconds per day.
  var MinMilli = 1000 * 60;
 var HrMilli = MinMilli * 60;
 var DyMilli = HrMilli * 24;

 var date = new Date("June 1, 1990");
 var year = date.getFullYear();
 var month = date.getMonth();
 var day = date.getDay();

 var newDay = new Date("January 16, 2020");
 var yeartoday = newDay.getUTCFullYear();
 var monthtoday = newDay.getUTCMonth();
 var dayofmonthtoday = newDay.getUTCDate();

 // Get the milliseconds since 1/1/1970 UTC.
 var t1 = Date.UTC(year, month - 1, day)
 var t2 = Date.UTC(yeartoday, monthtoday, dayofmonthtoday);

 // Determine the difference in days.
 var days = (t2 - t1) / DyMilli;

 document.write(days);
 // Output: 10848
```

## Remarks

The **Date.UTC** function returns the number of milliseconds between midnight, January 1, 1970 UTC and the supplied date. This return value can be used in the **setTime** method and in the Date object constructor. If the value of an argument is greater than its range, or is a negative number, other stored values are modified accordingly. For example, if you specify 150 seconds, JavaScript redefines that number as two minutes and 30 seconds.

The difference between the **Date.UTC** function and the Date object constructor that accepts a date is that the **Date.UTC** function assumes UTC, and the Date object constructor assumes local time.

## See also

### Other articles

-   [setTime Method (Date)](/javascript/Date/setTime)

