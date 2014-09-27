{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Specifies a link between resources, at the HTTP header level.

Carries same semantics as the <link/> and <a/> tags in HTML.
}}
{{HTTP Header
|Syntax=Link           = "Link" ":" #link-value
link-value     = "<" URI-Reference ">" *( ";" link-param )
link-param     = ( ( "rel" "=" relation-types )
               {{!}} ( "anchor" "=" <"> URI-Reference <"> )
               {{!}} ( "rev" "=" relation-types )
               {{!}} ( "hreflang" "=" Language-Tag )
               {{!}} ( "media" "=" ( MediaDesc {{!}} ( <"> MediaDesc <"> ) ) )
               {{!}} ( "title" "=" quoted-string )
               {{!}} ( "title*" "=" ext-value )
               {{!}} ( "type" "=" ( media-type {{!}} quoted-mt ) )
               {{!}} ( link-extension ) )
link-extension = ( parmname [ "=" ( ptoken {{!}} quoted-string ) ] )
               {{!}} ( ext-name-star "=" ext-value )
ext-name-star  = parmname "*" ; reserved for RFC2231-profiled
                              ; extensions.  Whitespace NOT
                              ; allowed in between.
ptoken         = 1*ptokenchar
ptokenchar     = "!" {{!}} "#" {{!}} "$" {{!}} "%" {{!}} "&" {{!}} "'" {{!}} "("
               {{!}} ")" {{!}} "*" {{!}} "+" {{!}} "-" {{!}} "." {{!}} "/" {{!}} DIGIT
               {{!}} ":" {{!}} "<" {{!}} "=" {{!}} ">" {{!}} "?" {{!}} "@" {{!}} ALPHA
               {{!}} "[" {{!}} "]" {{!}} "^" {{!}} "_" {{!}} "`" {{!}} "{" {{!}} "{{!}}"
               {{!}} "}" {{!}} "~"
media-type     = type-name "/" subtype-name
quoted-mt      = <"> media-type <">
relation-types = relation-type
               {{!}} <"> relation-type *( 1*SP relation-type ) <">
relation-type  = reg-rel-type {{!}} ext-rel-type
reg-rel-type   = LOALPHA *( LOALPHA {{!}} DIGIT {{!}} "." {{!}} "-" )
ext-rel-type   = URI
|Direction=Request and Response
|Required=
|( "anchor" "=" <"> URI-Reference <"> )
|( "rev" "=" relation-types )
|( "hreflang" "=" Language-Tag )
|( "media" "=" ( MediaDesc
|( "title" "=" quoted-string )
|( "title*" "=" ext-value )
|( "type" "=" ( media-type
|( link-extension ) )
link-extension=( parmname [ "=" ( ptoken | quoted-string ) ] )
|( ext-name-star "=" ext-value )
ext-name-star  = parmname "*" ; reserved for RFC2231-profiled extensions.  Whitespace NOT allowed in between.
ptoken         = 1*ptokenchar
ptokenchar     = "!"
|"="
|"~"
media-type=type-name "/" subtype-name
quoted-mt      = <"> media-type <">
relation-types = relation-type
|<"> relation-type *( 1*SP relation-type ) <">
relation-type=reg-rel-type
|ext-rel-type
reg-rel-type=LOALPHA *( LOALPHA
|"-" )
ext-rel-type=URI
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=
|Code=Link: <http://example.com/TheBook/chapter2>; rel="previous"; title="previous chapter"
|LiveURL=
}}{{Single Example
|Language=
|Description=The Link header carries the same semantics, and many Web browsers recognize this:
|Code=Link: </style/main.css>;rel="stylesheet";type="text/css"
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
|Name=RFC5988: Web Linking
|URL=http://tools.ietf.org/html/rfc5988
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