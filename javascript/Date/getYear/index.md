---
title: getYear
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Not Ready'
notes:
  - 'Obsolete; deletion candidate'
summary: 'Gets the year of a Date object. Deprecated in favor of getFullYear method.'
uri: javascript/Date/getYear

---
# getYear

## Summary

Gets the year of a Date object. Deprecated in favor of getFullYear method.

## Syntax

    dateObj.getYear()

'
:   The required dateObj reference is a Date object.

## Return Value

Returns the year.

**Needs Examples**: This section should include examples.

## Remarks

**Important** -- This method is obsolete, and is provided for backward compatibility only. Use the **getFullYear** method instead.

In Internet Explorer 3.0, and then in Internet Explorer versions starting with Internet Explorer 9 standards mode, the value returned is the stored year minus 1900. For example, the year 1899 is returned as -1 and the year 2000 is returned as 100.

In Internet Explorer 4.0 through Internet Explorer 8 standards mode, the formula depends on the year. For the years 1900 through 1999, the value returned is a 2-digit value that is the stored year minus 1900. For dates outside that range, the 4-digit year is returned. For example, 1996 is returned as 96, but 1825 and 2025 are returned as is.

## See also

### Other articles

-   [getFullYear Method (Date)](/javascript/Date/getFullYear)
-   [getUTCFullYear Method (Date)](/javascript/Date/getUTCFullYear)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)
-   [setUTCFullYear Method (Date)](/javascript/Date/setUTCFullYear)
-   [setYear Method (Date)](/javascript/Date/setYear)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/x0a9sc10(v=vs.94).aspx)

