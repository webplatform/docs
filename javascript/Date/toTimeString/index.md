---
title: 'toTimeString'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/y3xxxf8e(v=vs.94).aspx)'
compatibility:
  feature: toTimeString
  topic: javascript
readiness: 'Almost Ready'
summary: 'Returns the time component of a date as a human readable string.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/toTimeString

---
## Summary

Returns the time component of a date as a human readable string.

## Syntax

    toTimeString()

## Return Value

String value containing the time, in the current time zone, in a convenient, human readable format, e.g. `15:20:46 GMT+0200 (CEST)`

## Examples

``` js
var date = new Date();
console.log(date.toTimeString());
// outputs: "15:20:46 GMT+0200 (CEST)"
console.log(now.toString());
// outputs: "Wed Oct 08 2014 15:20:46 GMT+0200 (CEST)"
```

## Notes

According to the specification the contents of the String are implementation-dependent. That means that you cannot rely on the returned format being consistent across browsers. That said, all major browsers seem to agree on the format `15:20:46 GMT+0200 (CEST)`

*toTimeString()* adds the code of the current timezone to the output. Because the output format is not specified, some browsers might replace `(CEST)` (Central European Summer Time) with a fully localized text, e.g. the German `(Mitteleuropäische Sommerzeit)`.

## See also

### Other articles

-   [toString Method (Date)](/javascript/Date/toString)
-   [toDateString Method (Date)](/javascript/Date/toDateString)
-   [toGMTString Method (Date)](/javascript/Date/toGMTString)
-   [toISOString Method (Date)](/javascript/Date/toISOString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleDateString Method (Date)](/javascript/Date/toLocaleDateString)
-   [toLocaleTimeString Method (Date)](/javascript/Date/toLocaleTimeString)
-   [toUTCString Method (Date)](/javascript/Date/toUTCString)

### External resources

-   [toTimeString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toTimeString)
-   [toTimeString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/y3xxxf8e%28v=vs.94%29.aspx)

### Specification

[Date.prototype.toTimeString()](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.4)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

