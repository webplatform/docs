---
title: toUTCString
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7ew14035(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a date converted to a string formatted according to UTC conventions.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/toUTCString

---
## <span>Summary</span>

Returns a date converted to a string formatted according to UTC conventions.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    toUTCString()

## <span>Return Value</span>

String that contains the date formatted using UTC conventions: `Fri, 09 May 2014 00:00:00 GMT`

## <span>Examples</span>

``` js
var date = new Date("2014-05-09");
console.log(date.toUTCString()); // "Fri, 09 May 2014 00:00:00 GMT"
```

## <span>Remarks</span>

**UTC** is the acronym of Universal Coordinated Time.

The Format returned by this *toGMTString* was defined by [[1]](http://tools.ietf.org/html/rfc822#section-5) and was refined by [RFC-1123](http://tools.ietf.org/html/rfc1123#section-5.2.14)

## <span>See also</span>

### <span>Other articles</span>

-   [toString Method (Date)](/javascript/Date/toString)
-   [toDateString Method (Date)](/javascript/Date/toDateString)
-   [toGMTString Method (Date)](/javascript/Date/toGMTString)
-   [toISOString Method (Date)](/javascript/Date/toISOString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleDateString Method (Date)](/javascript/Date/toLocaleDateString)
-   [toLocaleTimeString Method (Date)](/javascript/Date/toLocaleTimeString)
-   [toTimeString Method (Date)](/javascript/Date/toTimeString)

### <span>External resources</span>

-   [toUTCString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toUTCString)
-   [toUTCString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/7ew14035%28v=vs.94%29.aspx)

### <span>Specification</span>

[Date.prototype.toUTCString()](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.42)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

