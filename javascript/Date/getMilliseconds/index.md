---
title: getMilliseconds
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/52s3k2tf(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the milliseconds of a Date, using local time.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getMilliseconds

---
## <span>Summary</span>

Gets the milliseconds of a Date, using local time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getMilliseconds()

## <span>Return Value</span>

Returns the milliseconds of a date. The value can range from 0-999. If a date has been constructed without specifying the milliseconds, the value returned is 0.

## <span>Examples</span>

The following example shows how to use the **getMilliseconds** method.

``` js
var date = new Date("1/1/2001");
 document.write(date.getMilliseconds());
 document.write("<br/>");

 date.setMilliseconds(5);
 document.write(date.getMilliseconds());
 // Output:
 // 0
 // 5
```

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the number of milliseconds in Universal Coordinated Time (UTC), use the **getUTCMilliseconds** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getUTCMilliseconds Method (Date)](/javascript/Date/getUTCMilliseconds)
-   [setMilliseconds Method (Date)](/javascript/Date/setMilliseconds)
-   [setUTCMilliseconds Method (Date)](/javascript/Date/setUTCMilliseconds)

