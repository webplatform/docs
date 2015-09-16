---
title: 'getDay'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/5wtd2bt8(v=vs.94).aspx)'
compatibility:
  feature: getDay
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the day of the week, using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getDay

---
## Summary

Gets the day of the week, using local time.

## Syntax

    dateObj.getDay()

## Return Value

An integer between 0 and 6 representing the day of the week (Sunday is 0, Saturday is 6).

## Examples

The following example shows how to use the **getDay** method.

``` js
var date = new Date("Saturday, February 9, 2008");
 day = date.getDay();
 document.write(day);

 // Output: 6
```

## Remarks

The required dateObj reference is a **Date** object. To get the day using Universal Coordinated Time (UTC), use the **getUTCDay** method.

## See also

### Other articles

-   [getUTCDay Method (Date)](/javascript/Date/getUTCDay)

