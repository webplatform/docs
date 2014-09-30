{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Specifies directives for caches along the path to the origin server. The header is found in both directions, but the directives may have different semantics depending on direction.

Request directives are:
* max-age
* max-stale
* min-fresh
* no-cache
* no-store
* no-transform
* only-if-cached

Response directives are:
* must-revalidate
* no-cache
* no-store
* no-transform
* public
* private
* proxy-revalidate
* max-age
* s-maxage
}}
{{HTTP Header
|Syntax=Cache-Control   = 1#cache-directive
cache-directive = token [ "=" ( token / quoted-string ) ]
|Direction=Request and Response
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=
|Code=
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
|Name=RFC7234: HTTP/1.1 Caching
|URL=http://tools.ietf.org/html/rfc7234#section-5.2
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