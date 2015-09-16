---
title: setMinutes
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/3sbd2ey3(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the minutes value in the Date object using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setMinutes

---
## Summary

Sets the minutes value in the Date object using local time.

## Syntax

<span class="language">JavaScript</span>

    dateObj.setMinutes( numMinutes [ ,  numSeconds [ ,  numMilli ]] )

**dateObj**
:   Required. Any Date object.

**numMinutes**
:   Required. A numeric value equal to the minutes value. Must be supplied if either of the following arguments is used.

**numSeconds**
:   Optional. A numeric value equal to the seconds value. Must be supplied if the numMilli argument is used.

**numMilli**
:   Optional. A numeric value equal to the milliseconds value.

## Examples

The following example illustrates the use of the **setMinutes** method.

``` js
function SetMinutesDemo(nmin, nsec){
    var d, s;                     // Declare variables.
    d = new Date();               // Create Date object.d.setMinutes( nmin , nsec ) ;     // Set minutes.
    s = "Current setting is " + d.toLocaleString()
    return(s);                    // Return new setting.
 }
```

## Remarks

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify an optional argument. For example, if the numSeconds argument not specified, JavaScript uses the value returned from the **getSeconds** method.

To set the minutes value using Universal Coordinated Time (UTC), use the **setUTCMinutes** method.

If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00" and **setMinutes(90)** is called, the date is changed to "Jan 5, 1996 01:30:00." Negative numbers have a similar behavior.

## See also

### Other articles

-   [getMinutes Method (Date)](/javascript/Date/getMinutes)
-   [getUTCMinutes Method (Date)](/javascript/Date/getUTCMinutes)
-   [setUTCMinutes Method (Date)](/javascript/Date/setUTCMinutes)

