---
title: getUTCFullYear
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/47f8w843(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the year using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCFullYear

---
## <span>Summary</span>

Gets the year using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getUTCFullYear()

## <span>Return Value</span>

Returns the year as a four-digit number. Years specified as two digits in the **Date** constructor or in **setFullYear** are assumed to be in the twentieth century, so given "5/14/12", **getUTCFullYear** returns "1912".

## <span>Examples</span>

The following example shows how to use the **getUTCFullYear** method.

``` js
var date = new Date("1/9/36");
 document.write(date.getUTCFullYear());

 // Output: 1936
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the year using local time, use the **getFullYear** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getFullYear Method (Date)](/javascript/Date/getFullYear)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)
-   [setUTCFullYear Method (Date)](/javascript/Date/setUTCFullYear)

