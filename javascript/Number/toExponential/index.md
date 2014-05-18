{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|The toExponential() method formats a number to exponential notation.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toExponential([ fractionDigits ])
}}
|Values={{JS Syntax Parameter
|Name=fractionDigits
|Required=Optional
|Description=The number of digits after the decimal point. Must be in the range 0 - 20, inclusive.
}}
}}
{{JS_Return_Value
|Description=Returns a string representation of a number in exponential notation. The string contains one digit before the decimal point, and may contain fractionDigits digits after it.

If fractionDigits is not supplied, the '''toExponential''' method returns as many digits necessary to uniquely specify the number.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var num = new Number(123);
 var exp = num.toExponential();
 document.write(exp);
 document.write("&lt;br/&gt;");
 
 num = new Number(123.456);
 exp = num.toExponential(5);
 document.write(exp);
 
 
 // Output: 
 // 1.23e+2
 // 1.23456e+2
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Number/toFixed{{!}}toFixed Method (Number)]]
* [[javascript/Number/toPrecision{{!}}toPrecision Method (Number)]]
* [[javascript/Number/toString{{!}}toString Method (Number)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toExponential toExponential(), by Mozilla Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.6 15.7.4.6 Number.prototype.toExponential(fractionDigits)]

ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Function
|Applies to=Number
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/023xd959(v=vs.94).aspx
|HTML5Rocks_link=
}}