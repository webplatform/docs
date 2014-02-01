{{Page_Title}}
{{Flags}}
{{Summary_Section|Encodes strings so they can be read on all computers. Deprecated.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= escape( charString ''')''' }}
}}
{{Remarks_Section
|Remarks=The required charString argument is any '''String''' object or literal to be encoded.

The '''escape''' function returns a string value (in Unicode format) that contains the contents of charstring. All spaces, punctuation, accented characters, and any other non-ASCII characters are replaced with % xx encoding, where xx is equivalent to the hexadecimal number representing the character. For example, a space is returned as "%20."

Characters with a value greater than 255 are stored using the '''%u''' xxxx format.

'''Note''' -- The '''escape''' function should not be used to encode Uniform Resource Identifiers (URI). Use '''encodeURI''' and '''encodeURIComponent''' functions instead.

'''Applies To''' : [[javascript/Global{{!}}Global Object]]
}}
{{See_Also_Section
|Manual_links=* [[javascript/encodeURI{{!}}encodeURI Function]]
* [[javascript/encodeURIComponent{{!}}encodeURIComponent Function]]
* [[javascript/String{{!}}String Object]]
* [[javascript/unescape{{!}}unescape Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9yzah1fh(v=vs.94).aspx
|HTML5Rocks_link=
}}