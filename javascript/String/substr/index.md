{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets a substring beginning at the specified location and having the specified length.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= stringvar.substr( start [, length ]) }}
|Values={{JS_Syntax_Parameter
|Name=stringvar
|Required=Required
|Description=A string literal or String object from which the substring is extracted.}}{{JS_Syntax_Parameter
|Name=start
|Required=Required
|Description=The starting position of the desired substring. The index of the first character in the string is zero.}}{{JS_Syntax_Parameter
|Name=length
|Required=Optional
|Description=The number of characters to include in the returned substring.}}
}}
{{Remarks_Section
|Remarks=If length is zero or negative, an empty string is returned. If not specified, the substring continues to the end of stringvar.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''substr''' method.

|Code= var s = "The quick brown fox jumps over the lazy dog.";
 var ss = s.substr(10, 5);  
 document.write("[" + ss + "] &lt;br&gt;");
 
 ss = s.substr(10);
 document.write("[" + ss + "] &lt;br&gt;");
 
 ss = s.substr(10, -5);
 document.write("[" + ss + "] &lt;br&gt;");
 
 // Output:
 // [brown] 
 // [brown fox jumps over the lazy dog.] 
 // []
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String/substring{{!}}substring Method (String)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/0esxc5wy(v=vs.94).aspx
|HTML5Rocks_link=
}}