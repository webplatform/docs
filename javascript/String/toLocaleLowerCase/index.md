{{Page_Title}}
{{Flags}}
{{Summary_Section|Converts all alphabetic characters to lowercase, taking into account the host environment's current locale.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= stringVar.toLocaleLowerCase( )}}
}}
{{Remarks_Section
|Remarks=The required stringVar reference is a String object or string literal.

The '''toLocaleLowerCase''' method converts the characters in a string, taking into account the host environment's current locale. In most cases, the result is the same as the result of the '''toLowerCase''' method. Results differ if the rules for a language conflict with the regular Unicode case mappings.
}}
{{See_Also_Section
|Manual_links=* [[javascript/String/toLocaleUpperCase{{!}}toLocaleUpperCase Method (String)]]
* [[javascript/String/toLowerCase{{!}}toLowerCase Method]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/94h6w1kx(v=vs.94).aspx
|HTML5Rocks_link=
}}