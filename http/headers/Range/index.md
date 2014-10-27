{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|The "Range" header field on a GET request modifies the method semantics to request transfer of only one or more subranges of the selected representation data, rather than the entire selected representation data.}}
{{HTTP Header
|Syntax=Range = byte-ranges-specifier / other-ranges-specifier
byte-ranges-specifier = bytes-unit "=" byte-range-set
bytes-unit = "bytes"
byte-range-set  = 1#( byte-range-spec / suffix-byte-range-spec )
other-ranges-specifier = other-range-unit "=" other-range-set
other-range-set = 1*VCHAR
byte-range-spec = first-byte-pos "-" [ last-byte-pos ]
suffix-byte-range-spec = "-" suffix-length
|Direction=Request
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=
|Code=Range: bytes 0-499, 1000-1499
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=RFC7233: HTTP/1.1 Range Requests
|URL=http://tools.ietf.org/html/rfc7233#section-3.1
|Status=
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}