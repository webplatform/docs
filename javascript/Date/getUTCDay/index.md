---
title: 'getUTCDay'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/aexkzf1c(v=vs.94).aspx)'
compatibility:
  feature: getUTCDay
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the day of the week using Universal Coordinated Time (UTC).'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/getUTCDay

---
## Summary

Gets the day of the week using Universal Coordinated Time (UTC).

## Syntax

    dateObj.getUTCDay()

## Return Value

Returns an integer between 0 (Sunday) and 6 (Saturday) that represents the day of the week.

## Examples

The following example shows how to use the **getUTCDay** method.

``` js
var date = new Date("2/6/2001");
 var day = date.getUTCDay();
 document.write(day);

 // Output: 2
```

## Remarks

The required dateObj reference is a **Date** object. To get the day of the week using local time, use the **getDate** method.

## See also

### Other articles

-   [getDay Method (Date)](/javascript/Date/getDay)

