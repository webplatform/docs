---
title: 'Number'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dwab3ed2(v=vs.94).aspx)'
compatibility:
  feature: Number
  topic: javascript
readiness: 'Ready to Use'
summary: 'An object that represents a number of any kind. All JavaScript numbers are 64-bit floating-point numbers.'
tags:
  - JS
  - Basic
uri: javascript/Number

---
## Summary

An object that represents a number of any kind. All JavaScript numbers are 64-bit floating-point numbers.

## Syntax

    new Number( value )

**value**
:   Required. The numeric value.

## Examples

``` js
// Returns an Object
var thousand = new Number(1000);
console.log(thousand.valueOf() === 1000);

// remember, objects are not primitives
console.log(thousand !== 1000);
// non-strict comparison calls valueOf() implicitly
console.log(thousand == 1000);
```

``` js
// Returns an Object
var googol = new Number(1e+100);
console.log(googol.valueOf() === 1e+100);
```

``` js
// Alfred B. Taylor octal notation for the decimal number 10
var untydu = new Number(012);
console.log(untydu.valueOf() === 10);
```

``` js
// Converting decimal variables to hexadecimal notation
// by http://stackoverflow.com/users/444910/mystifeid
function decimalToHex(d) {
 // converting negative numbers to positive using Math.abs()
  var hex = Number(Math.abs(d)).toString(16);
  hex = "000000".substr(0, 6 - hex.length) + hex;
  return hex;
}
console.log(decimalToHex(127) === "00007f");
console.log(parseInt("00007f", 16) === 127);
```

``` js
// Infinity JavaScript Number constant
var andBeyond = 3 / 0;
console.log(andBeyond === Infinity);
```

## Remarks

JavaScript creates **Number** objects when a variable is set to a number value, for example `var num = 255.336;`. It is seldom necessary to create **Number** objects explicitly.

The **Number** object has its own properties and methods, in addition to the properties and methods inherited from **Object**. Numbers are converted into strings under certain circumstances, for example when a number is added or concatenated with a string, as well as by means of the **toString** method. For more information, see [Addition Operator (+)](/javascript/operators/addition).

JavaScript has several number constants. For a complete list, see [Number Constants](/javascript/Number/constants).

For a value that can not be converted to a number, the `Number()` function returns the special value **NaN (Not-a-Number)** which indicates that the expression could not be evaluated to a number.

Only basic types such as strings and boolean values can be converted to numbers. Note, however, that a string can be converted to a number only if it is a numeric string:

``` js
Number("123"); // 123
Number("foo"); // NaN
Number("123foo"); // NaN
```

**Integer range**

Biggest int possible is 9007199254740992.
 Smallest int possible is -9007199254740992.

``` js
var biggestInt = Math.pow(2, 53); // 9007199254740992
console.log(biggestInt  + 1 === 9007199254740992) ;
console.log(biggestInt  + 2 === 9007199254740994) ;
```

**Octals and Hexadecimals**

Octal (base-8) and hexadecimal (base-16) numbers can be used in JavaScript.
 Octal numbers must begin with 0 (zero) followed by one or more octal digits.
 Hexadecimal numbers must begin with 0x.

## Properties

The following table lists the properties of the **Number** object.

|Property|Description|
|:-------|:----------|
|[constants](/javascript/Number/constants)|Lists the constants of the Number object.|
|[constructor](/javascript/Number/constructor)|Specifies the function that creates an object.|
|[prototype](/javascript/Number/prototype)|Returns a reference to the prototype for a class of number.|

## Methods

The following table lists the methods of the **Number** object.

|Method|Description|
|:-----|:----------|
|[toExponential](/javascript/Number/toExponential)|Returns a string that contains a number represented in exponential notation.|
|[toFixed](/javascript/Number/toFixed)|Returns a string that represents a number in fixed-point notation.|
|[toPrecision](/javascript/Number/toPrecision)|Returns a string that contains a number that is represented in either exponential or fixed-point notation and that has a specified number of digits.|
|[toString](/javascript/Number/toString)|Returns a string representation of an object.|
|[valueOf](/javascript/Number/valueOf)|Returns the primitive value of the specified object.|

## See also

### Related articles

#### Javascript

-   [propertyName](/dom/TransitionEvent/propertyName)

-   **Number**

-   [unicode](/javascript/RegExp/unicode)

-   [future reserved words](/javascript/future_reserved_words)

### Other articles

-   [JavaScript Objects](/javascript/objects)
-   [Math Object](/javascript/Math)
-   [new Operator](/javascript/operators/new)
-   [JavaScript NaN constant](/javascript/NaN)
-   [JavaScript Infinity constant](/javascript/Infinity)

### External resources

-   <http://en.wikipedia.org/wiki/Octal>
-   <http://en.wikipedia.org/wiki/Hexadecimal>
-   <http://www.2ality.com/2012/04/number-encoding.html>

### Specification

[8.5 The Number Type](http://www.ecma-international.org/ecma-262/5.1/#sec-8.5)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

