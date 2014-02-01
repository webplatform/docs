{{Page_Title}}
{{Flags}}
{{Summary_Section|Represents a number in fixed-point notation.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= numObj.toFixed([ fractionDigits ])}}
|Values={{JS_Syntax_Parameter
|Name=numObj
|Required=Required
|Description=A '''Number''' object.}}{{JS_Syntax_Parameter
|Name=fractionDigits
|Required=Optional
|Description=The number of digits after the decimal point. Must be in the range 0 - 20, inclusive.}}
}}
{{JS_Return_Value
|Description=Returns a string representation of a number in fixed-point notation, containing fractionDigits digits after the decimal point.

If fractionDigits is not supplied or '''undefined''' , the default value is zero.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to use '''toFixed'''.

|Code= var num = new Number(123);
 var fix = num.toFixed();
 document.write(fix);
 document.write("&lt;br/&gt;");
 
 num = new Number(123.456);
 fix = num.toFixed(5);
 document.write(fix);
 
 // Output:
 // 123
 123.45600
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Number/toExponential{{!}}toExponential Method (Number)]]
* [[javascript/Number/toPrecision{{!}}toPrecision Method (Number)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/sstyff0z(v=vs.94).aspx
|HTML5Rocks_link=
}}