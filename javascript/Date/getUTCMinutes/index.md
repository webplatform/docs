---
title: getUTCMinutes
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7xt0y1cc(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the minutes of a Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCMinutes

---
## <span>Summary</span>

Gets the minutes of a Date object using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getUTCMinutes()

## <span>Return Value</span>

Returns an integer between 0 and 59. Zero is returned the time is less than one minute after the hour. If a **Date** object was created without specifying the time, by default the UTC minute value is 0. However, in other time zones it may be different.

## <span>Examples</span>

The following example illustrates the use of the **getUTCMinutes** method.

``` js
var date = new Date("1/1/2001");
 document.write(date.getUTCMinutes());
 document.write("<br/>");

 date.setMinutes(5);
 document.write(date.getUTCMinutes());

 // Output:
 // 0
 // 5
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the number of minutes stored using local time, use the **getMinutes** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getMinutes Method (Date)](/javascript/Date/getMinutes)
-   [setMinutes Method (Date)](/javascript/Date/setMinutes)
-   [setUTCMinutes Method (Date)](/javascript/Date/setUTCMinutes)

