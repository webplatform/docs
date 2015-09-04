---
title: now
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Gets the current date and time.'
uri: javascript/Date/now

---
# now

## Summary

Gets the current date and time.

## Syntax

    Date.now()

## Return Value

The number of milliseconds between midnight, January 1, 1970, and the current date and time.

## Examples

The following example illustrates the use of the **now** method.

``` {.js}
var start = Date.now();
 var response = prompt("What is your name?", "");
 var end = Date.now();
 var elapsed = (end - start) / 1000;
 document.write("You took " + elapsed + " seconds" + " to type: " + response);

 // Output:
 // You took <seconds> seconds to type: <name>
```

## Remarks

The [getTime method](/javascript/Date/getTime) returns the number of milliseconds between January 1, 1970, and a specified date.

For information about how to calculate elapsed time and compare dates, see Date and Time Calculations (Windows Scripting - JScript).

## See also

### Other articles

-   [getTime Method (Date)](/javascript/Date/getTime)
-   [Date Object](/javascript/Date)
-   [JavaScript Methods](/javascript/methods)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff679974(v=vs.94).aspx)

