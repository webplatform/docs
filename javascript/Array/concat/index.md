---
title: concat
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
summary: 'Combines two or more arrays.'
uri: javascript/Array/concat

---
# concat

## Summary

Combines two or more arrays.

## Syntax

    concat([ item1 [, item2 [, . . . [, itemN ]]]])

**item1,. . ., itemN**
:   Optional. Additional items to add to the end of array1.

## Examples

The following example shows how to use the **concat** method when used with an array:

``` {.js}
var a, b, c, d;
 a = new Array(1,2,3);
 b = "dog";
 c = new Array(42, "cat");
 d = a.concat(b, c);
 document.write(d);

 //Output:
 1, 2, 3, "dog", 42, "cat"
```

## Remarks

The **concat** method returns an **Array** object containing the concatenation of array1 and any other supplied items.

The items to be added ( item1 itemN ) to the array are added, in order, starting from the first item in the list. If one of the items is an array, its contents are added to the end of array1. If the item is anything other than an array, it is added to the end of the array as a single array element.

Elements of source arrays are copied to the resulting array as follows:

-   If an object is copied from any of the arrays being concatenated to the new array, the object reference continues to point to the same object. A change in either the new array or the original array will result in a change to the other.
-   If a number or string value is added to the new array, only the value is copied. Changing the value in one array does not affect the value in the other.

## See also

### Specification

[15.4.4.4 Array.prototype.concat ( [ string1 [ , string2 [ , …](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.4) ] ] )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/2e06zxh0(v=vs.94).aspx)

