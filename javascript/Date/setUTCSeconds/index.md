---
title: 'setUTCSeconds'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/k0aw4t5d(v=vs.94).aspx)'
compatibility:
  feature: setUTCSeconds
  topic: javascript
readiness: 'Ready to Use'
summary: 'Sets the seconds value in the Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setUTCSeconds

---
## Summary

Sets the seconds value in the Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.setUTCSeconds( numSeconds [ , numMilli ] )

**dateObj**
:   Required. Any Date object.

**numSeconds**
:   Required. A numeric value equal to the seconds value.

**numMilli**
:   Optional. A numeric value equal to the milliseconds value.

## Examples

The following example illustrates the use of the **setUTCSeconds** method.

``` js
function SetUTCSecondsDemo(nsec){
 // Create Date object.
     var d = new Date();
 // Set UTC seconds.
     d.setUTCSeconds(nsec);
     var s = "Current setting is ";
     s += d.toUTCString();
 // Return new setting.
     return(s);
 }
```

## Remarks

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify an optional argument. For example, if the numMilli argument is not specified, JavaScript uses the value returned from the **getUTCMilliseconds** method.

To set the seconds value using local time, use the **setSeconds** method.

If the value of an argument is greater than its range or is a negative number, other stored values are modified accordingly. For example, if the stored date is "Jan 5, 1996 00:00:00.00" and **setSeconds(150)** is called, the date is changed to "Jan 5, 1996 00:02:30.00."

The **setUTCHours** method can be used to set the hours, minutes, seconds, and milliseconds.

## See also

### Other articles

-   [getSeconds Method (Date)](/javascript/Date/getSeconds)
-   [getUTCSeconds Method (Date)](/javascript/Date/getUTCSeconds)
-   [setSeconds Method (Date)](/javascript/Date/setSeconds)

