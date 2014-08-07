{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a string from a number of Unicode character values.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=String.fromCharCode([ code1 [, code2 [, ...[, codeN ]]]])
}}
|Values={{JS Syntax Parameter
|Name=String
|Required=Required
|Description=The String object.
}}{{JS Syntax Parameter
|Name=code1 , . . . , codeN
|Required=Optional
|Description=A series of Unicode character values to convert to a string. If no arguments are supplied, the result is the empty string.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=You call this function on the String object rather than on a string instance.

The following example shows how to use this method:
|Code=var test = String.fromCharCode(112, 108, 97, 105, 110);
document.write(test);
 
// Output: plain
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/String/charCodeAt{{!}}charCodeAt Method (String)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/wb4w0k66(v=vs.94).aspx
|HTML5Rocks_link=
}}