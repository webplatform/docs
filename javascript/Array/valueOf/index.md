---
title: valueOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155290(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the primitive value of the specified object.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/valueOf

---
## Summary

Returns the primitive value of the specified object.

## Syntax

    valueOf()

## Return Value

Returns the array instance.

## Examples

In the following example, the instantiated array object is the same as the return value of this method.

``` js
var arr = [1, 2, 3, 4];
 var s = arr.valueOf();

 if (arr === s)
 document.write("same");
 else
 document.write("different");

 // Output:
 // same
```

## See also

### Specification

[15.2.4.4 Object.prototype.valueOf ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.2.4.4) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

