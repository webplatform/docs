{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns a string representation of an array.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toString()
}}
|Values=
}}
{{JS_Return_Value
|Description=The string representation of the array.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toString''' method with an array.
|Code=var arr = [1, 2, 3, 4];
 var s = arr.toString();
 document.write(s);
 
 // Output: 1,2,3,4
}}
}}
{{Remarks_Section
|Remarks=The elements of an '''Array''' are converted to strings. The resulting strings are concatenated and separated by commas.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.2 15.4.4.2 Array.prototype.toString ( )]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Method
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155287(v=vs.94).aspx
|HTML5Rocks_link=
}}