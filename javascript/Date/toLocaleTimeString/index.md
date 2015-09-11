---
title: toLocaleTimeString
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/474de325(v=vs.94).aspx)'
notes:
  - 'An Internationalization/Localization center should be build to cover the basic concepts (like locale) so this stuff doesn''t have to be repeated over and over'
readiness: 'Ready to Use'
summary: 'Returns a time as a string value appropriate to the host environment''s current locale.'
tags:
  - JS
  - Basic
uri: javascript/Date/toLocaleTimeString

---
## <span>Summary</span>

Returns a time as a string value appropriate to the host environment's current locale.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    toLocaleTimeString()

## <span>Examples</span>

``` js
var nowdate = new Date();
alert(nowdate.toLocaleTimeString());
// output: "11:34:06 AM"
```

## <span>Remarks</span>

String that contains a time, in the current time zone, in a human readable format. The date is in the default format of the host environment's current locale.

## <span>Usage</span>

     The return value of toLocaleTimeString cannot be relied upon in scripting, as it will vary from computer to computer. The toLocaleTimeString method should only be used to format display - never as part of a computation.

## <span>See also</span>

### <span>Other articles</span>

-   [toString Method (Date)](/javascript/Date/toString)
-   [toDateString Method (Date)](/javascript/Date/toDateString)
-   [toGMTString Method (Date)](/javascript/Date/toGMTString)
-   [toISOString Method (Date)](/javascript/Date/toISOString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleDateString Method (Date)](/javascript/Date/toLocaleDateString)
-   [toTimeString Method (Date)](/javascript/Date/toTimeString)
-   [toUTCString Method (Date)](/javascript/Date/toUTCString)

### <span>External resources</span>

-   [toLocaleTimeString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleTimeString)
-   [toLocaleTimeString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/474de325(v=vs.94).aspx)

### <span>Specification</span>

[Date.prototype.toLocaleTimeString()](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.7)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

