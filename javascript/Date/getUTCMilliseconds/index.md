---
title: 'getUTCMilliseconds'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/tkx22wzs(v=vs.94).aspx)'
compatibility:
  feature: getUTCMilliseconds
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the milliseconds of a Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCMilliseconds

---
## Summary

Gets the milliseconds of a Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.getUTCMilliseconds()

## Return Value

Returns a millisecond value that can range from 0-999.

## Examples

The following example illustrates the use of the **getUTCMilliseconds** method.

``` js
var date = new Date("1/1/2001");
 document.write(date.getUTCMilliseconds());
 document.write("<br/>");

 date.setMilliseconds(34);
 document.writedate.getUTCMilliseconds());

 // Output:
 // 0
 // 34
```

## Remarks

The required dateObj reference is a **Date** object. To get the number of milliseconds in local time, use the **getMilliseconds** method.

## See also

### Other articles

-   [getMilliseconds Method (Date)](/javascript/Date/getMilliseconds)
-   [setMilliseconds Method (Date)](/javascript/Date/setMilliseconds)
-   [setUTCMilliseconds Method (Date)](/javascript/Date/setUTCMilliseconds)

