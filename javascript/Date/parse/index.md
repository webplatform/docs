---
title: parse
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Parses a string containing a date, and returns the number of milliseconds between that date and midnight, January 1, 1970.'
uri: javascript/Date/parse

---
# parse

## Summary

Parses a string containing a date, and returns the number of milliseconds between that date and midnight, January 1, 1970.

## Syntax

    Date.parse( dateVal )

## Examples

The following example illustrates the use of the **Date.parse** function.

``` {.js}
var dateString = "November 1, 1997 10:15 AM";
 var mSec = Date.parse(dateString);
 document.write(mSec);
 // Output: 878404500000
```

The following example returns the difference between the date provided and 1/1/1970.

``` {.js}
var minMilli = 1000 * 60;
 var hrMilli = minMilli * 60;
 var dyMilli = hrMilli * 24;

 var ms = Date.parse(new Date("June 1, 1990"));
 var days = Math.round(ms / dyMilli);

 var dateStr = "";
 dateStr += "There are " + days + " days ";
 dateStr += "between 01/01/1970 and " + testDate;
 document.write(dateStr);

 // Output: There are 7456 days between 01/01/1970 and Fri Jun 1 00:00:00 PDT 1990
```

## Remarks

The required dateVal argument is either a string containing a date or a VT\_DATE value retrieved from an ActiveX object or other object. For information about date strings that the **Date.parse** function can parse. see Formatting Date and Time Strings (Windows Scripting - JScript).

The **Date.parse** function returns an integer value representing the number of milliseconds between midnight, January 1, 1970 and the date supplied in dateVal.

## See also

### Other articles

-   [getDate Method (Date)](/javascript/Date/getDate)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/k4w173wk(v=vs.94).aspx)

