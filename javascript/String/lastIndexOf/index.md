{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the last occurrence of a substring in the string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= strObj.'''lastIndexOf(''' substring [, startindex ] ''')'''}}
|Values={{JS_Syntax_Parameter
|Name=strObj
|Required=Required
|Description=A String object or string literal.}}{{JS_Syntax_Parameter
|Name=substring
|Required=Required
|Description=The substring to search for.}}{{JS_Syntax_Parameter
|Name=startindex
|Required=Optional
|Description=The index at which to begin searching. If omitted, the search begins at the end of the string.}}
}}
{{Remarks_Section
|Remarks=The '''lastIndexOf''' method returns an integer value indicating the beginning of the substring within the String object. If the substring is not found, a -1 is returned.

If startindex is negative, startindex is treated as zero. If it is larger than the greatest character position index, it is treated as the largest possible index.

Searching is performed starting at the last character in the string. Otherwise, this method is identical to '''indexOf'''.

The following example illustrates the use of the '''lastIndexOf''' method.

 var str = "time, time";
 
 var s = "";
 s += "time is at position " + str.lastIndexOf("time");
 s += "&lt;br /&gt;";
 s += "abc is at position " + str.lastIndexOf("abc");
 
 document.write(s);
 
 // Output:
 // time is at position 6
 // abc is at position -1
}}
{{See_Also_Section
|Manual_links=* [[javascript/String/indexOf{{!}}indexOf Method (String)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/6d20k718(v=vs.94).aspx
|HTML5Rocks_link=
}}