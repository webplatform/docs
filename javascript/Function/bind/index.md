{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|For a given function, creates a bound function that has the same body as the original function. In the bound function, the this object resolves to the passed in object. The bound function has the specified initial parameters.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=function.bind( thisArg [, arg1 [, arg2 [, argN ]]])
}}
|Values={{JS Syntax Parameter
|Name=function
|Required=Required
|Description=A function object.
}}{{JS Syntax Parameter
|Name=thisArg
|Required=Required
|Description=An object to which the this keyword can refer inside the new function.
}}{{JS Syntax Parameter
|Name=arg1 [, arg2 [, argN ]]]
|Required=Optional
|Description=A list of arguments to be passed to the new function.
}}
}}
{{JS_Return_Value
|Description=A new function that is the same as the function function, except for the thisArg object and the initial arguments.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to use the '''bind''' method.
|Code=// Define the original function.
 var checkNumericRange = function (value) {
     if (typeof value !== 'number')
         return false;
     else
         return value &gt;= this.minimum &amp;&amp; value &lt;= this.maximum;
 }
 
 // The range object will become the this value in the callback function.
 var range = { minimum: 10, maximum: 20 };
 
 // Bind the checkNumericRange function.
 var boundCheckNumericRange = checkNumericRange.bind(range);
 
 // Use the new function to check whether 12 is in the numeric range.
 var result = boundCheckNumericRange (12);
 document.write(result);
 
 // Output: true
}}{{Single Example
|Language=JavaScript
|Description=In the following example, the thisArg object is different from the object that contains the original method.
|Code=// Create an object that contains the original function.
 var originalObject = {
     minimum: 50,
     maximum: 100,
     checkNumericRange: function (value) {
         if (typeof value !== 'number')
             return false;
         else
             return value &gt;= this.minimum &amp;&amp; value &lt;= this.maximum;
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
}}{{Single Example
|Language=JavaScript
|Description=The following code shows how to use the arg1[,arg2[,argN]]] arguments. The bound function uses the parameters specified in the '''bind''' method as the first and second parameters. Any parameters specified when the bound function is called are used as the third, fourth (and so on) parameters.
|Code=// Define the original function with four parameters.
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
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
==Exceptions==
If the specified function is not a function, a '''TypeError''' exception is thrown.


{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Function{{!}}Function Object]]
* [[javascript/Array/filter{{!}}filter Method (Array)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff841995(v=vs.94).aspx
|HTML5Rocks_link=
}}