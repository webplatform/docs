{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the character at the specified index.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= strObj. charAt( index )}}
|Values={{JS_Syntax_Parameter
|Name=strObj
|Required=Required
|Description=Any String object or string literal.}}{{JS_Syntax_Parameter
|Name=index
|Required=Required
|Description=The zero-based index of the desired character.}}
}}
{{Remarks_Section
|Remarks=The '''charAt''' method returns a character value equal to the character at the specified index. The first character in a string is at index 0, the second is at index 1, and so forth. Values of index that are out of range return an empty string.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''charAt''' method:

|Code= var str = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
 document.write(str.charAt(str.length - 1));
 
 // Output: Z
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String{{!}}String Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/65zt5h10(v=vs.94).aspx
|HTML5Rocks_link=
}}