{{Page_Title}}
{{Flags}}
{{Summary_Section|Represents a number either in exponential or fixed-point notation with a specified number of digits.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= numObj.toPrecision([ precision ])}}
|Values={{JS_Syntax_Parameter
|Name=numObj
|Required=Required
|Description=A '''Number''' object.}}{{JS_Syntax_Parameter
|Name=precision
|Required=Optional
|Description=The number of significant digits. Must be in the range 1 - 21, inclusive.}}
}}
{{JS_Return_Value
|Description=For numbers in exponential notation, precision - 1 digits are returned after the decimal point. For numbers in fixed notation, precision significant digits are returned.

If precision is not supplied or is '''undefined''' , the '''toString''' method is called instead.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to use '''toPrecision'''.

|Code= var num = new Number(123);
 var prec = num.toPrecision();
 document.write(prec);
 document.write("&lt;br/&gt;");
 
 num = new Number(123.456);
 prec = num.toPrecision(5);
 document.write(prec);
 
 // Output:
 // 123
 // 123.46
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Number/toFixed{{!}}toFixed Method (Number)]]
* [[javascript/Number/toExponential{{!}}toExponential Method (Number)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/kcs121ad(v=vs.94).aspx
|HTML5Rocks_link=
}}