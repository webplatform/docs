{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=* Details on when to use (or rather, when **not** to use) cookies
* Security concerns with using for authenticating users, background on CSRF
|Checked_Out=No
}}
{{Standardization_Status|Mixed}}
{{API_Name}}
{{Summary_Section|The Cookie headers may be used to receive the value of a cookie from a user agent. The value of the cookie will have been previously set though a script, or by the [[http/headers/Set-Cookie|Set-Cookie]] header.

Cookies have many issues associated with them, including security and CSRF attacks, privacy issues, and a nonstandard format compared to other HTTP headers.
}}
{{HTTP Header
|Syntax=cookie-header = "Cookie:" OWS cookie-string OWS
cookie-string = cookie-pair *( ";" SP cookie-pair )
cookie-pair       = cookie-name "=" cookie-value
cookie-name       = token
cookie-value      = *cookie-octet / ( DQUOTE *cookie-octet DQUOTE )
cookie-octet      = %x21 / %x23-2B / %x2D-3A / %x3C-5B / %x5D-7E
                       ; US-ASCII characters excluding CTLs,
                       ; whitespace DQUOTE, comma, semicolon,
                       ; and backslash
|Direction=Request
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=A user agent sending a cookie named "SID" with the value "31d4d96e407aad42".
|Code=Cookie: SID=31d4d96e407aad42
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
|Name=HTTP State Management Mechanism
|URL=http://tools.ietf.org/html/rfc6265
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