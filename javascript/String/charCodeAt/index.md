{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the Unicode value of the character at the specified location.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=strObj. charCodeAt( index )
}}
|Values={{JS Syntax Parameter
|Name=strObj
|Required=Required
|Description=Any String object or string literal.
}}{{JS Syntax Parameter
|Name=index
|Required=Required
|Description=The zero-based index of the desired character. If there is no character at the specified index, NaN is returned.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''charCodeAt''' method.
|Code=var str = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"; 
 document.write(str.charCodeAt(str.length - 1));
 
 // Output: 90
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/String/fromCharCode{{!}}String.fromCharCode Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hza4d04f(v=vs.94).aspx
|HTML5Rocks_link=
}}