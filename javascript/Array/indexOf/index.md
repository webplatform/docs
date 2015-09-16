---
title: indexOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff679977(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the index of the first occurrence of a value in an array.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/indexOf

---
## Summary

Returns the index of the first occurrence of a value in an array.

## Syntax

    indexOf( searchElement [, fromIndex ])

**searchElement**
:   Required. The value to locate in array1.

**fromIndex**
:   Optional. The array index at which to begin the search. If fromIndex is omitted, the search starts at index 0.

## Return Value

The index of the first occurrence of searchElement in the array, or -1 if searchElement is not found.

## Examples

The following examples illustrate the use of the **indexOf** method.

``` js
// Create an array. (The elements start at index 0.)
 var ar = ["ab", "cd", "ef", "ab", "cd"];

 // Determine the first location of "cd".
 document.write(ar.indexOf("cd") + "<br/>");

 // Output: 1

 // Find "cd" starting at index 2.
 document.write(ar.indexOf("cd", 2) + "<br/>");

 // Output: 4

 // Find "gh" (which is not found).
 document.write (ar.indexOf("gh")+ "<br/>");

 // Output: -1

 // Find "ab" with a fromIndex argument of -2.
 // The search starts at index 3, which is the array length plus -2.
 document.write (ar.indexOf("ab", -2) + "<br/>");
 // Output: 3
```

## Remarks

The **indexOf** method searches an array for a specified value. The method returns the index of the first occurrence, or -1 if the specified value is not found.

The search occurs in ascending index order.

The array elements are compared to the searchElement value by strict equality, similar to the === operator. For more information, see [Comparison Operators](/javascript/operators/comparison).

The optional fromIndex argument specifies the array index at which to begin the search. If fromIndex is greater than or equal to the array length, -1 is returned. If fromIndex is negative, the search starts at the array length plus fromIndex.

## See also

### Other articles

-   [JavaScript Methods](/javascript/methods)
-   [Array Object](/javascript/Array)

### Specification

[15.4.4.14 Array.prototype.indexOf ( searchElement [ , fromIndex](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.14) )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

