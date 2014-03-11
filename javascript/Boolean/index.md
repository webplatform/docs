{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Creates a new Boolean (true/false) value.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=new Boolean ([ boolValue ])
}}{{JS Syntax Format
|Format=([ boolValue ])
}}
|Values={{JS Syntax Parameter
|Name=boolValue
|Required=Required
|Description=The initial Boolean value for the new object. Possible values are true and false.

Other values (like 1 and 0) are converted to a Boolean expression. 
}}
}}
{{JS_Return_Value
|Description=If the boolean value is omitted, or is false , 0, null , NaN , or an empty string, Boolean returns false. Otherwise, it returns true true.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Using Boolean to define a test condition
|Code=var x = new Boolean(false);
// This value can also be expressed as x = false;
if (x) {
  // . . . this code will not be executed
}
}}{{Single Example
|Language=JavaScript
|Description=Using implicit Boolean constructor
|Code=// Implicit use of new Boolean(true)
var IsLoggedIn = true; 
if (isLoggedIn) {
  // actions that are only done when isLoggedIn is true
}
}}
}}
{{Remarks_Section
|Remarks=The '''Boolean''' object is a wrapper for the Boolean data type. JavaScript implicitly uses the '''Boolean''' object whenever a Boolean data type is converted to a '''Boolean''' object.

You rarely instantiate the '''Boolean''' object explicitly.
}}
{{Notes_Section}}
{{JS Object Listing}}

{{See_Also_Section
|Manual_sections====Specification===
[http://www.ecma-international.org/ecma-262/5.1/#sec-15.4 15.4 Array Objects]
ECMAScript® Language Specification
Standard ECMA-262
5.1 Edition / June 2011
}}
{{JS Topics
|JS Page Type=JS Object
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/t7bkhaz6(v=vs.94).aspx
|HTML5Rocks_link=
}}