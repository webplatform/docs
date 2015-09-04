---
title: push
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
summary: 'Appends new elements to an array, and returns the new length of the array.'
uri: javascript/Array/push

---
# push

## Summary

Appends new elements to an array, and returns the new length of the array.

## Syntax

    push([ item1  [ item2 [. . . [ itemN ]]]])

**item, item2,. . ., itemN**
:   Optional. New elements of the **Array**.

## Examples

The following example illustrates the use of the **push** method.

``` {.js}
var number;
 var my_array = new Array();

 my_array.push (5, 6, 7);
 my_array.push (8, 9);

 number = my_array.pop();
 while (number != undefined)
    {
    document.write (number + " ");
    number = my_array.pop();
    }

 // Output:
 // 9 8 7 6 5
```

## Remarks

The **push** and **pop** methods allow you to simulate a last in, first out stack.

The **push** method appends elements in the order in which they appear. If one of the arguments is an array, it is added as a single element. Use the **concat** method to join the elements from two or more arrays.

## See also

### Specification

[15.4.4.7 Array.prototype.push ( [ item1 [ , item2 [ , …](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.7) ] ] )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/6d0cbb1w(v=vs.94).aspx)

