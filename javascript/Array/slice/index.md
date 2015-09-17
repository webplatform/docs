---
title: 'slice'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/tkcsy6fe(v=vs.94).aspx)'
compatibility:
  feature: slice
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a section of an array.'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Array/slice

---
## Summary

Returns a section of an array.

## Syntax

    slice( start , [ end ])

**start**
:   Required. The beginning of the specified portion of arrayObj.

**end**
:   Optional. The end of the specified portion of arrayObj.

## Examples

The following examples show how to use the slice method. In the first example, all but the last element of `myArray` is copied into `newArray`. In the second example, only the last two elements of `myArray` are copied into `newArray`.

``` js
var origArray = [3, 5, 7, 9];
 var newArray = origArray.slice(0, -1);
 document.write(origArray);
 document.write("<br/>");
 newArray = origArray.slice(-2);
 document.write(newArray);

 // Output:
 // 3,5,7,9
 // 7,9
```

## Remarks

The **slice** method returns an **Array** object containing the specified portion of arrayObj.

The **slice** method copies up to, but not including, the element indicated by end. If start is negative, it is treated as length + start , where length is the length of the array. If end is negative, it is treated as length + end where length is the length of the array. If end is omitted, extraction continues to the end of arrayObj. If end occurs before start , no elements are copied to the new array.

## See also

### Specification

[15.4.4.10 Array.prototype.slice (start, end)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.10) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

