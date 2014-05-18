{{Page_Title}}
{{Flags
|High-level issues=Needs Topics
|Checked_Out=No
}}
{{Summary_Section|The toFixed() method formats a number to fixed-point notation (decimal).}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toFixed([ fractionDigits ])
}}
|Values={{JS Syntax Parameter
|Name=fractionDigits
|Required=Optional
|Description=The number of digits after the decimal point. Must be in the range 0 - 20, inclusive. Defaults to 0.
}}
}}
{{JS_Return_Value
|Description=Returns a string representation of a number in fixed-point notation, containing fractionDigits digits after the decimal point.

If fractionDigits is not supplied or '''undefined''' , the default value is 0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to use '''toFixed'''.
|Code=var num = new Number(123);
 var fix = num.toFixed();
 document.write(fix);
 document.write("&lt;br/&gt;");
 
 num = new Number(123.456);
 fix = num.toFixed(5);
 document.write(fix);
 
 // Output:
 // 123
 123.45600
}}
}}
{{Remarks_Section
|Remarks=
===Throws===

[[javascript/Error|<code>RangeError</code>] when a ''fractionDigits'' outside the bounds of 0 - 20 (inclusive) was given.
}}
{{Notes_Section
|Notes= <code>toFixed(3.9)</code> will be treated as <code>toFixed(3)</code>.
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Number/toExponential{{!}}toExponential Method (Number)]]
* [[javascript/Number/toPrecision{{!}}toPrecision Method (Number)]]
* [[javascript/Number/toString{{!}}toString Method (Number)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed toFixed(), by Mozilla Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.5 15.7.4.5 Number.prototype.toFixed(fractionDigits)]

ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/sstyff0z(v=vs.94).aspx
|HTML5Rocks_link=
}}