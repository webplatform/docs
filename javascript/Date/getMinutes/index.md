---
title: getMinutes
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/t919zcb7(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the minutes of a Date object, using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getMinutes

---
## <span>Summary</span>

Gets the minutes of a Date object, using local time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getMinutes()

## <span>Return Value</span>

Returns an integer between 0 and 59. Zero is returned the time is less than one minute after the hour. If a **Date** object was created without specifying the time, by default the minute value is 0.

## <span>Examples</span>

The following example shows how to the **getMinutes** method.

``` js
var date = new Date("1/1/2001");
 document.write(date.getMinutes());
 document.write("<br/>");

 date.setMinutes(5);
 document.write(date.getMinutes());

 // Output:
 // 0
 // 5
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the minutes value using Universal Coordinated Time (UTC), use the **getUTCMinutes** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getUTCMinutes Method (Date)](/javascript/Date/getUTCMinutes)
-   [setMinutes Method (Date)](/javascript/Date/setMinutes)
-   [setUTCMinutes Method (Date)](/javascript/Date/setUTCMinutes)

