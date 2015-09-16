---
title: 'shift'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9e7b4w20(v=vs.94).aspx)'
compatibility:
  feature: shift
  topic: javascript
readiness: 'Ready to Use'
summary: 'Removes the first element from an array and returns it.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/shift

---
## Summary

Removes the first element from an array and returns it.

## Syntax

    shift( )

## Return Value

Returns the element removed from the array.

## Examples

The following example illustrates the use of the shift method.

``` js
var arr = new Array(10, 11, 12);
 while (arr.length > 0)
     {
     var i = arr.shift();
     document.write (i.toString() + " ");
     }

 // Output:
 // 10 11 12
```

## See also

### Specification

[15.4.4.9 Array.prototype.shift ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.9) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

