{{Page_Title}}
{{Flags}}
{{Summary_Section|Converts all the alphabetic characters in a string to lowercase.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= strVariable.toLowerCase()}}{{JS_Syntax_Format
|Format= "String Literal".toLowerCase() }}
}}
{{Remarks_Section
|Remarks=The '''toLowerCase''' method has no effect on non-alphabetic characters.

The following example demonstrates the effects of the '''toLowerCase''' method:

 var str1 = "This is a STRING.";
 var str2 = str1. toLowerCase();
 document.write(str2);
 
 // Output: this is a string.
}}
{{See_Also_Section
|Manual_links=* [[javascript/String/toLocaleLowerCase{{!}}toLocaleLowerCase Method (String)]]
* [[javascript/String/toUpperCase{{!}}toUpperCase Method (String)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/es5c2d38(v=vs.94).aspx
|HTML5Rocks_link=
}}