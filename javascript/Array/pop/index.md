---
title: 'pop'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hx9fbx10(v=vs.94).aspx)'
compatibility:
  feature: pop
  topic: javascript
readiness: 'Ready to Use'
summary: 'Removes the last element from an array and returns it.'
tags:
  - JS_Basic
  - JS_Method
uri: javascript/Array/pop

---
## Summary

Removes the last element from an array and returns it.

## Syntax

    pop( )

## Examples

The following example illustrates the use of the pop method.

``` js
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

 // Output: 9 8 7 6 5
```

## Remarks

The [push](/javascript/Array/push) and **pop** methods enable you to simulate a stack, which uses the principle of last in, first out (LIFO) to store data.

The required arrayObj reference is an **Array** object.

If the array is empty, undefined is returned.

## See also

### Specification

[15.4.4.6 Array.prototype.pop ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.6) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

