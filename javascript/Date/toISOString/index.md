---
title: 'toISOString'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff925953(v=vs.94).aspx)'
compatibility:
  feature: toISOString
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a date as a string value in simplified ISO 8601 Extended format.'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Date/toISOString

---
## Summary

Returns a date as a string value in simplified ISO 8601 Extended format.

## Syntax

    toISOString()

## Return Value

String in simplified [ISO 8601 Extended](http://en.wikipedia.org/wiki/ISO_8601) format: `YYYY-MM-DDTHH:mm:ss.sssZ`

## Examples

``` js
var now = new Date();
console.log(date.toISOString());
// ouputs: "2014-10-08T12:54:27.487Z"
```

Manually assembling the ISO 8601 format (polyfill)

``` js
// if the environment does not support toISOString() yet
// add it to the Date prototype
if (!Date.prototype.toISOString) {
  Date.prototype.toISOString = (function() {
    function twoDigits(value) {
      return (value < 10 ? '0' : ') + value;
    }

    return function toISOString() {
      return this.getUTCFullYear()
        + '-' + twoDigits(this.getUTCMonth() + 1)
        + '-' + twoDigits(this.getUTCDate())
        + 'T' + twoDigits(this.getUTCHours())
        + ':' + twoDigits(this.getUTCMinutes())
        + ':' + twoDigits(this.getUTCSeconds())
        + '.' + (this.getUTCMilliseconds() / 1000).toFixed(3).slice(2, 5)
        + 'Z';
    };
  })();
}
```

## Remarks

### Throws

[`RangeError`](/javascript/Error) when called on a date object with an *invalid date* (e.g. `new Date("I am not a date");` - see [Time Values And Time Range](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.1.1))

## Usage

     The ISO 8601 Extended format is supported by Date.parse(), it is therefore a good choice when dates need to be exchanged between APIs.

## See also

### Other articles

-   [toString Method (Date)](/javascript/Date/toString)
-   [toDateString Method (Date)](/javascript/Date/toDateString)
-   [toGMTString Method (Date)](/javascript/Date/toGMTString)
-   [toLocaleString Method (Date)](/javascript/Date/toLocaleString)
-   [toLocaleDateString Method (Date)](/javascript/Date/toLocaleDateString)
-   [toLocaleTimeString Method (Date)](/javascript/Date/toLocaleTimeString)
-   [toTimeString Method (Date)](/javascript/Date/toTimeString)
-   [toUTCString Method (Date)](/javascript/Date/toUTCString)

### External resources

-   [toISOString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toISOString)
-   [toISOString(), by Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/ff925953%28v=vs.94%29.aspx)
-   [Date Time String Format, ECMAScript 5.1](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.1.15)
-   [Time Values and Time Range, ECMAScript 5.1](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.1.1)
-   [ISO 8601, Wikipedia](http://en.wikipedia.org/wiki/ISO_8601)

### Specification

[Date.prototype.toISOString()](http://www.ecma-international.org/ecma-262/5.1/#sec-15.9.5.43)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

