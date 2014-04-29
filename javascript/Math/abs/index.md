{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns the absolute value of a number (the value without regard to whether it is positive or negative). For example, the absolute value of -5 is the same as the absolute value of 5.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Math.abs( number )
}}
|Values={{JS Syntax Parameter
|Description=The required number argument is a numeric expression for which the absolute value is needed.
}}
}}
{{JS_Return_Value
|Description=The absolute value of the number argument.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''abs''' function.
|Code=var s;
 var v1 = Math.abs(6);
 var v2 = Math.abs(-6);
 if (v1 == v2) {
     document.write("Absolute values are the same.");
 }
 else {
 document.write("Absolute values are different.");
 }
 
 // Output: Absolute values are the same.
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Math{{!}}Math Object]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/09bx9f48(v=vs.94).aspx
|HTML5Rocks_link=
}}