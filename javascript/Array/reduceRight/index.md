---
title: reduceRight
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff679979(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Calls the specified callback function for all the elements in an array, in descending order. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/reduceRight

---
## <span>Summary</span>

Calls the specified callback function for all the elements in an array, in descending order. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    reduceRight( callbackfn [, initialValue ])

**callbackfn**
:   Required. A function that accepts up to four arguments. The **reduceRight** method calls the callbackfn function one time for each element in the array.

**initialValue**
:   Optional. If initialValue is specified, it is used as the initial value to start the accumulation. The first call to the callbackfn function provides this value as an argument instead of an array value.

## <span>Return Value</span>

An object that contains the accumulated result from the last call to the callback function.

## <span>Examples</span>

The following example concatenates array values into a string, separating the values with "::". Because no initial value is provided to the **reduceRight** method, the first call to the callback function has 456 as the previousValue argument and 123 as the currentValue argument.

``` js
// Define the callback function.
 function appendCurrent (previousValue, currentValue) {
     return previousValue + "::" + currentValue;
     }

 // Create an array.
 var elements = ["abc", "def", 123, 456];

 // Call the reduceRight method, which calls the callback function
 // for each array element, in descending index order.
 var result = elements.reduceRight(appendCurrent);

 document.write(result);

 // Output:
 //  456::123::def::abc
```

The following example finds the sum of the squares of the array elements. The **reduceRight** method is called with an initial value of 0.

``` js
// Define the callback function.
 function Process(previousValue, currentValue, index, array) {
     // Add the previous value to the current value squared.
     var nextValue = previousValue + (currentValue * currentValue);

     // If this is not the last call by the reduceRight method,
     // the return value is previousValue on the next call.
     // If this is the last call by the reduceRight method, the
     // return value is the return value of the reduceRight method.
     return nextValue;
 }

 // Create an array.
 var numbers = [3, 4, 5];

 // Call the reduceRight method with an initial value of 0.
 var sumOfSquares = numbers.reduceRight(Process, 0);

 document.write("sum of squares=" + sumOfSquares);

 // Output:
 //  sum of squares=50
```

The following example gets those elements of an array whose values are between 1 and 10. The initial value provided to the **reduceRight** method is an empty array.

``` js
function Process2(previousArray, currentValue) {
     // If currentValue is between 1 and 10,
     // append currentValue to the array.
     var nextArray;
     if (currentValue >= 1 && currentValue <= 10)
         nextArray = previousArray.concat(currentValue);
     else
         nextArray = previousArray;

     // If this is not the last call by the reduceRight method,
     // the returned array is previousArray on the next call.
     // If this is the last call by the reduceRight method, the
     // returned array is the return value of the reduceRight method.
     return nextArray;
 }

 // Create an array.
 var numbers = [20, 1, -5, 6, 50, 3];

 // Call the reduceRight method, starting with an empty array.
 var emptyArray = new Array();
 var resultArray = numbers.reduceRight(Process2, emptyArray);

 document.write("result array=" + resultArray);

 // Output:
 //  result array=3,6,1
```

The **reduceRight** method can be applied to a string. The following example shows how to use this method to reverse the characters in a string.

``` js
// Define the callback function.
 function AppendToArray(previousValue, currentValue) {
     return previousValue + currentValue;
 }

 var word = "retupmoc";

 // Create a string that reverses the characters of another string.
 // The commented-out statement shows an alternative syntax.
 var result = [].reduceRight.call(word, AppendToArray, "the ");
 // var result = Array.prototype.reduceRight.call(word, AppendToArray, "the ");

 document.write(result);

 // Output:
 // the computer
```

## <span>Remarks</span>

If an initialValue is provided, the **reduceRight** method calls the callbackfn function one time for each element in the array, in descending index order. If no initialValue is provided, the **reduceRight** method calls the callbackfn function on each element, starting with the second-to-last element, in descending index order.

The return value of the callback function is provided as the previousValue argument on the next call to the callback function. The return value of the last call to the callback function is the return value of the **reduceRight** method.

The callback function is not called for missing elements of the array.

To accumulate a result in ascending index order, use the [reduce Method (Array)](/javascript/Array/reduce).

The syntax of the callback function is as follows:

`function callbackfn(previousValue, currentValue, currentIndex, array1)`

You can declare the callback function by using up to four parameters.

The following table lists the callback function parameters.

|Callback argument|Definition|
|:----------------|:---------|
|previousValue|The value from the previous call to the callback function. If an initialValue is provided to the **reduceRight** method, the previousValue is initialValue the first time the function is called.|
|currentValue|The value of the current array element.|
|currentIndex|The numeric index of the current array element.|
|array1|The array object that contains the element.|

The first time the callback function is called, the values provided as arguments depend on whether the **reduceRight** method has an initialValue argument.

If an initialValue is provided to the **reduceRight** method:

-   The previousValue argument is initialValue.
-   The currentValue argument is the value of the last element present in the array.

If an initialValue is not provided:

-   The previousValue argument is the value of the last element present in the array.
-   The currentValue argument is the value of the second-to-last element present in the array.

The array object can be modified by the callback function.

The following table describes the results of modifying the array object after the **reduceRight** method starts.

|Condition after the **reduceRight** method starts|Element passed to callback function?|
|:------------------------------------------------|:-----------------------------------|
|Element is added beyond the original length of the array.|No.|
|Element is added to fill in a missing element of the array.|Yes, if that index has not yet been passed to the callback function.|
|Element is changed.|Yes, if that element has not yet been passed to the callback function.|
|Element is deleted from the array.|No, unless that element has already been passed to the callback function.|

## <span>Exceptions</span>

A **TypeError** exception is thrown when either of the following conditions is true:

-   The callbackfn argument is not a function object.
-   The array contains no elements and initialValue is not provided.

## <span>See also</span>

### <span>Specification</span>

[15.4.4.22 Array.prototype.reduceRight ( callbackfn [ , initialValue](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.22) )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

