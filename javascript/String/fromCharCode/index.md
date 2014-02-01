{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a string from a number of Unicode character values.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= String.fromCharCode([ code1 [, code2 [, ...[, codeN ]]]]) }}
|Values={{JS_Syntax_Parameter
|Name=String
|Required=Required
|Description=The String object.}}{{JS_Syntax_Parameter
|Name=code1 , . . . , codeN
|Required=Optional
|Description=A series of Unicode character values to convert to a string. If no arguments are supplied, the result is the empty string.}}
}}
{{Remarks_Section
|Remarks=You call this function on the String object rather than on a string instance.

The following example shows how to use this method:

 var test = String.fromCharCode(112, 108, 97, 105, 110);
 document.write(test);
 
 // Output: plain
}}
{{See_Also_Section
|Manual_links=* [[javascript/String/charCodeAt{{!}}charCodeAt Method (String)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/wb4w0k66(v=vs.94).aspx
|HTML5Rocks_link=
}}