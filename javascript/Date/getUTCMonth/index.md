---
title: getUTCMonth
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hkd7k0a3(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the month of a Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCMonth

---
## <span>Summary</span>

Gets the month of a Date object using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getUTCMonth()

## <span>Return Value</span>

Returns an integer between 0 (January) and 11 (December).

## <span>Examples</span>

The following example shows how to use the **getUTCMonth** method.

``` js
var date = new Date("2/2/2002");
 document.write(date.getUTCMonth());

 // Output: 1
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the month in local time, use the **getMonth** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getMonth Method (Date)](/javascript/Date/getMonth)
-   [setMonth Method (Date)](/javascript/Date/setMonth)
-   [setUTCMonth Method (Date)](/javascript/Date/setUTCMonth)

