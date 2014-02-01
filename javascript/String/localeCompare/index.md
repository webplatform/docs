{{Page_Title}}
{{Flags}}
{{Summary_Section|Determines whether two strings are equivalent in the current locale.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= stringVar.localeCompare( stringExp )}}
|Values={{JS_Syntax_Parameter
|Name=stringVar
|Required=Required
|Description=A String object or string literal.}}{{JS_Syntax_Parameter
|Name=stringExp
|Required=Required
|Description=String to compare to stringVar.}}
}}
{{Remarks_Section
|Remarks=The '''localeCompare''' performs a locale-sensitive string comparison of the stringVar and the stringExp and returns -1, 0, or +1, depending on the sort order of the system default locale.

If stringVar sorts before stringExp , '''localeCompare''' returns -1; if stringVar sorts after stringExp , +1 is returned. A return value of zero means that the two strings are equivalent.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following code shows how to use '''localeCompare'''.

|Code= var str1 = "def";
 var str2 = "abc"
 
 document.write(str1.localeCompare(str2) + "&lt;br/&gt;");
 
 // Output: 1
 var str3 = "ghi";
 
 document.write(str1.localeCompare(str3)+ "&lt;br/&gt;");
 
 // Output: -1
 var str4 = "def";
 
 document.write(str1.localeCompare(str4));
 
 // Output: 0
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/toLocaleString{{!}}toLocaleString Method (Object)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/62b7ahzy(v=vs.94).aspx
|HTML5Rocks_link=
}}