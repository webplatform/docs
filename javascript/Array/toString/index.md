---
title: toString
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155287(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a string representation of an array.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/toString

---
## <span>Summary</span>

Returns a string representation of an array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    toString()

## <span>Return Value</span>

The string representation of the array.

## <span>Examples</span>

The following example illustrates the use of the **toString** method with an array.

``` js
var arr = [1, 2, 3, 4];
 var s = arr.toString();
 document.write(s);

 // Output: 1,2,3,4
```

## <span>Remarks</span>

The elements of an **Array** are converted to strings. The resulting strings are concatenated and separated by commas.

## <span>See also</span>

### <span>Specification</span>

[15.4.4.2 Array.prototype.toString ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.2) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

