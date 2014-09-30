{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Makes a request conditional on a resource having changed from the specified ETag (version or representation), for refreshing caches.}}
{{HTTP Header
|Syntax=If-None-Match = "*" / 1#entity-tag
|Direction=Request
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=
|Code=If-None-Match: "xyzzy"
|LiveURL=
}}{{Single Example
|Language=
|Description=
|Code=If-None-Match: W/"xyzzy", W/"r2d2xxxx", W/"c3piozzzz"
|LiveURL=
}}{{Single Example
|Language=
|Description=
|Code=If-None-Match: *
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
|Name=RFC7232: HTTP/1.1 Conditional Requests
|URL=http://tools.ietf.org/html/rfc7232#section-3.2
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