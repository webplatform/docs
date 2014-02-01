{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a section of a string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= stringObj.slice( start , [ end ]) }}
|Values={{JS_Syntax_Parameter
|Name=stringObj
|Required=Required
|Description=A String object or string literal.}}{{JS_Syntax_Parameter
|Name=start
|Required=Required
|Description=The index to the beginning of the specified portion of stringObj.}}{{JS_Syntax_Parameter
|Name=end
|Required=Optional
|Description=The index to the end of the specified portion of stringObj. The substring includes the characters up to, but not including, the character indicated by end. If this value is not specified, the substring continues to the end of stringObj.}}
}}
{{Remarks_Section
|Remarks=The '''slice''' method returns a String object containing the specified portion of stringObj.

The '''slice''' method copies up to, but not including, the character indicated by end.

If start is negative, it is treated as length + start where length is the length of the string. If end is negative, it is treated as length + end. If end is omitted, copying continues to the end of stringObj. If end occurs before start , no characters are copied to the new string.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=In the first example, the slice method returns the entire string. In the second example, the slice method returns the entire string, except for the last character.

|Code= var str1 = "all good boys do fine";
 
 var slice1 = str1.slice(0);
 var slice2 = str1.slice(0,-1);
 var slice3 = str1.slice(4);
 var slice4 = str1.slice(4, 8);
 
 document.write(slice1 + "&lt;br/&gt;");
 document.write(slice2 + "&lt;br/&gt;");
 document.write(slice3 + "&lt;br/&gt;");
 document.write(slice4);
 
 // Output:
 // all good boys do fine
 // all good boys do fin
 // good boys do fine
 // good
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Array/slice{{!}}slice Method (Array)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/6w1bzf9f(v=vs.94).aspx
|HTML5Rocks_link=
}}