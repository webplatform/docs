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
## <span>Summary</span>

The toExponential() method formats a number to exponential notation.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    toExponential([ fractionDigits ])

**fractionDigits**
:   Optional. The number of digits after the decimal point. Must be in the range 0 - 20, inclusive.

## <span>Return Value</span>

Returns a string representation of a number in exponential notation. The string contains one digit before the decimal point, and may contain fractionDigits digits after it.

If fractionDigits is not supplied, the **toExponential** method returns as many digits necessary to uniquely specify the number.

## <span>Examples</span>

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

## <span>Remarks</span>

### <span>Throws</span>

[`RangeError`](/javascript/Error) when a *fractionDigits* outside the bounds of 0 - 20 (inclusive) was given.

## <span>See also</span>

### <span>Other articles</span>

-   [toFixed Method (Number)](/javascript/Number/toFixed)
-   [toPrecision Method (Number)](/javascript/Number/toPrecision)
-   [toString Method (Number)](/javascript/Number/toString)

### <span>External resources</span>

-   [toExponential(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toExponential)

### <span>Specification</span>

[15.7.4.6 Number.prototype.toExponential(fractionDigits)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.6)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

