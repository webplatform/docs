---
title: 'setMonth'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/tst8h9zw(v=vs.94).aspx)'
compatibility:
  feature: setMonth
  topic: javascript
readiness: 'Ready to Use'
summary: 'Sets the month value in the Date object using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setMonth

---
## Summary

Sets the month value in the Date object using local time.

## Syntax

    dateObj. setMonth( numMonth [ , dateVal ])

**dateObj**
:   Required. Any **Date** object.

**numMonth**
:   Required. A numeric value equal to the month. The value for January is 0, and other month values follow consecutively.

**dateVal**
:   Optional. A numeric value representing the day of the month. If this value is not supplied, the value from a call to the **getDate** method is used.

## Examples

The following example illustrates the use of the **setMonth** method.

``` js
date = new Date('1/1/1990');
 date.setMonth(14);
 document.write(date);

 // Output: Fri Mar 1 00:00:00 PST 1991
 // Note that the time zone corresponds to the time zone on the local computer.
```

## Remarks

To set the month value using Universal Coordinated Time (UTC), use the **setUTCMonth** method.

If the value of numMonth is greater than 11 (January is month 0) or is a negative number, the stored year is modified accordingly. For example, if the stored date is "Jan 5, 1996" and **setMonth(14)** is called, the date is changed to "Mar 5, 1997."

The **setFullYear** method can be used to set the year, month, and day of the month.

## See also

### Other articles

-   [getMonth Method (Date)](/javascript/Date/getMonth)
-   [getUTCMonth Method (Date)](/javascript/Date/getUTCMonth)
-   [setUTCMonth Method (Date)](/javascript/Date/setUTCMonth)

