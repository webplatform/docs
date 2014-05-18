{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns a string representation of a number.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=toString([ radix ] )
}}
|Values={{JS Syntax Parameter
|Name=number
|Required=Required
|Description=The number to represent as a string.
}}
}}
{{JS_Return_Value
|Description=The optional radix should be an integer value in the inclusive range 2 to 36. If radix not present or is undefined the Number 10 is used as the value of radix.
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

// Convert to hexidecimal
console.log(mph_number.toString(16));
// Output: ea.9126e978d5

// Convert to decimal
console.log(mph_number.toString(10));
// Output: 234.567

// Convert to binary
console.log(mph_number.toString(2));
//Output: 11101010.1001000100100110111010010111100011010101 

// Check the length of the binary string
console.log(mph_number.toString(2).length);
// Output: 49
}}{{Single Example
|Description=calling toString() implicitly by string concatenation
|Code=number + "" => string
String(number) => string (KEIN new davor!)
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Number/toExponential{{!}}toExponential Method (Number)]]
* [[javascript/Number/toPrecision{{!}}toPrecision Method (Number)]]
* [[javascript/Number/toFixed{{!}}toFixed Method (Number)]]
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.7.4.2 Number.prototype.toString(fractionDigits)]

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