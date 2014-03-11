{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Calls the specified callback function for all the elements in an array. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=reduce( callbackfn [, initialValue ])
}}
|Values={{JS Syntax Parameter
|Name=callbackfn
|Required=Required
|Description=A function that accepts up to four arguments. The '''reduce''' method calls the callbackfn function one time for each element in the array.
}}{{JS Syntax Parameter
|Name=initialValue
|Required=Optional
|Description=If initialValue is specified, it is used as the initial value to start the accumulation. The first call to the callbackfn function provides this value as an argument instead of an array value.
}}
}}
{{JS_Return_Value
|Description=The accumulated result from the last call to the callback function.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example concatenates array values into a string, separating the values with "::". Because no initial value is provided to the '''reduce''' method, the first call to the callback function has "abc" as the previousValue argument and "def" as the currentValue argument.
|Code=// Define the callback function.
 function appendCurrent (previousValue, currentValue) {
     return previousValue + "::" + currentValue;
     }
 
 // Create an array.
 var elements = ["abc", "def", 123, 456];
 
 // Call the reduce method, which calls the callback function
 // for each array element.
 var result = elements.reduce(appendCurrent);
 
 document.write(result);
 
 // Output:
 //  abc::def::123::456
}}{{Single Example
|Language=JavaScript
|Description=The following example adds the values of an array after they have been rounded. The '''reduce''' method is called with an initial value of 0.
|Code=// Define the callback function.
 function addRounded (previousValue, currentValue) {
     return previousValue + Math.round(currentValue);
     }
 
 // Create an array.
 var numbers = [10.9, 15.4, 0.5];
 
 // Call the reduce method, starting with an initial value of 0.
 var result = numbers.reduce(addRounded, 0);
 
 document.write (result);
 // Output: 27
}}{{Single Example
|Language=JavaScript
|Description=The following example adds the values in an array. The currentIndex and array1 parameters are used in the callback function.
|Code=function addDigitValue(previousValue, currentDigit, currentIndex, array) {
     var exponent = (array.length - 1) - currentIndex;
     var digitValue = currentDigit * Math.pow(10, exponent);
     return previousValue + digitValue;
     }
 
 var digits = [4, 1, 2, 5];
 
 // Determine an integer that is computed from values in the array.
 var result = digits.reduce(addDigitValue, 0);
 
 document.write (result);
 // Output: 4125
}}{{Single Example
|Language=JavaScript
|Description=The following example gets an array that contains only those values that are between 1 and 10 in another array. The initial value provided to the '''reduce''' method is an empty array.
|Code=function Process(previousArray, currentValue) {
     // If currentValue is between 1 and 10, 
     // append currentValue to the array.
     var nextArray;
     if (currentValue &gt;= 1 &amp;&amp; currentValue &lt;= 10)
         nextArray = previousArray.concat(currentValue);
     else
         nextArray = previousArray;
 
     // If this is not the last call by the reduce method,
     // the returned array is previousArray on the next call.
     // If this is the last call by the reduce method, the
     // returned array is the return value of the reduce method.
     return nextArray;
 }
 
 // Create an array.
 var numbers = [20, 1, -5, 6, 50, 3];
 
 // Call the reduce method, starting with an initial empty array.
 var emptyArray = new Array();
 var resultArray = numbers.reduce(Process, emptyArray);
 
 document.write("result array=" + resultArray);
 
 // Output:
 // result array=1,6,3
}}
}}
{{Remarks_Section
|Remarks=If an initialValue is provided, the '''reduce''' method calls the callbackfn function one time for each element present in the array, in ascending index order. If an initialValue is not provided, the '''reduce''' method calls the callbackfn function on each element, starting with the second element.

The return value of the callback function is provided as the previousValue argument on the next call to the callback function. The return value of the last call to the callback function is the return value of the '''reduce''' method.

The callback function is not called for missing elements of the array.

'''Note''' -- The [[javascript/Array/reduceRight{{!}}reduceRight Method (Array)]] processes the elements in descending index order.

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
{{!}} The value from the previous call to the callback function. If an initialValue is provided to the '''reduce''' method, the previousValue is initialValue the first time the function is called.
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
The first time the callback function is called, the values provided as arguments depend on whether the '''reduce''' method has an initialValue argument.

If an initialValue is provided to the reduce method:

* The previousValue argument is initialValue.
* The currentValue argument is the value of the first element present in the array.
If an initialValue is not provided:

* The previousValue argument is the value of the first element present in the array.
* The currentValue argument is the value of the second element present in the array.
The array object can be modified by the callback function.

The following table describes the results of modifying the array object after the '''reduce''' method starts.

{{{!}} class='wikitable'
{{!}}-
! Condition after the '''reduce''' method starts
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

{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679975(v=vs.94).aspx
|HTML5Rocks_link=
}}