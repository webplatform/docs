---
title: map
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff679976(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Calls a defined callback function on each element of an array, and returns an array that contains the results.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/map

---
## <span>Summary</span>

Calls a defined callback function on each element of an array, and returns an array that contains the results.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    map( callbackfn [, thisArg ])

**callbackfn**
:   Required. A function that accepts up to three arguments. The **map** method calls the callbackfn function one time for each element in the array.

**thisArg**
:   Optional. An object to which the this keyword can refer in the callbackfn function. If thisArg is omitted, undefined is used as the this value.

## <span>Return Value</span>

A new array in which each element is the callback function return value for the associated original array element.

## <span>Examples</span>

The following example illustrates the use of the **map** method.

``` js
// Define the callback function.
 function AreaOfCircle(radius) {
     var area = Math.PI * (radius * radius);
     return area.toFixed(0);
 }

 // Create an array.
 var radii = [10, 20, 30];

 // Get the areas from the radii.
 var areas = radii.map(AreaOfCircle);

 document.write(areas);

 // Output:
 // 314,1257,2827
```

The following example illustrates the use of the thisArg argument, which specifies an object to which the this keyword can refer.

``` js
// Define an object that contains a divisor property and
 // a remainder function.
 var obj = {
     divisor: 10,
     remainder: function (value) {
         return value % this.divisor;
     }
 }

 // Create an array.
 var numbers = [6, 12, 25, 30];

 // Get the remainders.
 // The obj argument specifies the this value in the callback function.
 var result = numbers.map(obj.remainder, obj);
 document.write(result);

 // Output:
 // 6,2,5,0
```

In the following example, a built-inJavaScript method is used as the callback function.

``` js
// Apply Math.sqrt(value) to each element in an array.
 var numbers = [9, 16];
 var result = numbers.map(Math.sqrt);

 document.write(result);
 // Output: 3,4
```

The **map** method can be applied to a string. The following example illustrates this.

``` js
// Define the callback function.
 function threeChars(value, index, str) {
     // Create a string that contains the previous, current,
     // and next character.
     return str.substring(index - 1, index + 2);
 }

 // Create a string.
 var word = "Thursday";

 // Apply the map method to the string.
 // Each array element in the result contains a string that
 // has the previous, current, and next character.
 // The commented out statement shows an alternative syntax.
 var result = [].map.call(word, threeChars);
 // var result = Array.prototype.map.call(word, threeChars);

 document.write(result);

 // Output:
 // Th,Thu,hur,urs,rsd,sda,day,ay
```

## <span>Remarks</span>

The **map** method calls the callbackfn function one time for each element in the array, in ascending index order. The callback function is not called for missing elements of the array.

In addition to array objects, the **map** method can be used by any object that has a length property and that has numerically indexed property names.

The syntax of the callback function is as follows:

`function callbackfn(value, index, array1)`

You can declare the callback function by using up to three parameters.

The following table lists the callback function parameters.

|Callback argument|Definition|
|:----------------|:---------|
|value|The value of the array element.|
|index|The numeric index of the array element.|
|array1|The array object that contains the element.|

The array object can be modified by the callback function.

The following table describes the results of modifying the array object after the **map** method starts.

|Condition after the **map** method starts|Element passed to callback function?|
|:----------------------------------------|:-----------------------------------|
|Element is added beyond the original length of the array.|No.|
|Element is added to fill in a missing element of the array.|Yes, if that index has not yet been passed to the callback function.|
|Element is changed.|Yes, if that element has not yet been passed to the callback function.|
|Element is deleted from the array.|No, unless that element has already been passed to the callback function.|

## <span>Exceptions</span>

If the callbackfn argument is not a function object, a **TypeError** exception is thrown.

## <span>See also</span>

### <span>Specification</span>

[15.4.4.19 Array.prototype.map ( callbackfn [ , thisArg](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.19) )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

