{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the Unicode value of the character at the specified location.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= strObj. charCodeAt( index )}}
|Values={{JS_Syntax_Parameter
|Name=strObj
|Required=Required
|Description=Any String object or string literal.}}{{JS_Syntax_Parameter
|Name=index
|Required=Required
|Description=The zero-based index of the desired character. If there is no character at the specified index, NaN is returned.}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''charCodeAt''' method.

|Code= var str = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"; 
 document.write(str.charCodeAt(str.length - 1));
 
 // Output: 90
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String/fromCharCode{{!}}String.fromCharCode Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hza4d04f(v=vs.94).aspx
|HTML5Rocks_link=
}}