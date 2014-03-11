{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Calls a defined callback function on each element of an array, and returns an array that contains the results.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=map( callbackfn [, thisArg ])
}}
|Values={{JS Syntax Parameter
|Name=callbackfn
|Required=Required
|Description=A function that accepts up to three arguments. The '''map''' method calls the callbackfn function one time for each element in the array.
}}{{JS Syntax Parameter
|Name=thisArg
|Required=Optional
|Description=An object to which the this keyword can refer in the callbackfn function. If thisArg is omitted, undefined is used as the this value.
}}
}}
{{JS_Return_Value
|Description=A new array in which each element is the callback function return value for the associated original array element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''map''' method.
|Code=// Define the callback function.
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
}}{{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the thisArg argument, which specifies an object to which the this keyword can refer.
|Code=// Define an object that contains a divisor property and
 // a remainder function.
 var obj = {
     divisor: 10,
     remainder: function (value) {
         return value % this.divisor;
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
}}{{Single Example
|Language=JavaScript
|Description=In the following example, a built-inJavaScript method is used as the callback function.
|Code=// Apply Math.sqrt(value) to each element in an array.
 var numbers = [9, 16];
 var result = numbers.map(Math.sqrt);
 
 document.write(result);
 // Output: 3,4
}}{{Single Example
|Language=JavaScript
|Description=The '''map''' method can be applied to a string. The following example illustrates this.
|Code=// Define the callback function.
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
}}
}}
{{Remarks_Section
|Remarks=The '''map''' method calls the callbackfn function one time for each element in the array, in ascending index order. The callback function is not called for missing elements of the array.

In addition to array objects, the '''map''' method can be used by any object that has a length property and that has numerically indexed property names.

The syntax of the callback function is as follows:

<code>function callbackfn(value, index, array1)</code>

You can declare the callback function by using up to three parameters.

The following table lists the callback function parameters.

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
The array object can be modified by the callback function.

The following table describes the results of modifying the array object after the '''map''' method starts.

{{{!}} class='wikitable'
{{!}}-
! Condition after the '''map''' method starts
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

{{See_Also_Section}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679976(v=vs.94).aspx
|HTML5Rocks_link=
}}