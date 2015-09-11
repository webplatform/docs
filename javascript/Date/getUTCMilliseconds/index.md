---
title: getUTCMilliseconds
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/tkx22wzs(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the milliseconds of a Date object using Universal Coordinated Time (UTC).'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/getUTCMilliseconds

---
## <span>Summary</span>

Gets the milliseconds of a Date object using Universal Coordinated Time (UTC).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dateObj.getUTCMilliseconds()

## <span>Return Value</span>

Returns a millisecond value that can range from 0-999.

## <span>Examples</span>

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

## <span>Remarks</span>

The required dateObj reference is a **Date** object. To get the number of milliseconds in local time, use the **getMilliseconds** method.

## <span>See also</span>

### <span>Other articles</span>

-   [getMilliseconds Method (Date)](/javascript/Date/getMilliseconds)
-   [setMilliseconds Method (Date)](/javascript/Date/setMilliseconds)
-   [setUTCMilliseconds Method (Date)](/javascript/Date/setUTCMilliseconds)

