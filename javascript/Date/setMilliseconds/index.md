---
title: setMilliseconds
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/a92fx7ha(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the milliseconds value in the Date object using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setMilliseconds

---
## <span>Summary</span>

Sets the milliseconds value in the Date object using local time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.setMilliseconds( numMilli )

**dateObj**
:   Required. Any Date object.

**numMilli**
:   Required. A numeric value equal to the millisecond value.

## <span>Examples</span>

The following example illustrates the use of the **setMilliseconds** method.

``` js
function SetMSecDemo(nmsec){
    var d, s;                    // Declare variables.
    d = new Date();              // Create Date object.d.setMilliseconds( nmsec ) ;    // Set milliseconds.
    s = "Current setting is ";
    s += d.toLocaleString();
    s += " and " + d.getMilliseconds();
    s += " milliseconds";
    return(s);                   // Return new date setting.
 }
```

## <span>Remarks</span>

To set the milliseconds value using Universal Coordinated Time (UTC), use the **setUTCMilliseconds** method.

If the value of numMilli is greater than 999 or is a negative number, the stored number of seconds (and minutes, hours, and so forth if necessary) is incremented an appropriate amount.

## <span>See also</span>

### <span>Other articles</span>

-   [getMilliseconds Method (Date)](/javascript/Date/getMilliseconds)
-   [getUTCMilliseconds Method (Date)](/javascript/Date/getUTCMilliseconds)
-   [setUTCMilliseconds Method (Date)](/javascript/Date/setUTCMilliseconds)

