{{Page_Title}}
{{Flags}}
{{Summary_Section|Converts all the alphabetic characters in a string to uppercase.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= strVariable.toUpperCase()}}{{JS_Syntax_Format
|Format= "String Literal".toUpperCase() }}
}}
{{Remarks_Section
|Remarks=The '''toUpperCase''' method has no effect on non-alphabetic characters.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example demonstrates the effects of the '''toUpperCase''' method:

|Code= var str1 = "This is a STRING.";
 var str2 = str1.toUpperCase();
 document.write(str2);
 
 // Output: THIS IS A STRING.
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String/toLocaleUpperCase{{!}}toLocaleUpperCase Method (String)]]
* [[javascript/String/toLowerCase{{!}}toLowerCase Method]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/kk06d70k(v=vs.94).aspx
|HTML5Rocks_link=
}}