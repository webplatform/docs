{{Page_Title|Allow}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Lists the methods supported by the target resource.}}
{{HTTP Header
|Syntax=Allow = #method
|Direction=Response
|Required=Along with 405 Method Not allowed
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=
|Code=Allow: GET, HEAD, PUT
|LiveURL=
}}{{Single Example
|Language=Other
|Description=
|Code=Allow: GET, HEAD, PUT, DELETE, POST
|LiveURL=
}}
}}
{{Notes_Section
|Usage=<i>Must</i> be sent in a 405 Method Not Allowed response.
<i>Should</i> be sent to an OPTIONS response.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=RFC7231: HTTP/1.1 Semantics and Content
|URL=http://tools.ietf.org/html/rfc7231#section-7.4.1
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