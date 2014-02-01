{{Page_Title}}
{{Flags}}
{{Summary_Section|Decodes '''String''' objects encoded with the '''escape''' function. Deprecated.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= unescape( charString ) }}
}}
{{Remarks_Section
|Remarks=The required charString argument is a '''String''' object or literal to be decoded.

The '''unescape''' function returns a string value that contains the contents of charstring. All characters encoded with the % xx hexadecimal form are replaced by their ASCII character set equivalents.

Characters encoded in '''%u''' xxxx format (Unicode characters) are replaced with the Unicode character with hexadecimal encoding xxxx.

'''Note''' -- The '''unescape''' function should not be used to decode Uniform Resource Identifiers (URI). Use '''decodeURI''' and '''decodeURIComponent''' functions instead.
}}
{{See_Also_Section
|Manual_links=* [[javascript/decodeURI{{!}}decodeURI Function]]
* [[javascript/decodeURIComponent{{!}}decodeURIComponent Function]]
* [[javascript/escape{{!}}escape Function]]
* [[javascript/String{{!}}String Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dz4x90hk(v=vs.94).aspx
|HTML5Rocks_link=
}}