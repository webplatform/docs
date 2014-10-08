{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Converts all alphabetic characters to lowercase, taking into account the host environment's current locale.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=stringVar.toLocaleLowerCase( )
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var hello = "wOrLd";
var foobar = hello.toLocaleLowerCase();
console.log(hello); // "wOrLd"
console.log(foobar); // "world"
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The required stringVar reference is a String object or string literal.

The '''toLocaleLowerCase''' method converts the characters in a string, taking into account the host environment's current locale. In most cases, the result is the same as the result of the '''toLowerCase''' method. Results differ if the rules for a language conflict with the regular Unicode case mappings, such as Turkish.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/String/toLocaleUpperCase{{!}}toLocaleUpperCase Method (String)]]
* [[javascript/String/toLowerCase{{!}}toLowerCase Method]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/94h6w1kx(v=vs.94).aspx
|HTML5Rocks_link=
}}