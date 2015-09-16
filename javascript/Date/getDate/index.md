---
title: 'getDate'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/217fw5tk(v=vs.94).aspx)'
compatibility:
  feature: getDate
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the day-of-the-month, using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getDate

---
## Summary

Gets the day-of-the-month, using local time.

## Syntax

    dateObj.getDate()

## Return Value

An integer between 1 and 31 that represents the day-of-the-month.

## Examples

The following example illustrates the use of the **getDate** method.

``` js
var date = new Date("Jan 01, 2001");
 var str = "Today's date is: ";
    str += (date.getMonth() + 1) + "/";
    str += date.getDate() + "/";
    str += date.getFullYear();
 document.write(str);

 // Output: Today's date is: 1/1/2001
```

## Remarks

The required dateObj reference is a **Date** object. To get the day-of-the-month using Universal Coordinated Time (UTC), use the **getUTCDate** method.

## See also

### Other articles

-   [getUTCDate Method (Date)](/javascript/Date/getUTCDate)
-   [setDate Method (Date)](/javascript/Date/setDate)
-   [setUTCDate Method (Date)](/javascript/Date/setUTCDate)

