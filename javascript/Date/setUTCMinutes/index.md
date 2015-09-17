---
title: 'setUTCMinutes'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/esssx44h(v=vs.94).aspx)'
compatibility:
  feature: setUTCMinutes
  topic: javascript
readiness: 'Ready to Use'
summary: 'Sets the minutes value in the Date object using Universal Coordinated Time (UTC).'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/setUTCMinutes

---
## Summary

Sets the minutes value in the Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.setUTCMinutes( numMinutes [ , numSeconds [ , numMilli ]] )

**dateObj**
:   Required. Any Date object.

**numMinutes**
:   Required. A numeric value equal to the minutes value. Must be supplied if either of the following arguments is used.

**numSeconds**
:   Optional. A numeric value equal to the seconds value. Must be supplied if numMilli is used.

**numMilli**
:   Optional. A numeric value equal to the milliseconds value.

## Examples

The following example illustrates the use of the **setUTCMinutes** method:

``` js
function SetUTCMinutesDemo(nmin, nsec){
    var d, s;                    // Declare variables.
    d = new Date();              // Create Date object.d.setUTCMinutes( nmin,nsec ) ;  // Set UTC minutes.
    s = "Current setting is " + d.toUTCString()
    return(s);                   // Return new setting.
 }
```

## Remarks

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify an optional argument. For example, if the numSeconds argument is not specified, JavaScript uses the value returned from the **getUTCSeconds** method.

To modify the minutes value using local time, use the **setMinutes** method.

If the value of an argument is greater than its range, or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00.00", and **setUTCMinutes(70)** is called, the date is changed to "Jan 5, 1996 01:10:00.00."

The **setUTCHours** method can be used to set the hours, minutes, seconds, and milliseconds.

## See also

### Other articles

-   [getMinutes Method (Date)](/javascript/Date/getMinutes)
-   [getUTCMinutes Method (Date)](/javascript/Date/getUTCMinutes)
-   [setMinutes Method (Date)](/javascript/Date/setMinutes)

