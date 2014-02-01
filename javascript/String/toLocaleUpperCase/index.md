{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns a string where all alphabetic characters have been converted to uppercase, taking into account the host environment's current locale.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= stringVar.toLocaleUpperCase( )}}
}}
{{Remarks_Section
|Remarks=The required stringVar reference is a String object or string literal.

The '''toLocaleUpperCase''' method converts the characters in a string, taking into account the host environment's current locale. In most cases, the result is the same as the result the '''toUpperCase''' method. Results differ if the rules for a language conflict with the regular Unicode case mappings.
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/6t6xaca8(v=vs.94).aspx
|HTML5Rocks_link=
}}