---
title: setUTCHours
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
summary: 'Sets the hours value in the Date object using Universal Coordinated Time (UTC).'
uri: javascript/Date/setUTCHours

---
# setUTCHours

## Summary

Sets the hours value in the Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.setUTCHours( numHours [ , numMin [ , numSec [ , numMilli ]]] )

**dateObj**
:   Required. Any Date object.

**numHours**
:   Required. A numeric value equal to the hours value.

**numMin**
:   Optional. A numeric value equal to the minutes value. Must be supplied if either numSec or numMilli are used.

**numSec**
:   Optional. A numeric value equal to the seconds value. Must be supplied if numMilli argument is used.

**numMilli**
:   Optional. A numeric value equal to the milliseconds value.

## Examples

The following example illustrates the use of the **setUTCHours** method.

``` {.js}
function SetUTCHoursDemo(nhr, nmin, nsec){
    var d, s;                        // Declare variables.
    d = new Date();                  // Create Date
    object.d.setUTCHours( nhr , nmin , nsec ) ;  // Set UTC hours, minutes, seconds.
    s = "Current setting is " + d.toUTCString()
    return(s);                       // Return new setting.
 }
```

## Remarks

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify an optional argument. For example, if the numMin argument is not specified, JavaScript uses the value returned from the **getUTCMinutes** method.

To set the hours value using local time, use the **setHours** method.

If the value of an argument is greater than its range, or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00.00", and **setUTCHours(30)** is called, the date is changed to "Jan 6, 1996 06:00:00.00."

## See also

### Other articles

-   [getHours Method (Date)](/javascript/Date/getHours)
-   [getUTCHours Method (Date)](/javascript/Date/getUTCHours)
-   [setHours Method (Date)](/javascript/Date/setHours)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/cwybddk2(v=vs.94).aspx)

