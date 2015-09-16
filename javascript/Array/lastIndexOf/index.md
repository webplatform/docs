---
title: 'lastIndexOf'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff679972(v=vs.94).aspx)'
compatibility:
  feature: lastIndexOf
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the index of the last occurrence of a specified value in an array.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/lastIndexOf

---
## Summary

Returns the index of the last occurrence of a specified value in an array.

## Syntax

    lastIndexOf( searchElement [, fromIndex ])

**searchElement**
:   Required. The value to locate in array1.

**fromIndex**
:   Optional. The array index at which to begin the search. If fromIndex is omitted, the search starts at the last index in the array.

## Return Value

The index of the last occurrence of searchElement in the array, or -1 if searchElement is not found.

## Examples

The following examples illustrate the use of the **lastIndexOf** method.

``` js
// Create an array.
 var ar = ["ab", "cd", "ef", "ab", "cd"];

 // Determine the first location, in descending order, of "cd".
 document.write(ar.lastIndexOf("cd") + "<br/>");

 // Output: 4

 // Find "cd" in descending order, starting at index 2.
 document.write(ar.lastIndexOf("cd", 2) + "<br/>");

 // Output: 1

 // Search for "gh" (which is not found).
 document.write(ar.lastIndexOf("gh")+ "<br/>");

 // Output: -1

 // Find "ab" with a fromIndex argument of -3.
 // The search in descending order starts at index 3,
 // which is the array length minus 2.
 document.write(ar.lastIndexOf("ab", -3) + "<br/>");
 // Output: 0
```

## Remarks

The **lastIndexOf** method searches an array for a specified value. The method returns the index of the last occurrence, or -1 if the specified value is not found.

The search occurs in descending index order (last member first). To search in ascending order, use the [indexOf Method (Array)](/javascript/Array/indexOf).

The array elements are compared to the searchElement value by strict equality, similar to the comparison made by the === operator. For more information, see [Comparison Operators](/javascript/operators/comparison).

The optional fromIndex argument specifies the array index at which to begin the search. If fromIndex is greater than or equal to the array length, the whole array is searched. If fromIndex is negative, the search starts at the array length plus fromIndex. If the computed index is less than 0, -1 is returned.

## See also

### Specification

[15.4.4.15 Array.prototype.lastIndexOf ( searchElement [ , fromIndex](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.15) )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

