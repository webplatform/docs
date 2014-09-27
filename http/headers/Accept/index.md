{{Page_Title|Accept}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Used by user agents to specify response media types that are acceptable.}}
{{HTTP Header
|Syntax=Accept = #( media-range [ accept-params ] )
media-range    = ( "*/*"
                 / ( type "/" "*" )
                 / ( type "/" subtype )
                 ) *( OWS ";" OWS parameter )
accept-params  = weight *( accept-ext )
accept-ext = OWS ";" OWS token [ "=" ( token / quoted-string ) ]
|Direction=Request
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=Prefer HTML or text/x-c, or text/x-dvi if it's the best the server has after a 20% markdown in quality, or plain text after a 50% markdown in quality:
|Code=Accept: text/plain; q=0.5, text/html, text/x-dvi; q=0.8, text/x-c
|LiveURL=
}}{{Single Example
|Language=Other
|Description=Prefer XHTML or HTML, or generic XML with a reduced preference, or else any content:
|Code=Accept: text/html, application/xhtml+xml, application/xml;q=0.9, */*;q=0.8
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
|URL=http://tools.ietf.org/html/rfc7231#section-5.3.2
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