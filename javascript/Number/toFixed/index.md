{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Needs Review
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
|Description=Using <code>toFixed</code> to format the decimal presentation of a number.
|Code=var pie = 3.14159;

// output a number without decimal digits
pie.toFixed(0);
// Returns: "3"

// decimal digits are rounded if necessary
pie.toFixed(4);
// Returns: "3.1416"

// missing decimal digits are added
pie.toFixed(10);
// Returns: "3.1415900000"

// Watch out for number range
(1.23e+20).toFixed(2);
// Returns: "123000000000000000000.00"
(1.23e-10).toFixed(2);
// Returns: "0.00"

// Watch out for operator precedence
-3.1415.toFixed(2); 
// Returns: -3.14
(-3.1415).toFixed(2);
// Returns: "-3.14"
}}
}}
{{Remarks_Section
|Remarks====Throws===

[[javascript/Error|<code>RangeError</code>]] when a ''fractionDigits'' outside the bounds of 0 - 20 (inclusive) was given.
}}
{{Notes_Section
|Notes=* <code>toFixed(3.9)</code> will be treated as <code>toFixed(3)</code>.
* If number is greater than <code>1e+21</code>, <code>toFixed()</code> calls [[javascript/Number/toString|<code>toString()</code>]] internally and returns a string in exponential notation.
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
|JS Page Type=JS Function
|Applies to=Number
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/sstyff0z(v=vs.94).aspx
|HTML5Rocks_link=
}}