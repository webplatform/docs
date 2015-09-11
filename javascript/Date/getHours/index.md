---
title: getHours
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/815z9tc9(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the hours in a date, using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getHours

---
## <span>Summary</span>

Gets the hours in a date, using local time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getHours()

## <span>Return Value</span>

An integer between 0 and 23, indicating the number of hours since midnight. Zero is returned if the time is before 1:00:00 am. If a **Date** object was created without specifying the time, by default the hour is 0.

## <span>Examples</span>

The following example shows how to use the **getHours** method.

``` js
var date = new Date("1/1/2001");
 document.write(date.getHours());
 document.write("<br/>");

 date.setTime(50000000);
 document.write(date.getHours());

 // Output:
 // 0
 // 5
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the hours value using Universal Coordinated Time (UTC), use the **getUTCHours** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getUTCHours Method (Date)](/javascript/Date/getUTCHours)
-   [setHours Method (Date)](/javascript/Date/setHours)
-   [setUTCHours Method (Date)](/javascript/Date/setUTCHours)

