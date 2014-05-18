{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Needs Review
|Checked_Out=No
}}
{{Summary_Section|Represents a number either in exponential or fixed-point notation with a specified number of digits.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toPrecision([ precision ])
}}
|Values={{JS Syntax Parameter
|Name=precision
|Required=Optional
|Description=The number of significant digits. Must be in the range 1 - 21, inclusive.
}}
}}
{{JS_Return_Value
|Description=For numbers in exponential notation, precision - 1 digits are returned after the decimal point. For numbers in fixed notation, precision significant digits are returned.

If precision is not supplied or is <code>undefined</code> , [[javascript/Number/toString|<code>toString()</code>]] is called instead.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code shows how to use <code>toPrecision</code>.
|Code=var pie = 3.14159;

// Call passed through to toString()
pie.toPrecision();
// Returns: "3.14159"

pie.toPrecision(5);
// Returns: "3.1416"

pie.toPrecision(2);
// Returns: "3.1"

pie.toPrecision(1);
// Returns: "3"

// Watch out for exponential notation
(1234.5).toPrecision(2);
// Returns "1.2e+3"
}}
}}
{{Remarks_Section
|Remarks====Throws===

[[javascript/Error|<code>RangeError</code>]] when a ''fractionDigits'' outside the bounds of 1 - 21 (inclusive) was given.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Number/toExponential{{!}}toExponential Method (Number)]]
* [[javascript/Number/toFixed{{!}}toFixed Method (Number)]]
* [[javascript/Number/toString{{!}}toString Method (Number)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toPrecision toPrecision(), by Mozilla Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.7 15.7.4.7 Number.prototype.toPrecision(precision)]

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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/kcs121ad(v=vs.94).aspx
|HTML5Rocks_link=
}}