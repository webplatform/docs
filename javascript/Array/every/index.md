---
title: every
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
summary: 'Determines whether all the members of an array satisfy the specified test.'
uri: javascript/Array/every

---
# every

## Summary

Determines whether all the members of an array satisfy the specified test.

## Syntax

    every( callbackfn [, thisArg ])

**callbackfn**
:   Required. A function that accepts up to three arguments. The **every** method calls the callbackfn function for each element in array1 until the callbackfn returns false , or until the end of the array.

**thisArg**
:   Optional. An object to which the this keyword can refer in the callbackfn function. If thisArg is omitted, undefined is used as the this value.

## Return Value

true if the callbackfn function returns true for all array elements; otherwise, false. If the array is has no elements, the **every** method returns true.

## Examples

The following example illustrates the use of the **every** method.

``` {.js}
// Define the callback function.
 function CheckIfEven(value, index, ar) {
     document.write(value + " ");

     if (value % 2 == 0)
         return true;
     else
         return false;
 }

 // Create an array.
 var numbers = [2, 4, 5, 6, 8];

 // Check whether the callback function returns true for all of the
 // array values.
 if (numbers.every(CheckIfEven))
     document.write("All are even.");
 else
     document.write("Some are not even.");

 // Output:
 // 2 4 5 Some are not even.
```

The following example illustrates the use of the thisArg argument, which specifies an object to which the this keyword can refer.

``` {.js}
// Create a function that returns true if the value is
 // numeric and within range.
 var checkNumericRange = function(value) {
     if (typeof value !== 'number')
         return false;
     else
         return value >= this.minimum && value <= this.maximum;
 }

 // Create an array of numbers.
 var numbers = [10, 15, 19];

 // Check whether the callback function returns true for
 // all of the array values.
 // The obj argument enables use of the this value
 // within the callback function.

 var obj = { minimum: 10, maximum: 20 }

 if (numbers.every(checkNumericRange, obj))
     document.write ("All are within range.");
 else
     document.write ("Some are not within range.");

 // Output:
 //   All are within range.
```

## Remarks

The **every** method calls the callbackfn function one time for each array element, in ascending index order, until the callbackfn function returns false. If an element that causes callbackfn to return false is found, the **every** method immediately returns false. Otherwise, the every method returns true.

The callback function is not called for missing elements of the array.

In addition to array objects, the **every** method can be used by any object that has a length property and that has numerically indexed property names.

**Note** -- You can use the [some Method (Array)](/javascript/Array/some) to check whether the callback function returns true for any element of an array.

The syntax of the callback function is as follows:

`function callbackfn(value, index, array1)`

You can declare the callback function with up to three parameters.

The following table lists the callback function parameters.

Callback parameter
:   Definition
value
:   The value of the array element.
index
:   The numeric index of the array element.
array1
:   The array object that contains the element.

The array object can be modified by the callback function.

The following table describes the results of modifying the array object after the **every** method starts.

Condition after the **every** method starts
:   Element passed to callback function?
Element is added beyond the original length of the array.
:   No.
Element is added to fill in a missing element of the array.
:   Yes, if that index has not yet been passed to the callback function.
Element is changed.
:   Yes, if that element has not yet been passed to the callback function.
Element is deleted from the array.
:   No, unless that element has already been passed to the callback function.

## Exceptions

If the callbackfn argument is not a function object, a **TypeError** exception is thrown.

## See also

### Specification

[15.4.4.16 Array.prototype.every ( callbackfn [ , thisArg](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.16) )]

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff679981(v=vs.94).aspx)

