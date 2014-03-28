{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Summary_Section|Gets a substring beginning at the specified location and having the specified length.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=stringvar.substr( start [, length ])
}}
|Values={{JS Syntax Parameter
|Name=stringvar
|Required=Required
|Description=A string literal or String object from which the substring is extracted.
}}{{JS Syntax Parameter
|Name=start
|Required=Required
|Description=The starting position of the desired substring. The index of the first character in the string is zero.
}}{{JS Syntax Parameter
|Name=length
|Required=Optional
|Description=The number of characters to include in the returned substring.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''substr''' method.
|Code=var s = "The quick brown fox jumps over the lazy dog.";
 var ss = s.substr(10, 5);  
 document.write("[" + ss + "] &lt;br&gt;");
 
 ss = s.substr(10);
 document.write("[" + ss + "] &lt;br&gt;");
 
 ss = s.substr(10, -5);
 document.write("[" + ss + "] &lt;br&gt;");
 
ss = s.substr(-4);
document.write("[" + ss + "] &lt;br&gt;");
 // Output:
 // [brown] 
 // [brown fox jumps over the lazy dog.] 
 // []
 // [dog.]
}}
}}
{{Remarks_Section
|Remarks=If length is zero or negative, an empty string is returned. If not specified, the substring continues to the end of stringvar.
If start is negative, it is treated as [stringvar.length+start] if length is omitted this would return the last `start` characters of the stringvar.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/String/substring{{!}}substring Method (String)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/0esxc5wy(v=vs.94).aspx
|HTML5Rocks_link=
}}