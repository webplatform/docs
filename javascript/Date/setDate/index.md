---
title: setDate
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/txfkf2t2(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the numeric day-of-the-month value of the Date object using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setDate

---
## Summary

Sets the numeric day-of-the-month value of the Date object using local time.

## Syntax

<span class="language">JavaScript</span>

    dateObj.setDate( numDate )

**dateObj**
:   Required. Any **Date** object.

**numDate**
:   Required. A numeric value equal to the day of the month.

## Examples

The following example shows how to use the **setDate** method.

``` js
var date = new Date("12/15/1990");
 date.setDate(30);
 document.write(date);

 // Output (for the PST time zone): Sun Dec 30 00:00:00 PST 1990
```

## Remarks

To set the day-of-the-month value using Universal Coordinated Time (UTC), use the **setUTCDate** method.

If the value of numDate is greater than the number of days in the month, the date rolls over to a later month and/or year. For example, if the stored date is January 5, 1996 and **setDate(32)** is called, the date changes to February 1, 1996. If numDate is a negative number, the date rolls back to an earlier month and/or year. For example, if the stored date is January 5, 1996 and **setDate(-32)** is called, the date changes to November 29, 1995.

The [setFullYear Method (Date)](/javascript/Date/setFullYear) can be used to set the year, month, and day of the month.

## See also

### Other articles

-   [getDate Method (Date)](/javascript/Date/getDate)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)
-   [setMonth Method (Date)](/javascript/Date/setMonth)
-   [setUTCDate Method (Date)](/javascript/Date/setUTCDate)

