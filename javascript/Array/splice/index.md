---
title: 'splice'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/wctc5k7s(v=vs.94).aspx)'
compatibility:
  feature: splice
  topic: javascript
readiness: 'Ready to Use'
summary: 'Removes elements from an array and, if necessary, inserts new elements in their place, returning the deleted elements.'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Array/splice

---
## Summary

Removes elements from an array and, if necessary, inserts new elements in their place, returning the deleted elements.

## Syntax

    splice( start, deleteCount,  [ item1 [, item2 [, . . . [, itemN ]]]])

**start**
:   Required. The zero-based location in the array from which to start removing elements.

**deleteCount**
:   Required. The number of elements to remove.

**item1, item2,. . ., itemN**
:   Optional. Elements to insert into the array in place of the deleted elements.

## Examples

The following code shows how to use the **splice** method.

``` js
var arr = new Array("4", "11", "2", "10", "3", "1");
 arr.splice(2, 2, "21", "31");
 document.write(arr);

 // Output: 4,11,21,31,3,1
```

## Remarks

The **splice** method modifies arrayObj by removing the specified number of elements from position start and inserting new elements. The deleted elements are returned as a new **Array** object.

## See also

### Specification

[15.4.4.12 Array.prototype.splice (start, deleteCount [ , item1 [ , item2 [ , …](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.12) ] ] )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

