---
title: getUTCDate
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/z8d0k600(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the day-of-the-month, using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCDate

---
## <span>Summary</span>

Gets the day-of-the-month, using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getUTCDate()

## <span>Return Value</span>

Returns an integer between 1 and 31 that represents the day-of-the-month.

## <span>Examples</span>

The following example shows how to use the **getUTCDate** method.

``` js
var date = new Date("1/23/2001");
 document.write(date.getUTCDate());

 // Output: 23
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the day of the month using local time, use the **getDate** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getDate Method (Date)](/javascript/Date/getDate)
-   [setDate Method (Date)](/javascript/Date/setDate)
-   [setUTCDate Method (Date)](/javascript/Date/setUTCDate)

