---
title: 'setUTCFullYear'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/c9sd3ksb(v=vs.94).aspx)'
compatibility:
  feature: setUTCFullYear
  topic: javascript
readiness: 'Ready to Use'
summary: 'Sets the year value in the Date object using Universal Coordinated Time (UTC).'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/setUTCFullYear

---
## Summary

Sets the year value in the Date object using Universal Coordinated Time (UTC).

## Syntax

    dateObj.setUTCFullYear( numYear [ ,  numMonth [ , numDate ]] )

**dateObj**
:   Required. Any Date object.

**numYear**
:   Required. A numeric value equal to the year.

**numMonth**
:   Optional. A numeric value equal to the month. The value for January is 0, and other month values follow consecutively. Must be supplied if numDate is supplied.

**numDate**
:   Optional. A numeric value equal to the day of the month.

## Examples

The following example illustrates the use of the **setUTCFullYear** method.

``` js
var dtFirst = new Date();
 dtFirst.setUTCFullYear(2007);

 var dtSecond = new Date();
 // 10 is the value for November.
 dtSecond.setUTCFullYear(2008, 10, 3);

 document.write (dtFirst.toUTCString());
 document.write ("<br />");
 document.write (dtSecond.toUTCString());
```

## Remarks

All **set** methods taking optional arguments use the value returned from corresponding **get** methods, if you do not specify an optional argument. For example, if the numMonth argument is not specified, JavaScript uses the value returned from the **getUTCMonth** method.

In addition, if the value of an argument is greater that its range or is a negative number, other stored values are modified accordingly.

To set the year using local time, use the **setFullYear** method.

The range of years supported in the Date object is approximately 285,616 years from either side of 1970.

## See also

### Other articles

-   [getFullYear Method (Date)](/javascript/Date/getFullYear)
-   [getUTCFullYear Method (Date)](/javascript/Date/getUTCFullYear)
-   [setFullYear Method (Date)](/javascript/Date/setFullYear)

