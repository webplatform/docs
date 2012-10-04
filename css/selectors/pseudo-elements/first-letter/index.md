{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The [[css/cssom/properties/background|'''background''']], [[css/properties/border|'''border''']], 
[[css/properties/border-bottom|'''border-bottom''']], [[css/properties/border-bottom-color|'''border-bottom-color''']], [[css/properties/border-bottom-style|'''border-bottom-style''']], [[css/properties/border-bottom-width|'''border-bottom-width''']], [[css/properties/border-collapse|'''border-collapse''']], [[css/properties/border-color|'''border-color''']], [[css/properties/border-left|'''border-left''']], [[css/properties/border-left-color|'''border-left-color''']], [[css/properties/border-left-style|'''border-left-style''']], [[css/properties/border-left-width|'''border-left-width''']], [[css/properties/border-right|'''border-right''']], [[css/properties/border-right-color|'''border-right-color''']], [[css/properties/border-right-style|'''border-right-style''']], [[css/properties/border-right-width|'''border-right-width''']], [[css/properties/border-style|'''border-style''']], [[css/properties/border-top|'''border-top''']], [[css/properties/border-top-color|'''border-top-color''']], [[css/properties/border-top-style|'''border-top-style''']], [[css/properties/border-top-width|'''border-top-width''']], [[css/properties/border-width|'''border-width''']], 
[[css/properties/clear|'''clear''']], [[css/properties/color|'''color''']],
[[css/properties/float|'''float''']], [[css/properties/font|'''font''']], 
[[css/properties/font-family|'''font-family''']], [[css/properties/font-size|'''font-size''']], [[css/properties/font-style|'''font-style''']], [[css/fonts/font-variant|'''font-variant''']], [[css/properties/font-weight|'''font-weight''']], 
[[css/properties/line-height|'''line-height''']], [[css/properties/margin|'''margin''']], [[css/properties/padding|'''padding''']], [[css/properties/text-decoration|'''text-decoration''']], 
[[css/properties/text-transform|'''text-transform''']], and [[css/properties/vertical-align|'''vertical-align''']] properties apply to the '''::first-letter''' pseudo-element.
The '''::first-letter''' pseudo-element can be used to create common typographical effects, such as drop caps.  Drop caps is the effect obtained when the first character of a paragraph is rendered in a font larger than the rest, and its baseline is lowered by at least one full line, which results in the second line of the text also being indented.
The '''::first-letter''' pseudo-element can be attached to block-level elements.  It can be attached to inline elements if you set the corresponding [[css/properties/display|'''display''']] property to ''block''.
In versions of Windows Internet Explorer prior to Windows Internet Explorer 9, as well as in IE8 Standards mode and earlier, only the one-colon form of this pseudo-element is recognized—that is, [[css/selectors/pseudo-elements/::before|''':first-letter''']].
Beginning with Internet Explorer 9, the [[css/selectors/pseudo-elements/::before|'''::first-letter''']] pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form. Microsoft and the World Wide Web Consortium (W3C) encourage web authors to use the two-colon form of the '''::first-letter''' pseudo-element. For more information, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241611 Pseudo-elements] section of the W3C's [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241612 CSS3 Selectors] specification.
|Import_Notes=
===Syntax===

sel
::first-letter
===Parameters===
;''sel'':A simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.12.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/selectors/pseudo-elements/::first-line|::first-line]]</code>
|Topic_clusters=Selectors, Pseudo-Elements
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}