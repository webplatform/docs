---
title: toGMTString
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/a34ehb82(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a date converted to a string formatted according to GMT conventions.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Date/toGMTString

---
## <span>Summary</span>

Returns a date converted to a string formatted according to GMT conventions.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    toGMTString()

## <span>Return Value</span>

String that contains the date formatted using GMT conventions: `Fri, 09 May 2014 00:00:00 GMT`

## <span>Examples</span>

``` js
var date = new Date("2014-05-09");
console.log(date.toGMTString()); // "Fri, 09 May 2014 00:00:00 GMT"
```

## <span>Remarks</span>

**GMT** is the acronym of Greenwich Mean Time.

The Format returned by this *toGMTString* was defined by [[1]](http://tools.ietf.org/html/rfc822#section-5) and was refined by [RFC-1123](http://tools.ietf.org/html/rfc1123#section-5.2.14)

## <span>Notes</span>

The **toGMTString** method is obsolete, and is provided for backwards compatibility only. It is recommended that you use the [toUTCString](/javascript/Date/toUTCString) method instead.

According to the specification, *toGMTString* and *toUTCString* should be the same function. This is not true in Google Chrome and Internet Explorer, yet both functions return the same result.

## <span>See also</span>

### <span>Other articles</span>

-   [toString Method (Date)](/javascript/Date/toString)
-   [toDateString Method (Date)](/javascript/Date/toDateString)
-   [toISOString Method (Date)](/javascript/Date/toISOString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleDateString Method (Date)](/javascript/Date/toLocaleDateString)
-   [toLocaleTimeString Method (Date)](/javascript/Date/toLocaleTimeString)
-   [toTimeString Method (Date)](/javascript/Date/toTimeString)
-   [toUTCString Method (Date)](/javascript/Date/toUTCString)

### <span>External resources</span>

-   [toGMTString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toGMTString)
-   [toGMTString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/a34ehb82%28v=vs.94%29.aspx)

### <span>Specification</span>

[Date.prototype.toGMTString( )](http://www.ecma-international.org/ecma-262/5.1/#sec-B.2.6)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

