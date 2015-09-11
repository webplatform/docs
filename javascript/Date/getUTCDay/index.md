---
title: getUTCDay
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/aexkzf1c(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the day of the week using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCDay

---
## <span>Summary</span>

Gets the day of the week using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getUTCDay()

## <span>Return Value</span>

Returns an integer between 0 (Sunday) and 6 (Saturday) that represents the day of the week.

## <span>Examples</span>

The following example shows how to use the **getUTCDay** method.

``` js
var date = new Date("2/6/2001");
 var day = date.getUTCDay();
 document.write(day);

 // Output: 2
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the day of the week using local time, use the **getDate** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getDay Method (Date)](/javascript/Date/getDay)

