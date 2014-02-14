{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Performs the specified action for each element in an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=array1.forEach( callbackfn [, thisArg ])
}}
|Values={{JS Syntax Parameter
|Name=array1
|Required=Required
|Description=An array object.
}}{{JS Syntax Parameter
|Name=callbackfn
|Required=Required
|Description=A function that accepts up to three arguments.'''forEach''' calls the callbackfn function one time for each element in the array.
}}{{JS Syntax Parameter
|Name=thisArg
|Required=Optional
|Description=An object to which the this keyword can refer in the callbackfn function. If thisArg is omitted, undefined is used as the this value.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates use of the '''forEach''' method.
|Code=// Define the callback function.
 function ShowResults(value, index, ar) {
     document.write("value: " + value);
     document.write(" index: " + index);
     document.write("&lt;br /&gt;");
 }
 
 // Create an array.
 var letters = ['ab', 'cd', 'ef'];
 
 // Call the ShowResults callback function for each
 // array element.
 letters.forEach(ShowResults);
 
 // Output:
 //  value: ab index: 0 
 //  value: cd index: 1 
 //  value: ef index: 2
}}{{Single Example
|Language=JavaScript
|Description=In the following example, the callbackfn argument includes the code of the callback function.
|Code=// Create an array.
 var numbers = [10, 11, 12];
 
 // Call the addNumber callback function for each array element.
 var sum = 0;
 numbers.forEach(
     function addNumber(value) { sum += value; }
 );
 
 document.write(sum);
 // Output: 33
}}{{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the thisArg argument, which specifies an object that can be referred to with the this keyword.
|Code=// Define the object that contains the callback function.
 var obj = {
     showResults: function(value, index) {
         // Call calcSquare by using the this value.
         var squared = this.calcSquare(value);
 
         document.write("value: " + value);
         document.write(" index: " + index);
         document.write(" squared: " + squared);
         document.write("&lt;br /&gt;");
     },
     calcSquare: function(x) { return x * x }
 };
 
 // Define an array.
 var numbers = [5, 6];
 
 // Call the showResults callback function for each array element.
 // The obj is the this value within the 
 // callback function.
 numbers.forEach(obj.showResults, obj);
 
 // Embed the callback function in the forEach statement.
 // The obj argument is the this value within the obj object.
 // The output is the same as for the previous statement.
 numbers.forEach(function(value, index) { this.showResults(value, index) }, obj);
 
 // Output:
 //  value: 5 index: 0 squared: 25
 //  value: 6 index: 1 squared: 36
 //  value: 5 index: 0 squared: 25
 //  value: 6 index: 1 squared: 36
}}
}}
{{Remarks_Section
|Remarks=The '''forEach''' method calls the callbackfn function one time for each element present in the array, in ascending index order. The callback function is not called for missing elements of the array.

In addition to array objects, the '''forEach''' method can be used by any object that has a length property and that has numerically indexed property names.

The syntax of the callback function is as follows:

<code>function callbackfn(value, index, array1)</code>

You can declare the callback function by using up to three parameters.

The callback function parameters are as follows.

{{{!}} class='wikitable'
{{!}}-
! Callback argument
! Definition
{{!}}-
{{!}} value
{{!}} The value of the array element.
{{!}}-
{{!}} index
{{!}} The numeric index of the array element.
{{!}}-
{{!}} array1
{{!}} The array object that contains the element.
{{!}}} 
The '''forEach''' method does not directly modify the original array, but the callback function might modify it. The following table describes the results of modifying the array object after the '''forEach''' method starts.

{{{!}} class='wikitable'
{{!}}-
! Condition after '''forEach''' method starts
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
If the callbackfn argument is not a function object, a '''TypeError''' exception is thrown.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Array/filter{{!}}filter Method (Array)]]
* [[javascript/Array/map{{!}}map Method (Array)]]
* [[javascript/Array/some{{!}}some Method (Array)]]
* [[javascript/Array{{!}}Array Object]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679980(v=vs.94).aspx
|HTML5Rocks_link=
}}