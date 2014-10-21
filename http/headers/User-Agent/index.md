{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Contains information about the user agent originating the request.}}
{{HTTP Header
|Syntax=User-Agent = product *( RWS ( product / comment ) )
product = token ["/" product-version]
product-version = token
|Direction=Request
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=
|Code=User-Agent: CERN-LineMode/2.15 libwww/2.17b3
|LiveURL=
}}{{Single Example
|Language=Other
|Description=Chromium 38 on Linux, showing a proliferation of other user agents it is "also compatible with", a practice common among modern Web browsers
|Code=User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/38.0.2125.101 Safari/537.36
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
|Name=HTTP/1.1 Semantics and Content
|URL=http://tools.ietf.org/html/rfc7231#section-5.5.3
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