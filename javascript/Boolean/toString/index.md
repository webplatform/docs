{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Returns a string representation of a Boolean object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=boolean.toString()
}}
|Values={{JS Syntax Parameter
|Name=boolean
|Required=Required
|Description=An object for which to get a string representation.
}}
}}
{{JS_Return_Value
|Description=If the Boolean value is true , returns "true". Otherwise, returns "false".
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''toString''' method.
|Code=var s = new Boolean(0);
 document.write(s.toString());
 
 // Output: false;
}}{{Single Example
|Language=JavaScript
|Description=Create a Boolean variable and convert it to a string
|Code=// Create a Boolean Variable
var flag = new Boolean(true);
// Convert the variable to a string
var myVar = flag.toString();
// myVar returns the string "true"
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections=For example:

===Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4 15.4 Array Objects]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011

}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Boolean
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/jj155292(v=vs.94).aspx
|HTML5Rocks_link=
}}