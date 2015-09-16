---
title: 'reverse'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/3333858x(v=vs.94).aspx)'
compatibility:
  feature: reverse
  topic: javascript
readiness: 'Ready to Use'
summary: 'Reverses the elements in an Array.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/reverse

---
## Summary

Reverses the elements in an Array.

## Syntax

    reverse()

## Return Value

The reversed array.

## Examples

The following example illustrates the use of the **reverse** method.

``` js
var arr = new Array(0,1,2,3,4);
 var reverseArr = arr.reverse();
 document.write(reverseArr);

 // Output:
 // 4,3,2,1,0
```

## Remarks

The required arrayObj reference is an **Array** object.

The **reverse** method reverses the elements of an **Array** object in place. It does not create a new **Array** object during execution.

If the array is not contiguous, the **reverse** method creates elements in the array that fill the gaps in the array. Each of these created elements has the value undefined.

## See also

### Specification

[15.4.4.8 Array.prototype.reverse ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.8) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

