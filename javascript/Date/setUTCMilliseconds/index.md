---
title: setUTCMilliseconds
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ytffzy7a(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the milliseconds value in the Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setUTCMilliseconds

---
## <span>Summary</span>

Sets the milliseconds value in the Date object using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.setUTCMilliseconds( numMilli )

**dateObj**
:   Required. Any Date object.

**numMilli**
:   Required. A numeric value equal to the millisecond value.

## <span>Examples</span>

The following example illustrates the use of the **setUTCMilliseconds** method.

``` js
function SetUTCMSecDemo(nmsec){
 // Create Date object.
    var d = new Date();
 // Set UTC milliseconds.
    d.setUTCMilliseconds(nmsec);

    var s = "Current setting is ";
    s += d.toUTCString();
    s += " and " + d.getUTCMilliseconds();
    s += " milliseconds"
    return(s);
 }
```

## <span>Remarks</span>

To set the milliseconds using local time, use the **setMilliseconds** method.

If the value of numMilli is greater than 999, or is a negative number, the stored number of seconds (and minutes, hours, and so forth, if necessary) is incremented an appropriate amount.

## <span>See also</span>

### <span>Other articles</span>

-   [getMilliseconds Method (Date)](/javascript/Date/getMilliseconds)
-   [getUTCMilliseconds Method (Date)](/javascript/Date/getUTCMilliseconds)
-   [setMilliseconds Method (Date)](/javascript/Date/setMilliseconds)

