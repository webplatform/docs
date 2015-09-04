---
title: bind
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'For a given function, creates a bound function that has the same body as the original function. In the bound function, the this object resolves to the passed in object. The bound function has the specified initial parameters.'
uri: javascript/Function/bind

---
# bind

## Summary

For a given function, creates a bound function that has the same body as the original function. In the bound function, the this object resolves to the passed in object. The bound function has the specified initial parameters.

## Syntax

    function.bind( thisArg [, arg1 [, arg2 [, argN ]]])

**function**
:   Required. A function object.

**thisArg**
:   Required. An object to which the this keyword can refer inside the new function.

**arg1 [, arg2 [, argN ]]]**
:   Optional. A list of arguments to be passed to the new function.

## Return Value

A new function that is the same as the function function, except for the thisArg object and the initial arguments.

## Examples

The following code shows how to use the **bind** method.

``` {.js}
// Define the original function.
 var checkNumericRange = function (value) {
     if (typeof value !== 'number')
         return false;
     else
         return value >= this.minimum && value <= this.maximum;
 }

 // The range object will become the this value in the callback function.
 var range = { minimum: 10, maximum: 20 };

 // Bind the checkNumericRange function.
 var boundCheckNumericRange = checkNumericRange.bind(range);

 // Use the new function to check whether 12 is in the numeric range.
 var result = boundCheckNumericRange (12);
 document.write(result);

 // Output: true
```

In the following example, the thisArg object is different from the object that contains the original method.

``` {.js}
// Create an object that contains the original function.
 var originalObject = {
     minimum: 50,
     maximum: 100,
     checkNumericRange: function (value) {
         if (typeof value !== 'number')
             return false;
         else
             return value >= this.minimum && value <= this.maximum;
     }
 }

 // Check whether 10 is in the numeric range.
 var result = originalObject.checkNumericRange(10);
 document.write(result + " ");
 // Output: false

 // The range object supplies the range for the bound function.
 var range = { minimum: 10, maximum: 20 };

 // Create a new version of the checkNumericRange function that uses range.
 var boundObjectWithRange = originalObject.checkNumericRange.bind(range);

 // Check whether 10 is in the numeric range.
 var result = boundObjectWithRange(10);
 document.write(result);
 // Output: true
```

The following code shows how to use the arg1[,arg2[,argN]]] arguments. The bound function uses the parameters specified in the **bind** method as the first and second parameters. Any parameters specified when the bound function is called are used as the third, fourth (and so on) parameters.

``` {.js}
// Define the original function with four parameters.
 var displayArgs = function (val1, val2, val3, val4) {
     document.write(val1 + " " + val2 + " " + val3 + " " + val4);
 }

 var emptyObject = {};

 // Create a new function that uses the 12 and "a" parameters
 // as the first and second parameters.
 var displayArgs2 = displayArgs.bind(emptyObject, 12, "a");

 // Call the new function. The "b" and "c" parameters are used
 // as the third and fourth parameters.
 displayArgs2("b", "c");
 // Output: 12 a b c
```

## Exceptions

If the specified function is not a function, a **TypeError** exception is thrown.

## See also

### Other articles

-   [Function Object](/javascript/Function)
-   [filter Method (Array)](/javascript/Array/filter)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff841995(v=vs.94).aspx)

