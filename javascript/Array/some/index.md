{{Page_Title}}
{{Flags}}
{{Summary_Section|Determines whether the specified callback function returns true for any element of an array.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= array1.some( callbackfn [, thisArg ])}}
|Values={{JS_Syntax_Parameter
|Name=array1
|Required=Required
|Description=An array object.}}{{JS_Syntax_Parameter
|Name=callbackfn
|Required=Required
|Description=A function that accepts up to three arguments. The '''some''' method calls the callbackfn function for each element in array1 until the callbackfn returns true , or until the end of the array.}}{{JS_Syntax_Parameter
|Name=thisArg
|Required=Optional
|Description=An object to which the this keyword can refer in the callbackfn function. If thisArg is omitted, undefined is used as the this value.}}
}}
{{JS_Return_Value
|Description=true if the callbackfn function returns true for any array element; otherwise, false.}}
==Exceptions==
If the callbackfn argument is not a function object, a '''TypeError''' exception is thrown.
{{Remarks_Section
|Remarks=The '''some''' method calls the callbackfn function on each array element, in ascending index order, until the callbackfn function returns true. If an element that causes callbackfn to return true is found, the some method immediately returns true. If the callback does not return true on any element, the some method returns false.

The callback function is not called for missing elements of the array.

In addition to array objects, the '''some''' method can be used by any object that has a length property and that has numerically indexed property names.

'''Note''' -- You can use the [[javascript/Array/every{{!}}every Method (Array)]] to check whether the callback function returns true for all the elements of an array.

The syntax of the callback function is as follows:

<code>function callbackfn(value, index, array1)</code>

You can declare the callback function with up to three parameters.

The following table lists the callback function parameters.

{{{!}} class='wikitable'
{{!}}-
! Callback parameter
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

The following table describes the results of modifying the array object after the '''some''' method starts.

{{{!}} class='wikitable'
{{!}}-
! Condition after the '''some''' method starts
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
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example uses the '''some''' method to find out if any elements in an array are even.

|Code= // The callback function.
 function CheckIfEven(value, index, ar) {
     if (value % 2 == 0)
         return true;
 }
 
 var numbers = [1, 15, 4, 10, 11, 22];
 
 var evens = numbers.some(CheckIfEven);
 document.write(evens);
 
 // Output:
 // true
}}{{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the thisArg parameter, which specifies an object to which the this keyword can refer. It checks whether any of the numbers in an array are outside the range provided by an object passed

|Code= // Create a function that returns true if the value is 
 // outside the range.
 var isOutsideRange = function (value) {
     return value &lt; this.minimum {{!}}{{!}} value &gt; this.maximum;
 }
 
 // Create an array of numbers.
 var numbers = [6, 12, 16, 22, -12];
 
 // The range object is to be the 'this' object.
 var range = { minimum: 10, maximum: 20 };
 
 document.write(numbers.some(isOutsideRange, range));
 
 // Output: true
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Array/every{{!}}every Method (Array)]]
* [[javascript/Array/filter{{!}}filter Method (Array)]]
* [[javascript/Array/map{{!}}map Method (Array)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679978(v=vs.94).aspx
|HTML5Rocks_link=
}}