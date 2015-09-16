---
title: 'getFullYear'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/29y2w2x3(v=vs.94).aspx)'
compatibility:
  feature: getFullYear
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the year, using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getFullYear

---
## Summary

Gets the year, using local time.

## Syntax

    dateObj.getFullYear()

## Return Value

The year as a four-digit number. For example, the year 1976 is returned as 1976. Years specified as two digits in the **Date** constructor or in **setFullYear** are assumed to be in the twentieth century, so given "5/14/12", **getFullYear** returns "1912".

## Examples

The following example illustrates the use of the **getFullYear** method.

``` js
var date = new Date("1/1/01");
 document.write(date.getFullYear());

 // Output: 1901
```

## Remarks

The required dateObj reference is a **Date** object. To get the year using Universal Coordinated Time (UTC), use the **getUTCFullYear** method.

## See also

### Other articles

-   [getUTCFullYear Method (Date)](/javascript/Date/getUTCFullYear)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)
-   [setUTCFullYear Method (Date)](/javascript/Date/setUTCFullYear)

