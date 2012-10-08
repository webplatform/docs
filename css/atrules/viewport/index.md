{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_At_Rule
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
You can use the '''@-ms-viewport''' rule in tandem with media queries to help optimize your layout. Typically, you nest the '''@-ms-viewport''' rule inside the media query, as shown in the following pseudocode snippet:
<code>@media [media query logic here] {
@-ms-viewport {
[viewport properties here]
}
[CSS for this layout combination here]
}</code>
|Import_Notes=
===Syntax===
<code>'''@-ms-viewport '''{ ''viewport-properties'' }</code>
===Parameters===
;''viewport-properties'':One or more property declarations, each with a trailing semicolon. Only the following viewport properties are supported.

{{{!}}
! Value
! Meaning
{{!}}-
{{!}}
; <nowiki>'''width'''</nowiki>
{{!}}
Indicates the preferred viewport width used in determining the size of the initial containing block. Can be one of the following values:

; <nowiki>'''auto'''</nowiki>
: The value is calculated based on the display device's normal mode of operation.
; <nowiki>'''device-width'''</nowiki>
: The width of the screen in CSS pixels at a zoom factor of 100%.
; <nowiki>'''device-height'''</nowiki>
: The height of the screen in CSS pixels at a zoom factor of 100%.
; <nowiki>''length''</nowiki>
: A positive absolute or relative length.
; <nowiki>''percentage''</nowiki>
: A positive percentage value relative to the width or height of the initial viewport at a zoom factor of 100%, for horizontal and vertical lengths respectively.
{{!}}-
{{!}}
; <nowiki>'''height'''</nowiki>
{{!}} <nowiki>Indicates the preferred viewport width used in determining the size of the initial containing block. See '''width''' for a list of possible values.</nowiki>
{{!}}}
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}233011 CSS Device Adaptation], Section 4


}}
{{See_Also_Section
|Topic_clusters=Syntax
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}