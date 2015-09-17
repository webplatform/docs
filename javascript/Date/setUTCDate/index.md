---
title: 'setUTCDate'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/xy2a08e6(v=vs.94).aspx)'
compatibility:
  feature: setUTCDate
  topic: javascript
readiness: 'Ready to Use'
summary: 'Sets the numeric day of the month in the Date object using Universal Coordinated Time (UTC).'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/setUTCDate

---
## Summary

Sets the numeric day of the month in the Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.setUTCDate( numDate )

**dateObj**
:   Required. Any Date object.

**numDate**
:   Required. A numeric value equal to the day of the month.

## Examples

The following example illustrates the use of the **setUTCDate** method.

``` js
function SetUTCDateDemo(newdayofmonth){
    var d = new Date();           // Create Date
    object.d.setUTCDate( newdayofmonth ) ;  // Set UTC day of month.
    var s = "Current setting is ";
    s += d.toUTCString();
    return(s);                    // Return new setting.
 }
```

## Remarks

To set the day of the month using local time, use the **setDate** method.

If the value of numDate is greater than the number of days in the month stored in the **Date** object or is a negative number, the date is set to a date equal to numDate minus the number of days in the stored month. For example, if the stored date is January 5, 1996, and **setUTCDate(32)** is called, the date changes to February 1, 1996. Negative numbers have a similar behavior.

The **setUTCFullYear** method can be used to set the year, month, and day of the month.

## See also

### Other articles

-   [getDate Method (Date)](/javascript/Date/getDate)
-   [getUTCDate Method (Date)](/javascript/Date/getUTCDate)
-   [setDate Method (Date)](/javascript/Date/setDate)

