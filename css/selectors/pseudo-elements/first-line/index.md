{{Page_Title|::first-line}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents the first line of an element. Note that the content of the first line varies depending on the available width and the styling of text (size, spacing).}}
{{CSS_Selector
|Content====Syntax===
{{Single Example
|Language=CSS
|Code=::first-line {}
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example puts the first line of any paragraph in bold text
|Code=p::first-line {
	font-weight: bold;
}
|LiveURL=https://code.webplatform.org/gist/fe1382a764e07a9c7917
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[css/cssom/properties/background|'''background''']], [[css/properties/clear|'''clear''']], [[css/properties/color|'''color''']], [[css/properties/font|'''font''']], 
[[css/properties/font-family|'''font-family''']], [[css/properties/font-size|'''font-size''']], [[css/properties/font-style|'''font-style''']], [[css/fonts/font-variant|'''font-variant''']], [[css/properties/font-weight|'''font-weight''']], 
[[css/properties/line-height|'''line-height''']], [[css/properties/text-decoration|'''text-decoration''']], 
[[css/properties/text-transform|'''text-transform''']], [[css/properties/vertical-align|'''vertical-align''']], and [[css/text/word-spacing/word-spacing|'''word-spacing''']] properties apply to the '''::first-line''' pseudo-element.
The length of the first line depends on a number of factors, such as the width of the document and the font size.
The '''::first-line''' pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding [[css/properties/display|'''display''']] property to ''block''.
In versions of Windows Internet Explorer prior to Windows Internet Explorer 9, as well as in IE8 Standards mode and earlier, only the one-colon form of this pseudo-element is recognized—that is, ''':first-line'''.
Beginning with Internet Explorer 9, the '''::first-line''' pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form. Microsoft and the World Wide Web Consortium (W3C) encourage web authors to use the two-colon form of the '''::first-line''' pseudo-element. For more information, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241611 Pseudo-elements] section of the W3C's [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241612 CSS3 Selectors] specification.
|Import_Notes====Syntax===

sel
::first-line
===Parameters===
;''sel'':A simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.12.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Elements, Selectors
|Manual_sections====Related pages (MSDN)===
*<code>[[css/selectors/pseudo-elements/::first-letter|::first-letter]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}