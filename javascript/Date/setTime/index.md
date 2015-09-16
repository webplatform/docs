---
title: setTime
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/767045xx(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the date and time value in the Date object.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setTime

---
## Summary

Sets the date and time value in the Date object.

## Syntax

<span class="language">JavaScript</span>

    dateObj.setTime( milliseconds )

**dateObj**
:   Required. Any Date object.

**milliseconds**
:   Required. A numeric value representing the number of elapsed milliseconds since midnight, January 1, 1970 GMT.

## Examples

The following example illustrates the use of the **setTime** method.

``` js
function SetTimeTest(newtime){
    var d, s;                  //Declare variables.
    d = new Date();            //Create Date object.d.setTime( newtime ) ;        //Set time.
    s = "Current setting is ";
    s += d.toUTCString();
    return(s);                 //Return new setting.
 }
```

## Remarks

If milliseconds is negative, it indicates a date before 1970. The range of available dates is approximately 285,616 years from either side of 1970.

Setting the date and time with the **setTime** method is independent of the time zone.

## See also

### Other articles

-   [getTime Method (Date)](/javascript/Date/getTime)

