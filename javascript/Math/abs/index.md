{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the absolute value of a number (the value without regard to whether it is positive or negative). For example, the absolute value of -5 is the same as the absolute value of 5.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Math.abs( number )}}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required number argument is a numeric expression for which the absolute value is needed.}}
}}
{{JS_Return_Value
|Description=The absolute value of the number argument.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''abs''' function.

|Code= var s;
 var v1 = Math.abs(6);
 var v2 = Math.abs(-6);
 if (v1 == v2) {
     document.write("Absolute values are the same.");
 }
 else {
 document.write("Absolute values are different.");
 }
 
 // Output: Absolute values are the same.
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Math{{!}}Math Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}