{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Allows a user agent to authenticate itself with an origin server.}}
{{HTTP Header
|Syntax=Authorization = credentials
credentials = auth-scheme [ 1*SP ( token68 / #auth-param ) ]
auth-scheme = token
auth-param = token BWS "=" BWS ( token / quoted-string )
token68 = 1*( ALPHA / DIGIT /  "-" / "." / "_" / "~" / "+" / "/" ) *"="
|Direction=
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=
|Code=Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=Other specifications define the authorization schemes that may be used with the header: A registry of these Authorization schemes is maintained by the IANA in the [http://www.iana.org/assignments/http-authschemes/http-authschemes.xhtml Hypertext Transfer Protocol (HTTP) Authentication Scheme Registry].
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=RFC7235: HTTP/1.1 Authentication
|URL=http://tools.ietf.org/html/rfc7235#section-4.2
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