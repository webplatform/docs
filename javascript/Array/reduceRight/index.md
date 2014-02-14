{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Calls the specified callback function for all the elements in an array, in descending order. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=array1.reduceRight( callbackfn [, initialValue ])
}}
|Values={{JS Syntax Parameter
|Name=array1
|Required=Required
|Description=An array object.
}}{{JS Syntax Parameter
|Name=callbackfn
|Required=Required
|Description=A function that accepts up to four arguments. The '''reduceRight''' method calls the callbackfn function one time for each element in the array.
}}{{JS Syntax Parameter
|Name=initialValue
|Required=Optional
|Description=If initialValue is specified, it is used as the initial value to start the accumulation. The first call to the callbackfn function provides this value as an argument instead of an array value.
}}
}}
{{JS_Return_Value
|Description=An object that contains the accumulated result from the last call to the callback function.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example concatenates array values into a string, separating the values with "::". Because no initial value is provided to the '''reduceRight''' method, the first call to the callback function has 456 as the previousValue argument and 123 as the currentValue argument.
|Code=// Define the callback function.
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
}}{{Single Example
|Language=JavaScript
|Description=The following example finds the sum of the squares of the array elements. The '''reduceRight''' method is called with an initial value of 0.
|Code=// Define the callback function.
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
}}{{Single Example
|Language=JavaScript
|Description=The following example gets those elements of an array whose values are between 1 and 10. The initial value provided to the '''reduceRight''' method is an empty array.
|Code=function Process2(previousArray, currentValue) {
     // If currentValue is between 1 and 10, 
     // append currentValue to the array.
     var nextArray;
     if (currentValue &gt;= 1 &amp;&amp; currentValue &lt;= 10)
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
}}{{Single Example
|Language=JavaScript
|Description=The '''reduceRight''' method can be applied to a string. The following example shows how to use this method to reverse the characters in a string.
|Code=// Define the callback function.
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
}}
}}
{{Remarks_Section
|Remarks=If an initialValue is provided, the '''reduceRight''' method calls the callbackfn function one time for each element in the array, in descending index order. If no initialValue is provided, the '''reduceRight''' method calls the callbackfn function on each element, starting with the second-to-last element, in descending index order.

The return value of the callback function is provided as the previousValue argument on the next call to the callback function. The return value of the last call to the callback function is the return value of the '''reduceRight''' method.

The callback function is not called for missing elements of the array.

To accumulate a result in ascending index order, use the [[javascript/Array/reduce{{!}}reduce Method (Array)]].

The syntax of the callback function is as follows:

<code>function callbackfn(previousValue, currentValue, currentIndex, array1)</code>

You can declare the callback function by using up to four parameters.

The following table lists the callback function parameters.

{{{!}} class='wikitable'
{{!}}-
! Callback argument
! Definition
{{!}}-
{{!}} previousValue
{{!}} The value from the previous call to the callback function. If an initialValue is provided to the '''reduceRight''' method, the previousValue is initialValue the first time the function is called.
{{!}}-
{{!}} currentValue
{{!}} The value of the current array element.
{{!}}-
{{!}} currentIndex
{{!}} The numeric index of the current array element.
{{!}}-
{{!}} array1
{{!}} The array object that contains the element.
{{!}}} 
The first time the callback function is called, the values provided as arguments depend on whether the '''reduceRight''' method has an initialValue argument.

If an initialValue is provided to the '''reduceRight''' method:

* The previousValue argument is initialValue.
* The currentValue argument is the value of the last element present in the array.
If an initialValue is not provided:

* The previousValue argument is the value of the last element present in the array.
* The currentValue argument is the value of the second-to-last element present in the array.
The array object can be modified by the callback function.

The following table describes the results of modifying the array object after the '''reduceRight''' method starts.

{{{!}} class='wikitable'
{{!}}-
! Condition after the '''reduceRight''' method starts
! Element passed to callback function?
{{!}}-
{{!}} Element is added beyond the original length of the array.
{{!}} No.
{{!}}-
{{!}} Element is added to fill in a missing element of the array.
{{!}} Yes, if that index has not yet been passed to the callback function.
{{!}}-
{{!}} Element is changed.
{{!}} Yes, if that element has not yet been passed to the callback function.
{{!}}-
{{!}} Element is deleted from the array.
{{!}} No, unless that element has already been passed to the callback function.
{{!}}}

==Exceptions==
A '''TypeError''' exception is thrown when either of the following conditions is true:

* The callbackfn argument is not a function object.
* The array contains no elements and initialValue is not provided.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Array/reduce{{!}}reduce Method (Array)]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679979(v=vs.94).aspx
|HTML5Rocks_link=
}}