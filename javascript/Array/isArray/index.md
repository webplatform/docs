---
title: isArray
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff848265(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Determines whether an object is an array.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/isArray

---
## Summary

Determines whether an object is an array.

## Syntax

    Array.isArray( object )

**object**
:   Required. The object to test.

## Return Value

Boolean value. Either true if object is an array; otherwise, false.

If the object argument is not an object, false or undefined is returned.

## Examples

The following example illustrates the use of the **Array.isArray** function.

``` js
// Using Array string litteral
var ar = [];
 var result = Array.isArray(ar);
 // Output: true

// Using new Array with an empty set
 var ar = new Array();
 var result = Array.isArray(ar);
 // Output: true

 var ar = [1, 2, 3];
 var result = Array.isArray(ar);
 // Output: true

// Testing with a string litteral "an array"
 var injectingString = Array.isArray("an array");
 document.write(injectingString);
 // Output: false

// Testing with an object litteral
 var injectingObject = Array.isArray({});
 document.write(injectingObject);
 // Output: false
```

## See also

### Other articles

-   [Array Object](/javascript/Array)
-   [typeof Operator](/javascript/operators/typeof)

### Specification

[15.4.3.2 Array.isArray ( arg )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.3.2) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

