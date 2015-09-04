---
title: toLocaleDateString
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
notes:
  - 'An Internationalization/Localization center should be build to cover the basic concepts (like locale) so this stuff doesn''t have to be repeated over and over'
summary: 'Returns a date as a string value appropriate to the host environment''s current locale.'
uri: javascript/Date/toLocaleDateString

---
# toLocaleDateString

## Summary

Returns a date as a string value appropriate to the host environment's current locale.

## Syntax

    toLocaleDateString()

## Return Value

String that contains a date, in the current time zone, in a human readable format. The date is in the default format of the host environment's current locale.

## Examples

``` {.js}
var nowdate = new Date();
alert(nowdate.toLocaleDateString());
// output: "Tuesday, November 04, 2014"
```

## Usage

     The return value of toLocaleDateString cannot be relied upon in scripting, as it will vary from computer to computer. The toLocaleDateString method should only be used to format display - never as part of a computation.

## See also

### Other articles

-   [toString Method (Date)](/javascript/Date/toString)
-   [toDateString Method (Date)](/javascript/Date/toDateString)
-   [toGMTString Method (Date)](/javascript/Date/toGMTString)
-   [toISOString Method (Date)](/javascript/Date/toISOString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleTimeString Method (Date)](/javascript/Date/toLocaleTimeString)
-   [toTimeString Method (Date)](/javascript/Date/toTimeString)
-   [toUTCString Method (Date)](/javascript/Date/toUTCString)

### External resources

-   [toDateTimeString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)
-   [toDateTimeString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/kecw102f(v=vs.94).aspx)

### Specification

[Date.prototype.toLocaleDateString()](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.6)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/kecw102f(v=vs.94).aspx)

