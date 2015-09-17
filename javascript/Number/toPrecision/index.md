---
title: 'toPrecision'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/kcs121ad(v=vs.94).aspx)'
compatibility:
  feature: toPrecision
  topic: javascript
readiness: 'Ready to Use'
summary: 'Represents a number either in exponential or fixed-point notation with a specified number of digits.'
tags:
  - JS_Basic
  - JS_Function
uri: javascript/Number/toPrecision

---
## Summary

Represents a number either in exponential or fixed-point notation with a specified number of digits.

## Syntax

    toPrecision([ precision ])

**precision**
:   Optional. The number of significant digits. Must be in the range 1 - 21, inclusive.

## Return Value

For numbers in exponential notation, precision - 1 digits are returned after the decimal point. For numbers in fixed notation, precision significant digits are returned.

If precision is not supplied or is `undefined` , [`toString()`](/javascript/Number/toString) is called instead.

## Examples

Using `toPrecision` to format the decimal presentation of a number.

``` js
var pie = 3.14159;

// Call passed through to toString()
pie.toPrecision();
// Returns: "3.14159"

pie.toPrecision(5);
// Returns: "3.1416"

pie.toPrecision(2);
// Returns: "3.1"

pie.toPrecision(1);
// Returns: "3"

// Watch out for exponential notation
(1234.5).toPrecision(2);
// Returns "1.2e+3"
```

## Remarks

### Throws

[`RangeError`](/javascript/Error) when a *fractionDigits* outside the bounds of 1 - 21 (inclusive) was given.

## See also

### Other articles

-   [toExponential Method (Number)](/javascript/Number/toExponential)
-   [toFixed Method (Number)](/javascript/Number/toFixed)
-   [toString Method (Number)](/javascript/Number/toString)

### External resources

-   [toPrecision(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toPrecision)

### Specification

[15.7.4.7 Number.prototype.toPrecision(precision)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.7)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

