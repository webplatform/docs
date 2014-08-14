{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Flags, Needs Topics
}}
{{Summary_Section|Returns a string representation of a number.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toString([ radix ])
}}
|Values={{JS Syntax Parameter
|Name=radix
|Required=Optional
|Description=The base number system to convert to given as 2 - 36, inclusive. Defaults to 10.
}}
}}
{{JS_Return_Value
|Description=String representing the number value in the given base number system. 

Negative numbers are simply preceded by the <code>-</code> sign, i.e. there is no conversion to a system like the [http://en.wikipedia.org/wiki/Two%27s_complement Two's Complement] for binary.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toString''' method with a number.
|Code=var mph_number = 234.567;
var mph_string = mph_number.toString();

console.log(mph_string);
// Output: "234.567"
console.log(mph_string.length);
// Output: 7
}}{{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the toString method with a radix argument.
|Code=var mph_number = 199;

// Convert to hexadecimal
mph_number.toString(16);
// Returns: "c7"

// Convert to decimal
mph_number.toString(10);
// Returns: "199"

// Convert to octal
mph_number.toString(8);
// Returns: "307"

// Convert to binary
mph_number.toString(2);
// Returns: "11000111"
}}{{Single Example
|Language=JavaScript
|Description=implicit use of <code>toString()</code>
|Code=var mph_number = 199;
String(mph_number) === mph_number.toString(10);
(mph_number + "") === mph_number.toString(10);
}}
}}
{{Remarks_Section
|Remarks====Throws===

[[javascript/Error|<code>RangeError</code>]] when a ''radix'' outside the bounds of 2 - 36 (inclusive) was given.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Number/toExponential{{!}}toExponential Method (Number)]]
* [[javascript/Number/toFixed{{!}}toFixed Method (Number)]]
* [[javascript/Number/toPrecision{{!}}toPrecision Method (Number)]]
|External_links=* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toString toString(), by Mozilla Developer Network]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.2 15.7.4.2 Number.prototype.toString(radix)]

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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj159596(v=vs.94).aspx
|HTML5Rocks_link=
}}