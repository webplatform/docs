{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Provides the entity-tag for the current selected representation, an opaque token that varies over revisions and representations.}}
{{HTTP Header
|Syntax=ETag       = entity-tag
entity-tag = [ weak ] opaque-tag
weak       = %x57.2F ; "W/", case-sensitive
opaque-tag = DQUOTE *etagc DQUOTE
etagc      = %x21 / %x23-7E / obs-text ; VCHAR except double quotes, plus obs-text
|Direction=Response
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=
|Code=ETag: "xyzzy"
|LiveURL=
}}{{Single Example
|Language=
|Description=
|Code=ETag: W/"xyzzy"
|LiveURL=
}}{{Single Example
|Language=
|Description=
|Code=ETag: ""
|LiveURL=
}}
}}
{{Notes_Section
|Usage=ETag is defined as a validator header field, and as such conveys information about the selected representation. In safe responses (GET, HEAD), this will provide metadata about the attached response. In unsafe responses (PUT, PATCH, POST, DELETE), the header describes the new resource that has replaced the old one (if any), and the server must not send the header if the resource has been altered or normalized in any way.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=RFC7232: HTTP/1.1 Conditional Requests
|URL=http://tools.ietf.org/html/rfc7232#section-2.3
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