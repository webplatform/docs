---
title: pop
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hx9fbx10(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Removes the last element from an array and returns it.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/pop

---
## <span>Summary</span>

Removes the last element from an array and returns it.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    pop( )

## <span>Examples</span>

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

## <span>Remarks</span>

The [push](/javascript/Array/push) and **pop** methods enable you to simulate a stack, which uses the principle of last in, first out (LIFO) to store data.

The required arrayObj reference is an **Array** object.

If the array is empty, undefined is returned.

## <span>See also</span>

### <span>Specification</span>

[15.4.4.6 Array.prototype.pop ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.6) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

