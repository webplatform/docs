---
title: setFullYear
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
summary: 'Sets the year of the Date object using local time.'
uri: javascript/Date/setFullYear

---
# setFullYear

## Summary

Sets the year of the Date object using local time.

## Syntax

    dateObj.setFullYear( numYear [, numMonth [, numDate ]])

**dateObj**
:   Required. Any **Date** object.

**numYear**
:   Required. A numeric value for the year.

**numMonth**
:   Optional. A zero-based numeric value for the month (0 for January, 11 for December). Must be specified if numDate is specified.

**numDate**
:   Optional. A numeric value equal for the day of the month.

## Examples

The following example illustrates the use of the **setFullYear** method:

``` {.js}
var date1 = new Date("1/1/2001");
 date1.setFullYear(2007);

 var date2 = new Date("1/1/2001");
 date2.setFullYear(2008, 10, 3);

 document.write (date1.toLocaleString());
 document.write ("<br />");
 document.write (date2.toLocaleString());

 // Output:
 // Monday, January 01, 2007 12:00:00 AM
 // Monday, November 03, 2008 12:00:00 AM
```

## Remarks

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify the optional argument. For example, if the numMonth argument is optional, but not specified, JavaScript uses the value returned from the **getMonth** method.

In addition, if the value of an argument is greater than its calendar range or is negative, the date rolls forward or backward as appropriate.

To set the year using Universal Coordinated Time (UTC), use the **setUTCFullYear** method.

The range of years supported in the date object is approximately 285,616 years before and after 1970.

## See also

### Other articles

-   [getFullYear Method (Date)](/javascript/Date/getFullYear)
-   [getUTCFullYear Method (Date)](/javascript/Date/getUTCFullYear)
-   [setUTCFullYear Method (Date)](/javascript/Date/setUTCFullYear)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/y367b7x8(v=vs.94).aspx)

