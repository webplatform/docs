{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|'''Deprecated'''

The deprecated '''escape()''' function encodes a string so it can be read on all computers.
}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=escape(str)
}}
|Values={{JS Syntax Parameter
|Name=str
|Required=Required
|Description=A String to be encoded
}}
}}
{{JS_Return_Value
|Description=Returns a string value in Unicode format that contains the encoded contents of the str parameter.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=unescape("webplatform"); // "webplatform"
unescape("ümlaut"); // "%FCmlaut"
unescape("日本語"); // "%u65E5%u672C%u8A9E"
}}
}}
{{Remarks_Section
|Remarks=All spaces, punctuation, accented characters, and any other non-ASCII characters are replaced with % xx encoding, where xx is equivalent to the hexadecimal number representing the character. For example, a space is returned as "%20."

Characters with a value greater than 255 are stored using the '''%u''' xxxx format.
}}
{{Notes_Section
|Notes=The '''escape''' function should not be used to encode URIs. Use [[javascript/encodeURI{{!}}encodeURI]] and 
[[javascript/encodeURIComponent{{!}}encodeURIComponent]] functions instead
}}
{{JS Object Listing}}

{{See_Also_Section
|Topic_clusters=Deprecated
|Manual_links=* [[javascript/encodeURI{{!}}encodeURI Function]]
* [[javascript/encodeURIComponent{{!}}encodeURIComponent Function]]
* [[javascript/String{{!}}String Object]]
* [[javascript/unescape{{!}}unescape Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/9yzah1fh(v=vs.94).aspx
|HTML5Rocks_link=
}}