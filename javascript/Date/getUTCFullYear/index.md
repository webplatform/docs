---
title: 'getUTCFullYear'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/47f8w843(v=vs.94).aspx)'
compatibility:
  feature: getUTCFullYear
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the year using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCFullYear

---
## Summary

Gets the year using Universal Coordinated Time (UTC).

## Syntax

    dateObj.getUTCFullYear()

## Return Value

Returns the year as a four-digit number. Years specified as two digits in the **Date** constructor or in **setFullYear** are assumed to be in the twentieth century, so given "5/14/12", **getUTCFullYear** returns "1912".

## Examples

The following example shows how to use the **getUTCFullYear** method.

``` js
var date = new Date("1/9/36");
 document.write(date.getUTCFullYear());

 // Output: 1936
```

## Remarks

The required dateObj reference is a **Date** object. To get the year using local time, use the **getFullYear** method.

## See also

### Other articles

-   [getFullYear Method (Date)](/javascript/Date/getFullYear)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)
-   [setUTCFullYear Method (Date)](/javascript/Date/setUTCFullYear)

