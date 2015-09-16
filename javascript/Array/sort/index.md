---
title: sort
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/4b4fbfhk(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sorts an Array.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/sort

---
## Summary

Sorts an Array.

## Syntax

<span class="language">JavaScript</span>

    sort( sortFunction )

**sortFunction**
:   Optional. The name of the function used to determine the order of the elements. If omitted, the elements are sorted in ascending, ASCII character order.

## Return Value

The sorted array.

## Examples

The following example shows how to use the **sort** method.

``` js
var a = new Array(4, 11, 2, 10, 3, 1);

 var b = a.sort();
 document.write(b);
 document.write("<br/>");

 // This is ASCII character order.
 // Output: 1,10,11,2,3,4)

 // Sort the array elements with a function that compares array elements.
 b = a.sort(CompareForSort);
 document.write(b);
 document.write("<br/>");
 // Output: 1,2,3,4,10,11.

 // Sorts array elements in ascending order numerically.
 function CompareForSort(first, second)
 {
     if (first == second)
         return 0;
     if (first < second)
         return -1;
     else
         return 1;
 }
```

## Remarks

The **sort** method sorts the **Array** object in place; no new **Array** object is created during execution.

If you supply a function in the sortFunction argument, it must return one of the following values:

-   A negative value if the first argument passed is less than the second argument.
-   Zero if the two arguments are equivalent.
-   A positive value if the first argument is greater than the second argument.

## See also

### Specification

[15.4.4.11 Array.prototype.sort (comparefn)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.11) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

