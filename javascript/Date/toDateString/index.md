---
title: toDateString
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/3k6ahb3a(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the date component of a date as a human readable string.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/toDateString

---
## Summary

Returns the date component of a date as a human readable string.

## Syntax

<span class="language">JavaScript</span>

    toDateString()

## Return Value

String value containing the date, in the current time zone, in a convenient, human readable format, e.g. `Fri May 09 2014`

## Examples

``` js
var date = new Date("2014-05-09");
console.log(date.toDateString());
// outputs: "Fri May 09 2014"
```

## Notes

According to the specification the contents of the String are implementation-dependent. That means that you cannot rely on the returned format being consistent across browsers. That said, all major browsers seem to agree on the format `Wed Oct 08 2014`

## See also

### Other articles

-   [toString Method (Date)](/javascript/Date/toString)
-   [toGMTString Method (Date)](/javascript/Date/toGMTString)
-   [toISOString Method (Date)](/javascript/Date/toISOString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleDateString Method (Date)](/javascript/Date/toLocaleDateString)
-   [toLocaleTimeString Method (Date)](/javascript/Date/toLocaleTimeString)
-   [toTimeString Method (Date)](/javascript/Date/toTimeString)
-   [toUTCString Method (Date)](/javascript/Date/toUTCString)

### External resources

-   [toDateString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toDateString)
-   [toDateString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/3k6ahb3a%28v=vs.94%29.aspx)

### Specification

[Date.prototype.toDateString()](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.3)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

