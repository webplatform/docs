---
title: toExponential
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/023xd959(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'The toExponential() method formats a number to exponential notation.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Number/toExponential

---
## Summary

The toExponential() method formats a number to exponential notation.

## Syntax

<span class="language">JavaScript</span>

    toExponential([ fractionDigits ])

**fractionDigits**
:   Optional. The number of digits after the decimal point. Must be in the range 0 - 20, inclusive.

## Return Value

Returns a string representation of a number in exponential notation. The string contains one digit before the decimal point, and may contain fractionDigits digits after it.

If fractionDigits is not supplied, the **toExponential** method returns as many digits necessary to uniquely specify the number.

## Examples

Using `toExponential` to format the text presentation of a number.

``` js
var pie = 3.14159;

pie.toPrecision();
// Returns: "3.14159e+0"

pie.toPrecision(3);
// Returns: "3.142e+0"

pie.toPrecision(1);
// Returns: "3.1e+0"

pie.toPrecision(0);
// Returns: "3e+0"
```

## Remarks

### Throws

[`RangeError`](/javascript/Error) when a *fractionDigits* outside the bounds of 0 - 20 (inclusive) was given.

## See also

### Other articles

-   [toFixed Method (Number)](/javascript/Number/toFixed)
-   [toPrecision Method (Number)](/javascript/Number/toPrecision)
-   [toString Method (Number)](/javascript/Number/toString)

### External resources

-   [toExponential(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toExponential)

### Specification

[15.7.4.6 Number.prototype.toExponential(fractionDigits)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.6)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

