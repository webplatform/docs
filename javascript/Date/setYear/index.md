---
title: setYear
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/0f0shhbs(v=vs.94).aspx)'
notes:
  - 'Obsolete; deletion candidate'
readiness: 'Not Ready'
summary: 'Sets the year value in the Date object. Deprecated in favor of the setFullYear method.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/setYear

---
## Summary

Sets the year value in the Date object. Deprecated in favor of the setFullYear method.

## Syntax

    dateObj.setYear( numYear )

**dateObj**
:   Required. Any Date object.

**numYear**
:   Required. For the years 1900 through 1999, this is a numeric value equal to the year minus 1900. For dates outside that range, this is a 4-digit numeric value.

**Needs Examples**: This section should include examples.

## Remarks

This method is obsolete, and is maintained for backwards compatibility only. Use the **setFullYear** method instead.

To set the year of a Date object to 1997, call **setYear(97)**. To set the year to 2010, call **setYear(2010)**. Finally, to set the year to a year in the range 0-99, use the **setFullYear** method.

**Note** -- For JavaScript version 1.0, **setYear** uses a value that is the result of the addition of 1900 to the year value provided by numYear , regardless of the value of the year. For example, to set the year to 1899 numYear is -1 and to set the year 2000 numYear is 100.

## See also

### Other articles

-   [getFullYear Method (Date)](/javascript/Date/getFullYear)
-   [getUTCFullYear Method (Date)](/javascript/Date/getUTCFullYear)
-   [getYear Method (Date)](/javascript/Date/getYear)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)
-   [setUTCFullYear Method (Date)](/javascript/Date/setUTCFullYear)

