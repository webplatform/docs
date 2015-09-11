---
title: setUTCMonth
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/d82ks7xe(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the month value in the Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setUTCMonth

---
## <span>Summary</span>

Sets the month value in the Date object using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.setUTCMonth( numMonth [ , dateVal ] )

**dateObj**
:   Required. Any Date object.

**numMonth**
:   Required. A numeric value equal to the month. The value for January is 0, and other month values follow consecutively.

**dateVal**
:   Optional. A numeric value representing the day of the month. If it is not supplied, the value from a call to the **getUTCDate** method is used.

## <span>Examples</span>

The following example illustrates the use of the **setUTCMonth** method.

``` js
function SetUTCMonthDemo(newmonth){
    var d, s;                       // Declare variables.
    d = new Date();                 // Create Date object.d.setUTCMonth( newmonth ) ;        // Set UTC month.
    s = "Current setting is ";
    s += d.toUTCString();
    return(s);                      // Return new setting.
 }
```

## <span>Remarks</span>

To set the month value using local time, use the **setMonth** method.

If the value of numMonth is greater than 11 (January is month 0), or is a negative number, the stored year is incremented or decremented appropriately. For example, if the stored date is "Jan 5, 1996 00:00:00.00", and **setUTCMonth(14)** is called, the date is changed to "Mar 5, 1997 00:00:00.00."

The **setUTCFullYear** method can be used to set the year, month, and day of the month.

## <span>See also</span>

### <span>Other articles</span>

-   [getMonth Method (Date)](/javascript/Date/getMonth)
-   [getUTCMonth Method (Date)](/javascript/Date/getUTCMonth)
-   [setMonth Method (Date)](/javascript/Date/setMonth)

