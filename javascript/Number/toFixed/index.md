---
title: toFixed
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/sstyff0z(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'The toFixed() method formats a number to fixed-point notation (decimal).'
tags:
  0: JS
  1: Basic
  3: Function
uri: javascript/Number/toFixed

---
## Summary

The toFixed() method formats a number to fixed-point notation (decimal).

## Syntax

    toFixed([ fractionDigits ])

**fractionDigits**
:   Optional. The number of digits after the decimal point. Must be in the range 0 - 20, inclusive. Defaults to 0.

## Return Value

Returns a string representation of a number in fixed-point notation, containing fractionDigits digits after the decimal point.

If fractionDigits is not supplied or **undefined** , the default value is 0.

## Examples

Using `toFixed` to format the decimal presentation of a number.

``` js
var pie = 3.14159;

// output a number without decimal digits
pie.toFixed(0);
// Returns: "3"

// decimal digits are rounded if necessary
pie.toFixed(4);
// Returns: "3.1416"

// missing decimal digits are added
pie.toFixed(10);
// Returns: "3.1415900000"

// Watch out for number range
(1.23e+20).toFixed(2);
// Returns: "123000000000000000000.00"
(1.23e-10).toFixed(2);
// Returns: "0.00"

// Watch out for operator precedence
-3.1415.toFixed(2);
// Returns: -3.14
(-3.1415).toFixed(2);
// Returns: "-3.14"
```

## Remarks

### Throws

[`RangeError`](/javascript/Error) when a *fractionDigits* outside the bounds of 0 - 20 (inclusive) was given.

## Notes

-   `toFixed(3.9)` will be treated as `toFixed(3)`.
-   If number is greater than `1e+21`, `toFixed()` calls [`toString()`](/javascript/Number/toString) internally and returns a string in exponential notation.

## See also

### Other articles

-   [toExponential Method (Number)](/javascript/Number/toExponential)
-   [toPrecision Method (Number)](/javascript/Number/toPrecision)
-   [toString Method (Number)](/javascript/Number/toString)

### External resources

-   [toFixed(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed)

### Specification

[15.7.4.5 Number.prototype.toFixed(fractionDigits)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.5)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

