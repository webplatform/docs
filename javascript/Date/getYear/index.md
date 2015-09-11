---
title: getYear
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/x0a9sc10(v=vs.94).aspx)'
notes:
  - 'Obsolete; deletion candidate'
readiness: 'Not Ready'
summary: 'Gets the year of a Date object. Deprecated in favor of getFullYear method.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getYear

---
## <span>Summary</span>

Gets the year of a Date object. Deprecated in favor of getFullYear method.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getYear()

'
:   The required dateObj reference is a Date object.

## <span>Return Value</span>

Returns the year.

**Needs Examples**: This section should include examples.

## <span>Remarks</span>

**Important** -- This method is obsolete, and is provided for backward compatibility only. Use the **getFullYear** method instead.

In Internet Explorer 3.0, and then in Internet Explorer versions starting with Internet Explorer 9 standards mode, the value returned is the stored year minus 1900. For example, the year 1899 is returned as -1 and the year 2000 is returned as 100.

In Internet Explorer 4.0 through Internet Explorer 8 standards mode, the formula depends on the year. For the years 1900 through 1999, the value returned is a 2-digit value that is the stored year minus 1900. For dates outside that range, the 4-digit year is returned. For example, 1996 is returned as 96, but 1825 and 2025 are returned as is.

## <span>See also</span>

### <span>Other articles</span>

-   [getFullYear Method (Date)](/javascript/Date/getFullYear)
-   [getUTCFullYear Method (Date)](/javascript/Date/getUTCFullYear)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)
-   [setUTCFullYear Method (Date)](/javascript/Date/setUTCFullYear)
-   [setYear Method (Date)](/javascript/Date/setYear)

