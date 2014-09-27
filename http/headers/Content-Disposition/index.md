{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Used to convey additional information about how to process the response payload.}}
{{HTTP Header
|Syntax=content-disposition = "Content-Disposition" ":"
                       disposition-type *( ";" disposition-parm )

disposition-type    = "inline" {{!}} "attachment" {{!}} disp-ext-type
                    ; case-insensitive
disp-ext-type       = token

disposition-parm    = filename-parm {{!}} disp-ext-parm

filename-parm       = "filename" "=" value
                    {{!}} "filename*" "=" ext-value

disp-ext-parm       = token "=" value
                    {{!}} ext-token "=" ext-value
ext-token           = <the characters in token, followed by "*">
|Direction=Response
|Required=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=
|Code=Content-Disposition: Attachment; filename=example.html
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=Content-Disposition as used in HTTP is a subset of the [http://tools.ietf.org/html/rfc2183 same header  defined in MIME]
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=RFC6266: Use of the Content-Disposition Header Field in HTTP
|URL=http://tools.ietf.org/html/rfc6266
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