---
title: toString
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns a human readbale string representation of a date.'
uri: javascript/Date/toString

---
# toString

## Summary

Returns a human readbale string representation of a date.

## Syntax

    toString()

## Return Value

String that contains the date, time and timezone in a human readable format.

## Examples

``` {.js}
var now = new Date();
console.log(now.toString());
// outputs: "Wed Oct 08 2014 13:46:37 GMT+0200 (CEST)"
```

## Notes

According to the specification the contents of the String are implementation-dependent. That means that you cannot rely on the returned format being consistent across browsers. That said, all major browsers seem to agree on the format `Wed Oct 08 2014 13:46:37 GMT+0200 (CEST)`.

*toString()* adds the code of the current timezone to the output. Because the output format is not specified, some browsers might replace `(CEST)` (Central European Summer Time) with a fully localized text, e.g. the German `(Mitteleuropäische Sommerzeit)`.

## See also

### Other articles

-   [toDateString Method (Date)](/javascript/Date/toDateString)
-   [toGMTString Method (Date)](/javascript/Date/toGMTString)
-   [toISOString Method (Date)](/javascript/Date/toISOString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleDateString Method (Date)](/javascript/Date/toLocaleDateString)
-   [toLocaleTimeString Method (Date)](/javascript/Date/toLocaleTimeString)
-   [toTimeString Method (Date)](/javascript/Date/toTimeString)
-   [toUTCString Method (Date)](/javascript/Date/toUTCString)

### External resources

-   [toString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toString)
-   [toUTCString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/jj155294%28v=vs.94%29.aspx)

### Specification

[Date.prototype.toString()](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.2)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155294(v=vs.94).aspx)

