{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Determines whether an object is an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Array.isArray( object )
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=The object to test.
}}
}}
{{JS_Return_Value
|Description=Boolean value. Either true if object is an array; otherwise, false. 

If the object argument is not an object, false is returned.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Array.isArray''' function.
|Code=// Using Array string litteral
var ar = []; 
 var result = Array.isArray(ar);
 // Output: true
 
// Using new Array with an empty set
 var ar = new Array(); 
 var result = Array.isArray(ar);
 // Output: true
 
 var ar = [1, 2, 3];
 var result = Array.isArray(ar);
 // Output: true
 
// Testing with a string litteral "an array"
 var injectingString = Array.isArray("an array");
 document.write(injectingString);
 // Output: false
 
// Testing with an object litteral
 var injectingObject = Array.isArray({});
 document.write(injectingObject);
 // Output: false
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_links=* [[javascript/Array{{!}}Array Object]]
* [[javascript/operators/typeof{{!}}typeof Operator]]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.3.2 15.4.3.2 Array.isArray ( arg )]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Function
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff848265(v=vs.94).aspx
|HTML5Rocks_link=
}}