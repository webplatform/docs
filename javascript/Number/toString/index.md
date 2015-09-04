---
title: toString
tags:
  0: JS
  1: Basic
  3: Function
readiness: 'Ready to Use'
summary: 'Returns a string representation of a number.'
uri: javascript/Number/toString

---
# toString

## Summary

Returns a string representation of a number.

## Syntax

    toString([ radix ])

**radix**
:   Optional. The base number system to convert to given as 2 - 36, inclusive. Defaults to 10.

## Return Value

String representing the number value in the given base number system.

Negative numbers are simply preceded by the `-` sign, i.e. there is no conversion to a system like the [Two's Complement](http://en.wikipedia.org/wiki/Two%27s_complement) for binary.

## Examples

The following example illustrates the use of the **toString** method with a number.

``` {.js}
var mph_number = 234.567;
var mph_string = mph_number.toString();

console.log(mph_string);
// Output: "234.567"
console.log(mph_string.length);
// Output: 7
```

The following example illustrates the use of the toString method with a radix argument.

``` {.js}
var mph_number = 199;

// Convert to hexadecimal
mph_number.toString(16);
// Returns: "c7"

// Convert to decimal
mph_number.toString(10);
// Returns: "199"

// Convert to octal
mph_number.toString(8);
// Returns: "307"

// Convert to binary
mph_number.toString(2);
// Returns: "11000111"
```

implicit use of `toString()`

``` {.js}
var mph_number = 199;
String(mph_number) === mph_number.toString(10);
(mph_number + "") === mph_number.toString(10);
```

## Remarks

### Throws

[`RangeError`](/javascript/Error) when a *radix* outside the bounds of 2 - 36 (inclusive) was given.

## See also

### Other articles

-   [toExponential Method (Number)](/javascript/Number/toExponential)
-   [toFixed Method (Number)](/javascript/Number/toFixed)
-   [toPrecision Method (Number)](/javascript/Number/toPrecision)

### External resources

-   [toString(), by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toString)

### Specification

[15.7.4.2 Number.prototype.toString(radix)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.2)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj159596(v=vs.94).aspx)

