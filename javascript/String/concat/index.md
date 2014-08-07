{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a string that contains the concatenation of two or more strings.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=string1. concat([ string2 [, string3 [, . . . [, stringN ]]]])
}}
|Values={{JS Syntax Parameter
|Name=string1
|Required=Required
|Description=The String object or string literal to which all other specified strings are concatenated.
}}{{JS Syntax Parameter
|Name=string2,. . ., stringN
|Required=Optional
|Description=The strings to append to the end of string1.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''concat''' method when used with a string:
|Code=var str1 = "ABCD"
 var str2 = "EFGH";
 var str3 = "1234";
 var str4 = "5678";
 document.write(str1.concat(str2, str3, str4));
 
 // Output: "ABCDEFGH12345678"
}}
}}
{{Remarks_Section
|Remarks=The result of the '''concat''' method is equivalent to: result = string1 + string2 + string3 + stringN. A change of value in either a source or result string does not affect the value in the other string. If any of the arguments are not strings, they are first converted to strings before being concatenated to string1.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/addition{{!}}Addition Operator (+)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/c751eb33(v=vs.94).aspx
|HTML5Rocks_link=
}}