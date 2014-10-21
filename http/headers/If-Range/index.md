{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Asks the server to apply the range request only if the provided ETag or Last-Modified date is current; otherwise send the entire resource.}}
{{HTTP Header
|Syntax=If-Range = entity-tag / HTTP-date
|Direction=Request
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=A client MUST NOT generate an If-Range header field containing an entity-tag that is marked as weak.

A client MUST NOT generate an If-Range header field containing an HTTP-date unless the client has no entity-tag for the corresponding representation and the date is a strong validator in the sense defined by [http://tools.ietf.org/html/rfc7232#section-2.2.2 Section 2.2.2 of RFC7232].
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=RFC7233: HTTP/1.1 Range Requests
|URL=http://tools.ietf.org/html/rfc7233#section-3.2
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