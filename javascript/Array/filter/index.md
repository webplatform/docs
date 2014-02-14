{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns the elements of an array that meet the condition specified in a callback function.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=array1.filter( callbackfn [, thisArg ])
}}
|Values={{JS Syntax Parameter
|Name=array1
|Required=Required
|Description=An array object.
}}{{JS Syntax Parameter
|Name=callbackfn
|Required=Required
|Description=A function that accepts up to three arguments. The '''filter''' method calls the callbackfn function one time for each element in the array.
}}{{JS Syntax Parameter
|Name=thisArg
|Required=Optional
|Description=An object to which the this keyword can refer in the callbackfn function. If thisArg is omitted, undefined is used as the this value.
}}
}}
{{JS_Return_Value
|Description=A new array that contains all the values for which the callback function returns true. If the callback function returns false for all elements of array1 , the length of the new array is 0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''filter''' method.
|Code=// Define a callback function.
 function CheckIfPrime(value, index, ar) {
     high = Math.floor(Math.sqrt(value)) + 1;
     
     for (var div = 2; div &lt;= high; div++) {
         if (value % div == 0) {
             return false;
         }
     } 
     return true;
 }
 
 // Create the original array.
 var numbers = [31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53];
 
 // Get the prime numbers that are in the original array. 
 var primes = numbers.filter(CheckIfPrime);
 
 document.write(primes);
 // Output: 31,37,41,43,47,53
}}{{Single Example
|Language=JavaScript
|Description=In the following example, the callbackfn argument includes the code of the callback function.
|Code=// Create the original array.
 var arr = [5, "element", 10, "the", true];
 
 // Create an array that contains the string
 // values that are in the original array.
 var result = arr.filter(
     function (value) {
         return (typeof value === 'string');
     }
 );
 
 document.write(result);
 // Output: element, the
}}{{Single Example
|Language=JavaScript
|Description=The following example displays the names of properties that start with the letter "css" in the <code>window</code> DOM object.
|Code=var filteredNames = Object.getOwnPropertyNames(window).filter(IsC);
 
     for (i in filteredNames)
         document.write(filteredNames[i] + "&lt;br/&gt;");
 
 // Check whether the string starts with "css".
 function IsC(value) {
     var firstChar = value.substr(0, 3);
     if (firstChar.toLowerCase() == "css")
         return true;
     else
         return false;
     }
 
 // Output:
 // CSSRule
 // CSSFontFaceRule
 // CSSImportRule
 // CSSMediaRule
 // CSSNamespaceRule
 // CSSPageRule
 // CSSRuleList
 // CSSStyleDeclaration
 // CSSStyleRule
 // CSSStyleSheet
}}{{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the thisArg argument, which specifies an object to which the this keyword can refer.
|Code=var checkNumericRange = function(value) {
     if (typeof value !== 'number')
         return false;
     else 
         return value &gt;= this.minimum &amp;&amp; value &lt;= this.maximum;
 }
 
 var numbers = [6, 12, "15", 16, "the", -12];
 
 // The obj argument enables use of the this value
 // within the callback function.
 var obj = { minimum: 10, maximum: 20 }
 
 var result = numbers.filter(checkNumericRange, obj);
 
 document.write(result);
 // Output: 12,16
}}{{Single Example
|Language=JavaScript
|Description=The '''filter''' method can be applied to a string instead of an array. The following example shows how to do this.
|Code=// Define a callback function that returns true
 // if the current array element follows a space
 // or is the first character.
 function CheckValue(value, index, ar) {
     if (index == 0)
         return true;
     else
         return ar[index - 1] === " ";
 }
 
 // Create a string.
 var sentence = "The quick brown fox jumps over the lazy dog."; 
 
 // Create an array that contains all characters that follow a space.
 var subset = [].filter.call(sentence, CheckValue); 
 
 // You can use this alternative syntax.
 //var subset = Array.prototype.filter.call(sentence, CheckValue);
 
 document.write(subset);
 // Output: T,q,b,f,j,o,t,l,d
}}
}}
{{Remarks_Section
|Remarks=The '''filter''' method calls the callbackfn function one time for each element in the array, in ascending index order. The callback function is not called for missing elements of the array.

In addition to array objects, the '''filter''' method can be used by any object that has a length property and that has numerically indexed property names.

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
The '''filter''' method does not directly modify the original array, but the callback function might modify it. The following table describes the results of modifying the array object after the '''filter''' method starts.

{{{!}} class='wikitable'
{{!}}-
! Condition after the '''filter''' method starts
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
|Manual_links=* [[javascript/Array{{!}}Array Object]]
* [[javascript/Array/map{{!}}map Method (Array)]]
* [[javascript/Array/forEach{{!}}forEach Method (Array)]]
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff679973(v=vs.94).aspx
|HTML5Rocks_link=
}}